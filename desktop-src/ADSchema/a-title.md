---
title: Titelattribut
description: Enthält die Position des Benutzers. Diese Eigenschaft wird häufig verwendet, um die formale Position anzugeben, z. B. Senior Programmer, anstatt die klasse , z. B. Programmierer. Sie wird in der Regel nicht für Suffixtitel wie Esq verwendet. oder DDS.
ms.assetid: 4a6899a7-ddbf-4dd0-b088-3739716f33df
ms.tgt_platform: multiple
keywords:
- Titelattribut AD-Schema
- TITLE-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Title
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8885a557e8fbec17d6d58d68fdea0f99039f0e09e34a8da01954dc7b4979fc3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119645030"
---
# <a name="title-attribute-ad-schema"></a>Titelattribut (AD-Schema)

Enthält die Position des Benutzers. Diese Eigenschaft wird häufig verwendet, um die formale Position anzugeben, z. B. Senior Programmer, anstatt die klasse , z. B. Programmierer. Sie wird in der Regel nicht für Suffixtitel wie Esq verwendet. oder DDS.



| Eingabe | Wert |
|-------------------|---------------------------------------------------------------------------|
| CN                | Titel                                                                     |
| Ldap-Anzeigename | title                                                                     |
| Size              | \-                                                                        |
| Aktualisieren von Berechtigungen  | Domänenadministrator oder Kontobesitzer.                                    |
| Updatehäufigkeit  | Wenn der Datensatz des Benutzers erstellt wird und wann immer der Titel geändert werden muss. |
| Attribute-Id      | 2.5.4.12                                                                  |
| System-ID-GUID    | bf967a55-0de6-11d0-a285-00aa003049e2                                      |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                               |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | False                                                                                                                           |
| Ist einwertig       | True                                                                                                                            |
| Ist indiziert             | False                                                                                                                           |
| Im globalen Katalog      | False                                                                                                                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 64                                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| In verwendete Klassen        | [**Unternehmensperson**](c-organizationalperson.md)<br/> [**1600-000-**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | False                                                                                                                           |
| Ist einwertig       | True                                                                                                                            |
| Ist indiziert             | False                                                                                                                           |
| Im globalen Katalog      | False                                                                                                                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 64                                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| In verwendete Klassen        | [**Unternehmensperson**](c-organizationalperson.md)<br/> [**1600-000-**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | False                                                                                                                           |
| Ist einwertig       | True                                                                                                                            |
| Ist indiziert             | False                                                                                                                           |
| Im globalen Katalog      | False                                                                                                                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 64                                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| In verwendete Klassen        | [**Unternehmensperson**](c-organizationalperson.md)<br/> [**1600-000-**](c-residentialperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | False                                                                                                                           |
| Ist einwertig       | True                                                                                                                            |
| Ist indiziert             | False                                                                                                                           |
| Im globalen Katalog      | False                                                                                                                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 128                                                                                                                             |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| In verwendete Klassen        | [**Unternehmensperson**](c-organizationalperson.md)<br/> [**1600-000-**](c-residentialperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | False                                                                                                                           |
| Ist einwertig       | True                                                                                                                            |
| Ist indiziert             | False                                                                                                                           |
| Im globalen Katalog      | False                                                                                                                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 128                                                                                                                             |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| In verwendete Klassen        | [**Unternehmensperson**](c-organizationalperson.md)<br/> [**1600-000-**](c-residentialperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | False                                                                                                                           |
| Ist einwertig       | True                                                                                                                            |
| Ist indiziert             | False                                                                                                                           |
| Im globalen Katalog      | False                                                                                                                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 128                                                                                                                             |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| In verwendete Klassen        | [**Unternehmensperson**](c-organizationalperson.md)<br/> [**1600-000-**](c-residentialperson.md)<br/> |



 

 





