---
title: Desktop-Profile-Attribut
description: Der Speicherort des Desktopprofils für einen Benutzer oder eine Gruppe von Benutzern. Wird nicht verwendet.
ms.assetid: cbab8930-ce18-4b9c-ad60-5875bb23b822
ms.tgt_platform: multiple
keywords:
- Desktop-Profile AD-Schema
- desktopProfile-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Desktop-Profile
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cc9157730bce827c51a8705385afa61a92abc1d0d8f874844ac74d57fc31557
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119925990"
---
# <a name="desktop-profile-attribute"></a>Desktop-Profile-Attribut

Der Speicherort des Desktopprofils für einen Benutzer oder eine Gruppe von Benutzern. Wird nicht verwendet.



| Eingabe | Wert |
|-------------------|---------------------------------------------|
| CN                | Desktop-Profile                             |
| Ldap-Anzeigename | desktopProfile                              |
| Size              | \-                                          |
| Aktualisieren von Berechtigungen  | \-                                          |
| Updatehäufigkeit  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.346                      |
| System-Id-Guid    | sechs65906-8ac6-11d0-afda-00c04fd930c9        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                                                                |
| System-Only            | Falsch                                                                                                                                                                             |
| Is-Single-Valued       | Richtig                                                                                                                                                                              |
| Ist indiziert             | Falsch                                                                                                                                                                             |
| Im globalen Katalog      | Falsch                                                                                                                                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                      |
| Range-Lower            | \-                                                                                                                                                                                |
| Range-Upper            | \-                                                                                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                                                                        |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                                                                |
| System-Only            | Falsch                                                                                                                                                                             |
| Is-Single-Valued       | Richtig                                                                                                                                                                              |
| Ist indiziert             | Falsch                                                                                                                                                                             |
| Im globalen Katalog      | Falsch                                                                                                                                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                      |
| Range-Lower            | \-                                                                                                                                                                                |
| Range-Upper            | \-                                                                                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                                                                        |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                 |
| MAPI-Id                | \-                                                                                                 |
| System-Only            | Falsch                                                                                              |
| Is-Single-Valued       | Richtig                                                                                               |
| Ist indiziert             | Falsch                                                                                              |
| Im globalen Katalog      | Falsch                                                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                       |
| Range-Lower            | \-                                                                                                 |
| Range-Upper            | \-                                                                                                 |
| Search-Flags           | 0x00000000                                                                                         |
| System-Flags           | 0x00000010                                                                                         |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                                                                |
| System-Only            | Falsch                                                                                                                                                                             |
| Is-Single-Valued       | Richtig                                                                                                                                                                              |
| Ist indiziert             | Falsch                                                                                                                                                                             |
| Im globalen Katalog      | Falsch                                                                                                                                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                      |
| Range-Lower            | \-                                                                                                                                                                                |
| Range-Upper            | \-                                                                                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                                                                        |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                                                                |
| System-Only            | Falsch                                                                                                                                                                             |
| Is-Single-Valued       | Richtig                                                                                                                                                                              |
| Ist indiziert             | Falsch                                                                                                                                                                             |
| Im globalen Katalog      | Falsch                                                                                                                                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                      |
| Range-Lower            | \-                                                                                                                                                                                |
| Range-Upper            | \-                                                                                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                                                                        |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                                                                |
| System-Only            | Falsch                                                                                                                                                                             |
| Is-Single-Valued       | Richtig                                                                                                                                                                              |
| Ist indiziert             | Falsch                                                                                                                                                                             |
| Im globalen Katalog      | Falsch                                                                                                                                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                      |
| Range-Lower            | \-                                                                                                                                                                                |
| Range-Upper            | \-                                                                                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                                                                        |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                                                                |
| System-Only            | Falsch                                                                                                                                                                             |
| Is-Single-Valued       | Richtig                                                                                                                                                                              |
| Ist indiziert             | Falsch                                                                                                                                                                             |
| Im globalen Katalog      | Falsch                                                                                                                                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                      |
| Range-Lower            | \-                                                                                                                                                                                |
| Range-Upper            | \-                                                                                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                                                                        |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**Benutzer**](c-user.md)<br/> |



 

 





