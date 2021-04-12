---
title: Well-Known-Objects-Attribut
description: Dieses Attribut enthält eine Liste bekannter Objekt Container nach GUID und Distinguished Name.
ms.assetid: e3c2d243-6734-4c2f-9ead-bc4ec071d1f1
ms.tgt_platform: multiple
keywords:
- Well-Known-Objects-Attribut AD-Schema
- wellKnownObjects-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Well-Known-Objects
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e21df3db14a29de137af4792f0e9ca6df27b90
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480199"
---
# <a name="well-known-objects-attribute"></a>Well-Known-Objects-Attribut

Dieses Attribut enthält eine Liste bekannter Objekt Container nach GUID und Distinguished Name. Bei den bekannten Objekten handelt es sich um System Container. Diese Informationen werden verwendet, um ein Objekt abzurufen, nachdem es mit nur der GUID und dem Domänen Namen verschoben wurde. Wenn das-Objekt verschoben wird, aktualisiert das System automatisch den Distinguished Name-Teil der Well-Known Objects-Werte, die auf das-Objekt verwiesen haben. Die Datei NTDSAPI. h enthält die folgenden Definitionen, die zum Abrufen eines Objekts verwendet werden können (die GUIDs, die diesen Objekten zugeordnet sind, sind in NTDSAPI. h enthalten):

-   GUID- \_ Benutzer \_ Container \_ W
-   GUID- \_ computrs- \_ Container \_ W
-   GUID- \_ Systeme \_ Container \_ W
-   GUID- \_ Domänen \_ Controller \_ Container \_ W
-   GUID- \_ Infrastruktur \_ Container \_ W
-   GUID- \_ Gelöschte \_ Objekte \_ Container \_ W
-   GUID \_ LostAndFound- \_ Container \_ W
-   GUID fremd \_ nsecurityprincipals \_ Container \_ W
-   GUID- \_ Programm \_ Daten \_ Container \_ W
-   GUID \_ Microsoft- \_ Programm \_ Daten \_ Container \_ W
-   GUID \_ NTDS- \_ Kontingente \_ Container \_ W



| Eingabe | Wert |
|-------------------|-------------------------------------------------|
| CN                | Bekannte Objekte                              |
| LDAP-Display-Name | wellKnownObjects                                |
| Size              | \-                                              |
| Berechtigung aktualisieren  | Dieser Wert wird vom System festgelegt.                |
| Aktualisierungshäufigkeit  | Jedes Mal, wenn einer der System Container verschoben wird. |
| Attribute-Id      | 1.2.840.113556.1.4.618                          |
| System-ID-GUID    | 05308983-7688-11d1-aded-00c04f d8d5cd            |
| Syntax            | [**Object(DN-Binary)**](s-object-dn-binary.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Richtig                            |
| Ist-einwertig       | False                           |
| Ist indiziert             | False                           |
| Im globalen Katalog      | Richtig                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Richtig                            |
| Ist-einwertig       | False                           |
| Ist indiziert             | False                           |
| Im globalen Katalog      | Richtig                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Richtig                            |
| Ist-einwertig       | False                           |
| Ist indiziert             | False                           |
| Im globalen Katalog      | Richtig                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Richtig                            |
| Ist-einwertig       | False                           |
| Ist indiziert             | False                           |
| Im globalen Katalog      | Richtig                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Richtig                            |
| Ist-einwertig       | False                           |
| Ist indiziert             | False                           |
| Im globalen Katalog      | Richtig                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Richtig                            |
| Ist-einwertig       | False                           |
| Ist indiziert             | False                           |
| Im globalen Katalog      | Richtig                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Richtig                            |
| Ist-einwertig       | False                           |
| Ist indiziert             | False                           |
| Im globalen Katalog      | Richtig                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



 

 





