- Handle file input with FileReader()

```js
// File size limit (500 KB)
const FILE_SIZE_LIMIT = 500 * 1024;

// Function to check file size and display the image
function checkFileSize(file) {
  if (!file) return;

  if (file.size > FILE_SIZE_LIMIT) {
    // Show error if file size exceeds limit
    sizeWarning.style.display = "none";
    fileError.style.display = "block";
    btnContainer.style.display = "none";
    dragText.style.display = "block";
    return;
  }

  // Preview the uploaded image
  const reader = new FileReader();
  reader.readAsDataURL(file);
  reader.onload = () => {
    uploadedImg.src = reader.result;
    avatar.src = reader.result;
    uploadedImg.style.display = "block";
    uploadIcon.style.display = "none";
    btnContainer.style.display = "block";
    dragText.style.display = "none";
  };
}

// Handle drag and drop events
label.addEventListener("dragover", (e) => {
  e.preventDefault();
  label.classList.add("dragOver");
});

label.addEventListener("dragleave", (e) => {
  e.preventDefault();
  label.classList.remove("dragOver");
});

label.addEventListener("drop", (e) => {
  e.preventDefault();
  label.classList.remove("dragOver");
  const file = e.dataTransfer.files[0];
  checkFileSize(file); // Validate file size
});

// Handle file selection via upload input
uploadLabel.addEventListener("change", () => {
  const file = uploadLabel.files[0];
  checkFileSize(file); // Validate file size
});
```