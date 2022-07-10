```js:title=app.js
const themeToggleBtn = document.querySelector('.js-theme-toggle');

themeToggleBtn.addEventListener('click', () => onToggleClick());

const onToggleClick = () => {
  const { theme } = document.documentElement.dataset;
  const themeTo = theme && theme === 'light' ? 'dark' : 'light';
  const label = `Activate ${theme} mode`;

  document.documentElement.setAttribute('data-theme', themeTo);
  localStorage.setItem('theme', themeTo);

  themeToggleBtn.setAttribute('aria-label', label);
  themeToggleBtn.setAttribute('title', label);
};
```

## Resources
