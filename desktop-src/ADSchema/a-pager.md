---
title: Telefon-Pager-Primary-Attribut
description: Die primäre Pagernummer.
ms.assetid: e5230e09-f76b-4d2a-b56b-d989d315f9bb
ms.tgt_platform: multiple
keywords:
- ad-Schema des Telefon-Pager-Primary-Attributs
- AD-Schema des Pagerattributs
topic_type:
- apiref
api_name:
- Phone-Pager-Primary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1ebfa52809d53ebf42679b303ebd03fb1f4056f725f08624269c3bdcca8683a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647870"
---
# <a name="phone-pager-primary-attribute"></a>Telefon-Pager-Primary-Attribut

Die primäre Pagernummer.



| Eingabe | Wert |
|-------------------|----------------------------------------------------------------------------------|
| CN                | Telefon-Pager-Primary                                                              |
| Ldap-Anzeigename | pager                                                                            |
| Size              | \-                                                                               |
| Aktualisieren von Berechtigungen  | Domänenadministrator oder Kontobesitzer.                                           |
| Updatehäufigkeit  | Wenn der Datensatz des Benutzers erstellt wird und die Telefonnummer geändert werden muss. |
| Attribute-Id      | 0.9.2342.19200300.100.1.42                                                       |
| System-ID-GUID    | f0f8ffa6-1191-11d0-a060-00aa006c33ed                                             |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                      |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------------|
| Link-ID                | \-                                                                 |
| MAPI-Id                | 0x3A21                                                             |
| System-Only            | False                                                              |
| Ist einwertig       | True                                                               |
| Ist indiziert             | False                                                              |
| Im globalen Katalog      | False                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                       |
| Range-Lower            | 1                                                                  |
| Range-Upper            | 64                                                                 |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| In verwendete Klassen        | [**Unternehmensperson**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A21                                                                                                                                                   |
| System-Only            | False                                                                                                                                                    |
| Ist einwertig       | True                                                                                                                                                     |
| Ist indiziert             | False                                                                                                                                                    |
| Im globalen Katalog      | False                                                                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| In verwendete Klassen        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A21                                                                                                                                                   |
| System-Only            | False                                                                                                                                                    |
| Ist einwertig       | True                                                                                                                                                     |
| Ist indiziert             | False                                                                                                                                                    |
| Im globalen Katalog      | False                                                                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| In verwendete Klassen        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A21                                                                                                                                                   |
| System-Only            | False                                                                                                                                                    |
| Is-Single-Valued       | True                                                                                                                                                     |
| Ist indiziert             | False                                                                                                                                                    |
| Im globalen Katalog      | False                                                                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| In verwendete Klassen        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A21                                                                                                                                                   |
| System-Only            | False                                                                                                                                                    |
| Is-Single-Valued       | True                                                                                                                                                     |
| Ist indiziert             | False                                                                                                                                                    |
| Im globalen Katalog      | False                                                                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| In verwendete Klassen        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A21                                                                                                                                                   |
| System-Only            | False                                                                                                                                                    |
| Is-Single-Valued       | True                                                                                                                                                     |
| Ist indiziert             | False                                                                                                                                                    |
| Im globalen Katalog      | False                                                                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| In verwendete Klassen        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Benutzer**](c-user.md)<br/> |



 

 





