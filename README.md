# Open-source small group management for churches

A home for your church's small groups: a public directory, join requests, recurring meetings, and attendance taken from an emailed checklist.

This repository is the **Small Groups** edition of [Church4Christ](https://github.com/leveo/church4christ), an open-source
church management system and website. It contains no separate code: the quick start below
installs Church4Christ v1.7.0 with only the Small Groups features switched on (Fellowships, Groups, People & Households).
Everything else stays off until you turn it on.

**[Try the live demo](https://demo.church4christ.org/en/sandbox)** · [Main repository](https://github.com/leveo/church4christ) · [Setup guide](https://github.com/leveo/church4christ/blob/v1.7.0/docs/setup.md)

## What you get

- **Public and private groups.** Public groups appear in the directory; private groups are invisible to anyone who is not a member.
- **Join requests.** A visitor signs in with just a name and email (magic link, no password) and taps Request to join; a group leader approves or declines.
- **Group leaders run their own group.** Roster, requests, the public/private switch, and meetings all live on one manage page, with no admin-area access needed.
- **Members without email still count.** Add someone by name only; add an email later and they get a real profile.
- **Recurring meetings.** Weekly, every other week, or monthly meetings are put on the calendar automatically.
- **Attendance without homework.** After a tracked meeting, leaders get an email link to a simple checklist; tick who came and save.
- **Involvement history.** Each person's profile shows their groups and attendance.
- **A fellowship directory** for larger fellowships alongside small groups.
- **12 interface languages** throughout, including English and Chinese.

## Screenshots

![The public small groups directory](https://raw.githubusercontent.com/leveo/church4christ/v1.7.0/docs/images/groups/directory.png)

![Creating groups and assigning group leaders](https://raw.githubusercontent.com/leveo/church4christ/v1.7.0/docs/images/admin/groups.png)

![The attendance checklist a group leader fills in after a meeting](https://raw.githubusercontent.com/leveo/church4christ/v1.7.0/docs/images/groups/member-checklist.png)

![The fellowship directory](https://raw.githubusercontent.com/leveo/church4christ/v1.7.0/docs/images/public/fellowships.png)

## Try the live demo

Open the [public sandbox](https://demo.church4christ.org/en/sandbox). Open **Groups** in the site menu to see the public directory, then choose **Administrator** and open **Groups** in the admin menu. All data is fictional and resets every night.

## Quick start

You need [Git](https://git-scm.com/) and [Node.js](https://nodejs.org/) 22.22.1 or newer.
These commands work in macOS and Linux terminals and in Windows PowerShell.

```bash
git clone --depth 1 --branch v1.7.0 https://github.com/leveo/church4christ.git my-church
cd my-church
npm ci
npm run onboard -- --preset small-groups
```

`npm run onboard` opens a local form in your browser for your church's name, colors, logo,
and first administrator, with the Small Groups features already checked. Save the form, press
Ctrl+C in the terminal, then apply it and start the site:

```bash
node scripts/setup/index.mjs --preferences .church/preferences.json --yes --dry-run
node scripts/setup/index.mjs --preferences .church/preferences.json --yes
npm run dev
```

Prefer the terminal only? Run `npm run setup -- --mode local --preset small-groups`
instead of the form and answer the prompts.

Open the address the installer prints (usually `http://localhost:4321`). On your own
computer, sign-in links print to the terminal instead of being emailed.

## Good to know

- Paid or open sign-up events for a group use the Registration feature, which needs the optional Supabase database. This edition runs on the default Cloudflare D1 database, where that section simply does not appear.
- Attendance emails need an email provider when deployed; on your own computer they print to the terminal.

## Grow into the full system

This is the complete Church4Christ codebase with a focused starting point. When you are
ready, an administrator can turn on more features (sermons, events, volunteers, groups,
check-in, and more) in **Settings → Modules**, without reinstalling. Upgrades follow the
main repository's [upgrade guide](https://github.com/leveo/church4christ/blob/v1.7.0/docs/upgrade.md).

## Learn more

- [Small groups](https://github.com/leveo/church4christ/blob/v1.7.0/docs/features/groups.md)
- [People & households](https://github.com/leveo/church4christ/blob/v1.7.0/docs/features/people-households.md)
- [Putting it online with Cloudflare](https://github.com/leveo/church4christ/blob/v1.7.0/docs/setup.md)

## 中文简介

### 开源教会小组管理系统

为教会小组建一个家：公开小组目录、加入申请、定期聚会，聚会后用邮件里的清单点名。

- 公开或私密小组，私密小组对非成员完全不可见。
- 访客用姓名和邮箱登录（无需密码）即可申请加入，组长审核。
- 组长自己管理名单、申请和聚会，不需要后台权限。
- 没有邮箱的成员也能只用姓名加入。
- 每周、隔周或每月的定期聚会自动排进日历。
- 聚会结束后组长收到点名清单链接，勾选即可。
- 附带团契目录；支持 12 种界面语言。

本仓库是 [Church4Christ](https://github.com/leveo/church4christ) 的单一功能版本，不包含另外的代码。按上面的快速开始安装后，
得到的是完整的 Church4Christ v1.7.0，只预先开启了这一组功能；以后可以在「设置 → 模块」里开启更多功能。

## Questions and issues

Please open issues and questions in the [main repository](https://github.com/leveo/church4christ/issues), where all the code
lives. Report security problems privately through its
[security advisories](https://github.com/leveo/church4christ/security/advisories/new).

## License

[GNU GPL v3](LICENSE), the same license as Church4Christ.
