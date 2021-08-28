---
title: ms-DNS-NSEC3-User-Salt-Attribut
description: Ein Attribut, das eine benutzerdefinierte NSEC3-Salt-Zeichenfolge definiert, die beim Signieren der DNS-Zone verwendet werden soll. Wenn es leer ist, wird zufälliges Salt verwendet.
ms.assetid: b9829732-8a79-4f07-8644-9fe4ba05ba8f
ms.tgt_platform: multiple
keywords:
- MS-DNS-NSEC3-User-Salt-Attribut AD-Schema
- msDNS-NSEC3UserSalt-Attribut AD-Schema
topic_type:
- apiref
api_name:
- ms-DNS-NSEC3-User-Salt
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dbd1725675487ae5a6812dd77c400745b6671de0ef7db360e1c1980dd25b1b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553020"
---
# <a name="ms-dns-nsec3-user-salt-attribute"></a>ms-DNS-NSEC3-User-Salt-Attribut

Ein Attribut, das eine benutzerdefinierte NSEC3-Salt-Zeichenfolge definiert, die beim Signieren der DNS-Zone verwendet werden soll. Wenn es leer ist, wird zufälliges Salt verwendet.



| Eingabe | Wert |
|-------------------|---------------------------------------------|
| CN                | ms-DNS-NSEC3-User-Salt                      |
| Ldap-Anzeigename | msDNS-NSEC3UserSalt                         |
| Size              | \-                                          |
| Aktualisieren von Berechtigungen  | \-                                          |
| Updatehäufigkeit  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.2148                     |
| System-ID-GUID    | aff16770-9622-4fbc-a128-3088777605b9        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|------------------------------------------|
| Link-ID                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | False                                    |
| Ist einwertig       | True                                     |
| Ist indiziert             | False                                    |
| Im globalen Katalog      | False                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                             |
| Range-Lower            | 0                                        |
| Range-Upper            | 510                                      |
| Search-Flags           | 0x00000008                               |
| System-Flags           | 0x00000010                               |
| In verwendete Klassen        | [**Dns-Zone**](c-dnszone.md)<br/> |



 

 





