---
title: Flat-Name-Attribut
description: Bei Windows NT-Domänen ist der flache Name der NetBIOS-Name. Für Links mit nicht \8211; Windows NT-Domänen, der flache Name ist der identifizierende Name dieser Domäne, oder er ist NULL.
ms.assetid: ec368657-a0e7-4416-ab80-1d18d98bbcfa
ms.tgt_platform: multiple
keywords:
- Flat-Name AD-Schema
- flatName-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Flat-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 587fd4424c8373427a31e34864c200cc20e78ba4bf36e9fea735c28fd5817384
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804610"
---
# <a name="flat-name-attribute"></a>Flat-Name-Attribut

Bei Windows NT-Domänen ist der flache Name der NetBIOS-Name. Bei Links mit nicht Windows NT-Domänen ist der flache Name der identifizierende Name dieser Domäne, oder er ist **NULL.**



| Eingabe | Wert |
|-------------------|---------------------------------------------|
| CN                | Flat-Name                                   |
| Ldap-Anzeigename | flatName                                    |
| Size              | \-                                          |
| Aktualisieren von Berechtigungen  | \-                                          |
| Updatehäufigkeit  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.511                      |
| System-Id-Guid    | b7b13117-b82e-11d0-afee-0000f80367c1        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Is-Single-Valued       | True                                                 |
| Ist indiziert             | True                                                 |
| Im globalen Katalog      | False                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000001                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Trusted-Domain**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Is-Single-Valued       | True                                                 |
| Ist indiziert             | True                                                 |
| Im globalen Katalog      | False                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000001                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Trusted-Domain**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Is-Single-Valued       | True                                                 |
| Ist indiziert             | True                                                 |
| Im globalen Katalog      | False                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000001                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Trusted-Domain**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Ist einwertig       | True                                                 |
| Ist indiziert             | True                                                 |
| Im globalen Katalog      | False                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000001                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Ist einwertig       | True                                                 |
| Ist indiziert             | True                                                 |
| Im globalen Katalog      | False                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000001                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Ist einwertig       | True                                                 |
| Ist indiziert             | True                                                 |
| Im globalen Katalog      | False                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000001                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> |



 

 





