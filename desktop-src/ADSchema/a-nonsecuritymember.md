---
title: Nicht-Sicherheitsmitglied-Attribut
description: Mitglieder einer Gruppe ohne Sicherheit. Wird für Exchange Verteilerlisten verwendet.
ms.assetid: 0db135e4-dcba-4afb-a174-3c7b2b40688e
ms.tgt_platform: multiple
keywords:
- AD-Schema des Nicht-Sicherheitsmitglieds
- nonSecurityMember-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Non-Security-Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dba59e37e4d4be5549e9ab5f36747f1cfd0046a9fb01ca91e2a9e79f353f148a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648380"
---
# <a name="non-security-member-attribute"></a>Nicht-Sicherheitsmitglied-Attribut

Mitglieder einer Gruppe ohne Sicherheit. Wird für Exchange Verteilerlisten verwendet.



| Eingabe | Wert |
|-------------------|--------------------------------------------------|
| CN                | Nicht-Sicherheitsmitglied                              |
| Ldap-Anzeigename | nonSecurityMember                                |
| Size              | \-                                               |
| Aktualisieren von Berechtigungen  | Domänenadministrator                             |
| Updatehäufigkeit  | Jedes Mal, wenn ein Benutzer der DL hinzugefügt oder daraus entfernt wird. |
| Attribute-Id      | 1.2.840.113556.1.4.530                           |
| System-Id-Guid    | 52458018-ca6a-11d0-afff-0000f80367c1             |
| Syntax            | [**Object(DS-DN)**](s-object-ds-dn.md)          |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|-------------------------------------|
| Link-ID                | 50                                  |
| MAPI-Id                | \-                                  |
| System-Only            | False                               |
| Is-Single-Valued       | False                               |
| Ist indiziert             | False                               |
| Im globalen Katalog      | False                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000010                          |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-------------------------------------|
| Link-ID                | 50                                  |
| MAPI-Id                | \-                                  |
| System-Only            | False                               |
| Is-Single-Valued       | False                               |
| Ist indiziert             | False                               |
| Im globalen Katalog      | False                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000010                          |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-------------------------------------|
| Link-ID                | 50                                  |
| MAPI-Id                | \-                                  |
| System-Only            | False                               |
| Is-Single-Valued       | False                               |
| Ist indiziert             | False                               |
| Im globalen Katalog      | False                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000010                          |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-------------------------------------|
| Link-ID                | 50                                  |
| MAPI-Id                | \-                                  |
| System-Only            | False                               |
| Ist einwertig       | False                               |
| Ist indiziert             | False                               |
| Im globalen Katalog      | False                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000010                          |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-------------------------------------|
| Link-ID                | 50                                  |
| MAPI-Id                | \-                                  |
| System-Only            | False                               |
| Ist einwertig       | False                               |
| Ist indiziert             | False                               |
| Im globalen Katalog      | False                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000010                          |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-------------------------------------|
| Link-ID                | 50                                  |
| MAPI-Id                | \-                                  |
| System-Only            | False                               |
| Ist einwertig       | False                               |
| Ist indiziert             | False                               |
| Im globalen Katalog      | False                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000010                          |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> |



 

 





