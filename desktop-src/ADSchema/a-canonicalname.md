---
title: Canonical-Name-Attribut
description: Der Name des Objekts im kanonischen Format.
ms.assetid: f217e5fa-f70b-4f4d-afa6-53e4f7e8a0e1
ms.tgt_platform: multiple
keywords:
- Canonical-Name AD-Attributschema
- canonicalName-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Canonical-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09d88b31dd351e255c252188388bd1ba06b3a1c073163f5cd2cc9d2deac16a74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119307190"
---
# <a name="canonical-name-attribute"></a>Canonical-Name-Attribut

Der Name des Objekts im kanonischen Format. myserver2.fabrikam.com/users/jeffsmith ist ein Beispiel für einen Distinguished Name im kanonischen Format. Dies ist ein konstruiertes Attribut. Die zurückgegebenen Ergebnisse sind identisch mit denen, die von der folgenden Active Directory-Funktion zurückgegeben werden: DsCrackNames(NULL, DS \_ NAME \_ FLAG \_ SYNTACTICAL \_ ONLY, DS \_ FQDN \_ 1779 \_ NAME, DS \_ CANONICAL \_ NAME, ...).

Weitere Informationen zu Namensformaten finden Sie unter [**DsCrackNames**](/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa).



| Eingabe | Wert |
|-------------------|---------------------------------------------|
| CN                | Canonical-Name                              |
| Ldap-Anzeigename | canonicalName                               |
| Size              | \-                                          |
| Aktualisieren von Berechtigungen  | \-                                          |
| Updatehäufigkeit  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.916                      |
| System-ID-GUID    | 9a7ad945-ca53-11d1-bbd0-0080c76670c0        |
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
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Ist einwertig       | False                           |
| Ist indiziert             | False                           |
| Im globalen Katalog      | False                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Ist einwertig       | False                           |
| Ist indiziert             | False                           |
| Im globalen Katalog      | False                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Ist einwertig       | False                           |
| Ist indiziert             | False                           |
| Im globalen Katalog      | False                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Ist einwertig       | False                           |
| Ist indiziert             | False                           |
| Im globalen Katalog      | False                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Ist einwertig       | False                           |
| Ist indiziert             | False                           |
| Im globalen Katalog      | False                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Ist einwertig       | False                           |
| Ist indiziert             | False                           |
| Im globalen Katalog      | False                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Ist einwertig       | False                           |
| Ist indiziert             | False                           |
| Im globalen Katalog      | False                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



 

