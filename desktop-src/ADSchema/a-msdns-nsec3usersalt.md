---
title: MS-DNS-NSEC3-User-Salt-Attribut
description: Ein Attribut, das eine vom Benutzer angegebene NSEC3 Salt-Zeichenfolge definiert, die beim Signieren der DNS-Zone verwendet werden soll. Wenn leer, wird zufälliger Salt verwendet.
ms.assetid: b9829732-8a79-4f07-8644-9fe4ba05ba8f
ms.tgt_platform: multiple
keywords:
- AD-Schema für MS-DNS-NSEC3-User-Salt-Attribut
- MSDNs-NSEC3UserSalt-Attribut AD-Schema
topic_type:
- apiref
api_name:
- ms-DNS-NSEC3-User-Salt
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7d28acb28dec95ef13afc37f9d7f26d713d5cf9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744753"
---
# <a name="ms-dns-nsec3-user-salt-attribute"></a>MS-DNS-NSEC3-User-Salt-Attribut

Ein Attribut, das eine vom Benutzer angegebene NSEC3 Salt-Zeichenfolge definiert, die beim Signieren der DNS-Zone verwendet werden soll. Wenn leer, wird zufälliger Salt verwendet.



| Eingabe | Wert |
|-------------------|---------------------------------------------|
| CN                | MS-DNS-NSEC3-User-Salt                      |
| LDAP-Display-Name | MSDNs-NSEC3UserSalt                         |
| Size              | \-                                          |
| Berechtigung aktualisieren  | \-                                          |
| Aktualisierungshäufigkeit  | \-                                          |
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
| Ist-einwertig       | Richtig                                     |
| Ist indiziert             | False                                    |
| Im globalen Katalog      | False                                    |
| NT-Security-Descriptor | o:Bag: schlecht: S:                             |
| Range-Lower            | 0                                        |
| Range-Upper            | 510                                      |
| Search-Flags           | 0x00000008                               |
| System-Flags           | 0x00000010                               |
| In verwendete Klassen        | [**DNS-Zone**](c-dnszone.md)<br/> |



 

 





