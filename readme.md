Converts a string to a URL-friendly slug.

Use String.prototype.toLowerCase() and String.prototype.trim() to normalize the string.
Use String.prototype.replace() to replace spaces, dashes and underscores with - and remove special characters.

<code>
  const slugify = str =>
  str
    .toLowerCase()
    .trim()
    .replace(/[^\w\s-]/g, '')
    .replace(/[\s_-]+/g, '-')
    .replace(/^-+|-+$/g, '');
slugify('Hello World!'); // 'hello-world'
</code>
