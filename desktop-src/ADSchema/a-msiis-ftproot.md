---
title: ms-IIS-FTP-Root-Attribut
description: Dieses Attribut bestimmt die Dateiserverfreigabe. Sie wird in Verbindung mit ms-IIS-FTP-Dir verwendet, um das Stammverzeichnis des FTP-Benutzers zu bestimmen.
ms.assetid: b86dcafb-0b0d-4225-924c-690f739092a8
ms.tgt_platform: multiple
keywords:
- MS-IIS-FTP-Root-Attribut AD-Schema
- MSIIS-FTPRoot-Attribut AD-Schema
topic_type:
- apiref
api_name:
- ms-IIS-FTP-Root
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa4def81aa39c9df5aaa336a05514ab4581aa14533917fad008fc9c49d32d13e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118682524"
---
# <a name="ms-iis-ftp-root-attribute"></a>ms-IIS-FTP-Root-Attribut

Dieses Attribut bestimmt die Dateiserverfreigabe. Sie wird in Verbindung mit ms-IIS-FTP-Dir verwendet, um das Stammverzeichnis des FTP-Benutzers zu bestimmen.



| Eingabe | Wert |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------|
| CN                | ms-IIS-FTP-Root                                                                                                                 |
| Ldap-Anzeigename | msIIS-FTPRoot                                                                                                                   |
| Size              | 30 bis 50 Zeichen (15 bis 25 Unicode-Zeichen für jede Eigenschaft)                                                                   |
| Aktualisieren von Berechtigungen  | Domänenadministrator & lokales System                                                                                             |
| Updatehäufigkeit  | Diese Eigenschaft wird festgelegt, wenn der Administrator die Website erstellt und die FTP-Isolation festlegt. Danach ändert sich dies nur selten. |
| Attribute-Id      | 1.2.840.113556.1.4.1785                                                                                                         |
| System-ID-GUID    | 2a7827a4-1483-49a5-9d84-52e3812156b4                                                                                            |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                                                                     |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falsch                             |
| Ist einwertig       | Richtig                              |
| Ist indiziert             | Falsch                             |
| Im globalen Katalog      | Falsch                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | 1                                 |
| Range-Upper            | 256                               |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falsch                             |
| Ist einwertig       | Richtig                              |
| Ist indiziert             | Falsch                             |
| Im globalen Katalog      | Falsch                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | 1                                 |
| Range-Upper            | 256                               |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falsch                             |
| Ist einwertig       | Richtig                              |
| Ist indiziert             | Falsch                             |
| Im globalen Katalog      | Falsch                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | 1                                 |
| Range-Upper            | 256                               |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falsch                             |
| Is-Single-Valued       | Richtig                              |
| Ist indiziert             | Falsch                             |
| Im globalen Katalog      | Falsch                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | 1                                 |
| Range-Upper            | 256                               |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falsch                             |
| Is-Single-Valued       | Richtig                              |
| Ist indiziert             | Falsch                             |
| Im globalen Katalog      | Falsch                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | 1                                 |
| Range-Upper            | 256                               |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



 

 





