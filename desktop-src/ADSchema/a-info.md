---
title: Kommentarattribut
description: Die Kommentare des Benutzers. Diese Zeichenfolge kann eine NULL-Zeichenfolge sein.
ms.assetid: c57493b3-a42a-49ad-8f8c-0afadbb3ba09
ms.tgt_platform: multiple
keywords:
- Ad-Schema des Kommentarattributs
- Infoattribut AD-Schema
topic_type:
- apiref
api_name:
- Comment
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 739203abd9cfbeb383ca4365bdc8b19135010830c4c23305aff18d86d9b03be3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119925490"
---
# <a name="comment-attribute-ad-schema"></a>Kommentarattribut (AD-Schema)

Die Kommentare des Benutzers. Diese Zeichenfolge kann eine NULL-Zeichenfolge sein.



| Eingabe | Wert |
|-------------------|--------------------------------------------------------------------------|
| CN                | Kommentar                                                                  |
| Ldap-Anzeigename | info                                                                     |
| Size              | \-                                                                       |
| Aktualisieren von Berechtigungen  | Domänenadministrator oder Kontobesitzer.                                   |
| Updatehäufigkeit  | Jedes Mal, wenn der Benutzer oder Administrator Kommentare zum Konto hinzufügen muss. |
| Attribute-Id      | 1.2.840.113556.1.2.81                                                    |
| System-Id-Guid    | bf96793e-0de6-11d0-a285-00aa003049e2                                     |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                              |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | 0x3004                                               |
| System-Only            | Falsch                                                |
| Is-Single-Valued       | Richtig                                                 |
| Ist indiziert             | Falsch                                                |
| Im globalen Katalog      | Falsch                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | 1                                                    |
| Range-Upper            | 1024                                                 |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | 0x3004                                               |
| System-Only            | Falsch                                                |
| Is-Single-Valued       | Richtig                                                 |
| Ist indiziert             | Falsch                                                |
| Im globalen Katalog      | Falsch                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | 1                                                    |
| Range-Upper            | 1024                                                 |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | 0x3004                                               |
| System-Only            | Falsch                                                |
| Is-Single-Valued       | Richtig                                                 |
| Ist indiziert             | Falsch                                                |
| Im globalen Katalog      | Falsch                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | 1                                                    |
| Range-Upper            | 1024                                                 |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | 0x3004                                               |
| System-Only            | Falsch                                                |
| Ist einwertig       | Richtig                                                 |
| Ist indiziert             | Falsch                                                |
| Im globalen Katalog      | Falsch                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | 1                                                    |
| Range-Upper            | 1024                                                 |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | 0x3004                                               |
| System-Only            | Falsch                                                |
| Ist einwertig       | Richtig                                                 |
| Ist indiziert             | Falsch                                                |
| Im globalen Katalog      | Falsch                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | 1                                                    |
| Range-Upper            | 1024                                                 |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | 0x3004                                               |
| System-Only            | Falsch                                                |
| Ist einwertig       | Richtig                                                 |
| Ist indiziert             | Falsch                                                |
| Im globalen Katalog      | Falsch                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | 1                                                    |
| Range-Upper            | 1024                                                 |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> |



 

 





