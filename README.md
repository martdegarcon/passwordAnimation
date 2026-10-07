# Password Weight

A sign-up flow concept where **password strength is expressed through font weight** instead of a progress bar.

The heavier the password looks, the stronger it is.

**Live demo:** `https://<your-username>.github.io/password-weight/`

## Flow

1. **Log in.** The placeholder floats up into a label when the field gets focus.
2. **Email.** As you type, `@gmail.com` is suggested in grey; accept it with Tab, → or Enter.
3. **Checking.** The email is checked. When no account is found, the label reads *New account* and the screen turns into **Sign up**: the title morphs letter by letter, an explanation appears under it, and the button and link change their text.
4. **Password.** Focusing the password field slides in *Repeat password*. Strength changes the weight of the password and its label:

   | Strength | Weight |
   |----------|--------|
   | Weak     | 500 Medium |
   | Medium   | 700 Bold |
   | Strong   | 800 ExtraBold |

   The eye icon cross-fades the text into `****` and back.
5. **Repeat password.** Until it matches, the label shows *Passwords don’t match*, wrong characters turn red and the field gets a red outline. When it matches, the label shows *Passwords match*.
6. **Create account.** The button collapses into a circular loader, then expands, inverts and draws a check before showing *Account created*.

## Motion

Everything is plain CSS transitions on one easing curve (`cubic-bezier(.25,1,.5,1)`), so states blend into each other the way Figma Smart Animate does. The timings are CSS variables at the top of `styles.css`:

```css
--ease: cubic-bezier(.25,1,.5,1);
--move: .5s;   /* position / size */
--fade: .35s;  /* opacity / blur */
```

`prefers-reduced-motion` is respected.

## Stack

- HTML, CSS and vanilla JS, with no build step and no dependencies
- [Onest](https://fonts.google.com/specimen/Onest) variable font (100–900) from Google Fonts

## Run locally

Open `index.html` in a browser, or serve the folder:

```bash
npx serve .
```

## Deploy to GitHub Pages

1. Push the repo to GitHub.
2. Go to **Settings → Pages → Build and deployment → Deploy from a branch**.
3. Pick `main` and `/ (root)`, then save.

## Credits

Design and code by Marat Murzagaliev.

## License

MIT
# passwordAnimation
