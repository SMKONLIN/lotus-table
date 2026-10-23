# Lotus Table: GitHub Pages package

| Folder | What it is |
|---|---|
| `menu/` | The customer QR menu. Works for everyone, no sign-in. |
| `pos/`  | The staff POS (single-device mode, see the note below). |

## Put it online (no command line needed)
1. Sign in at github.com and click **New repository**. Name it `lotus-table`, choose **Public**, click **Create repository**.
2. Click **uploading an existing file**. Drag in everything from this folder (including the `menu` and `pos` folders and the `.nojekyll` file), then click **Commit changes**.
3. Go to **Settings, then Pages**. Under "Build and deployment" choose **Deploy from a branch**, branch **main**, folder **/ (root)**, and click **Save**.
4. Wait one to two minutes. Your site is at `https://smkonlin.github.io/lotus-table/`.
   - Customer menu: `.../lotus-table/menu/`
   - Staff POS: `.../lotus-table/pos/`

## The QR code
The POS is already set to your address (`https://smkonlin.github.io/lotus-table/menu/`), so **Menu, then QR menu** prints the correct code. This only works if the repository is named `lotus-table` and is public. If you use another repository name, open `pos/index.html` on GitHub, click the pencil, find the line starting `const MENU_URL=`, change the name, and commit.

## Important limits
- GitHub Pages only serves files. It has **no database**. The POS here saves data **only in the browser you use**, so two devices will not share orders, and clearing the browser data deletes everything. For several devices at once, keep using the Claude-hosted POS, or connect a free database (Firebase or Supabase).
- The repository is public, so anything in these files is public. Never put real PINs, passwords or customer details in them.
- To change a menu price or add a photo on the customer menu, edit `menu/index.html` on GitHub (or send the changes to me and I will prepare the file).
