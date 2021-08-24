---
title: NT-Mixed-Domain-Attribut
description: Gibt an, dass sich die Domäne im nativen oder gemischten Modus befindet. Dieses Attribut befindet sich im DomainDNS-Objekt (Head) für die Domäne.
ms.assetid: 49872cbc-844f-4d60-89b6-0150b9116740
ms.tgt_platform: multiple
keywords:
- AD-Schema des NT-Mixed-Domain-Attributs
- AD-Schema des nTMixedDomain-Attributs
topic_type:
- apiref
api_name:
- NT-Mixed-Domain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39148883e2b5d57157c334854ab7ebdfa61b69ac61d7a0100fc8470b741909c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119703030"
---
# <a name="nt-mixed-domain-attribute"></a>NT-Mixed-Domain-Attribut

Gibt an, dass sich die Domäne im nativen oder gemischten Modus befindet. Dieses Attribut befindet sich im DomainDNS-Objekt (Head) für die Domäne.



| Eingabe | Wert |
|-------------------|---------------------------------------|
| CN                | NT-Mixed-Domain                       |
| Ldap-Anzeigename | nTMixedDomain                         |
| Size              | 4 Bytes. Gemischter Modus 1, nativer Modus 0. |
| Aktualisieren von Berechtigungen  | \-                                    |
| Updatehäufigkeit  | \-                                    |
| Attribute-Id      | 1.2.840.113556.1.4.357                |
| System-Id-Guid    | 3e97891f-8c01-11d0-afda-00c04fd930c9  |
| Syntax            | [**Enumeration**](s-enumeration.md)  |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
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
| Is-Single-Valued       | True                                         |
| Ist indiziert             | False                                        |
| Im globalen Katalog      | False                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**Sam-Domain**](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | False                                                                                   |
| Is-Single-Valued       | True                                                                                    |
| Ist indiziert             | False                                                                                   |
| Im globalen Katalog      | False                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000010                                                                              |
| In verwendete Klassen        | [**Ref-übergreifend**](c-crossref.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | False                                                                                   |
| Is-Single-Valued       | True                                                                                    |
| Ist indiziert             | False                                                                                   |
| Im globalen Katalog      | False                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000010                                                                              |
| In verwendete Klassen        | [**Ref-übergreifend**](c-crossref.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | False                                                                                   |
| Is-Single-Valued       | True                                                                                    |
| Ist indiziert             | False                                                                                   |
| Im globalen Katalog      | False                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000010                                                                              |
| In verwendete Klassen        | [**Ref-übergreifend**](c-crossref.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | False                                                                                   |
| Is-Single-Valued       | True                                                                                    |
| Ist indiziert             | False                                                                                   |
| Im globalen Katalog      | False                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000010                                                                              |
| In verwendete Klassen        | [**Ref-übergreifend**](c-crossref.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | False                                                                                   |
| Is-Single-Valued       | True                                                                                    |
| Ist indiziert             | False                                                                                   |
| Im globalen Katalog      | False                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000010                                                                              |
| In verwendete Klassen        | [**Ref-übergreifend**](c-crossref.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> |



 

 





