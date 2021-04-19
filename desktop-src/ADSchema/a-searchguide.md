---
title: Search-Guide-Attribut
description: Gibt Informationen zu vorgeschlagenen Suchkriterien an, die in einigen Einträgen enthalten sein können, die als nützliches Basisobjekt für den Suchvorgang, z. b. Land/Region oder Organisation, erwartet werden.
ms.assetid: 69823ef3-efa8-4732-bbec-27ed8fec81cc
ms.tgt_platform: multiple
keywords:
- AD-Schema für Search-Guide-Attribut
- searchguide-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Search-Guide
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 711202ebc39649e7e1aea2a4459c3a7147eb2ff6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106342904"
---
# <a name="search-guide-attribute"></a>Search-Guide-Attribut

Gibt Informationen zu vorgeschlagenen Suchkriterien an, die in einigen Einträgen enthalten sein können, die als nützliches Basisobjekt für den Suchvorgang, z. b. Land/Region oder Organisation, erwartet werden.



| Eingabe | Wert |
|-------------------|-------------------------------------------------------|
| CN                | Search-Guide                                          |
| LDAP-Display-Name | searchguide                                           |
| Size              | \-                                                    |
| Berechtigung aktualisieren  | Domänen Administrator                                  |
| Aktualisierungshäufigkeit  | Jedes Mal, wenn ein neues Such Handbuch gewünscht wird.               |
| Attribute-Id      | 2.5.4.14                                              |
| System-ID-GUID    | bf967a2e-0de6-11d0-a285-00aa003049e2                  |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md) |



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
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x812e                                                                                                                                                                                                                                                                    |
| System-Only            | False                                                                                                                                                                                                                                                                     |
| Ist-einwertig       | False                                                                                                                                                                                                                                                                     |
| Ist indiziert             | False                                                                                                                                                                                                                                                                     |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                     |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                              |
| Range-Lower            | \-                                                                                                                                                                                                                                                                        |
| Range-Upper            | \-                                                                                                                                                                                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> [**Country**](c-country.md)<br/> [**Ort**](c-locality.md)<br/> [**Organisation**](c-organization.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x812e                                                                                                                                                                                                                                                                    |
| System-Only            | False                                                                                                                                                                                                                                                                     |
| Ist-einwertig       | False                                                                                                                                                                                                                                                                     |
| Ist indiziert             | False                                                                                                                                                                                                                                                                     |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                     |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                              |
| Range-Lower            | \-                                                                                                                                                                                                                                                                        |
| Range-Upper            | \-                                                                                                                                                                                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> [**Country**](c-country.md)<br/> [**Ort**](c-locality.md)<br/> [**Organisation**](c-organization.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                 |
| MAPI-Id                | 0x812e                                                                                                                                                                                             |
| System-Only            | False                                                                                                                                                                                              |
| Ist-einwertig       | False                                                                                                                                                                                              |
| Ist indiziert             | False                                                                                                                                                                                              |
| Im globalen Katalog      | False                                                                                                                                                                                              |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| In verwendete Klassen        | [**Country**](c-country.md)<br/> [**Ort**](c-locality.md)<br/> [**Organisation**](c-organization.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x812e                                                                                                                                                                                                                                                                    |
| System-Only            | False                                                                                                                                                                                                                                                                     |
| Ist-einwertig       | False                                                                                                                                                                                                                                                                     |
| Ist indiziert             | False                                                                                                                                                                                                                                                                     |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                     |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                              |
| Range-Lower            | \-                                                                                                                                                                                                                                                                        |
| Range-Upper            | \-                                                                                                                                                                                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> [**Country**](c-country.md)<br/> [**Ort**](c-locality.md)<br/> [**Organisation**](c-organization.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x812e                                                                                                                                                                                                                                                                    |
| System-Only            | False                                                                                                                                                                                                                                                                     |
| Ist-einwertig       | False                                                                                                                                                                                                                                                                     |
| Ist indiziert             | False                                                                                                                                                                                                                                                                     |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                     |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                              |
| Range-Lower            | \-                                                                                                                                                                                                                                                                        |
| Range-Upper            | \-                                                                                                                                                                                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> [**Country**](c-country.md)<br/> [**Ort**](c-locality.md)<br/> [**Organisation**](c-organization.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x812e                                                                                                                                                                                                                                                                    |
| System-Only            | False                                                                                                                                                                                                                                                                     |
| Ist-einwertig       | False                                                                                                                                                                                                                                                                     |
| Ist indiziert             | False                                                                                                                                                                                                                                                                     |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                     |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                              |
| Range-Lower            | \-                                                                                                                                                                                                                                                                        |
| Range-Upper            | \-                                                                                                                                                                                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> [**Country**](c-country.md)<br/> [**Ort**](c-locality.md)<br/> [**Organisation**](c-organization.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x812e                                                                                                                                                                                                                                                                    |
| System-Only            | False                                                                                                                                                                                                                                                                     |
| Ist-einwertig       | False                                                                                                                                                                                                                                                                     |
| Ist indiziert             | False                                                                                                                                                                                                                                                                     |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                     |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                              |
| Range-Lower            | \-                                                                                                                                                                                                                                                                        |
| Range-Upper            | \-                                                                                                                                                                                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> [**Country**](c-country.md)<br/> [**Ort**](c-locality.md)<br/> [**Organisation**](c-organization.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> |



 

 





