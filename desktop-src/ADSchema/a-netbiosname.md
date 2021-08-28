---
title: NETBIOS-Name-Attribut
description: Der Name des Objekts, das über NetBIOS verwendet werden soll.
ms.assetid: 03cbfa61-b747-4f3e-9bf5-17fd6da2e7be
ms.tgt_platform: multiple
keywords:
- NETBIOS-Name AD-Attributschema
- AD-Schema des nETBIOSName-Attributs
topic_type:
- apiref
api_name:
- NETBIOS-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5e5b7b28237facd30fb6fbfbcfc8f20f93699a8e8ab548889150250b38be4f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118424091"
---
# <a name="netbios-name-attribute"></a>NETBIOS-Name-Attribut

Der Name des Objekts, das über NetBIOS verwendet werden soll.



| Eingabe | Wert |
|-------------------|---------------------------------------------|
| CN                | NETBIOS-Name                                |
| Ldap-Anzeigename | nETBIOSName                                 |
| Size              | \-                                          |
| Aktualisieren von Berechtigungen  | Domänenadministrator                        |
| Updatehäufigkeit  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.87                       |
| System-ID-GUID    | bf9679d8-0de6-11d0-a285-00aa003049e2        |
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
|------------------------|-----------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | False                                                                                   |
| Ist einwertig       | True                                                                                    |
| Ist indiziert             | True                                                                                    |
| Im globalen Katalog      | False                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                            |
| Range-Lower            | 1                                                                                       |
| Range-Upper            | 16                                                                                      |
| Search-Flags           | 0x00000001                                                                              |
| System-Flags           | 0x00000010                                                                              |
| In verwendete Klassen        | [**Cross-Ref**](c-crossref.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | False                                                                                   |
| Ist einwertig       | True                                                                                    |
| Ist indiziert             | True                                                                                    |
| Im globalen Katalog      | False                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                            |
| Range-Lower            | 1                                                                                       |
| Range-Upper            | 16                                                                                      |
| Search-Flags           | 0x00000001                                                                              |
| System-Flags           | 0x00000010                                                                              |
| In verwendete Klassen        | [**Cross-Ref**](c-crossref.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------|
| Link-ID                | \-                                                                               |
| MAPI-Id                | \-                                                                               |
| System-Only            | False                                                                            |
| Ist einwertig       | True                                                                             |
| Ist indiziert             | True                                                                             |
| Im globalen Katalog      | False                                                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                     |
| Range-Lower            | 1                                                                                |
| Range-Upper            | 16                                                                               |
| Search-Flags           | 0x00000001                                                                       |
| System-Flags           | 0x00000010                                                                       |
| In verwendete Klassen        | [**Ref-übergreifend**](c-crossref.md)<br/> [**Server**](c-server.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | False                                                                                   |
| Is-Single-Valued       | True                                                                                    |
| Ist indiziert             | True                                                                                    |
| Im globalen Katalog      | False                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                            |
| Range-Lower            | 1                                                                                       |
| Range-Upper            | 16                                                                                      |
| Search-Flags           | 0x00000001                                                                              |
| System-Flags           | 0x00000010                                                                              |
| In verwendete Klassen        | [**Ref-übergreifend**](c-crossref.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | False                                                                                   |
| Is-Single-Valued       | True                                                                                    |
| Ist indiziert             | True                                                                                    |
| Im globalen Katalog      | False                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                            |
| Range-Lower            | 1                                                                                       |
| Range-Upper            | 16                                                                                      |
| Search-Flags           | 0x00000001                                                                              |
| System-Flags           | 0x00000010                                                                              |
| In verwendete Klassen        | [**Ref-übergreifend**](c-crossref.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | False                                                                                   |
| Is-Single-Valued       | True                                                                                    |
| Ist indiziert             | True                                                                                    |
| Im globalen Katalog      | False                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                            |
| Range-Lower            | 1                                                                                       |
| Range-Upper            | 16                                                                                      |
| Search-Flags           | 0x00000001                                                                              |
| System-Flags           | 0x00000010                                                                              |
| In verwendete Klassen        | [**Ref-übergreifend**](c-crossref.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | False                                                                                   |
| Is-Single-Valued       | True                                                                                    |
| Ist indiziert             | True                                                                                    |
| Im globalen Katalog      | False                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                            |
| Range-Lower            | 1                                                                                       |
| Range-Upper            | 16                                                                                      |
| Search-Flags           | 0x00000001                                                                              |
| System-Flags           | 0x00000010                                                                              |
| In verwendete Klassen        | [**Cross-Ref**](c-crossref.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> |



 

 





