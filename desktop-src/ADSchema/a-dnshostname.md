---
title: DNS-Host-Name-Attribut
description: Name des Computers, wie in DNS registriert.
ms.assetid: ba655adb-cb70-47f2-820f-c5b0749d3e70
ms.tgt_platform: multiple
keywords:
- DNS-Host-Name-Attribut AD-Schema
- Ad-Schema des dNSHostName-Attributs
topic_type:
- apiref
api_name:
- DNS-Host-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2241ea7144db7895e521c2844627d77b2f0ce54b5da518d180c87c6e9f834140
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085960"
---
# <a name="dns-host-name-attribute"></a>DNS-Host-Name-Attribut

Name des Computers, wie in DNS registriert.



| Eingabe | Wert |
|-------------------|-----------------------------------------------------------------------------|
| CN                | DNS-Hostname                                                               |
| Ldap-Anzeigename | dNSHostName                                                                 |
| Size              | Jedes Segment kann 63 Zeichen lang sein. Die gesamte Länge kann 255 Zeichen umfassen. |
| Aktualisieren von Berechtigungen  | Domänenadministrator                                                        |
| Updatehäufigkeit  | Wenn der Computer benannt wird.                                                 |
| Attribute-Id      | 1.2.840.113556.1.4.619                                                      |
| System-ID-GUID    | 72e39547-7b18-11d1-adef-00c04fd8d5cd                                        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                 |



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
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | Falsch                                                                                                                                                                                                                      |
| Ist einwertig       | Richtig                                                                                                                                                                                                                       |
| Ist indiziert             | Falsch                                                                                                                                                                                                                      |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**PKI-Enrollment-Service**](c-pkienrollmentservice.md)<br/> [**Server**](c-server.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | Falsch                                                                                                                                                                                                                      |
| Ist einwertig       | Richtig                                                                                                                                                                                                                       |
| Ist indiziert             | Falsch                                                                                                                                                                                                                      |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**PKI-Enrollment-Service**](c-pkienrollmentservice.md)<br/> [**Server**](c-server.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|---------------------------------------|
| Link-ID                | \-                                    |
| MAPI-Id                | \-                                    |
| System-Only            | Falsch                                 |
| Ist einwertig       | Richtig                                  |
| Ist indiziert             | Falsch                                 |
| Im globalen Katalog      | Richtig                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                          |
| Range-Lower            | 0                                     |
| Range-Upper            | 2048                                  |
| Search-Flags           | 0x00000000                            |
| System-Flags           | 0x00000010                            |
| In verwendete Klassen        | [**Server**](c-server.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | Falsch                                                                                                                                                                                                                      |
| Ist einwertig       | Richtig                                                                                                                                                                                                                       |
| Ist indiziert             | Falsch                                                                                                                                                                                                                      |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**PKI-Enrollment-Service**](c-pkienrollmentservice.md)<br/> [**Server**](c-server.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | Falsch                                                                                                                                                                                                                      |
| Ist einwertig       | Richtig                                                                                                                                                                                                                       |
| Ist indiziert             | Falsch                                                                                                                                                                                                                      |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**PKI-Enrollment-Service**](c-pkienrollmentservice.md)<br/> [**Server**](c-server.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | Falsch                                                                                                                                                                                                                      |
| Ist einwertig       | Richtig                                                                                                                                                                                                                       |
| Ist indiziert             | Falsch                                                                                                                                                                                                                      |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**PKI-Enrollment-Service**](c-pkienrollmentservice.md)<br/> [**Server**](c-server.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | Falsch                                                                                                                                                                                                                      |
| Is-Single-Valued       | Richtig                                                                                                                                                                                                                       |
| Ist indiziert             | Falsch                                                                                                                                                                                                                      |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**PKI-Enrollment-Service**](c-pkienrollmentservice.md)<br/> [**Server**](c-server.md)<br/> |



 

 





