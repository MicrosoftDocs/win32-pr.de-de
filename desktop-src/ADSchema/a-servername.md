---
title: Server-Name-Attribut
description: Der Name eines Servers.
ms.assetid: 60c2afb4-5c3d-4628-95f8-f57dc7b9cb79
ms.tgt_platform: multiple
keywords:
- Server-Name AD-Attributschema
- SERVERNAME-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Server-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 985c4119c44b0e60f83712590f7c7ee453601159fec75770c2c2569329f8b093
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119022198"
---
# <a name="server-name-attribute"></a>Server-Name-Attribut

Der Name eines Servers.



| Eingabe | Wert |
|-------------------|---------------------------------------------|
| CN                | Server-Name                                 |
| Ldap-Anzeigename | serverName                                  |
| Size              | \-                                          |
| Aktualisieren von Berechtigungen  | \-                                          |
| Updatehäufigkeit  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.223                      |
| System-ID-GUID    | 09dcb7a0-165f-11d0-a064-00aa006c33ed        |
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
|------------------------|------------------------------------------------|
| Link-ID                | \-                                             |
| MAPI-Id                | \-                                             |
| System-Only            | Falsch                                          |
| Ist einwertig       | Richtig                                           |
| Ist indiziert             | Falsch                                          |
| Im globalen Katalog      | Richtig                                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                                   |
| Range-Lower            | 0                                              |
| Range-Upper            | 1024                                           |
| Search-Flags           | 0x00000000                                     |
| System-Flags           | 0x00000010                                     |
| In verwendete Klassen        | [**Druckwarteschlange**](c-printqueue.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|------------------------------------------------|
| Link-ID                | \-                                             |
| MAPI-Id                | \-                                             |
| System-Only            | Falsch                                          |
| Ist einwertig       | Richtig                                           |
| Ist indiziert             | Falsch                                          |
| Im globalen Katalog      | Richtig                                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                                   |
| Range-Lower            | 0                                              |
| Range-Upper            | 1024                                           |
| Search-Flags           | 0x00000000                                     |
| System-Flags           | 0x00000010                                     |
| In verwendete Klassen        | [**Druckwarteschlange**](c-printqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                        |
| MAPI-Id                | \-                                                                                                                        |
| System-Only            | Falsch                                                                                                                     |
| Ist einwertig       | Richtig                                                                                                                      |
| Ist indiziert             | Falsch                                                                                                                     |
| Im globalen Katalog      | Richtig                                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                              |
| Range-Lower            | 0                                                                                                                         |
| Range-Upper            | 1024                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                |
| In verwendete Klassen        | [**ms-Print-ConnectionPolicy**](c-msprint-connectionpolicy.md)<br/> [**Druckwarteschlange**](c-printqueue.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                        |
| MAPI-Id                | \-                                                                                                                        |
| System-Only            | Falsch                                                                                                                     |
| Is-Single-Valued       | Richtig                                                                                                                      |
| Ist indiziert             | Falsch                                                                                                                     |
| Im globalen Katalog      | Richtig                                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                              |
| Range-Lower            | 0                                                                                                                         |
| Range-Upper            | 1024                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                |
| In verwendete Klassen        | [**ms-Print-ConnectionPolicy**](c-msprint-connectionpolicy.md)<br/> [**Druckwarteschlange**](c-printqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                        |
| MAPI-Id                | \-                                                                                                                        |
| System-Only            | Falsch                                                                                                                     |
| Is-Single-Valued       | Richtig                                                                                                                      |
| Ist indiziert             | Falsch                                                                                                                     |
| Im globalen Katalog      | Richtig                                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                              |
| Range-Lower            | 0                                                                                                                         |
| Range-Upper            | 1024                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                |
| In verwendete Klassen        | [**ms-Print-ConnectionPolicy**](c-msprint-connectionpolicy.md)<br/> [**Druckwarteschlange**](c-printqueue.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                        |
| MAPI-Id                | \-                                                                                                                        |
| System-Only            | Falsch                                                                                                                     |
| Is-Single-Valued       | Richtig                                                                                                                      |
| Ist indiziert             | Falsch                                                                                                                     |
| Im globalen Katalog      | Richtig                                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                              |
| Range-Lower            | 0                                                                                                                         |
| Range-Upper            | 1024                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                |
| In verwendete Klassen        | [**ms-Print-ConnectionPolicy**](c-msprint-connectionpolicy.md)<br/> [**Druckwarteschlange**](c-printqueue.md)<br/> |



 

 





