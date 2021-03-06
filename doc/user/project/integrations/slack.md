# Slack Notifications Service

## On Slack

To enable Slack integration you must create an incoming webhook integration on
Slack:

1. [Sign in to Slack](https://slack.com/signin)
1. Visit [Incoming WebHooks](https://my.slack.com/services/new/incoming-webhook/)
1. Choose the channel name you want to send notifications to.
1. Click **Add Incoming WebHooks Integration**
1. Copy the **Webhook URL**, we'll need this later for GitLab.

## On GitLab

After you set up Slack, it's time to set up GitLab.

Navigate to the [Integrations page](project_services.md#accessing-the-project-services)
and select the **Slack notifications** service to configure it.
There, you will see a checkbox with the following events that can be triggered:

- Push
- Issue
- Confidential issue
- Merge request
- Note
- Tag push
- Pipeline
- Wiki page

Below each of these event checkboxes, you have an input field to enter
which Slack channel you want to send that event message. Enter your preferred channel name **without** the hash sign (`#`).

At the end, fill in your Slack details:

| Field | Description |
| ----- | ----------- |
| **Webhook**  | The [incoming webhook URL][slackhook] which you have to setup on Slack. |
| **Username** | Optional username which can be on messages sent to Slack. Fill this in if you want to change the username of the bot. |
| **Notify only broken pipelines** | If you choose to enable the **Pipeline** event and you want to be only notified about failed pipelines. |

After you are all done, click **Save changes** for the changes to take effect.

>**Note:**
You can set "branch,pushed,Compare changes" as highlight words on your Slack
profile settings, so that you can be aware of new commits when somebody pushes
them.

![Slack configuration](img/slack_configuration.png)

[slackhook]: https://my.slack.com/services/new/incoming-webhook
