<wizard-report>
# PostHog post-wizard report

The wizard has completed a deep integration of your project. Six new client-side analytics events were added to `index.html` to supplement the four events already in place. Three HTML sections received `id` attributes (`curriculum`, `bonuses`, `about`) so they could be observed by `IntersectionObserver`. A new PostHog tracking script block was appended that fires video-progress milestones (25 / 50 / 75 / 100 %), a video-ended event, and four section-viewed events as visitors scroll down the landing page. Environment variables (`POSTHOG_API_KEY`, `POSTHOG_HOST`) were written to `.env` and covered by `.gitignore`.

| Event | Description | File |
|---|---|---|
| `cta clicked` *(existing)* | Fires on every `.shiny-btn` anchor click; captures `cta_text` and `cta_href`. | `index.html` |
| `video played` *(existing)* | Fires when the hero VSL video starts playing. | `index.html` |
| `pricing viewed` *(existing)* | Fires once when the pricing section enters the viewport. | `index.html` |
| `faq item expanded` *(existing)* | Fires when a FAQ `<details>` element is opened; captures the question text. | `index.html` |
| `video progress` | Fires at 25 %, 50 %, 75 %, and 100 % of the hero video duration; captures `video_id` and `percent`. | `index.html` |
| `video ended` | Fires when the hero VSL video plays to completion; captures `video_id`. | `index.html` |
| `testimonials section viewed` | Fires once when the reviews section scrolls into view. | `index.html` |
| `curriculum section viewed` | Fires once when the "What We Cover" section scrolls into view. | `index.html` |
| `bonuses section viewed` | Fires once when the "Free Bonuses Inside" section scrolls into view. | `index.html` |
| `about section viewed` | Fires once when the "Meet Kyle" section scrolls into view. | `index.html` |

## Next steps

We've built some insights and a dashboard for you to keep an eye on user behavior, based on the events we just instrumented:

- **Dashboard – Analytics basics**: https://us.posthog.com/project/409251/dashboard/1542362
- **Conversion Funnel: Pricing → CTA**: https://us.posthog.com/project/409251/insights/bfSYbk5O
- **Video Engagement Funnel**: https://us.posthog.com/project/409251/insights/hYSRpuZo
- **Full Page Conversion Funnel**: https://us.posthog.com/project/409251/insights/24skRMkx
- **CTA Clicks Over Time**: https://us.posthog.com/project/409251/insights/87CL5Ajw
- **Top FAQ Questions**: https://us.posthog.com/project/409251/insights/9VjpCILE

### Agent skill

We've left an agent skill folder in your project. You can use this context for further agent development when using Claude Code. This will help ensure the model provides the most up-to-date approaches for integrating PostHog.

</wizard-report>
