# Online Video Streaming

Java EE web application for uploading, managing, and streaming videos with admin and user dashboards.

## Features
- Admin CRUD for users, videos, and site content.
- User login and profile dashboards.
- Video upload, listing, and playback pages.
- Contact/feedback handling.
- Simple stats display for creators.

## Project Layout
- Java sources: `src/main/java/com/video`
  - Model: [`com.video.model.Admin`](src/main/java/com/video/model/Admin.java), `User`, `Video`, `Contact`, `CreatorVideoStats`
  - Service: `AdminService`, `UserService`, `VideoService`, `ContactService`
  - Servlets: `AdminServlet`, `CreateAdminServlet`, `AdminEditServlet`, `AdminDeleteServlet`, `ContactServlet`, etc.
- Web resources: `src/main/webapp`
  - JSPs: `index.jsp`, `login.jsp`, `videoList.jsp`, `videoPage.jsp`, `upload.jsp`, `dashboard.jsp`, `AdminActions/`
  - Assets: `css/`, `js/`, `includes/`, `WEB-INF/web.xml`

## Prerequisites
- JDK 8+  
- Apache Tomcat (or any Servlet 3+ container)  
- Maven (if you add a `pom.xml`) or Eclipse WTP setup.

## Build & Run (Eclipse WTP)
1. Import as Existing Eclipse Dynamic Web Project.
2. Ensure the target runtime is set to Tomcat.
3. Clean & build the project.
4. Run on Server → select Tomcat.

## Build & Run (Manual WAR)
1. Export WAR from Eclipse: **File → Export → WAR file**.
2. Deploy the WAR to Tomcat’s `webapps` directory.
3. Start Tomcat and open `http://localhost:8080/online-video-streaming-main`.

## Notes
- Configure database connection in `com.video.util.DatabaseUtil` (JDBC URL, user, password).
- Update `WEB-INF/web.xml` for servlet mappings and welcome pages as needed.
- Default entry point: `index.jsp`.
