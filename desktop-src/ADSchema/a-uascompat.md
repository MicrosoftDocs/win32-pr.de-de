---
title: UAS-Compat-Attribut
description: Gibt an, ob der Sicherheits Konto-Manager Datengrößen erzwingt, um Active Directory kompatibel mit dem Benutzerkonto System von LanManager zu machen.
ms.assetid: 745e271e-28f4-4012-83a8-606d88de0221
ms.tgt_platform: multiple
keywords:
- AD-Schema für UAS-Compat-Attribut
- AD-Schema für uascompat-Attribut
topic_type:
- apiref
api_name:
- UAS-Compat
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6bbf1088f48c697b03c4ef423930be2dbd24617
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106343518"
---
# <a name="uas-compat-attribute"></a>UAS-Compat-Attribut

Gibt an, ob der Sicherheits Konto-Manager Datengrößen erzwingt, um Active Directory kompatibel mit dem Benutzerkonto System von LanManager zu machen. Wenn dieser Wert 0 ist, werden keine Grenzwerte erzwungen. Wenn dieser Wert 1 ist, werden die folgenden Grenzwerte erzwungen.



| Wert                          | Länge                         |
|--------------------------------|--------------------------------|
| Kennwort<br/>            | 0 bis 14 Zeichen<br/>  |
| Kontoname<br/>        | 0 bis 20 Zeichen<br/>  |
| Domänenname<br/>         | 0 bis 15 Zeichen<br/>  |
| Computername<br/>       | 0 bis 15 Zeichen<br/>  |
| Kommentare<br/>            | 0 bis 48 Zeichen<br/>  |
| Basisverzeichnis<br/>      | 0 bis 256 Zeichen<br/> |
| Skript Pfad<br/>         | 0 bis 256 Zeichen<br/> |
| Zeiteinheiten pro Woche<br/> | 168 Bits (21 Bytes)<br/> |



 



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | UAS-Compat                           |
| LDAP-Display-Name | uascompat                            |
| Size              | \-                                   |
| Berechtigung aktualisieren  | Wird von einem Administrator ausgeführt.       |
| Aktualisierungshäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.155               |
| System-ID-GUID    | bf967a61-0de6-11d0-a285-00aa003049e2 |
| Syntax            | [**Enumeration**](s-enumeration.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|-------------------------------------------------------|
| Link-ID                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | False                                                 |
| Ist-einwertig       | Richtig                                                  |
| Ist indiziert             | False                                                 |
| Im globalen Katalog      | False                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| In verwendete Klassen        | [**SAM-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-------------------------------------------------------|
| Link-ID                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | False                                                 |
| Ist-einwertig       | Richtig                                                  |
| Ist indiziert             | False                                                 |
| Im globalen Katalog      | False                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| In verwendete Klassen        | [**SAM-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------|
| Link-ID                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | False                                                 |
| Ist-einwertig       | Richtig                                                  |
| Ist indiziert             | False                                                 |
| Im globalen Katalog      | False                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| In verwendete Klassen        | [**SAM-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-------------------------------------------------------|
| Link-ID                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | False                                                 |
| Ist-einwertig       | Richtig                                                  |
| Ist indiziert             | False                                                 |
| Im globalen Katalog      | False                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| In verwendete Klassen        | [**SAM-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------|
| Link-ID                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | False                                                 |
| Ist-einwertig       | Richtig                                                  |
| Ist indiziert             | False                                                 |
| Im globalen Katalog      | False                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| In verwendete Klassen        | [**SAM-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-------------------------------------------------------|
| Link-ID                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | False                                                 |
| Ist-einwertig       | Richtig                                                  |
| Ist indiziert             | False                                                 |
| Im globalen Katalog      | False                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| In verwendete Klassen        | [**SAM-Domain-Base**](c-samdomainbase.md)<br/> |



 

 





