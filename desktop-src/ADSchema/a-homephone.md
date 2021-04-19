---
title: Telefon-Home-Primary-Attribut
description: Die Haupt Telefonnummer des Benutzers.
ms.assetid: 624d89fd-942c-448d-bd51-7d93954370b1
ms.tgt_platform: multiple
keywords:
- "\"Phone-Home-Primary Attribute ad Schema\""
- AD-Schema für HomePhone-Attribut
topic_type:
- apiref
api_name:
- Phone-Home-Primary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c2d2e68116a15dcbf4431d33bb56b4ffed8ee2e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106346568"
---
# <a name="phone-home-primary-attribute"></a>Telefon-Home-Primary-Attribut

Die Haupt Telefonnummer des Benutzers.



| Eingabe | Wert |
|-------------------|----------------------------------------------------------------------------------|
| CN                | Telefon-Home-primär                                                               |
| LDAP-Display-Name | homePhone                                                                        |
| Size              | \-                                                                               |
| Berechtigung aktualisieren  | Domänen Administrator oder Konto Besitzer.                                           |
| Aktualisierungshäufigkeit  | Wenn der Benutzerdaten Satz erstellt und die Telefonnummer geändert werden muss. |
| Attribute-Id      | 0.9.2342.19200300.100.1.20                                                       |
| System-ID-GUID    | f0f8ffa1-1191-11d0-a060-00aa006c33ed                                             |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                      |



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
| MAPI-Id                | 0x3a09                                                             |
| System-Only            | False                                                              |
| Ist-einwertig       | Richtig                                                               |
| Ist indiziert             | False                                                              |
| Im globalen Katalog      | Richtig                                                               |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                       |
| Range-Lower            | 1                                                                  |
| Range-Upper            | 64                                                                 |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| In verwendete Klassen        | [**Unternehmensperson**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3a09                                                                                                                                                   |
| System-Only            | False                                                                                                                                                    |
| Ist-einwertig       | Richtig                                                                                                                                                     |
| Ist indiziert             | False                                                                                                                                                    |
| Im globalen Katalog      | Richtig                                                                                                                                                     |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| In verwendete Klassen        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3a09                                                                                                                                                   |
| System-Only            | False                                                                                                                                                    |
| Ist-einwertig       | Richtig                                                                                                                                                     |
| Ist indiziert             | False                                                                                                                                                    |
| Im globalen Katalog      | Richtig                                                                                                                                                     |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| In verwendete Klassen        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3a09                                                                                                                                                   |
| System-Only            | False                                                                                                                                                    |
| Ist-einwertig       | Richtig                                                                                                                                                     |
| Ist indiziert             | False                                                                                                                                                    |
| Im globalen Katalog      | Richtig                                                                                                                                                     |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| In verwendete Klassen        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3a09                                                                                                                                                   |
| System-Only            | False                                                                                                                                                    |
| Ist-einwertig       | Richtig                                                                                                                                                     |
| Ist indiziert             | False                                                                                                                                                    |
| Im globalen Katalog      | Richtig                                                                                                                                                     |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| In verwendete Klassen        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3a09                                                                                                                                                   |
| System-Only            | False                                                                                                                                                    |
| Ist-einwertig       | Richtig                                                                                                                                                     |
| Ist indiziert             | False                                                                                                                                                    |
| Im globalen Katalog      | Richtig                                                                                                                                                     |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| In verwendete Klassen        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Benutzer**](c-user.md)<br/> |



 

 





