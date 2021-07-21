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
import * as React from 'react';
import { Button } from 'antd';
import { faUser, faTrashAlt } from '@fortawesome/free-solid-svg-icons';
import { FontAwesomeIcon } from '@fortawesome/react-fontawesome';

const styleWithText = { marginRight: '8px' } as React.CSSProperties;
const styleNoText = { marginRight: '8px', marginLeft: '8px' } as React.CSSProperties;

const iconUserWithText = <FontAwesomeIcon icon={faUser} style={styleWithText} />;
const iconUserNoText = <FontAwesomeIcon icon={faUser} style={styleNoText} />;
const iconTrashWithText = <FontAwesomeIcon icon={faTrashAlt} style={styleWithText}/>
const iconTrashNoText = <FontAwesomeIcon icon={faTrashAlt} style={styleNoText}/>

const sizeLarge = "large";

const typePrimary = "primary";
const typeDefault = "default";
const typeText = "text";

const titleSize = text => <div style={{ marginBottom: '10px' }}><i> {text} </i></div>;

// Não é necessário utilizar classes 'doc-exemple' elas são somente para exemplos dos estados hover, active e focus nesta documentação!

ReactDOM.render(
  <>
    <b>Primary - Filled</b>
    <br />
    <i>São botões para ações de alta importância dentro do sistema.</i>
    <br />
    <br />
    {titleSize('Tamanho padrão')}
    <Button type={typePrimary} size={sizeLarge} icon={iconUserWithText}>Enabled</Button>
    <Button type={typePrimary} size={sizeLarge} icon={iconUserWithText} disabled>Disabled</Button>
    <Button type={typePrimary} size={sizeLarge} icon={iconUserWithText} className="hover-button-primary-doc-exemple">Hover</Button>
    <Button type={typePrimary} size={sizeLarge} icon={iconUserWithText} className="pressed-button-primary-doc-exemple">Pressed</Button>
    <br />
    <Button type={typePrimary} size={sizeLarge} >Enabled</Button>
    <Button type={typePrimary} size={sizeLarge} disabled>Disabled</Button>
    <Button type={typePrimary} size={sizeLarge} className="hover-button-primary-doc-exemple">Hover</Button>
    <Button type={typePrimary} size={sizeLarge} className="pressed-button-primary-doc-exemple">Pressed</Button>
    <br />
    <Button type={typePrimary} size={sizeLarge} icon={iconUserNoText}/>
    <Button type={typePrimary} size={sizeLarge} icon={iconUserNoText} disabled />
    <Button type={typePrimary} size={sizeLarge} icon={iconUserNoText} className="hover-button-primary-doc-exemple" />
    <Button type={typePrimary} size={sizeLarge} icon={iconUserNoText} className="pressed-button-primary-doc-exemple" />
    <br />
    <br />
    {titleSize('Tamanho pequeno')}
    <Button type={typePrimary} icon={iconUserWithText}>Enabled</Button>
    <Button type={typePrimary} icon={iconUserWithText} disabled>Disabled</Button>
    <Button type={typePrimary} icon={iconUserWithText} className="hover-button-primary-doc-exemple">Hover</Button>
    <Button type={typePrimary} icon={iconUserWithText} className="pressed-button-primary-doc-exemple">Pressed</Button>
    <br />
    <Button type={typePrimary} >Enabled</Button>
    <Button type={typePrimary} disabled>Disabled</Button>
    <Button type={typePrimary} className="hover-button-primary-doc-exemple">Hover</Button>
    <Button type={typePrimary} className="pressed-button-primary-doc-exemple">Pressed</Button>
    <br />
    <Button type={typePrimary} icon={iconUserNoText}/>
    <Button type={typePrimary} icon={iconUserNoText} disabled />
    <Button type={typePrimary} icon={iconUserNoText} className="hover-button-primary-doc-exemple" />
    <Button type={typePrimary} icon={iconUserNoText} className="pressed-button-primary-doc-exemple" />
    <br />
    <br />
    <br />
    <b>Secundary - Outlined</b>
    <br />
    <i>São botões para ações de média importância dentro do sistema.</i>
    <br />
    <br />
    {titleSize('Tamanho padrão')}
    <Button type={typeDefault} size={sizeLarge} icon={iconUserWithText}>Enabled</Button>
    <Button type={typeDefault} size={sizeLarge} icon={iconUserWithText} disabled>Disabled</Button>
    <Button type={typeDefault} size={sizeLarge} icon={iconUserWithText} className="hover-button-default-doc-exemple">Hover</Button>
    <Button type={typeDefault} size={sizeLarge} icon={iconUserWithText} className="pressed-button-default-doc-exemple">Pressed</Button>
    <br />
    <Button type={typeDefault} size={sizeLarge} >Enabled</Button>
    <Button type={typeDefault} size={sizeLarge} disabled>Disabled</Button>
    <Button type={typeDefault} size={sizeLarge} className="hover-button-default-doc-exemple">Hover</Button>
    <Button type={typeDefault} size={sizeLarge} className="pressed-button-default-doc-exemple">Pressed</Button>
    <br />
    <Button type={typeDefault} size={sizeLarge} icon={iconUserNoText}/>
    <Button type={typeDefault} size={sizeLarge} icon={iconUserNoText} disabled />
    <Button type={typeDefault} size={sizeLarge} icon={iconUserNoText} className="hover-button-default-doc-exemple" />
    <Button type={typeDefault} size={sizeLarge} icon={iconUserNoText} className="pressed-button-default-doc-exemple" />
    <br />
    <br />
    {titleSize('Tamanho pequeno')}
    <Button type={typeDefault} icon={iconUserWithText}>Enabled</Button>
    <Button type={typeDefault} icon={iconUserWithText} disabled>Disabled</Button>
    <Button type={typeDefault} icon={iconUserWithText} className="hover-button-default-doc-exemple">Hover</Button>
    <Button type={typeDefault} icon={iconUserWithText} className="pressed-button-default-doc-exemple">Pressed</Button>
    <br />
    <Button type={typeDefault} >Enabled</Button>
    <Button type={typeDefault} disabled>Disabled</Button>
    <Button type={typeDefault} className="hover-button-default-doc-exemple">Hover</Button>
    <Button type={typeDefault} className="pressed-button-default-doc-exemple">Pressed</Button>
    <br />
    <Button type={typeDefault} icon={iconUserNoText}/>
    <Button type={typeDefault} icon={iconUserNoText} disabled />
    <Button type={typeDefault} icon={iconUserNoText} className="hover-button-default-doc-exemple" />
    <Button type={typeDefault} icon={iconUserNoText} className="pressed-button-default-doc-exemple" />
    <br />
    <br />
    <br />
    <b>Tertiary - Text</b>
    <br />
    <i>São botões para ações de menor importância para o sistema.</i>
    <br />
    <br />
    {titleSize('Tamanho padrão')}
    <Button type={typeText} size={sizeLarge} icon={iconUserWithText}>Enabled</Button>
    <Button type={typeText} size={sizeLarge} icon={iconUserWithText} disabled>Disabled</Button>
    <Button type={typeText} size={sizeLarge} icon={iconUserWithText} className="hover-button-default-doc-exemple">Hover</Button>
    <Button type={typeText} size={sizeLarge} icon={iconUserWithText} className="pressed-button-default-doc-exemple">Pressed</Button>
    <br />
    <Button type={typeText} size={sizeLarge} >Enabled</Button>
    <Button type={typeText} size={sizeLarge} disabled>Disabled</Button>
    <Button type={typeText} size={sizeLarge} className="hover-button-default-doc-exemple">Hover</Button>
    <Button type={typeText} size={sizeLarge} className="pressed-button-default-doc-exemple">Pressed</Button>
    <br />
    <Button type={typeText} size={sizeLarge} icon={iconUserNoText}/>
    <Button type={typeText} size={sizeLarge} icon={iconUserNoText} disabled />
    <Button type={typeText} size={sizeLarge} icon={iconUserNoText} className="hover-button-default-doc-exemple" />
    <Button type={typeText} size={sizeLarge} icon={iconUserNoText} className="pressed-button-default-doc-exemple" />
    <br />
    <br />
    {titleSize('Tamanho pequeno')}
    <Button type={typeText} icon={iconUserWithText}>Enabled</Button>
    <Button type={typeText} icon={iconUserWithText} disabled>Disabled</Button>
    <Button type={typeText} icon={iconUserWithText} className="hover-button-default-doc-exemple">Hover</Button>
    <Button type={typeText} icon={iconUserWithText} className="pressed-button-default-doc-exemple">Pressed</Button>
    <br />
    <Button type={typeText}>Enabled</Button>
    <Button type={typeText} disabled>Disabled</Button>
    <Button type={typeText} className="hover-button-default-doc-exemple">Hover</Button>
    <Button type={typeText} className="pressed-button-default-doc-exemple">Pressed</Button>
    <br />
    <Button type={typeText} icon={iconUserNoText}/>
    <Button type={typeText} icon={iconUserNoText} disabled />
    <Button type={typeText} icon={iconUserNoText} className="hover-button-default-doc-exemple" />
    <Button type={typeText} icon={iconUserNoText} className="pressed-button-default-doc-exemple" />
    <br />
    <br />
    <br />
    <b>Danger - Outlined</b>
    <br />
    <i>São botões de negativa utilizados somente no estágio de confirmação de uma ação</i>
    <br />
    <br />
    {titleSize('Tamanho padrão')}
    <Button danger size={sizeLarge} icon={iconTrashWithText}>Enabled</Button>
    <Button danger size={sizeLarge} icon={iconTrashWithText} disabled>Disabled</Button>
    <Button danger size={sizeLarge} icon={iconTrashWithText} className="hover-button-danger-doc-exemple">Hover</Button>
    <Button danger size={sizeLarge} icon={iconTrashWithText} className="pressed-button-danger-doc-exemple">Pressed</Button>
    <br />
    <Button danger size={sizeLarge}>Enabled</Button>
    <Button danger size={sizeLarge} disabled>Disabled</Button>
    <Button danger size={sizeLarge} className="hover-button-danger-doc-exemple">Hover</Button>
    <Button danger size={sizeLarge} className="pressed-button-danger-doc-exemple">Pressed</Button>
    <br />
    <Button danger size={sizeLarge} icon={iconTrashNoText} />
    <Button danger size={sizeLarge} icon={iconTrashNoText} disabled />
    <Button danger size={sizeLarge} icon={iconTrashNoText} className="hover-button-danger-doc-exemple" />
    <Button danger size={sizeLarge} icon={iconTrashNoText} className="pressed-button-danger-doc-exemple" />
    <br />
    <br />
    {titleSize('Tamanho pequeno')}
    <Button danger icon={iconTrashWithText}>Enabled</Button>
    <Button danger icon={iconTrashWithText} disabled>Disabled</Button>
    <Button danger icon={iconTrashWithText} className="hover-button-danger-doc-exemple">Hover</Button>
    <Button danger icon={iconTrashWithText} className="pressed-button-danger-doc-exemple">Pressed</Button>
    <br />
    <Button danger>Enabled</Button>
    <Button danger disabled>Disabled</Button>
    <Button danger className="hover-button-danger-doc-exemple">Hover</Button>
    <Button danger className="pressed-button-danger-doc-exemple">Pressed</Button>
    <br />
    <Button danger icon={iconTrashNoText} />
    <Button danger icon={iconTrashNoText} disabled />
    <Button danger icon={iconTrashNoText} className="hover-button-danger-doc-exemple" />
    <Button danger icon={iconTrashNoText} className="pressed-button-danger-doc-exemple" />
  </>,
  mountNode,
);
```
