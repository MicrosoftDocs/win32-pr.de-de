---
title: DHCP-Type-Attribut
description: Der Typ des DHCP-Servers.
ms.assetid: 46ab7db7-a752-45aa-a10b-1195b5cf6f80
ms.tgt_platform: multiple
keywords:
- AD-Schema für DHCP-Type-Attribut
- dhcptype-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- dhcp-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b5a5a331ff7298854f4ca070799a05e2a3497f2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957351"
---
# <a name="dhcp-type-attribute"></a>DHCP-Type-Attribut

Der Typ des DHCP-Servers. Dieses Attribut wird für alle Objekte von objectClass [**dhcpclass**](c-dhcpclass.md)festgelegt. Der zugehörige Wert definiert den Objekttyp:

``` syntax
  0 - DHCP Root Object
  1 - DHCP Server
```



| Eingabe | Wert |
|-------------------|--------------------------------------------------------|
| CN                | DHCP-Typ                                              |
| LDAP-Display-Name | dhcptype                                               |
| Size              | 4 Bytes                                                |
| Berechtigung aktualisieren  | Domänen Administrator.                                  |
| Aktualisierungshäufigkeit  | Wenn ein neuer Server der Gesamtstruktur hinzugefügt oder daraus entfernt wird. |
| Attribute-Id      | 1.2.840.113556.1.4.699                                 |
| System-ID-GUID    | 963d273b-48be-11d1-a9c3-0000b80367c1                   |
| Syntax            | [**Enumeration**](s-enumeration.md)                   |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Ist-einwertig       | Richtig                                         |
| Ist indiziert             | Richtig                                         |
| Im globalen Katalog      | False                                        |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**DHCP-Klasse**](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Ist-einwertig       | Richtig                                         |
| Ist indiziert             | Richtig                                         |
| Im globalen Katalog      | False                                        |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**DHCP-Klasse**](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Ist-einwertig       | Richtig                                         |
| Ist indiziert             | Richtig                                         |
| Im globalen Katalog      | False                                        |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**DHCP-Klasse**](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Ist-einwertig       | Richtig                                         |
| Ist indiziert             | Richtig                                         |
| Im globalen Katalog      | False                                        |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**DHCP-Klasse**](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Ist-einwertig       | Richtig                                         |
| Ist indiziert             | Richtig                                         |
| Im globalen Katalog      | False                                        |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**DHCP-Klasse**](c-dhcpclass.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Ist-einwertig       | Richtig                                         |
| Ist indiziert             | Richtig                                         |
| Im globalen Katalog      | False                                        |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**DHCP-Klasse**](c-dhcpclass.md)<br/> |



 

 





