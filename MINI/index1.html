const registerContainer = document.getElementById('register-container');
const loginContainer = document.getElementById('login-container');
const compressorContainer = document.getElementById('compressor-container');

const registerForm = document.getElementById('register-form');
const loginForm = document.getElementById('login-form');

const uploadInput = document.getElementById('upload');
const canvas = document.getElementById('canvas');
const ctx = canvas.getContext('2d');
const compressBtn = document.getElementById('compress');
const qualitySlider = document.getElementById('quality');
const qualityValue = document.getElementById('quality-value');
const sizeInfo = document.getElementById('size-info');
const compressedImageDiv = document.getElementById('compressed-image');

let registeredUsers = {};

function isValidPassword(password) {
  const startsWithCapital = /^[A-Z]/.test(password);
  const hasNumber = /[0-9]/.test(password);
  const hasSpecial = /[^A-Za-z0-9]/.test(password);
  return startsWithCapital && hasNumber && hasSpecial;
}

// Registration
registerForm.addEventListener('submit', (e) => {
  e.preventDefault();
  const name = document.getElementById('name').value;
  const age = document.getElementById('age').value;
  const dob = document.getElementById('dob').value;
  const gender = document.getElementById('gender').value;
  const username = document.getElementById('reg-username').value;
  const password = document.getElementById('reg-password').value;

  if (!isValidPassword(password)) {
    alert("❌ Password must start with a capital letter, contain at least one number, and one special character.");
    return;
  }

  registeredUsers[username] = { password, name, age, dob, gender };
  alert("✅ Registration successful! Please login.");
  showLogin();
});

// Login
loginForm.addEventListener('submit', (e) => {
  e.preventDefault();
  const username = document.getElementById('username').value;
  const password = document.getElementById('password').value;

  if (!registeredUsers[username] || registeredUsers[username].password !== password) {
    alert("❌ Invalid username or password.");
    return;
  }

  loginContainer.style.display = "none";
  compressorContainer.style.display = "block";
});

// Toggle Views
function showLogin() {
  registerContainer.style.display = "none";
  loginContainer.style.display = "block";
  compressorContainer.style.display = "none";
}

// Image Compression
qualitySlider.addEventListener('input', () => {
  qualityValue.textContent = qualitySlider.value;
});

uploadInput.addEventListener('change', (e) => {
  const file = e.target.files[0];
  const reader = new FileReader();
  reader.onload = function (event) {
    const img = new Image();
    img.onload = function () {
      const scale = 0.8;
      canvas.width = img.width * scale;
      canvas.height = img.height * scale;
      ctx.drawImage(img, 0, 0, canvas.width, canvas.height);
    };
    img.src = event.target.result;
  };
  reader.readAsDataURL(file);
});

compressBtn.addEventListener('click', () => {
  if (!uploadInput.files.length) {
    alert("Please upload an image first.");
    return;
  }

  const quality = parseFloat(qualitySlider.value);

  canvas.toBlob((blob) => {
    const url = URL.createObjectURL(blob);
    const originalSize = (uploadInput.files[0].size / 1024).toFixed(2);
    const compressedSize = (blob.size / 1024).toFixed(2);

    sizeInfo.textContent = `Original size: ${originalSize} KB | Compressed size: ${compressedSize} KB | Reduced: ${(originalSize - compressedSize).toFixed(2)} KB`;

    const link = document.createElement('a');
    link.href = url;
    link.download = "compressed-image.jpg";
    link.textContent = "Download Compressed Image";
    link.style.display = "block";
    link.style.marginTop = "10px";

    const preview = new Image();
    preview.src = url;
    preview.style.maxWidth = "100%";
    preview.style.marginTop = "10px";

    compressedImageDiv.innerHTML = "";
    compressedImageDiv.appendChild(preview);
    compressedImageDiv.appendChild(link);
  }, 'image/jpeg', quality);
});
