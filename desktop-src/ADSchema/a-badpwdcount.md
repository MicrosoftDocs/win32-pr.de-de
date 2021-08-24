---
title: Bad-Pwd-Count-Attribut
description: Gibt an, wie oft sich der Benutzer mit einem falschen Kennwort beim Konto anmeldet.
ms.assetid: 1161b0c1-1b28-4349-ad43-82ce68428c44
ms.tgt_platform: multiple
keywords:
- Bad-Pwd-Count-Attribut AD-Schema
- badPwdCount-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Bad-Pwd-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 608e587627bd8b470582e247bc8586e7e1576a2ff865a64bd9bd6fb60bd07c0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119081924"
---
# <a name="bad-pwd-count-attribute"></a>Bad-Pwd-Count-Attribut

Gibt an, wie oft sich der Benutzer mit einem falschen Kennwort beim Konto anmeldet. Der Wert 0 gibt an, dass der Wert unbekannt ist.



| Eingabe | Wert |
|-------------------|-------------------------------------------|
| CN                | Bad-Pwd-Count                             |
| Ldap-Anzeigename | badPwdCount                               |
| Size              | 4 Bytes                                   |
| Aktualisieren von Berechtigungen  | Dieser Wert wird vom System festgelegt.          |
| Updatehäufigkeit  | Jedes Mal, wenn der Benutzer ein fehlerhaftes Kennwort ein gibt. |
| Attribute-Id      | 1.2.840.113556.1.4.12                     |
| System-Id-Guid    | bf96792e-0de6-11d0-a285-00aa003049e2      |
| Syntax            | [**Enumeration**](s-enumeration.md)      |



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
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falsch                             |
| Is-Single-Valued       | Richtig                              |
| Ist indiziert             | Falsch                             |
| Im globalen Katalog      | Falsch                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000011                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falsch                             |
| Is-Single-Valued       | Richtig                              |
| Ist indiziert             | Falsch                             |
| Im globalen Katalog      | Falsch                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000011                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------|
| Link-ID                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | Richtig                                                              |
| Is-Single-Valued       | Richtig                                                              |
| Ist indiziert             | Falsch                                                             |
| Im globalen Katalog      | Falsch                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000011                                                        |
| In verwendete Klassen        | [**ms-DS-Bindable-Object**](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falsch                             |
| Ist einwertig       | Richtig                              |
| Ist indiziert             | Falsch                             |
| Im globalen Katalog      | Falsch                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000011                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falsch                             |
| Ist einwertig       | Richtig                              |
| Ist indiziert             | Falsch                             |
| Im globalen Katalog      | Falsch                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000011                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falsch                             |
| Ist einwertig       | Richtig                              |
| Ist indiziert             | Falsch                             |
| Im globalen Katalog      | Falsch                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000011                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falsch                             |
| Ist einwertig       | Richtig                              |
| Ist indiziert             | Falsch                             |
| Im globalen Katalog      | Falsch                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000011                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="remarks"></a>Hinweise

Dieses Attribut wird nicht repliziert und auf jedem Domänencontroller in der Domäne separat verwaltet.

Dieses Attribut wird auf einem bestimmten Domänencontroller zurückgesetzt, wenn sich der Benutzer erfolgreich bei diesem Domänencontroller anmeldet.

 

 





