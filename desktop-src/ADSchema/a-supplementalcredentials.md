---
title: Supplemental-Credentials-Attribut
description: Gespeicherte Anmeldeinformationen für die Authentifizierung. Die verschlüsselte Version des Kennworts des Benutzers. Dieses Attribut ist weder lesbar noch beschreibbar.
ms.assetid: 642aa699-094e-40ed-a2f8-ec7219c85de2
ms.tgt_platform: multiple
keywords:
- Supplemental-Credentials AD-Schema
- AD-Schema des supplementalCredentials-Attributs
topic_type:
- apiref
api_name:
- Supplemental-Credentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c677e3f8f7c290dddc00b1754c611f68d778e6539086f3c5c6a0f2a0e9af8775
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119836080"
---
# <a name="supplemental-credentials-attribute"></a>Supplemental-Credentials-Attribut

Gespeicherte Anmeldeinformationen für die Authentifizierung. Die verschlüsselte Version des Kennworts des Benutzers. Dieses Attribut ist weder lesbar noch beschreibbar.



| Eingabe | Wert |
|-------------------|-------------------------------------------------------|
| CN                | Supplemental-Credentials                              |
| Ldap-Anzeigename | supplementalCredentials                               |
| Size              | \-                                                    |
| Aktualisieren von Berechtigungen  | Dieser Wert wird vom System festgelegt.                      |
| Updatehäufigkeit  | Wenn sich das Kennwort des Benutzers ändert.                     |
| Attribute-Id      | 1.2.840.113556.1.4.125                                |
| System-Id-Guid    | bf967a3f-0de6-11d0-a285-00aa003049e2                  |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md) |



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
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falsch                                                        |
| Is-Single-Valued       | Falsch                                                        |
| Ist indiziert             | Falsch                                                        |
| Im globalen Katalog      | Falsch                                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x00000010                                                   |
| In verwendete Klassen        | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falsch                                                        |
| Is-Single-Valued       | Falsch                                                        |
| Ist indiziert             | Falsch                                                        |
| Im globalen Katalog      | Falsch                                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x00000010                                                   |
| In verwendete Klassen        | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falsch                                                        |
| Is-Single-Valued       | Falsch                                                        |
| Ist indiziert             | Falsch                                                        |
| Im globalen Katalog      | Falsch                                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x00000010                                                   |
| In verwendete Klassen        | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falsch                                                        |
| Ist einwertig       | Falsch                                                        |
| Ist indiziert             | Falsch                                                        |
| Im globalen Katalog      | Falsch                                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x00000010                                                   |
| In verwendete Klassen        | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falsch                                                        |
| Ist einwertig       | Falsch                                                        |
| Ist indiziert             | Falsch                                                        |
| Im globalen Katalog      | Falsch                                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x00000010                                                   |
| In verwendete Klassen        | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falsch                                                        |
| Ist einwertig       | Falsch                                                        |
| Ist indiziert             | Falsch                                                        |
| Im globalen Katalog      | Falsch                                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x00000010                                                   |
| In verwendete Klassen        | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falsch                                                        |
| Ist einwertig       | Falsch                                                        |
| Ist indiziert             | Falsch                                                        |
| Im globalen Katalog      | Falsch                                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x00000010                                                   |
| In verwendete Klassen        | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> |



 

 





