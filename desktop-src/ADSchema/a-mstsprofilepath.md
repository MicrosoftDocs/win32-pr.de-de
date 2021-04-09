---
title: MS-TS-profile-path-Attribut
description: Der Terminal Dienste-Profilpfad gibt einen roamingpfad oder obligatorischen Profilpfad an, der verwendet wird, wenn sich der Benutzer am Terminal Server anmeldet. Der Profilpfad befindet sich im folgenden Netzwerkpfad Format \\ \\ Servername \\ Profile Name Profile Name \\ username.
ms.assetid: 9b13f91d-c3ee-4862-800c-fda831dce859
ms.tgt_platform: multiple
keywords:
- AD-Schema für MS-TS-profile-path-Attribut
- mstsprofilepath-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- ms-TS-Profile-Path
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67243c2ef588bd1470a50417c0948b1ea4ea7fa9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957474"
---
# <a name="ms-ts-profile-path-attribute"></a>MS-TS-profile-path-Attribut

Der Terminal Dienste-Profilpfad gibt einen roamingpfad oder obligatorischen Profilpfad an, der verwendet wird, wenn sich der Benutzer am Terminal Server anmeldet. Der Profilpfad weist das folgende Format für den Netzwerkpfad auf: **\\\\** _Server_ Name *_\\_* _profilesfoldername_ *_\\_* _Benutzername_.



| Eingabe | Wert |
|-------------------|---------------------------------------------|
| CN                | MS-TS-profile-Path                          |
| LDAP-Display-Name | mstsprofilepath                             |
| Size              | \-                                          |
| Berechtigung aktualisieren  | \-                                          |
| Aktualisierungshäufigkeit  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.1976                     |
| System-ID-GUID    | e65c30db-316c-4060-a3a0-387b083-CD        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Ist-einwertig       | Richtig                              |
| Ist indiziert             | False                             |
| Im globalen Katalog      | False                             |
| NT-Security-Descriptor | o:Bag: schlecht: S:                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 32767                             |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Ist-einwertig       | Richtig                              |
| Ist indiziert             | False                             |
| Im globalen Katalog      | False                             |
| NT-Security-Descriptor | o:Bag: schlecht: S:                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 32767                             |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Ist-einwertig       | Richtig                              |
| Ist indiziert             | False                             |
| Im globalen Katalog      | False                             |
| NT-Security-Descriptor | o:Bag: schlecht: S:                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 32767                             |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



 

 





