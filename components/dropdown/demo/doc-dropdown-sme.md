---
order: -1
title:
  zh-CN:
  en-US: Padrão - SME
---

## zh-CN

## en-US

Os botões permitem que o usuário realize ações e façam escolhas dentro do sistema. Os botões podem ser aplicados em diversos lugares como Cards, Modal e Forms.

```jsx
import { Menu, Dropdown, Button, message, Space, Tooltip } from 'antd';
import { DownOutlined, UserOutlined } from '@ant-design/icons';
import { faUser, faTrashAlt } from '@fortawesome/free-solid-svg-icons';
import { FontAwesomeIcon } from '@fortawesome/react-fontawesome';

const styleIcon = { marginRight: '8px' } as React.CSSProperties;

const iconUser = <FontAwesomeIcon icon={faUser} style={styleIcon}/>;
const iconTrash = <FontAwesomeIcon icon={faTrashAlt} style={styleIcon}/>

const sizeLarge = "large";

const typePrimary = "primary";
const typeDefault = "default";

function handleButtonClick(e) {
  message.info('Click on left button.');
  console.log('click left button', e);
}

function handleMenuClick(e) {
  message.info('Click on menu item.');
  console.log('click', e);
}

const titleSize = text => <div style={{ marginBottom: '10px' }}><i> {text} </i></div>;

const menu = (
  <Menu onClick={handleMenuClick}>
    <Menu.Item key="1" icon={<UserOutlined />}>
      1st menu item
    </Menu.Item>
    <Menu.Item key="2" icon={<UserOutlined />}>
      2nd menu item
    </Menu.Item>
    <Menu.Item key="3" icon={<UserOutlined />}>
      3rd menu item
    </Menu.Item>
  </Menu>
);

ReactDOM.render(
  <>
    <b>Primary - Filled</b>
    <br />
    <i>São botões para ações de alta importância dentro do sistema com menu contextual</i>
    <br />
    <br />
    {titleSize('Tamanho padrão')}
    <Dropdown.Button
      overlay={menu}
      trigger={['click']}
      type={typePrimary}
      typeLeftButton="primary-dropdown"
      iconLeftButton={iconUser}
      size={sizeLarge}
    >
      Enabled
    </Dropdown.Button>
    <Dropdown.Button
      onClick={handleButtonClick}
      overlay={menu}
      iconLeftButton={iconUser}
      size={sizeLarge} disabled
    >
      Disabled
    </Dropdown.Button>
    <br />
    <Dropdown.Button
      overlay={menu}
      trigger={['click']}
      type={typePrimary}
      typeLeftButton="primary-dropdown"
      size={sizeLarge}
    >
      Enabled
    </Dropdown.Button>
    <Dropdown.Button
      onClick={handleButtonClick}
      overlay={menu}
      size={sizeLarge} disabled
    >
      Disabled
    </Dropdown.Button>
    <br />
    <br />
    {titleSize('Tamanho pequeno')}
    <Dropdown.Button
      overlay={menu}
      trigger={['click']}
      type={typePrimary}
      typeLeftButton="primary-dropdown"
      iconLeftButton={iconUser}
    >
      Enabled
    </Dropdown.Button>
    <Dropdown.Button
      onClick={handleButtonClick}
      overlay={menu}
      iconLeftButton={iconUser}
      disabled
    >
      Disabled
    </Dropdown.Button>
    <br />
    <Dropdown.Button
      overlay={menu}
      trigger={['click']}
      type={typePrimary}
      typeLeftButton="primary-dropdown"
    >
      Enabled
    </Dropdown.Button>
    <Dropdown.Button
      onClick={handleButtonClick}
      overlay={menu}
      disabled
    >
      Disabled
    </Dropdown.Button>
    <br />
    <br />
    <br />
    <b>Secundary - Outlined</b>
    <br />
    <i>São botões para ações de média importância dentro do sistema com menu contextual</i>
    <br />
    <br />
    {titleSize('Tamanho padrão')}
    <Dropdown.Button
      overlay={menu}
      trigger={['click']}
      type={typeDefault}
      typeLeftButton="default-dropdown"
      iconLeftButton={iconUser}
      size={sizeLarge}
    >
      Enabled
    </Dropdown.Button>
    <Dropdown.Button
      type={typeDefault}
      typeLeftButton="default-dropdown"
      iconLeftButton={iconUser}
      size={sizeLarge}
      disabled
    >
      Disabled
    </Dropdown.Button>
    <br />
    <Dropdown.Button
      overlay={menu}
      trigger={['click']}
      type={typeDefault}
      typeLeftButton="default-dropdown"
      size={sizeLarge}
    >
      Enabled
    </Dropdown.Button>
    <Dropdown.Button
      type={typeDefault}
      typeLeftButton="default-dropdown"
      size={sizeLarge}
      disabled
    >
      Disabled
    </Dropdown.Button>
    <br />
    <br />
    {titleSize('Tamanho pequeno')}
    <Dropdown.Button
      overlay={menu}
      trigger={['click']}
      type={typeDefault}
      typeLeftButton="default-dropdown"
      iconLeftButton={iconUser}
    >
      Enabled
    </Dropdown.Button>
    <Dropdown.Button
      type={typeDefault}
      typeLeftButton="default-dropdown"
      iconLeftButton={iconUser}
      disabled
    >
      Disabled
    </Dropdown.Button>
    <br />
    <Dropdown.Button
      overlay={menu}
      trigger={['click']}
      type={typeDefault}
      typeLeftButton="default-dropdown"
    >
      Enabled
    </Dropdown.Button>
    <Dropdown.Button
      type={typeDefault}
      typeLeftButton="default-dropdown"
      disabled
    >
      Disabled
    </Dropdown.Button>
    <br />
    <br />
    <br />
    <b>Danger - Outlined</b>
    <br />
    <i>São botões de negativa utilizados somente no estágio de confirmação de uma ação com menu contextual</i>
    <br />
    <br />
    {titleSize('Tamanho padrão')}
    <Dropdown.Button
      overlay={menu}
      trigger={['click']}
      type={typeDefault}
      typeLeftButton="danger-dropdown"
      iconLeftButton={iconTrash}
      size={sizeLarge}
      danger
    >
      Enabled
    </Dropdown.Button>
    <Dropdown.Button
      type={typeDefault}
      typeLeftButton="danger-dropdown"
      iconLeftButton={iconTrash}
      size={sizeLarge}
      danger
      disabled
    >
      Disabled
    </Dropdown.Button>
    <br />
    <Dropdown.Button
      overlay={menu}
      trigger={['click']}
      type={typeDefault}
      typeLeftButton="danger-dropdown"
      size={sizeLarge}
      danger
    >
      Enabled
    </Dropdown.Button>
    <Dropdown.Button
      type={typeDefault}
      typeLeftButton="danger-dropdown"
      size={sizeLarge}
      danger
      disabled
    >
      Disabled
    </Dropdown.Button>
    <br />
    <br />
    {titleSize('Tamanho pequeno')}
    <Dropdown.Button
      overlay={menu}
      trigger={['click']}
      type={typeDefault}
      typeLeftButton="danger-dropdown"
      iconLeftButton={iconTrash}
      danger
    >
      Enabled
    </Dropdown.Button>
    <Dropdown.Button
      type={typeDefault}
      typeLeftButton="danger-dropdown"
      iconLeftButton={iconTrash}
      danger
      disabled
    >
      Disabled
    </Dropdown.Button>
    <br />
        <Dropdown.Button
      overlay={menu}
      trigger={['click']}
      type={typeDefault}
      typeLeftButton="danger-dropdown"
      danger
    >
      Enabled
    </Dropdown.Button>
    <Dropdown.Button
      type={typeDefault}
      typeLeftButton="danger-dropdown"
      danger
      disabled
    >
      Disabled
    </Dropdown.Button>
  </>,
  mountNode,
);
```
