---
title: NT-Mixed-Domain-Attribut
description: Gibt an, dass sich die Domäne im einheitlichen Modus oder gemischten Modus befindet. Dieses Attribut befindet sich im domainDNS (Head)-Objekt für die Domäne.
ms.assetid: 49872cbc-844f-4d60-89b6-0150b9116740
ms.tgt_platform: multiple
keywords:
- Active Directory-Domänen Attribut (AD-Schema)
- AD-Schema des nTMixedDomain-Attributs
topic_type:
- apiref
api_name:
- NT-Mixed-Domain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 217d73291f392141b80ca8916b86fffa0055226c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106341066"
---
# <a name="nt-mixed-domain-attribute"></a>NT-Mixed-Domain-Attribut

Gibt an, dass sich die Domäne im einheitlichen Modus oder gemischten Modus befindet. Dieses Attribut befindet sich im domainDNS (Head)-Objekt für die Domäne.



| Eingabe | Wert |
|-------------------|---------------------------------------|
| CN                | NT-gemischte Domäne                       |
| LDAP-Display-Name | ntMixedDomain                         |
| Size              | 4 Bytes. Gemischter Modus 1, einheitlicher Modus 0. |
| Berechtigung aktualisieren  | \-                                    |
| Aktualisierungshäufigkeit  | \-                                    |
| Attribute-Id      | 1.2.840.113556.1.4.357                |
| System-ID-GUID    | 3e97891f -8c01-11D0-AFDA-00c04f 930c9  |
| Syntax            | [**Enumeration**](s-enumeration.md)  |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Ist-einwertig       | Richtig                                         |
| Ist indiziert             | False                                        |
| Im globalen Katalog      | False                                        |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**Sam-Domäne**](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | False                                                                                   |
| Ist-einwertig       | Richtig                                                                                    |
| Ist indiziert             | False                                                                                   |
| Im globalen Katalog      | False                                                                                   |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000010                                                                              |
| In verwendete Klassen        | [**Kreuz Verweis**](c-crossref.md)<br/> [**Sam-Domäne**](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | False                                                                                   |
| Ist-einwertig       | Richtig                                                                                    |
| Ist indiziert             | False                                                                                   |
| Im globalen Katalog      | False                                                                                   |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000010                                                                              |
| In verwendete Klassen        | [**Kreuz Verweis**](c-crossref.md)<br/> [**Sam-Domäne**](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | False                                                                                   |
| Ist-einwertig       | Richtig                                                                                    |
| Ist indiziert             | False                                                                                   |
| Im globalen Katalog      | False                                                                                   |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000010                                                                              |
| In verwendete Klassen        | [**Kreuz Verweis**](c-crossref.md)<br/> [**Sam-Domäne**](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | False                                                                                   |
| Ist-einwertig       | Richtig                                                                                    |
| Ist indiziert             | False                                                                                   |
| Im globalen Katalog      | False                                                                                   |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000010                                                                              |
| In verwendete Klassen        | [**Kreuz Verweis**](c-crossref.md)<br/> [**Sam-Domäne**](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | False                                                                                   |
| Ist-einwertig       | Richtig                                                                                    |
| Ist indiziert             | False                                                                                   |
| Im globalen Katalog      | False                                                                                   |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000010                                                                              |
| In verwendete Klassen        | [**Kreuz Verweis**](c-crossref.md)<br/> [**Sam-Domäne**](c-samdomain.md)<br/> |



 

 





