---
title: User-Password-Attribut
description: Das Kennwort des Benutzers im UTF-8-Format. Dies ist ein Schreib geschütztes Attribut.
ms.assetid: fcbd5e46-93fc-461e-aa6e-26d08114e73a
ms.tgt_platform: multiple
keywords:
- AD-Schema für User-Password-Attribut
- userPassword-Attribut AD-Schema
topic_type:
- apiref
api_name:
- User-Password
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f84dbb0b8bbc9ebf6995738050cddb226049658b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106346555"
---
# <a name="user-password-attribute"></a>User-Password-Attribut

Das Kennwort des Benutzers im UTF-8-Format. Dies ist ein Schreib geschütztes Attribut.



| Eingabe | Wert |
|-------------------|-------------------------------------------------------|
| CN                | User-Password                                         |
| LDAP-Display-Name | User Password                                          |
| Size              | \-                                                    |
| Berechtigung aktualisieren  | Domänen Administrator oder Konto Besitzer.                |
| Aktualisierungshäufigkeit  | \-                                                    |
| Attribute-Id      | 2.5.4.35                                              |
| System-ID-GUID    | bf967a6e-0de6-11d0-a285-00aa003049e2                  |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                     |
| MAPI-Id                | 0x8153                                                                                                                                                 |
| System-Only            | False                                                                                                                                                  |
| Ist-einwertig       | False                                                                                                                                                  |
| Ist indiziert             | False                                                                                                                                                  |
| Im globalen Katalog      | False                                                                                                                                                  |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                           |
| Range-Lower            | 1                                                                                                                                                      |
| Range-Upper            | 128                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                             |
| System-Flags           | 0x00000010                                                                                                                                             |
| In verwendete Klassen        | [**Organisation**](c-organization.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Person**](c-person.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                       |
| MAPI-Id                | 0x8153                                                                                                                                                                                                                   |
| System-Only            | False                                                                                                                                                                                                                    |
| Ist-einwertig       | False                                                                                                                                                                                                                    |
| Ist indiziert             | False                                                                                                                                                                                                                    |
| Im globalen Katalog      | False                                                                                                                                                                                                                    |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                                                                                        |
| Range-Upper            | 128                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                                                                                               |
| In verwendete Klassen        | [**Organisation**](c-organization.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Person**](c-person.md)<br/> [**simplesecurityobject**](c-simplesecurityobject.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                               |
| MAPI-Id                | 0x8153                                                                                                           |
| System-Only            | False                                                                                                            |
| Ist-einwertig       | False                                                                                                            |
| Ist indiziert             | False                                                                                                            |
| Im globalen Katalog      | False                                                                                                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                     |
| Range-Lower            | 1                                                                                                                |
| Range-Upper            | 128                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                       |
| System-Flags           | 0x00000010                                                                                                       |
| In verwendete Klassen        | [**Organisation**](c-organization.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                           |
| MAPI-Id                | 0x8153                                                                                                                                                                                                                                                                                                                                                                       |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                        |
| Ist-einwertig       | False                                                                                                                                                                                                                                                                                                                                                                        |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                        |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                                                                                                                        |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                                 |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                            |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                   |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                   |
| In verwendete Klassen        | [**Organisation**](c-organization.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Person**](c-person.md)<br/> [**simplesecurityobject**](c-simplesecurityobject.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixgroup**](c-posixgroup.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                           |
| MAPI-Id                | 0x8153                                                                                                                                                                                                                                                                                                                                                                       |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                        |
| Ist-einwertig       | False                                                                                                                                                                                                                                                                                                                                                                        |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                        |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                                                                                                                        |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                                 |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                            |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                   |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                   |
| In verwendete Klassen        | [**Organisation**](c-organization.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Person**](c-person.md)<br/> [**simplesecurityobject**](c-simplesecurityobject.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixgroup**](c-posixgroup.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                           |
| MAPI-Id                | 0x8153                                                                                                                                                                                                                                                                                                                                                                       |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                        |
| Ist-einwertig       | False                                                                                                                                                                                                                                                                                                                                                                        |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                        |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                                                                                                                        |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                                 |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                            |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                   |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                   |
| In verwendete Klassen        | [**Organisation**](c-organization.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Person**](c-person.md)<br/> [**simplesecurityobject**](c-simplesecurityobject.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixgroup**](c-posixgroup.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                           |
| MAPI-Id                | 0x8153                                                                                                                                                                                                                                                                                                                                                                       |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                        |
| Ist-einwertig       | False                                                                                                                                                                                                                                                                                                                                                                        |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                        |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                                                                                                                        |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                                 |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                            |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                   |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                   |
| In verwendete Klassen        | [**Organisation**](c-organization.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Person**](c-person.md)<br/> [**simplesecurityobject**](c-simplesecurityobject.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixgroup**](c-posixgroup.md)<br/> |



 

 





