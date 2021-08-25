---
title: ms-TS-Profile-Path-Attribut
description: Der Profilpfad für Terminaldienste gibt einen Roaming- oder obligatorischen Profilpfad an, der verwendet werden soll, wenn sich der Benutzer beim Terminalserver anmeldet. Der Profilpfad hat das folgende Netzwerkpfadformat \\ \\ ServerName \\ ProfilesFolderName \\ UserName.
ms.assetid: 9b13f91d-c3ee-4862-800c-fda831dce859
ms.tgt_platform: multiple
keywords:
- MS-TS-Profile-Path-Attribut AD-Schema
- AD-Schema des msTSProfilePath-Attributs
topic_type:
- apiref
api_name:
- ms-TS-Profile-Path
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08ee0a712581bf122d3ee8bdb5a2c035a088008d6a0841c26fd0a0b9f3d90ecc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119924290"
---
# <a name="ms-ts-profile-path-attribute"></a>ms-TS-Profile-Path-Attribut

Der Profilpfad für Terminaldienste gibt einen Roaming- oder obligatorischen Profilpfad an, der verwendet werden soll, wenn sich der Benutzer beim Terminalserver anmeldet. Der Profilpfad hat das folgende Netzwerkpfadformat: **\\\\** _ServerName_ *_\\_* _ProfilesFolderName_ *_\\_* _UserName_.



| Eingabe | Wert |
|-------------------|---------------------------------------------|
| CN                | ms-TS-Profile-Path                          |
| Ldap-Anzeigename | msTSProfilePath                             |
| Size              | \-                                          |
| Aktualisieren von Berechtigungen  | \-                                          |
| Updatehäufigkeit  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.1976                     |
| System-Id-Guid    | e65c30db-316c-4060-a3a0-387b083f09cd        |
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
| System-Only            | Falsch                             |
| Is-Single-Valued       | Richtig                              |
| Ist indiziert             | Falsch                             |
| Im globalen Katalog      | Falsch                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
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
| System-Only            | Falsch                             |
| Is-Single-Valued       | Richtig                              |
| Ist indiziert             | Falsch                             |
| Im globalen Katalog      | Falsch                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
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
| System-Only            | Falsch                             |
| Is-Single-Valued       | Richtig                              |
| Ist indiziert             | Falsch                             |
| Im globalen Katalog      | Falsch                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 32767                             |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



 

 





