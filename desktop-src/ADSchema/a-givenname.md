---
title: Given-Name-Attribut
description: Enthält den angegebenen Namen (Vorname) des Benutzers.
ms.assetid: acffe751-9911-4e80-8a26-351a21a6385e
ms.tgt_platform: multiple
keywords:
- AD-Schema für Given-Name-Attribut
- givenName-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Given-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a76ab181c6aaf03c2a497be1718df789bfddc6b0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859732"
---
# <a name="given-name-attribute"></a>Given-Name-Attribut

Enthält den angegebenen Namen (Vorname) des Benutzers.



| Eingabe | Wert |
|-------------------|---------------------------------------------|
| CN                | Vorname                                  |
| LDAP-Display-Name | givenName                                   |
| Size              | \-                                          |
| Berechtigung aktualisieren  | Domänen Administrator oder Konto Besitzer.      |
| Aktualisierungshäufigkeit  | Wenn der Benutzerdaten Satz erstellt wird.          |
| Attribute-Id      | 2.5.4.42                                    |
| System-ID-GUID    | f0f8ff8e-1191-11d0-a060-00aa006c33ed        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------------|
| Link-ID                | \-                                                                 |
| MAPI-Id                | 0x3a06                                                             |
| System-Only            | False                                                              |
| Ist-einwertig       | Richtig                                                               |
| Ist indiziert             | Richtig                                                               |
| Im globalen Katalog      | Richtig                                                               |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                       |
| Range-Lower            | 1                                                                  |
| Range-Upper            | 64                                                                 |
| Search-Flags           | 0x00000005                                                         |
| System-Flags           | 0x00000010                                                         |
| In verwendete Klassen        | [**Unternehmensperson**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                     |
| MAPI-Id                | 0x3a06                                                                                                                 |
| System-Only            | False                                                                                                                  |
| Ist-einwertig       | Richtig                                                                                                                   |
| Ist indiziert             | Richtig                                                                                                                   |
| Im globalen Katalog      | Richtig                                                                                                                   |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 64                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| In verwendete Klassen        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                     |
| MAPI-Id                | 0x3a06                                                                                                                 |
| System-Only            | False                                                                                                                  |
| Ist-einwertig       | Richtig                                                                                                                   |
| Ist indiziert             | Richtig                                                                                                                   |
| Im globalen Katalog      | Richtig                                                                                                                   |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 64                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| In verwendete Klassen        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                     |
| MAPI-Id                | 0x3a06                                                                                                                 |
| System-Only            | False                                                                                                                  |
| Ist-einwertig       | Richtig                                                                                                                   |
| Ist indiziert             | Richtig                                                                                                                   |
| Im globalen Katalog      | Richtig                                                                                                                   |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 64                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| In verwendete Klassen        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                     |
| MAPI-Id                | 0x3a06                                                                                                                 |
| System-Only            | False                                                                                                                  |
| Ist-einwertig       | Richtig                                                                                                                   |
| Ist indiziert             | Richtig                                                                                                                   |
| Im globalen Katalog      | Richtig                                                                                                                   |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 64                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| In verwendete Klassen        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                     |
| MAPI-Id                | 0x3a06                                                                                                                 |
| System-Only            | False                                                                                                                  |
| Ist-einwertig       | Richtig                                                                                                                   |
| Ist indiziert             | Richtig                                                                                                                   |
| Im globalen Katalog      | Richtig                                                                                                                   |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 64                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| In verwendete Klassen        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> |



 

 





