---
title: Domain-Component-Attribut
description: Das Benennungs Attribut für Domänen-und DNS-Objekte. Wird normalerweise als Domänen Controller Domänen Name angezeigt.
ms.assetid: 1d674af1-ed2f-4266-9704-8c6ed5a9bdd8
ms.tgt_platform: multiple
keywords:
- AD-Schema für Domain-Component-Attribut
- AD-Schema für DC-Attribut
topic_type:
- apiref
api_name:
- Domain-Component
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a97a6958d51c6e0e29f70685b2624fb194d42e05
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107150"
---
# <a name="domain-component-attribute"></a>Domain-Component-Attribut

Das Benennungs Attribut für Domänen-und DNS-Objekte. Wird normalerweise als DC = Domänen Name angezeigt.



| Eingabe | Wert |
|-------------------|---------------------------------------------|
| CN                | Domain-Component                            |
| LDAP-Display-Name | dc                                          |
| Size              | \-                                          |
| Berechtigung aktualisieren  | Domänen Administrator                        |
| Aktualisierungshäufigkeit  | Wenn die Domäne erstellt wird.                 |
| Attribute-Id      | 0.9.2342.19200300.100.1.25                  |
| System-ID-GUID    | 19195a55-6da0-11D0-afd3-00c04f 930c9        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
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
| System-Only            | False                                                                                                                   |
| Ist-einwertig       | Richtig                                                                                                                    |
| Ist indiziert             | False                                                                                                                   |
| Im globalen Katalog      | Richtig                                                                                                                    |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| In verwendete Klassen        | [**DNS-Knoten**](c-dnsnode.md)<br/> [**DNS-Zone**](c-dnszone.md)<br/> [**Domain**](c-domain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | False                                                                                                                   |
| Ist-einwertig       | Richtig                                                                                                                    |
| Ist indiziert             | False                                                                                                                   |
| Im globalen Katalog      | Richtig                                                                                                                    |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| In verwendete Klassen        | [**DNS-Knoten**](c-dnsnode.md)<br/> [**DNS-Zone**](c-dnszone.md)<br/> [**Domain**](c-domain.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|---------------------------------------|
| Link-ID                | \-                                    |
| MAPI-Id                | \-                                    |
| System-Only            | False                                 |
| Ist-einwertig       | Richtig                                  |
| Ist indiziert             | False                                 |
| Im globalen Katalog      | Richtig                                  |
| NT-Security-Descriptor | o:Bag: schlecht: S:                          |
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
| System-Only            | False                                                                                                                   |
| Ist-einwertig       | Richtig                                                                                                                    |
| Ist indiziert             | False                                                                                                                   |
| Im globalen Katalog      | Richtig                                                                                                                    |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| In verwendete Klassen        | [**DNS-Knoten**](c-dnsnode.md)<br/> [**DNS-Zone**](c-dnszone.md)<br/> [**Domain**](c-domain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | False                                                                                                                   |
| Ist-einwertig       | Richtig                                                                                                                    |
| Ist indiziert             | False                                                                                                                   |
| Im globalen Katalog      | Richtig                                                                                                                    |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| In verwendete Klassen        | [**DNS-Knoten**](c-dnsnode.md)<br/> [**DNS-Zone**](c-dnszone.md)<br/> [**Domain**](c-domain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | False                                                                                                                   |
| Ist-einwertig       | Richtig                                                                                                                    |
| Ist indiziert             | False                                                                                                                   |
| Im globalen Katalog      | Richtig                                                                                                                    |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| In verwendete Klassen        | [**DNS-Knoten**](c-dnsnode.md)<br/> [**DNS-Zone**](c-dnszone.md)<br/> [**Domain**](c-domain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | False                                                                                                                   |
| Ist-einwertig       | Richtig                                                                                                                    |
| Ist indiziert             | False                                                                                                                   |
| Im globalen Katalog      | Richtig                                                                                                                    |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| In verwendete Klassen        | [**DNS-Knoten**](c-dnsnode.md)<br/> [**DNS-Zone**](c-dnszone.md)<br/> [**Domain**](c-domain.md)<br/> |



 

 





