---
title: Certificate-Revocation-List-Attribut
description: Stellt eine Liste von Zertifikaten dar, die widerrufen wurden.
ms.assetid: fb7b4888-15c0-475b-a87a-7cb0656963bb
ms.tgt_platform: multiple
keywords:
- AD-Schema des Zertifikatsperrlisten-Attributs
- certificateRevocationList-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Certificate-Revocation-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03d3977093099bb3935db9833ae96f7cc3e689bb6265d679513164c67a1a9e62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119509770"
---
# <a name="certificate-revocation-list-attribute"></a>Certificate-Revocation-List-Attribut

Stellt eine Liste von Zertifikaten dar, die widerrufen wurden.



| Eingabe | Wert |
|-------------------|-------------------------------------------------------|
| CN                | Zertifikatsperrliste                           |
| Ldap-Anzeigename | certificateRevocationList                             |
| Size              | \-                                                    |
| Aktualisieren von Berechtigungen  | \-                                                    |
| Updatehäufigkeit  | \-                                                    |
| Attribute-Id      | 2.5.4.39                                              |
| System-Id-Guid    | 1677579f-47f3-11d1-a9c3-0000f80367c1                  |
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
| MAPI-Id                | 0x8016                                                                                                                                     |
| System-Only            | False                                                                                                                                      |
| Is-Single-Valued       | True                                                                                                                                       |
| Ist indiziert             | False                                                                                                                                      |
| Im globalen Katalog      | False                                                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                               |
| Range-Lower            | \-                                                                                                                                         |
| Range-Upper            | \-                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                 |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> [**CRL-Verteilungspunkt**](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                         |
| MAPI-Id                | 0x8016                                                                                                                                     |
| System-Only            | False                                                                                                                                      |
| Is-Single-Valued       | True                                                                                                                                       |
| Ist indiziert             | False                                                                                                                                      |
| Im globalen Katalog      | False                                                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                               |
| Range-Lower            | \-                                                                                                                                         |
| Range-Upper            | \-                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                 |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> [**CRL-Verteilungspunkt**](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                         |
| MAPI-Id                | 0x8016                                                                                                                                     |
| System-Only            | False                                                                                                                                      |
| Is-Single-Valued       | True                                                                                                                                       |
| Ist indiziert             | False                                                                                                                                      |
| Im globalen Katalog      | False                                                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                               |
| Range-Lower            | \-                                                                                                                                         |
| Range-Upper            | \-                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                 |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> [**CRL-Verteilungspunkt**](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                         |
| MAPI-Id                | 0x8016                                                                                                                                     |
| System-Only            | False                                                                                                                                      |
| Ist einwertig       | True                                                                                                                                       |
| Ist indiziert             | False                                                                                                                                      |
| Im globalen Katalog      | False                                                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                               |
| Range-Lower            | \-                                                                                                                                         |
| Range-Upper            | \-                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                 |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> [**CRL-Verteilungspunkt**](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                         |
| MAPI-Id                | 0x8016                                                                                                                                     |
| System-Only            | False                                                                                                                                      |
| Ist einwertig       | True                                                                                                                                       |
| Ist indiziert             | False                                                                                                                                      |
| Im globalen Katalog      | False                                                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                               |
| Range-Lower            | \-                                                                                                                                         |
| Range-Upper            | \-                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                 |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> [**CRL-Verteilungspunkt**](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                         |
| MAPI-Id                | 0x8016                                                                                                                                     |
| System-Only            | False                                                                                                                                      |
| Ist einwertig       | True                                                                                                                                       |
| Ist indiziert             | False                                                                                                                                      |
| Im globalen Katalog      | False                                                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                               |
| Range-Lower            | \-                                                                                                                                         |
| Range-Upper            | \-                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                 |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> [**CRL-Verteilungspunkt**](c-crldistributionpoint.md)<br/> |



 

 





