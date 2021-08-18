---
title: Delta-Revocation-List-Attribut
description: Liste der Zertifikate, die seit dem letzten Deltaupdate widerrufen wurden.
ms.assetid: fc755c22-6d4f-4509-abb8-47c4f2f37545
ms.tgt_platform: multiple
keywords:
- AD-Schema des Delta-Revocation-List-Attributs
- deltaRevocationList-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Delta-Revocation-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a23cc8c5c01195429ba126632ed6c888354c66a4bc5d3cede75d28126fbafba7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961739"
---
# <a name="delta-revocation-list-attribute"></a>Delta-Revocation-List-Attribut

Liste der Zertifikate, die seit dem letzten Deltaupdate widerrufen wurden.



| Eingabe | Wert |
|-------------------|-------------------------------------------------------|
| CN                | Delta-Revocation-List                                 |
| Ldap-Anzeigename | deltaRevocationList                                   |
| Size              | \-                                                    |
| Aktualisieren von Berechtigungen  | \-                                                    |
| Updatehäufigkeit  | \-                                                    |
| Attribute-Id      | 2.5.4.53                                              |
| System-Id-Guid    | 167757b5-47f3-11d1-a9c3-0000f80367c1                  |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                         |
| MAPI-Id                | 0x8C46                                                                                                                                     |
| System-Only            | False                                                                                                                                      |
| Is-Single-Valued       | False                                                                                                                                      |
| Ist indiziert             | False                                                                                                                                      |
| Im globalen Katalog      | False                                                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                               |
| Range-Lower            | \-                                                                                                                                         |
| Range-Upper            | \-                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                 |
| System-Flags           | 0x00000000                                                                                                                                 |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> [**CRL-Verteilungspunkt**](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                         |
| MAPI-Id                | 0x8C46                                                                                                                                     |
| System-Only            | False                                                                                                                                      |
| Is-Single-Valued       | False                                                                                                                                      |
| Ist indiziert             | False                                                                                                                                      |
| Im globalen Katalog      | False                                                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                               |
| Range-Lower            | \-                                                                                                                                         |
| Range-Upper            | \-                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                 |
| System-Flags           | 0x00000000                                                                                                                                 |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> [**CRL-Verteilungspunkt**](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                         |
| MAPI-Id                | 0x8C46                                                                                                                                     |
| System-Only            | False                                                                                                                                      |
| Is-Single-Valued       | False                                                                                                                                      |
| Ist indiziert             | False                                                                                                                                      |
| Im globalen Katalog      | False                                                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                               |
| Range-Lower            | \-                                                                                                                                         |
| Range-Upper            | \-                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                 |
| System-Flags           | 0x00000000                                                                                                                                 |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> [**CRL-Verteilungspunkt**](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                         |
| MAPI-Id                | 0x8C46                                                                                                                                     |
| System-Only            | False                                                                                                                                      |
| Ist einwertig       | False                                                                                                                                      |
| Ist indiziert             | False                                                                                                                                      |
| Im globalen Katalog      | False                                                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                               |
| Range-Lower            | \-                                                                                                                                         |
| Range-Upper            | \-                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                 |
| System-Flags           | 0x00000000                                                                                                                                 |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> [**CRL-Verteilungspunkt**](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                         |
| MAPI-Id                | 0x8C46                                                                                                                                     |
| System-Only            | False                                                                                                                                      |
| Ist einwertig       | False                                                                                                                                      |
| Ist indiziert             | False                                                                                                                                      |
| Im globalen Katalog      | False                                                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                               |
| Range-Lower            | \-                                                                                                                                         |
| Range-Upper            | \-                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                 |
| System-Flags           | 0x00000000                                                                                                                                 |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> [**CRL-Verteilungspunkt**](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                         |
| MAPI-Id                | 0x8C46                                                                                                                                     |
| System-Only            | False                                                                                                                                      |
| Ist einwertig       | False                                                                                                                                      |
| Ist indiziert             | False                                                                                                                                      |
| Im globalen Katalog      | False                                                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                               |
| Range-Lower            | \-                                                                                                                                         |
| Range-Upper            | \-                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                 |
| System-Flags           | 0x00000000                                                                                                                                 |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> [**CRL-Verteilungspunkt**](c-crldistributionpoint.md)<br/> |



 

 





