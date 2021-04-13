---
title: MS-TAPI-Unique-Identifier-Attribut
description: Stellt den Namen einer TAPI-Multicast Konferenz bereit. Dabei handelt es sich um das Naming-Attribut der Rt-Conference-Klasse.
ms.assetid: a8162af7-0169-4381-8edc-3dbbf178e8ed
ms.tgt_platform: multiple
keywords:
- AD-Schema für MS-TAPI-Unique-Identifier-Attribut
- AD-Schema des MSTAPI-UID-Attributs
topic_type:
- apiref
api_name:
- ms-TAPI-Unique-Identifier
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 528d34d9d4282dac3f5bd5a41231094fd2666c2c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104392274"
---
# <a name="ms-tapi-unique-identifier-attribute"></a>MS-TAPI-Unique-Identifier-Attribut

Stellt den Namen einer TAPI-Multicast Konferenz bereit. Dabei handelt es sich um das Naming-Attribut der Rt-Conference-Klasse.



| Eingabe | Wert |
|-------------------|-----------------------------------------------------------------------|
| CN                | MS-TAPI-Unique-Identifier                                             |
| LDAP-Display-Name | MSTAPI-UID                                                            |
| Size              | Kann eine beliebige Zeichenfolge sein, in der Regel mit einer Länge von 100 Zeichen. |
| Berechtigung aktualisieren  | Es sind keine besonderen Berechtigungen erforderlich.                                       |
| Aktualisierungshäufigkeit  | Wird einmal zum Zeitpunkt der Erstellung des Rt-Conference Objekts festgelegt.            |
| Attribute-Id      | 1.2.840.113556.1.4.1698                                               |
| System-ID-GUID    | 70a4e7ea-b3b9-4643-8918-e6dd2471bbd4                                  |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                           |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                          |
| MAPI-Id                | \-                                                                                                                          |
| System-Only            | False                                                                                                                       |
| Ist-einwertig       | Richtig                                                                                                                        |
| Ist indiziert             | False                                                                                                                       |
| Im globalen Katalog      | False                                                                                                                       |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                |
| Range-Lower            | \-                                                                                                                          |
| Range-Upper            | \-                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                  |
| System-Flags           | 0x00000010                                                                                                                  |
| In verwendete Klassen        | [**MS-TAPI-RT-Konferenz**](c-mstapi-rtconference.md)<br/> [**MS-TAPI-RT-Person**](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                          |
| MAPI-Id                | \-                                                                                                                          |
| System-Only            | False                                                                                                                       |
| Ist-einwertig       | Richtig                                                                                                                        |
| Ist indiziert             | False                                                                                                                       |
| Im globalen Katalog      | False                                                                                                                       |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                |
| Range-Lower            | \-                                                                                                                          |
| Range-Upper            | \-                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                  |
| System-Flags           | 0x00000010                                                                                                                  |
| In verwendete Klassen        | [**MS-TAPI-RT-Konferenz**](c-mstapi-rtconference.md)<br/> [**MS-TAPI-RT-Person**](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                          |
| MAPI-Id                | \-                                                                                                                          |
| System-Only            | False                                                                                                                       |
| Ist-einwertig       | Richtig                                                                                                                        |
| Ist indiziert             | False                                                                                                                       |
| Im globalen Katalog      | False                                                                                                                       |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                |
| Range-Lower            | \-                                                                                                                          |
| Range-Upper            | \-                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                  |
| System-Flags           | 0x00000010                                                                                                                  |
| In verwendete Klassen        | [**MS-TAPI-RT-Konferenz**](c-mstapi-rtconference.md)<br/> [**MS-TAPI-RT-Person**](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                          |
| MAPI-Id                | \-                                                                                                                          |
| System-Only            | False                                                                                                                       |
| Ist-einwertig       | Richtig                                                                                                                        |
| Ist indiziert             | False                                                                                                                       |
| Im globalen Katalog      | False                                                                                                                       |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                |
| Range-Lower            | \-                                                                                                                          |
| Range-Upper            | \-                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                  |
| System-Flags           | 0x00000010                                                                                                                  |
| In verwendete Klassen        | [**MS-TAPI-RT-Konferenz**](c-mstapi-rtconference.md)<br/> [**MS-TAPI-RT-Person**](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                          |
| MAPI-Id                | \-                                                                                                                          |
| System-Only            | False                                                                                                                       |
| Ist-einwertig       | Richtig                                                                                                                        |
| Ist indiziert             | False                                                                                                                       |
| Im globalen Katalog      | False                                                                                                                       |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                |
| Range-Lower            | \-                                                                                                                          |
| Range-Upper            | \-                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                  |
| System-Flags           | 0x00000010                                                                                                                  |
| In verwendete Klassen        | [**MS-TAPI-RT-Konferenz**](c-mstapi-rtconference.md)<br/> [**MS-TAPI-RT-Person**](c-mstapi-rtperson.md)<br/> |



 

 





