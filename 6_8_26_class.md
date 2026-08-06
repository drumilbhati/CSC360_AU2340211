# Class Questions and Answers

## 1. How is computer graphics different from digital image processing?

**Computer graphics** creates images from mathematical models, geometric objects, colors, lighting, and other data. For example, a graphics program may render a three-dimensional model of a building.

**Digital image processing** takes an existing digital image as input and modifies or analyzes it. Common operations include resizing, sharpening, noise removal, compression, and object detection.

In short, computer graphics generally **generates images**, whereas image processing generally **works on existing images**.

## 2. What are the geometric primitives of drawing?

Geometric primitives are the basic shapes from which more complex drawings are constructed. Common primitives include:

- **Point:** A single location specified by coordinates.
- **Line or line segment:** A straight path between two points.
- **Polyline:** A sequence of connected line segments.
- **Polygon:** A closed shape made from line segments, such as a triangle or rectangle.
- **Circle and ellipse:** Curved shapes defined by a center and radius or axes.
- **Curve or arc:** A smooth path, such as a Bézier curve.
- **Text:** Characters drawn at specified positions using a font.

In three-dimensional graphics, primitives also include triangles, planes, cubes, spheres, and other meshes or surfaces.

## 3. Describe the graphical frameworks in Java.

Java provides several frameworks for creating graphical applications:

- **AWT (Abstract Window Toolkit):** Java's original GUI framework. It provides windows, buttons, menus, graphics, layout managers, and event handling. Many AWT components use the operating system's native interface controls.
- **Swing:** A richer GUI toolkit built on AWT. It supplies mostly lightweight components such as `JFrame`, `JButton`, `JTable`, and `JPanel`, and supports a pluggable look and feel.
- **Java 2D:** An API used with AWT and Swing for drawing shapes, text, and images and for applying colors, strokes, transforms, and compositing effects through classes such as `Graphics2D`.
- **JavaFX:** A newer framework for desktop applications with a scene graph, CSS styling, property binding, animation, media support, and FXML-based interface descriptions.

## 4. What is the design pattern for creating user interfaces?

A common pattern is **Model-View-Controller (MVC)**:

- The **Model** stores the application's data and business rules.
- The **View** displays the user interface.
- The **Controller** receives user input and coordinates updates to the model and view.

Java graphical interfaces also use the **event-listener model**, which is a form of the Observer pattern. A source component, such as a button, produces an event. Registered listener objects receive that event and execute the appropriate handler. For example, an `ActionListener` can be registered with a `JButton` to respond when the user clicks it.

## 5. How is static graphics different from interactive graphics?

**Static graphics** do not change in response to user actions. Once rendered, their content remains fixed, as in a printed diagram or a non-animated chart.

**Interactive graphics** respond to input such as mouse movement, clicks, keyboard commands, touch, or data changes. The program repeatedly updates or redraws the display, allowing users to select, move, resize, rotate, zoom, or otherwise manipulate graphical objects.

## 6. How is a curve connected with calculus?

A curve can be represented mathematically by a function, such as `y = f(x)`, or by parametric functions, such as `x = x(t)` and `y = y(t)`. Calculus helps analyze and construct curves:

- The **first derivative** gives the curve's slope or tangent direction.
- The **second derivative** describes how the slope changes and helps determine concavity.
- Derivatives of parametric curves can be used to calculate curvature and normals.
- **Integration** can calculate quantities such as the area under a curve and its arc length.

Computer graphics uses these ideas to create smooth curves, animate movement along paths, and maintain smooth joins between curve segments.

## 7. Describe SSH and HTTPS protocols for accessing Git repositories.

Both protocols provide secure ways to communicate with a remote Git repository:

- **SSH (Secure Shell):** Uses an SSH URL such as `git@github.com:user/repository.git`. Authentication normally uses a public/private key pair. After the public key has been added to the hosting service, Git operations can usually be performed without entering a username or access token each time. SSH commonly uses port 22.
- **HTTPS (Hypertext Transfer Protocol Secure):** Uses a URL such as `https://github.com/user/repository.git`. TLS encrypts the connection. Authentication typically uses a personal access token, credential manager, or browser-based sign-in rather than an account password. HTTPS commonly uses port 443 and is often easier to use on networks that block SSH.

The protocol changes how Git connects and authenticates; it does not change the repository's contents.

## 8. Mention the tools used for SSH operations.

Common SSH tools include:

- `ssh`: Connects securely to a remote host.
- `ssh-keygen`: Generates and manages SSH key pairs.
- `ssh-agent`: Holds private keys in memory for authenticated sessions.
- `ssh-add`: Adds private keys to or removes them from `ssh-agent`.
- `ssh-copy-id`: Installs a public key on a remote Unix-like host.
- `scp`: Securely copies files between hosts.
- `sftp`: Provides interactive secure file transfer.
- `ssh-keyscan`: Retrieves a server's public host keys.

Git uses the SSH client when a remote repository is configured with an SSH URL.

## 9. What are public and private keys?

A **public key** and a **private key** form an asymmetric cryptographic key pair:

- The **public key** may be shared. In SSH authentication, it is placed on the remote server or added to a Git hosting account.
- The **private key** must remain secret on the user's computer. It proves the user's identity by creating a cryptographic signature that can be verified with the corresponding public key.

The private key is not sent to the server during SSH authentication. It should be protected with appropriate file permissions and, ideally, a strong passphrase. If it is exposed, it should be revoked and replaced immediately.