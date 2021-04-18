---
title: MS-TAPI-Conference-BLOB-Attribut
description: Ein binäres Blob von Daten, das verschiedene Eigenschaften einer TAPI-Multicast Konferenz beschreibt. Das Format und der Inhalt werden durch den Wert des Attributs Protocol-Id im selben Objekt bestimmt. Die Daten in diesem BLOB entsprechen in der Regel RFC2327.
ms.assetid: f1d5baed-df3f-423e-aa2f-005e77e79725
ms.tgt_platform: multiple
keywords:
- MS-TAPI-Conference-BLOB-Attribut AD-Schema
- AD-Schema des MSTAPI-conferenceblob-Attributs
topic_type:
- apiref
api_name:
- ms-TAPI-Conference-Blob
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f4e3ec8b74144daca7af1788c08270d998c139c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106340046"
---
# <a name="ms-tapi-conference-blob-attribute"></a>MS-TAPI-Conference-BLOB-Attribut

Ein binäres Blob von Daten, das verschiedene Eigenschaften einer TAPI-Multicast Konferenz beschreibt. Das Format und der Inhalt werden durch den Wert des Attributs Protocol-Id im selben Objekt bestimmt. Die Daten in diesem BLOB entsprechen in der Regel RFC2327.



| Eingabe | Wert |
|-------------------|--------------------------------------------------------------------------------------------------------------|
| CN                | MS-TAPI-Conference-BLOB                                                                                      |
| LDAP-Display-Name | MSTAPI-confererceblob                                                                                        |
| Size              | Kann eine beliebige Länge aufweisen.                                                                                  |
| Berechtigung aktualisieren  | Es sind keine besonderen Berechtigungen erforderlich.                                                                              |
| Aktualisierungshäufigkeit  | Kann nach dem Ermessen eines TAPI-Konferenz Besitzers geändert werden, wenn sich einige Daten über die Konferenz ändern müssen. |
| Attribute-Id      | 1.2.840.113556.1.4.1700                                                                                      |
| System-ID-GUID    | 4cc4601e-7201-4141-abc8-3e529ae88863                                                                         |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md)                                                        |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------|
| Link-ID                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | False                                                             |
| Ist-einwertig       | Richtig                                                              |
| Ist indiziert             | False                                                             |
| Im globalen Katalog      | False                                                             |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| In verwendete Klassen        | [**MS-TAPI-RT-Konferenz**](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------|
| Link-ID                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | False                                                             |
| Ist-einwertig       | Richtig                                                              |
| Ist indiziert             | False                                                             |
| Im globalen Katalog      | False                                                             |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| In verwendete Klassen        | [**MS-TAPI-RT-Konferenz**](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------|
| Link-ID                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | False                                                             |
| Ist-einwertig       | Richtig                                                              |
| Ist indiziert             | False                                                             |
| Im globalen Katalog      | False                                                             |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| In verwendete Klassen        | [**MS-TAPI-RT-Konferenz**](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------|
| Link-ID                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | False                                                             |
| Ist-einwertig       | Richtig                                                              |
| Ist indiziert             | False                                                             |
| Im globalen Katalog      | False                                                             |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| In verwendete Klassen        | [**MS-TAPI-RT-Konferenz**](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------|
| Link-ID                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | False                                                             |
| Ist-einwertig       | Richtig                                                              |
| Ist indiziert             | False                                                             |
| Im globalen Katalog      | False                                                             |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| In verwendete Klassen        | [**MS-TAPI-RT-Konferenz**](c-mstapi-rtconference.md)<br/> |



 

 





