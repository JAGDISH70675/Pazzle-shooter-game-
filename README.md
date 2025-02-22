using UnityEngine;

public class PlayerMovement : MonoBehaviour
{
    public float moveSpeed = 5f;
    public Rigidbody2D rb;
    private Vector2 moveInput;

    void Update()
    {
        moveInput.x = Input.GetAxis("Horizontal");
        moveInput.y = Input.GetAxis("Vertical");
    }

    void FixedUpdate()
    {
        rb.velocity = moveInput * moveSpeed;
    }
} Pazzle-shooter-game-