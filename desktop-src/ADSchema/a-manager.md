---
title: Manager-Attribut
description: Enthält den Distinguished Name des Benutzers, der der Vorgesetzte des Benutzers ist. Das Benutzerobjekt des Managers enthält eine directReports-Eigenschaft, die Verweise auf alle Benutzerobjekte enthält, deren Managereigenschaften auf diesen Distinguished Name festgelegt sind.
ms.assetid: 40743784-a99c-4ec0-9140-9f865c073244
ms.tgt_platform: multiple
keywords:
- AD-Schema des Manager-Attributs
- AD-Schema des Manager-Attributs
topic_type:
- apiref
api_name:
- Manager
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e87b17f3252963e03c86b5b25a3651606a004afe672f1c8ec07f419ddff3a826
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119301260"
---
# <a name="manager-attribute"></a>Manager-Attribut

Enthält den Distinguished Name des Benutzers, der der Vorgesetzte des Benutzers ist. Das Benutzerobjekt des Managers enthält eine directReports-Eigenschaft, die Verweise auf alle Benutzerobjekte enthält, deren Managereigenschaften auf diesen Distinguished Name festgelegt sind.



| Eingabe | Wert |
|-------------------|-----------------------------------------------------------------------------|
| CN                | Manager                                                                     |
| Ldap-Anzeigename | manager                                                                     |
| Size              | \-                                                                          |
| Aktualisieren von Berechtigungen  | Domänenadministrator oder Kontobesitzer.                                      |
| Updatehäufigkeit  | Wenn der Datensatz des Benutzers erstellt wird und wann immer der Manager geändert werden muss. |
| Attribute-Id      | 0.9.2342.19200300.100.1.10                                                  |
| System-ID-GUID    | bf9679b5-0de6-11d0-a285-00aa003049e2                                        |
| Syntax            | [**Object(DS-DN)**](s-object-ds-dn.md)                                     |



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
| Link-ID                | 42                                                                 |
| MAPI-Id                | 0x8005                                                             |
| System-Only            | False                                                              |
| Ist einwertig       | True                                                               |
| Ist indiziert             | False                                                              |
| Im globalen Katalog      | True                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000010                                                         |
| System-Flags           | 0x00000010                                                         |
| In verwendete Klassen        | [**Unternehmensperson**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | False                                                                                                                  |
| Ist einwertig       | True                                                                                                                   |
| Ist indiziert             | False                                                                                                                  |
| Im globalen Katalog      | True                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| In verwendete Klassen        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | False                                                                                                                  |
| Ist einwertig       | True                                                                                                                   |
| Ist indiziert             | False                                                                                                                  |
| Im globalen Katalog      | True                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| In verwendete Klassen        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | False                                                                                                                  |
| Is-Single-Valued       | True                                                                                                                   |
| Ist indiziert             | False                                                                                                                  |
| Im globalen Katalog      | True                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| In verwendete Klassen        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | False                                                                                                                  |
| Is-Single-Valued       | True                                                                                                                   |
| Ist indiziert             | False                                                                                                                  |
| Im globalen Katalog      | True                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| In verwendete Klassen        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | False                                                                                                                  |
| Is-Single-Valued       | True                                                                                                                   |
| Ist indiziert             | False                                                                                                                  |
| Im globalen Katalog      | True                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| In verwendete Klassen        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> |



 

 





