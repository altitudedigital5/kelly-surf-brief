# Al's Cowabunga Surf Report

Public static site for Kelly’s daily San Diego surf briefs.

- Live: https://d2gwgujzd9dqcv.cloudfront.net/
- Source: `docs/` (committed HTML/PDF)
- Deploy: GitHub Actions → S3 `kelly-surf-brief-891377350041` + CloudFront `EPG55OY8P0OQS` via OIDC (no long-lived AWS keys on the box)

## Kelly: publish after each AM brief

```bash
/home/box/kelly-surf/push-to-github.sh /home/box/kelly-surf/brief-YYYY-MM-DD.html /home/box/kelly-surf/brief-YYYY-MM-DD.pdf
```

That copies into `docs/`, commits, and pushes `main`. Actions updates the live site.
