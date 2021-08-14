---
title: ms-DS-Trust-Forest-Trust-Info-Attribut
description: Enthält Gesamtstruktur-Vertrauensstellungsinformationen (ein binäres BLOB), die vom System für ein Trusted-Domain werden.
ms.assetid: 60944ff6-d2b1-4f53-8557-7d79a7d9df51
ms.tgt_platform: multiple
keywords:
- AD-Schema des Ms-DS-Trust-Forest-Trust-Info-Attributs
- AD-Schema des msDS-TrustForestTrustInfo-Attributs
topic_type:
- apiref
api_name:
- ms-DS-Trust-Forest-Trust-Info
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae350001aa616052c1f0358497364ecfbce55d40e91314c56100d12848efc0ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118960569"
---
# <a name="ms-ds-trust-forest-trust-info-attribute"></a>ms-DS-Trust-Forest-Trust-Info-Attribut

Enthält Gesamtstruktur-Vertrauensstellungsinformationen (ein binäres BLOB), die vom System für ein Trusted-Domain werden.



| Eingabe | Wert |
|-------------------|--------------------------------------------------------------------------------------------------------------------|
| CN                | ms-DS-Trust-Forest-Trust-Info                                                                                      |
| Ldap-Anzeigename | msDS-TrustForestTrustInfo                                                                                          |
| Size              | \-                                                                                                                 |
| Aktualisieren von Berechtigungen  | \-                                                                                                                 |
| Updatehäufigkeit  | Nur wenn sich die Vertrauensstellung zwischen Gesamtstrukturen ändert. Dies kann passieren, wenn sich die Topologie einer vertrauenswürdigen Gesamtstruktur ändert. |
| Attribute-Id      | 1.2.840.113556.1.4.1702                                                                                            |
| System-Id-Guid    | 29cc866e-49d3-4969-942e-1dbc0925d183                                                                               |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md)                                                              |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Is-Single-Valued       | True                                                 |
| Ist indiziert             | False                                                |
| Im globalen Katalog      | True                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Trusted-Domain**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Is-Single-Valued       | True                                                 |
| Ist indiziert             | False                                                |
| Im globalen Katalog      | True                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Trusted-Domain**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Is-Single-Valued       | True                                                 |
| Ist indiziert             | False                                                |
| Im globalen Katalog      | True                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Trusted-Domain**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Ist einwertig       | True                                                 |
| Ist indiziert             | False                                                |
| Im globalen Katalog      | True                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Ist einwertig       | True                                                 |
| Ist indiziert             | False                                                |
| Im globalen Katalog      | True                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> |



 

 





