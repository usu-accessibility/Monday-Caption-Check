# Monday Caption Check

## WARNING: This tool has been replaced by [Canvas Captions API](https://github.com/usu-accessibility/canvas-captions-api)

Monday Caption Check is a tool that searches a Canvas course for all embedded videos to ensure that video materials are properly captioned. This tool integrates into a Monday board to automate the process of checking and updating the caption status of videos in any given Canvas course.

It looks through all videos (Kaltura audio/video embeds and Youtube links/embeds) embedded in any Canvas page within a Canvas course, listing each video as a subitem of the course item. Each listed video, however, is *not guaranteed* to be in active use within a course, and therefore, not guaranteed to need captioning. They may be in an unused Canvas page as a result of copying a previous course. Frequent use of TidyUp by course owners will minimize this issue.

Hosted [on Coolify.](https://app.coolify.io/project/fow8gws)

## Technology Stack

- **AWS Lambda**: All components of this application are hosted on AWS Lambda, ensuring scalability and cost-effectiveness.

- **Monday API**: Integration with Monday board to fetch course URLs and update caption statuses.

- **Canvas LMS API**: Scans Canvas courses to fetch videos for caption checking.

- **YouTube API**: Checks the caption status of YouTube videos.

- **Kaltura API**: Checks the caption status of Kaltura videos.

![Blank board - Page 1-2](https://github.com/usu-access/monday-captioncheck/assets/41461773/26e0720b-1bf4-4f2e-97f9-01839054ac39)

## Workflow

1. **Integrate with Monday Board**: Connect the application to your Monday board.

2. **Initiate the Caption Check**: Change the status column to "Begin Check" to trigger the caption checking process. The status will change to "Check in Progress."

![Screenshot 2023-10-23 at 4 57 08 PM](https://github.com/usu-access/monday-captioncheck/assets/41461773/c74bb6f5-0b22-46ce-9564-8d6ad039eec0)

3. **Caption Checking**: The tool scans the Canvas courses, fetches the videos, and checks their caption status. It adds and updates the status as subitems in the Monday board.

![Screenshot 2023-10-23 at 4 58 15 PM](https://github.com/usu-access/monday-captioncheck/assets/41461773/d79a5c46-3e1f-484b-a48d-f1fb40c8f22d)

4. **Caption Type**: If videos are captioned, the tool specifies whether the captions are "Auto-generated" or "Human-generated."

![Screenshot 2023-10-23 at 4 59 26 PM](https://github.com/usu-access/monday-captioncheck/assets/41461773/8c5089aa-d368-411f-a586-1c385c6aadfb)

5. **3PLAY Tagging**: In the subitem tree, use the "3PLAY" column to tag videos that need captioning, making it easy to send them for captioning.

![Screenshot 2023-10-23 at 4 58 59 PM](https://github.com/usu-access/monday-captioncheck/assets/41461773/ca666bd0-c172-43a0-98bd-6112bfd0d58f)

6. **Completion**: Once all videos have been checked, the status column will change to "Check Complete."

## Future Enhancements

We have ambitious plans to further improve Monday Caption Check:

- **Node.js Migration**: We're considering migrating the application to Node.js and deploying it on AWS EC2 to overcome Lambda's runtime limitations.

- **Monday App**: Our ultimate goal is to transform Monday Caption Check into a full-fledged Monday application, making it accessible to a broader audience.

## Contributors

This project was developed by a team of dedicated Digital Accessibility Specialists with valuable contributions from the following individuals:

- [Contributor 1 Name](Link to Contributor 1's GitHub Profile)
- [Contributor 2 Name](Link to Contributor 2's GitHub Profile)

This project is open-source and licensed under the [License Name] - for more details, please refer to the [LICENSE.md](link-to-license-file) file.

We believe that Monday Caption Check is a valuable resource for ensuring educational content's accessibility and inclusivity. We welcome your feedback and contributions to make it even better. Thank you for using our tool!
