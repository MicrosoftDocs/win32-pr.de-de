---
title: Domänen-ID-Attribut
description: Verweis auf eine Domäne, die einer Zertifizierungsstelle zugeordnet ist.
ms.assetid: dd2f0822-cf94-485b-8d21-8954dddb81ad
ms.tgt_platform: multiple
keywords:
- AD-Schema des Domänen-ID-Attributs
- AD-Schema des domainID-Attributs
topic_type:
- apiref
api_name:
- Domain-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ae98294df75cdd2fdd69576629b87dbea8410b17d91ba525024a2a0a43ce7c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119925970"
---
# <a name="domain-id-attribute"></a>Domänen-ID-Attribut

Verweis auf eine Domäne, die einer Zertifizierungsstelle zugeordnet ist.



| Eingabe | Wert |
|-------------------|-----------------------------------------|
| CN                | Domänen-ID                               |
| Ldap-Anzeigename | domainID                                |
| Size              | \-                                      |
| Aktualisieren von Berechtigungen  | \-                                      |
| Updatehäufigkeit  | \-                                      |
| Attribute-Id      | 1.2.840.113556.1.4.686                  |
| System-ID-GUID    | 963d2734-48be-11d1-a9c3-0000f80367c1    |
| Syntax            | [**Object(DS-DN)**](s-object-ds-dn.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------|
| Link-ID                | \-                                                                     |
| MAPI-Id                | \-                                                                     |
| System-Only            | Falsch                                                                  |
| Ist einwertig       | Richtig                                                                   |
| Ist indiziert             | Falsch                                                                  |
| Im globalen Katalog      | Falsch                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                           |
| Range-Lower            | \-                                                                     |
| Range-Upper            | \-                                                                     |
| Search-Flags           | 0x00000000                                                             |
| System-Flags           | 0x00000010                                                             |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------|
| Link-ID                | \-                                                                     |
| MAPI-Id                | \-                                                                     |
| System-Only            | Falsch                                                                  |
| Ist einwertig       | Richtig                                                                   |
| Ist indiziert             | Falsch                                                                  |
| Im globalen Katalog      | Falsch                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                           |
| Range-Lower            | \-                                                                     |
| Range-Upper            | \-                                                                     |
| Search-Flags           | 0x00000000                                                             |
| System-Flags           | 0x00000010                                                             |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------|
| Link-ID                | \-                                                                     |
| MAPI-Id                | \-                                                                     |
| System-Only            | Falsch                                                                  |
| Ist einwertig       | Richtig                                                                   |
| Ist indiziert             | Falsch                                                                  |
| Im globalen Katalog      | Falsch                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                           |
| Range-Lower            | \-                                                                     |
| Range-Upper            | \-                                                                     |
| Search-Flags           | 0x00000000                                                             |
| System-Flags           | 0x00000010                                                             |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------|
| Link-ID                | \-                                                                     |
| MAPI-Id                | \-                                                                     |
| System-Only            | Falsch                                                                  |
| Is-Single-Valued       | Richtig                                                                   |
| Ist indiziert             | Falsch                                                                  |
| Im globalen Katalog      | Falsch                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                           |
| Range-Lower            | \-                                                                     |
| Range-Upper            | \-                                                                     |
| Search-Flags           | 0x00000000                                                             |
| System-Flags           | 0x00000010                                                             |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------|
| Link-ID                | \-                                                                     |
| MAPI-Id                | \-                                                                     |
| System-Only            | Falsch                                                                  |
| Is-Single-Valued       | Richtig                                                                   |
| Ist indiziert             | Falsch                                                                  |
| Im globalen Katalog      | Falsch                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                           |
| Range-Lower            | \-                                                                     |
| Range-Upper            | \-                                                                     |
| Search-Flags           | 0x00000000                                                             |
| System-Flags           | 0x00000010                                                             |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------|
| Link-ID                | \-                                                                     |
| MAPI-Id                | \-                                                                     |
| System-Only            | Falsch                                                                  |
| Is-Single-Valued       | Richtig                                                                   |
| Ist indiziert             | Falsch                                                                  |
| Im globalen Katalog      | Falsch                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                           |
| Range-Lower            | \-                                                                     |
| Range-Upper            | \-                                                                     |
| Search-Flags           | 0x00000000                                                             |
| System-Flags           | 0x00000010                                                             |
| In verwendete Klassen        | [**Zertifizierungsstelle**](c-certificationauthority.md)<br/> |



 

 





