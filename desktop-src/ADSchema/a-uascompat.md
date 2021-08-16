---
title: UAS-Compat-Attribut
description: Gibt an, ob der Sicherheitskonto-Manager Datengrößen erzwingt, um Active Directory mit dem LanManager-Benutzerkontosystem (UAS) kompatibel zu machen.
ms.assetid: 745e271e-28f4-4012-83a8-606d88de0221
ms.tgt_platform: multiple
keywords:
- UAS-Compat AD-Schema
- AD-Schema des uASCompat-Attributs
topic_type:
- apiref
api_name:
- UAS-Compat
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72fa7a0cb7b8787a55c710f283dbcd37bbe0f6a296505c75a5335bf35ea69c34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118681539"
---
# <a name="uas-compat-attribute"></a>UAS-Compat-Attribut

Gibt an, ob der Sicherheitskonto-Manager Datengrößen erzwingt, um Active Directory mit dem LanManager-Benutzerkontosystem (UAS) kompatibel zu machen. Wenn dieser Wert 0 ist, werden keine Grenzwerte erzwungen. Wenn dieser Wert 1 ist, werden die folgenden Grenzwerte erzwungen.



| Wert                          | Länge                         |
|--------------------------------|--------------------------------|
| Kennwort<br/>            | 0 bis 14 Zeichen<br/>  |
| Kontoname<br/>        | 0 bis 20 Zeichen<br/>  |
| Domänenname<br/>         | 0 bis 15 Zeichen<br/>  |
| Computername<br/>       | 0 bis 15 Zeichen<br/>  |
| Kommentare<br/>            | 0 bis 48 Zeichen<br/>  |
| Basisverzeichnis<br/>      | 0 bis 256 Zeichen<br/> |
| Skriptpfad<br/>         | 0 bis 256 Zeichen<br/> |
| Zeiteinheiten pro Woche<br/> | 168 Bits (21 Bytes)<br/> |



 



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | UAS-Compat                           |
| Ldap-Anzeigename | uASCompat                            |
| Size              | \-                                   |
| Aktualisieren von Berechtigungen  | Wird von einem Administrator ausgeführt.       |
| Updatehäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.155               |
| System-Id-Guid    | bf967a61-0de6-11d0-a285-00aa003049e2 |
| Syntax            | [**Enumeration**](s-enumeration.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|-------------------------------------------------------|
| Link-ID                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Falsch                                                 |
| Is-Single-Valued       | Richtig                                                  |
| Ist indiziert             | Falsch                                                 |
| Im globalen Katalog      | Falsch                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| In verwendete Klassen        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-------------------------------------------------------|
| Link-ID                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Falsch                                                 |
| Is-Single-Valued       | Richtig                                                  |
| Ist indiziert             | Falsch                                                 |
| Im globalen Katalog      | Falsch                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| In verwendete Klassen        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------|
| Link-ID                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Falsch                                                 |
| Is-Single-Valued       | Richtig                                                  |
| Ist indiziert             | Falsch                                                 |
| Im globalen Katalog      | Falsch                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| In verwendete Klassen        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-------------------------------------------------------|
| Link-ID                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Falsch                                                 |
| Is-Single-Valued       | Richtig                                                  |
| Ist indiziert             | Falsch                                                 |
| Im globalen Katalog      | Falsch                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| In verwendete Klassen        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------|
| Link-ID                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Falsch                                                 |
| Is-Single-Valued       | Richtig                                                  |
| Ist indiziert             | Falsch                                                 |
| Im globalen Katalog      | Falsch                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| In verwendete Klassen        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-------------------------------------------------------|
| Link-ID                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Falsch                                                 |
| Is-Single-Valued       | Richtig                                                  |
| Ist indiziert             | Falsch                                                 |
| Im globalen Katalog      | Falsch                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| In verwendete Klassen        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



 

 





