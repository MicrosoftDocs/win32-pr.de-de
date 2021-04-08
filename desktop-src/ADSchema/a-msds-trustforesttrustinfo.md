---
title: ms-DS-Trust-Forest-Trust-Info-Attribut
description: Enthält Gesamtstruktur-Vertrauensstellungs Informationen (ein binäres Blob), die vom System für ein Trusted-Domain Objekt verwendet werden.
ms.assetid: 60944ff6-d2b1-4f53-8557-7d79a7d9df51
ms.tgt_platform: multiple
keywords:
- ms-DS-Trust-Forest-Trust-Info-Attribut AD-Schema
- das msDS-trustforesttrustinfo-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- ms-DS-Trust-Forest-Trust-Info
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e259abaeae4d99b80b8ff6a390901f1c9f51e6a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744680"
---
# <a name="ms-ds-trust-forest-trust-info-attribute"></a>ms-DS-Trust-Forest-Trust-Info-Attribut

Enthält Gesamtstruktur-Vertrauensstellungs Informationen (ein binäres Blob), die vom System für ein Trusted-Domain Objekt verwendet werden.



| Eingabe | Wert |
|-------------------|--------------------------------------------------------------------------------------------------------------------|
| CN                | ms-DS-Trust-Forest-Trust-Info                                                                                      |
| LDAP-Display-Name | MSDS-trustforesttrustinfo                                                                                          |
| Size              | \-                                                                                                                 |
| Berechtigung aktualisieren  | \-                                                                                                                 |
| Aktualisierungshäufigkeit  | Nur, wenn die Vertrauensstellung zwischen Gesamtstrukturen geändert wird. Dies kann vorkommen, wenn die Topologie einer vertrauenswürdigen Gesamtstruktur geändert wird. |
| Attribute-Id      | 1.2.840.113556.1.4.1702                                                                                            |
| System-ID-GUID    | 29cc866e-49d3-4969-942e-1dbc0925d183                                                                               |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md)                                                              |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Ist-einwertig       | Richtig                                                 |
| Ist indiziert             | False                                                |
| Im globalen Katalog      | Richtig                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Ist-einwertig       | Richtig                                                 |
| Ist indiziert             | False                                                |
| Im globalen Katalog      | Richtig                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Ist-einwertig       | Richtig                                                 |
| Ist indiziert             | False                                                |
| Im globalen Katalog      | Richtig                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Ist-einwertig       | Richtig                                                 |
| Ist indiziert             | False                                                |
| Im globalen Katalog      | Richtig                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                         |
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
| Ist-einwertig       | Richtig                                                 |
| Ist indiziert             | False                                                |
| Im globalen Katalog      | Richtig                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> |



 

 





