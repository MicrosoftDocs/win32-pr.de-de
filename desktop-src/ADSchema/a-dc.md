---
title: Domain-Component-Attribut
description: Das Benennungsattribut für Domänen- und DNS-Objekte. Wird in der Regel als dc DomainName angezeigt.
ms.assetid: 1d674af1-ed2f-4266-9704-8c6ed5a9bdd8
ms.tgt_platform: multiple
keywords:
- Domain-Component AD-Schema
- DC-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Domain-Component
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe93b6629ac176452edbe5cdf13bf35afa955890cde369273f87990034bcd3e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118177770"
---
# <a name="domain-component-attribute"></a>Domain-Component-Attribut

Das Benennungsattribut für Domänen- und DNS-Objekte. Wird normalerweise als dc=DomainName angezeigt.



| Eingabe | Wert |
|-------------------|---------------------------------------------|
| CN                | Domain-Component                            |
| Ldap-Anzeigename | dc                                          |
| Size              | \-                                          |
| Aktualisieren von Berechtigungen  | Domänenadministrator                        |
| Updatehäufigkeit  | Wenn die Domäne erstellt wird.                 |
| Attribute-Id      | 0.9.2342.19200300.100.1.25                  |
| System-Id-Guid    | 19195a55-6da0-11d0-afd3-00c04fd930c9        |
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
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | Falsch                                                                                                                   |
| Is-Single-Valued       | True                                                                                                                    |
| Ist indiziert             | Falsch                                                                                                                   |
| Im globalen Katalog      | True                                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| In verwendete Klassen        | [**Dns-Node**](c-dnsnode.md)<br/> [**DNS-Zone**](c-dnszone.md)<br/> [**Domain**](c-domain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | Falsch                                                                                                                   |
| Is-Single-Valued       | True                                                                                                                    |
| Ist indiziert             | Falsch                                                                                                                   |
| Im globalen Katalog      | True                                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| In verwendete Klassen        | [**Dns-Node**](c-dnsnode.md)<br/> [**DNS-Zone**](c-dnszone.md)<br/> [**Domain**](c-domain.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|---------------------------------------|
| Link-ID                | \-                                    |
| MAPI-Id                | \-                                    |
| System-Only            | Falsch                                 |
| Is-Single-Valued       | True                                  |
| Ist indiziert             | Falsch                                 |
| Im globalen Katalog      | True                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                          |
| Range-Lower            | 1                                     |
| Range-Upper            | 255                                   |
| Search-Flags           | 0x00000000                            |
| System-Flags           | 0x00000012                            |
| In verwendete Klassen        | [**Domain**](c-domain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | Falsch                                                                                                                   |
| Is-Single-Valued       | True                                                                                                                    |
| Ist indiziert             | Falsch                                                                                                                   |
| Im globalen Katalog      | True                                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| In verwendete Klassen        | [**Dns-Node**](c-dnsnode.md)<br/> [**DNS-Zone**](c-dnszone.md)<br/> [**Domain**](c-domain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | Falsch                                                                                                                   |
| Is-Single-Valued       | True                                                                                                                    |
| Ist indiziert             | Falsch                                                                                                                   |
| Im globalen Katalog      | True                                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| In verwendete Klassen        | [**Dns-Node**](c-dnsnode.md)<br/> [**DNS-Zone**](c-dnszone.md)<br/> [**Domain**](c-domain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | Falsch                                                                                                                   |
| Is-Single-Valued       | True                                                                                                                    |
| Ist indiziert             | Falsch                                                                                                                   |
| Im globalen Katalog      | True                                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| In verwendete Klassen        | [**Dns-Node**](c-dnsnode.md)<br/> [**DNS-Zone**](c-dnszone.md)<br/> [**Domain**](c-domain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | Falsch                                                                                                                   |
| Ist einwertig       | True                                                                                                                    |
| Ist indiziert             | Falsch                                                                                                                   |
| Im globalen Katalog      | True                                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| In verwendete Klassen        | [**Dns-Node**](c-dnsnode.md)<br/> [**Dns-Zone**](c-dnszone.md)<br/> [**Domain**](c-domain.md)<br/> |



 

 





