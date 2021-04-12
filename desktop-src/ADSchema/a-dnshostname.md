---
title: DNS-Host-Name-Attribut
description: Der Name des Computers, der in DNS registriert ist.
ms.assetid: ba655adb-cb70-47f2-820f-c5b0749d3e70
ms.tgt_platform: multiple
keywords:
- AD-Schema für DNS-Host-Name-Attribut
- dNSHostName-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- DNS-Host-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7580a58e5d3042633a9dd665354bc883b4fdb87c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519487"
---
# <a name="dns-host-name-attribute"></a>DNS-Host-Name-Attribut

Der Name des Computers, der in DNS registriert ist.



| Eingabe | Wert |
|-------------------|-----------------------------------------------------------------------------|
| CN                | DNS-Hostname                                                               |
| LDAP-Display-Name | dNSHostName                                                                 |
| Size              | Jedes Segment kann 63 Zeichen umfassen. Die gesamte Länge kann 255 Zeichen umfassen. |
| Berechtigung aktualisieren  | Domänen Administrator                                                        |
| Aktualisierungshäufigkeit  | Wenn der Computer benannt ist.                                                 |
| Attribute-Id      | 1.2.840.113556.1.4.619                                                      |
| System-ID-GUID    | 72e39547-7b18-11d1-ADEF-00c04ld8d5cd                                        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                 |



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
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | False                                                                                                                                                                                                                      |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                       |
| Ist indiziert             | False                                                                                                                                                                                                                      |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                       |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**PKI-Registrierung-Dienst**](c-pkienrollmentservice.md)<br/> [**Servers**](c-server.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | False                                                                                                                                                                                                                      |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                       |
| Ist indiziert             | False                                                                                                                                                                                                                      |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                       |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**PKI-Registrierung-Dienst**](c-pkienrollmentservice.md)<br/> [**Servers**](c-server.md)<br/> |



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
| Range-Lower            | 0                                     |
| Range-Upper            | 2048                                  |
| Search-Flags           | 0x00000000                            |
| System-Flags           | 0x00000010                            |
| In verwendete Klassen        | [**Servers**](c-server.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | False                                                                                                                                                                                                                      |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                       |
| Ist indiziert             | False                                                                                                                                                                                                                      |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                       |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**PKI-Registrierung-Dienst**](c-pkienrollmentservice.md)<br/> [**Servers**](c-server.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | False                                                                                                                                                                                                                      |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                       |
| Ist indiziert             | False                                                                                                                                                                                                                      |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                       |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**PKI-Registrierung-Dienst**](c-pkienrollmentservice.md)<br/> [**Servers**](c-server.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | False                                                                                                                                                                                                                      |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                       |
| Ist indiziert             | False                                                                                                                                                                                                                      |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                       |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**PKI-Registrierung-Dienst**](c-pkienrollmentservice.md)<br/> [**Servers**](c-server.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | False                                                                                                                                                                                                                      |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                       |
| Ist indiziert             | False                                                                                                                                                                                                                      |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                       |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**PKI-Registrierung-Dienst**](c-pkienrollmentservice.md)<br/> [**Servers**](c-server.md)<br/> |



 

 





