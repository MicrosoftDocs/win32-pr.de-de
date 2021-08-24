---
title: Network-Address-Attribut
description: Die TCP/IP-Adresse für ein Netzwerksegment. Wird auch als Subnetzadresse bezeichnet.
ms.assetid: caccb00f-8418-43b8-87c7-7ccb7e2ee51d
ms.tgt_platform: multiple
keywords:
- Network-Address AD-Schema
- networkAddress-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Network-Address
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aecb62701350c0a954a23dc403a314331920810b0b6778f90099c600ca738a60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704760"
---
# <a name="network-address-attribute"></a>Network-Address-Attribut

Die TCP/IP-Adresse für ein Netzwerksegment. Wird auch als Subnetzadresse bezeichnet.



| Eingabe | Wert |
|-------------------|---------------------------------------------|
| CN                | Network-Address                             |
| Ldap-Anzeigename | networkAddress                              |
| Size              | \-                                          |
| Aktualisieren von Berechtigungen  | \-                                          |
| Updatehäufigkeit  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.2.459                      |
| System-Id-Guid    | bf9679d9-0de6-11d0-a285-00aa003049e2        |
| Syntax            | [**String(Teletex)**](s-string-teletex.md) |



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
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                |
| MAPI-Id                | 0x8170                                                                                                                                                            |
| System-Only            | Falsch                                                                                                                                                             |
| Is-Single-Valued       | Falsch                                                                                                                                                             |
| Ist indiziert             | Falsch                                                                                                                                                             |
| Im globalen Katalog      | Falsch                                                                                                                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                      |
| Range-Lower            | 0                                                                                                                                                                 |
| Range-Upper            | 256                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                        |
| System-Flags           | 0x00000000                                                                                                                                                        |
| In verwendete Klassen        | [**Computer**](c-computer.md)<br/> [**DHCP-Klasse**](c-dhcpclass.md)<br/> [**NTDS-DSA**](c-ntdsdsa.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                |
| MAPI-Id                | 0x8170                                                                                                                                                            |
| System-Only            | Falsch                                                                                                                                                             |
| Is-Single-Valued       | Falsch                                                                                                                                                             |
| Ist indiziert             | Falsch                                                                                                                                                             |
| Im globalen Katalog      | Falsch                                                                                                                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                      |
| Range-Lower            | 0                                                                                                                                                                 |
| Range-Upper            | 256                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                        |
| System-Flags           | 0x00000000                                                                                                                                                        |
| In verwendete Klassen        | [**Computer**](c-computer.md)<br/> [**DHCP-Klasse**](c-dhcpclass.md)<br/> [**NTDS-DSA**](c-ntdsdsa.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|------------------------------------------|
| Link-ID                | \-                                       |
| MAPI-Id                | 0x8170                                   |
| System-Only            | Falsch                                    |
| Is-Single-Valued       | Falsch                                    |
| Ist indiziert             | Falsch                                    |
| Im globalen Katalog      | Falsch                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                             |
| Range-Lower            | 0                                        |
| Range-Upper            | 256                                      |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000000                               |
| In verwendete Klassen        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                |
| MAPI-Id                | 0x8170                                                                                                                                                            |
| System-Only            | Falsch                                                                                                                                                             |
| Ist einwertig       | Falsch                                                                                                                                                             |
| Ist indiziert             | Falsch                                                                                                                                                             |
| Im globalen Katalog      | Falsch                                                                                                                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                      |
| Range-Lower            | 0                                                                                                                                                                 |
| Range-Upper            | 256                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                        |
| System-Flags           | 0x00000000                                                                                                                                                        |
| In verwendete Klassen        | [**Computer**](c-computer.md)<br/> [**DHCP-Klasse**](c-dhcpclass.md)<br/> [**NTDS-DSA**](c-ntdsdsa.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                |
| MAPI-Id                | 0x8170                                                                                                                                                            |
| System-Only            | Falsch                                                                                                                                                             |
| Ist einwertig       | Falsch                                                                                                                                                             |
| Ist indiziert             | Falsch                                                                                                                                                             |
| Im globalen Katalog      | Falsch                                                                                                                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                      |
| Range-Lower            | 0                                                                                                                                                                 |
| Range-Upper            | 256                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                        |
| System-Flags           | 0x00000000                                                                                                                                                        |
| In verwendete Klassen        | [**Computer**](c-computer.md)<br/> [**DHCP-Klasse**](c-dhcpclass.md)<br/> [**NTDS-DSA**](c-ntdsdsa.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                |
| MAPI-Id                | 0x8170                                                                                                                                                            |
| System-Only            | Falsch                                                                                                                                                             |
| Ist einwertig       | Falsch                                                                                                                                                             |
| Ist indiziert             | Falsch                                                                                                                                                             |
| Im globalen Katalog      | Falsch                                                                                                                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                      |
| Range-Lower            | 0                                                                                                                                                                 |
| Range-Upper            | 256                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                        |
| System-Flags           | 0x00000000                                                                                                                                                        |
| In verwendete Klassen        | [**Computer**](c-computer.md)<br/> [**DHCP-Klasse**](c-dhcpclass.md)<br/> [**NTDS-DSA**](c-ntdsdsa.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                |
| MAPI-Id                | 0x8170                                                                                                                                                            |
| System-Only            | Falsch                                                                                                                                                             |
| Is-Single-Valued       | Falsch                                                                                                                                                             |
| Ist indiziert             | Falsch                                                                                                                                                             |
| Im globalen Katalog      | Falsch                                                                                                                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                      |
| Range-Lower            | 0                                                                                                                                                                 |
| Range-Upper            | 256                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                        |
| System-Flags           | 0x00000000                                                                                                                                                        |
| In verwendete Klassen        | [**Computer**](c-computer.md)<br/> [**DHCP-Klasse**](c-dhcpclass.md)<br/> [**NTDS-DSA**](c-ntdsdsa.md)<br/> [**Benutzer**](c-user.md)<br/> |



 

 





