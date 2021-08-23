---
title: Memberattribut
description: Die Liste der Benutzer, die der Gruppe angehören.
ms.assetid: 0f5e249e-1fa1-4191-90e6-94c0b657b7fc
ms.tgt_platform: multiple
keywords:
- AD-Schema des Memberattributs
- Memberattribut AD-Schema
topic_type:
- apiref
api_name:
- Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1efe13163946cb5be6ca83b5d0c7f964b8d6b1981ce45f79166af01bd62e6c9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119705510"
---
# <a name="member-attribute"></a>Memberattribut

Die Liste der Benutzer, die der Gruppe angehören.



| Eingabe | Wert |
|-------------------|-------------------------------------------------------|
| CN                | Member                                                |
| Ldap-Anzeigename | Member                                                |
| Size              | \-                                                    |
| Aktualisieren von Berechtigungen  | Domänenadministrator                                  |
| Updatehäufigkeit  | Jedes Mal, wenn ein Benutzer einer Gruppe hinzugefügt oder daraus entfernt wird. |
| Attribute-Id      | 2.5.4.31                                              |
| System-ID-GUID    | bf9679c0-0de6-11d0-a285-00aa003049e2                  |
| Syntax            | [**Object(DS-DN)**](s-object-ds-dn.md)               |



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
|------------------------|-----------------------------------------------------------------------------------------|
| Link-ID                | 2                                                                                       |
| MAPI-Id                | 0x8009                                                                                  |
| System-Only            | False                                                                                   |
| Ist einwertig       | False                                                                                   |
| Ist indiziert             | False                                                                                   |
| Im globalen Katalog      | True                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000012                                                                              |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> [**Gruppe von Namen**](c-groupofnames.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | False                                                                                                                                 |
| Ist einwertig       | False                                                                                                                                 |
| Ist indiziert             | False                                                                                                                                 |
| Im globalen Katalog      | True                                                                                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> [**Gruppe von Namen**](c-groupofnames.md)<br/> [**MSMQ-Group**](c-msmq-group.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|-------------------------------------|
| Link-ID                | 2                                   |
| MAPI-Id                | 0x8009                              |
| System-Only            | False                               |
| Ist einwertig       | False                               |
| Ist indiziert             | False                               |
| Im globalen Katalog      | True                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000012                          |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | False                                                                                                                                 |
| Ist einwertig       | False                                                                                                                                 |
| Ist indiziert             | False                                                                                                                                 |
| Im globalen Katalog      | True                                                                                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> [**Gruppe von Namen**](c-groupofnames.md)<br/> [**MSMQ-Group**](c-msmq-group.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | False                                                                                                                                 |
| Ist einwertig       | False                                                                                                                                 |
| Ist indiziert             | False                                                                                                                                 |
| Im globalen Katalog      | True                                                                                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> [**Gruppe von Namen**](c-groupofnames.md)<br/> [**MSMQ-Group**](c-msmq-group.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | False                                                                                                                                 |
| Ist einwertig       | False                                                                                                                                 |
| Ist indiziert             | False                                                                                                                                 |
| Im globalen Katalog      | True                                                                                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> [**Gruppe von Namen**](c-groupofnames.md)<br/> [**MSMQ-Group**](c-msmq-group.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | False                                                                                                                                 |
| Ist einwertig       | False                                                                                                                                 |
| Ist indiziert             | False                                                                                                                                 |
| Im globalen Katalog      | True                                                                                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> [**Gruppe von Namen**](c-groupofnames.md)<br/> [**MSMQ-Group**](c-msmq-group.md)<br/> |



 

 





