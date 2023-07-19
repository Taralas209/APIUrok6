# Comic Publication

This project is an automated tool for publishing random comics from the XKCD website on the wall of a VKontakte group.

### How to install

1. Clone the repository to your local computer.
2. Install the necessary packages using `pip install -r requirements.txt` (assuming that you have a requirements.txt file with all dependencies).
3. Create a `.env` file in the root directory of the project.
4. Add the following variables to the `.env` file:
    - `API_ID` - your VKontakte application ID.
    - `ACCESS_TOKEN` - your access key for the VKontakte application.
    - `USER_ID` - your VKontakte user ID.
    - `GROUP_ID` - ID of the VKontakte group on whose wall the comics will be published.
5. Run the script using the command `python main.py` in the command line.

### Project Objective

The code is written for educational purposes on an online course for web developers [dvmn.org](https://dvmn.org/).

---

### Code Description

1. Import of necessary libraries.
2. Loading environment variables from the `.env` file.
3. The `get_last_comic_number` function gets the number of the latest comic on the XKCD website.
4. The `fetch_comic_info` function retrieves information about a random comic, including the image URL and comment.
5. The `get_vk_upload_id` function gets the URL for uploading photos to VKontakte servers.
6. The `upload_photo_to_vk_server` function uploads the comic to the VKontakte server.
7. The `save_photo_to_vk_wall` function saves the comic photo on the wall of the VKontakte group.
8. The `public_post_to_wall` function publishes the comic on the wall of the VKontakte group along with a comment.
9. The main code that calls all of the above functions in the necessary order.
