---
title: ms-IIS-FTP-Dir-Attribut
description: Dieses Attribut bestimmt das Startverzeichnis des Benutzers relativ zur Dateiserverfreigabe. Es wird in Verbindung mit ms-IIS-FTP-Root verwendet, um das FTP-Benutzerstammverzeichnis zu bestimmen.
ms.assetid: 99b22b79-1d42-440d-b92b-33bac3e811cb
ms.tgt_platform: multiple
keywords:
- MS-IIS-FTP-Dir-Attribut AD-Schema
- MSIIS-FTPDir-Attribut AD-Schema
topic_type:
- apiref
api_name:
- ms-IIS-FTP-Dir
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8599d484609a28fbd80763215eccd4b0299bf8ec190a8804a2f6994114245ae6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119543950"
---
# <a name="ms-iis-ftp-dir-attribute"></a>ms-IIS-FTP-Dir-Attribut

Dieses Attribut bestimmt das Startverzeichnis des Benutzers relativ zur Dateiserverfreigabe. Es wird in Verbindung mit ms-IIS-FTP-Root verwendet, um das FTP-Benutzerstammverzeichnis zu bestimmen.



| Eingabe | Wert |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------|
| CN                | ms-IIS-FTP-Dir                                                                                                                  |
| Ldap-Anzeigename | msIIS-FTPDir                                                                                                                    |
| Size              | 30-50 Zeichen (15-25 Unicode-Zeichen für jede Eigenschaft)                                                                   |
| Aktualisieren von Berechtigungen  | Domänenadministrator & lokalen Systems                                                                                             |
| Updatehäufigkeit  | Diese Eigenschaft wird festgelegt, wenn der Administrator die Website erstellt und die FTP-Isolation festgelegt hat. Danach ändert sich dies nur selten. |
| Attribute-Id      | 1.2.840.113556.1.4.1786                                                                                                         |
| System-Id-Guid    | 8a5c99e9-2230-46eb-b8e8-e59d712eb9ee                                                                                            |
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
| System-Only            | False                             |
| Is-Single-Valued       | True                              |
| Ist indiziert             | False                             |
| Im globalen Katalog      | False                             |
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
| System-Only            | False                             |
| Is-Single-Valued       | True                              |
| Ist indiziert             | False                             |
| Im globalen Katalog      | False                             |
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
| System-Only            | False                             |
| Is-Single-Valued       | True                              |
| Ist indiziert             | False                             |
| Im globalen Katalog      | False                             |
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
| System-Only            | False                             |
| Ist einwertig       | True                              |
| Ist indiziert             | False                             |
| Im globalen Katalog      | False                             |
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
| System-Only            | False                             |
| Ist einwertig       | True                              |
| Ist indiziert             | False                             |
| Im globalen Katalog      | False                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | 1                                 |
| Range-Upper            | 256                               |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



 

 





