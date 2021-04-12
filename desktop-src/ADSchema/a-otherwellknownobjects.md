---
title: Anderes-Well-Known-Objects-Attribut
description: Enthält eine Liste der Container nach GUID und Distinguished Name. Dies ermöglicht das Abrufen eines Objekts, nachdem es mit nur der GUID und dem Domänen Namen verschoben wurde. Wenn das Objekt verschoben wird, aktualisiert das System automatisch den Distinguished Name.
ms.assetid: 2f33c4ac-235c-47a1-9340-5b90f7edb73b
ms.tgt_platform: multiple
keywords:
- AD-Schema für ein anderes-Well-Known-Objects-Attribut
- OtherWellKnownObjects-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Other-Well-Known-Objects
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d38b4f4b86f90368859f9fb966031f539f0399f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480271"
---
# <a name="other-well-known-objects-attribute"></a>Anderes-Well-Known-Objects-Attribut

Enthält eine Liste der Container nach GUID und Distinguished Name. Dies ermöglicht das Abrufen eines Objekts, nachdem es mit nur der GUID und dem Domänen Namen verschoben wurde. Wenn das Objekt verschoben wird, aktualisiert das System automatisch den Distinguished Name.



| Eingabe | Wert |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CN                | Andere-bekannte Objekte                                                                                                                                                                                      |
| LDAP-Display-Name | otherWellKnownObjects                                                                                                                                                                                         |
| Size              | Beispiel für das Abrufen des Benutzer Containers in der Microsoft-Domäne: LDAP://(wkguid = a9d1ca15768811d1aded00c04fd8d5cd, DC = Microsoft, DC = com). Hinweis: durch Klammern ersetzte spitzen Klammern, um XML-Konflikte zu vermeiden. |
| Berechtigung aktualisieren  | Schema Administrator                                                                                                                                                                                          |
| Aktualisierungshäufigkeit  | Immer dann, wenn das-Objekt verschoben wird.                                                                                                                                                                                 |
| Attribute-Id      | 1.2.840.113556.1.4.1359                                                                                                                                                                                       |
| System-ID-GUID    | 1ea64e5d-ac0f -11d2-90df-00c04f d91ab1                                                                                                                                                                          |
| Syntax            | [**Object(DN-Binary)**](s-object-dn-binary.md)                                                                                                                                                               |



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
| System-Only            | False                           |
| Ist-einwertig       | False                           |
| Ist indiziert             | False                           |
| Im globalen Katalog      | False                           |
| NT-Security-Descriptor | o:Bag: schlecht: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | False                           |
| Ist-einwertig       | False                           |
| Ist indiziert             | False                           |
| Im globalen Katalog      | False                           |
| NT-Security-Descriptor | o:Bag: schlecht: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | False                           |
| Ist-einwertig       | False                           |
| Ist indiziert             | False                           |
| Im globalen Katalog      | False                           |
| NT-Security-Descriptor | o:Bag: schlecht: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | False                           |
| Ist-einwertig       | False                           |
| Ist indiziert             | False                           |
| Im globalen Katalog      | False                           |
| NT-Security-Descriptor | o:Bag: schlecht: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | False                           |
| Ist-einwertig       | False                           |
| Ist indiziert             | False                           |
| Im globalen Katalog      | False                           |
| NT-Security-Descriptor | o:Bag: schlecht: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | False                           |
| Ist-einwertig       | False                           |
| Ist indiziert             | False                           |
| Im globalen Katalog      | False                           |
| NT-Security-Descriptor | o:Bag: schlecht: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | False                           |
| Ist-einwertig       | False                           |
| Ist indiziert             | False                           |
| Im globalen Katalog      | False                           |
| NT-Security-Descriptor | o:Bag: schlecht: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



 

 





