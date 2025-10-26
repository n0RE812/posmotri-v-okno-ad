*,
*::before,
*::after {
  box-sizing: border-box;
}

html {
  block-size: 100%;
}

body {
  margin: 0;
  padding: 0;
}

.page {
  inline-size: 1200px;
  block-size: 100%;
  margin: auto;
  color: #fff;
  font-family: 'Fira Sans Condensed', sans-serif;
  font-size: 18px;
  background-color: #1b1919;
  display: flex;
  justify-content: center;
  align-items: center;
}

h1,
h2,
h3,
h4,
p,
ul,
ol,
li,
blockquote,
fieldset {
  margin: 0;
  padding: 0;
}

ul,
ol {
  list-style: none;
}

.visually-hidden {
  position: absolute;
  inline-size: 1px;
  block-size: 1px;
  overflow: hidden;
  clip: rect(0 0 0 0);
  clip-path: inset(50%);
  white-space: nowrap;
}

.content {
  display: grid;
  grid-template-columns: 1fr 399px;
  grid-template-rows: auto 1fr;
  gap: 30px;
  align-items: end;
  inline-size: 1140px;
  block-size: 534px;
  grid-template-areas: 
    "result details"
    "result details";
}

.result {
  grid-area: result;
  display: flex;
  flex-direction: column;
  gap: 16px;
}

.result__video-container {
  position: relative;
  inline-size: 711px;
  block-size: 386px;
}

.result__video {
  inline-size: 100%;
  block-size: 100%;
  object-fit: cover;
  object-position: center;
}

.search-form {
  display: flex;
  align-items: flex-start;
  gap: 40px;
}

.search-form__fieldset {
  border: none;
  display: flex;
  flex-direction: column;
  gap: 5px;
}

.search-form__fieldset-title {
  font-size: 18px;
  font-weight: 400;
  line-height: 1;
}

.search-form__label {
  display: flex;
  align-items: center;
  gap: 5px;
  cursor: pointer;
  width: fit-content;
}

.search-form__label:has(.search-form__textfield) {
  flex-direction: column;
  align-items: flex-start;
  width: 225px;
}

.search-form__label-text {
  font-size: 18px;
  font-weight: 400;
  color: #fff;
}

.search-form__label:hover .search-form__label-text {
  text-decoration: underline;
}

.search-form__textfield {
  appearance: none;
  background: transparent;
  border: none;
  border-top: 1px solid #fff;
  border-bottom: 1px solid #fff;
  color: #fff;
  font-family: inherit;
  font-size: 18px;
  padding: 2px 0;
  width: 100%;
  min-height: 27px;
}

.search-form__textfield::placeholder {
  color: rgba(255, 255, 255, 0.7);
}

.search-form__textfield:focus {
  outline: none;
}

.search-form__label:has(:focus-visible) {
  outline: 1px solid #fff;
  outline-offset: 1px;
}

.search-form__checkbox-list {
  display: flex;
  gap: 15px;
}

.search-form__pseudo-checkbox {
  position: relative;
  display: inline-block;
  width: 19px;
  height: 19px;
  background-color: #000;
  border: 1px solid #fff;
  flex-shrink: 0;
}

.search-form__pseudo-checkbox::after {
  content: '';
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 15px;
  height: 15px;
  background-color: #fff;
  opacity: 0;
}

.search-form__checkbox:checked + .search-form__pseudo-checkbox::after {
  opacity: 1;
}

.search-form__label:has(.search-form__checkbox:focus-visible) {
  outline: 1px solid #fff;
  outline-offset: 1px;
}

.button {
  background: transparent;
  border: 1px solid #fff;
  color: #fff;
  font-family: 'Fira Sans Condensed', sans-serif;
  font-size: 18px;
  font-weight: 400;
  text-align: center;
  cursor: pointer;
  appearance: none;
  display: block;
  min-height: 34px;
}

.button:focus {
  outline: none;
}

.button:hover {
  text-decoration: underline;
}

.button:active {
  background: #545050;
  text-decoration: none;
}

.button:focus-visible {
  outline: 1px solid #fff;
  outline-offset: 1px;
}

.search-form__submit-button {
  align-self: flex-end;
  padding: 6px 73px;
}

.more-button {
  width: 100%;
  padding: 6px 0;
  margin-top: 30px;
}

.content__details {
  grid-area: details;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  width: 100%;
  height: 100%;
}

.content__list-container {
  position: relative;
  height: 298px;
  overflow-y: auto;
}

.content__list-container::-webkit-scrollbar {
  width: 4px;
}

.content__list-container::-webkit-scrollbar-track {
  background: rgb(217 217 217 / 10%);
}

.content__list-container::-webkit-scrollbar-thumb {
  background-color: #D9D9D9;
}

.content__list {
  display: flex;
  flex-direction: column;
  gap: 30px;
}

.content__list-item {
  padding: 0 3px;
}

.content__card-link {
  display: block;
  color: #fff;
  text-decoration: none;
  padding: 2px;
  cursor: pointer;
}

.content__card-link_current {
  background: #545050;
}

.content__card-link:hover {
  text-decoration: underline;
}

.content__card-link:hover .content__video-card-title,
.content__card-link:hover .content__video-card-description {
  text-decoration: inherit;
}

.content__card-link:focus {
  outline: none;
}

.content__card-link:focus-visible {
  outline: 1px solid #fff;
  outline-offset: 1px;
}

.content__card-link:active {
  background: #545050;
  text-decoration: none;
}

.content__video-card {
  display: flex;
  align-items: flex-start;
  gap: 10px;
}

.content__video-card-description-container {
  flex-grow: 1;
  min-width: 0;
}

.content__video-card-title {
  font-family: 'Oswald', sans-serif;
  font-size: 30px;
  font-weight: 700;
  line-height: 1;
  text-transform: uppercase;
  margin-bottom: 6px;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}

.content__video-card-description {
  font-size: 18px;
  font-weight: 400;
  line-height: 0.9;
  display: -webkit-box;
  -webkit-line-clamp: 4;
  -webkit-box-orient: vertical;
  overflow: hidden;
}

.content__video-card-thumbnail {
  width: 194px;
  height: 103px;
  object-fit: cover;
  object-position: center;
  flex-shrink: 0;
}

.title {
  font-family: 'Oswald', sans-serif;
  font-size: 75px;
  font-weight: 700;
  line-height: 0.94;
  text-transform: uppercase;
  margin-bottom: 20px;
}

.content__accent {
  color: #545050;
}
