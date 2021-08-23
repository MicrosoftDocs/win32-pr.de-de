---
title: GP-Link-Attribut
description: Eine sortierte Liste Gruppenrichtlinie Optionen. Jede Option ist ein DWORD. Die Verwendung der UNICODE-Zeichenfolge ist praktisch.
ms.assetid: 7ddb1ee9-195c-47e5-83ce-6cc0d2e86e42
ms.tgt_platform: multiple
keywords:
- GP-Link AD-Attributschema
- gPLink-Attribut AD-Schema
topic_type:
- apiref
api_name:
- GP-Link
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bdf975322ee1391abd4825326a2db05016ea0276a16c50cce92a4c53a4ccf6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119705990"
---
# <a name="gp-link-attribute"></a>GP-Link-Attribut

Eine sortierte Liste Gruppenrichtlinie Optionen. Jede Option ist ein **DWORD-**. Die Verwendung der UNICODE-Zeichenfolge ist praktisch.



| Eingabe | Wert |
|-------------------|---------------------------------------------|
| CN                | GP-Link                                     |
| Ldap-Anzeigename | gPLink                                      |
| Size              | \-                                          |
| Aktualisieren von Berechtigungen  | \-                                          |
| Updatehäufigkeit  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.891                      |
| System-ID-GUID    | f30e3bbe-9ff0-11d1-b603-0000f80367c1        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                            |
| MAPI-Id                | \-                                                                                                                                            |
| System-Only            | False                                                                                                                                         |
| Ist einwertig       | True                                                                                                                                          |
| Ist indiziert             | False                                                                                                                                         |
| Im globalen Katalog      | True                                                                                                                                          |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                  |
| Range-Lower            | \-                                                                                                                                            |
| Range-Upper            | \-                                                                                                                                            |
| Search-Flags           | 0x00000000                                                                                                                                    |
| System-Flags           | 0x00000010                                                                                                                                    |
| In verwendete Klassen        | [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**Website**](c-site.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                                                                                |
| System-Only            | False                                                                                                                                                                                             |
| Ist einwertig       | True                                                                                                                                                                                              |
| Ist indiziert             | False                                                                                                                                                                                             |
| Im globalen Katalog      | True                                                                                                                                                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                      |
| Range-Lower            | \-                                                                                                                                                                                                |
| Range-Upper            | \-                                                                                                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                                                                                        |
| In verwendete Klassen        | [**Konfiguration**](c-configuration.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**Website**](c-site.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                                                                                |
| System-Only            | False                                                                                                                                                                                             |
| Ist einwertig       | True                                                                                                                                                                                              |
| Ist indiziert             | False                                                                                                                                                                                             |
| Im globalen Katalog      | True                                                                                                                                                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                      |
| Range-Lower            | \-                                                                                                                                                                                                |
| Range-Upper            | \-                                                                                                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                                                                                        |
| In verwendete Klassen        | [**Konfiguration**](c-configuration.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**Website**](c-site.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                                                                                |
| System-Only            | False                                                                                                                                                                                             |
| Is-Single-Valued       | True                                                                                                                                                                                              |
| Ist indiziert             | False                                                                                                                                                                                             |
| Im globalen Katalog      | True                                                                                                                                                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                      |
| Range-Lower            | \-                                                                                                                                                                                                |
| Range-Upper            | \-                                                                                                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                                                                                        |
| In verwendete Klassen        | [**Konfiguration**](c-configuration.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**Website**](c-site.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                                                                                |
| System-Only            | False                                                                                                                                                                                             |
| Is-Single-Valued       | True                                                                                                                                                                                              |
| Ist indiziert             | False                                                                                                                                                                                             |
| Im globalen Katalog      | True                                                                                                                                                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                      |
| Range-Lower            | \-                                                                                                                                                                                                |
| Range-Upper            | \-                                                                                                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                                                                                        |
| In verwendete Klassen        | [**Konfiguration**](c-configuration.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**Website**](c-site.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                                                                                |
| System-Only            | False                                                                                                                                                                                             |
| Is-Single-Valued       | True                                                                                                                                                                                              |
| Ist indiziert             | False                                                                                                                                                                                             |
| Im globalen Katalog      | True                                                                                                                                                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                      |
| Range-Lower            | \-                                                                                                                                                                                                |
| Range-Upper            | \-                                                                                                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                                                                                        |
| In verwendete Klassen        | [**Konfiguration**](c-configuration.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**Website**](c-site.md)<br/> |



 

 





