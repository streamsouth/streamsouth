# streamsouth
## Development

First, run the development server:

```bash
pnpm dev
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

## Contribution

### NODE Manager (ในกรณีที่ต้องใช้งานใน NODE VERSION ต่างกัน)

#### NPM

> for [Windows](https://github.com/coreybutler/nvm-windows/releases)

> for [macOS/Linux](https://github.com/nvm-sh/nvm#install--update-script)

    ```bash
    install with curl
    curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash
    source ~/.bashrc
    //check version nodeJS
        nvm install 16.20 or <any version>
        nvm list
        nvm use 16.20
    ```

### Library Manager

- yarn
- pnpm

### CSS Framework

- MUI,ANTD

### CSS

- TAILWIND

### Naming

- `folder` - ไม่ต้องใส่ plural ในชื่อ ex. page, component ยกเว้น pages ของ nextjs,
  (กรณี Implement NPM Package อณุญาตให้ใส่ plural ได้ เนื่องจากเมื่อbuild จะซ้ำซ้อนกับ File build)
- `file & folder` - ต้องเป็น kebab-case เท่านั้น ex. `src/component/ui/navigation-bar/profile-badge.tsx`
- `Component & Class` - UpperCamelCase ex. `FunctionComponent`
- `variables` - camelCase ex. `variablesFirst`

### Folder Structure

- `src/component/ui` - component ที่เป็น ui พื้นฐานสำหรับ project เช่น button, container, modal, typo etc
- `src/component/page` - component ที่เก็บ page component สำหรับ render page ต่างๆ
- `src/component/common` - component ที่ใช้ร่วมกันหลายๆ page เช่น navbar, login popup etc
- `src/lib` or `src/util` - utility สำหรับ project ex.
- `src/hook` - common hook
- `src/model` - entity สำหรับ project นี้ ex. user
- `src/pages` - next route management
- `src/store` - global business logic must define here,
- `src/contexts` - context
- `src/styles` - global styles
- `src/vendor` - vendor source code
- `src/type` - reuse type
- `src/route` - (React) เก็บ route ของ React Router

### Module Export

- Don't use export default, use naming instead.

### Fetching

- Use SWR (nextjs), axios interceptor(Common),apollo (GraphQl)

### Localization

- Use i18nNext (language)

### Linter

- Use ESLINT,PRETTIER

# GIT

### Branch Name

- `feature/...` เปิด feature ใหม่
- `refactor/...` จัดระเบียบ code
- `fix-bug/...` แก้ไข
- `develop` ทุกbranch ต้อง pull request หรือ merge request ขึ้น develop ก่อนเสมอ
- `main` or `publish` or `release` pull request หรือ merge request เมื่อทดสอบใน develop แล้ว
