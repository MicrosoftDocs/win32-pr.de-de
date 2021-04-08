---
title: SD-Rechte effektives Attribut
description: Dieses konstruierte Attribut gibt einen einzelnen DWORD-Wert zurück, der bis zu drei Bits festgelegt werden kann Sicherheits \_ \_ Informationen Sicherheits \_ \_ informationsacl Sicherheits informationsacl \_ Sicherheits \_ Informationen wenn ein Bit festgelegt ist, dann verfügt der Benutzer über Schreibzugriff auf den entsprechenden Teil der Sicherheits Beschreibung. Owner bedeutet Besitzer und Gruppe.
ms.assetid: 66d1aefb-49be-42fc-b144-3fb95c59dd0f
ms.tgt_platform: multiple
keywords:
- AD-Schema für SD-Rights-effektive Attribute
- AD-Schema des sdrightseffective-Attributs
topic_type:
- apiref
api_name:
- SD-Rights-Effective
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac449cd18b3fb75a61f04fffc266c290b7763295
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859575"
---
# <a name="sd-rights-effective-attribute"></a>SD-Rechte effektives Attribut

Dieses konstruierte Attribut gibt einen einzelnen **DWORD** -Wert zurück, für den bis zu drei Bits festgelegt werden können:

-   \_Sicherheits \_ Informationen für den Besitzer
-   DACL- \_ Sicherheits \_ Informationen
-   SACL- \_ Sicherheits \_ Informationen

Wenn ein Bit festgelegt ist, hat der Benutzer Schreibzugriff auf den entsprechenden Teil der Sicherheits Beschreibung. Owner bedeutet Besitzer und Gruppe.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | SD-Rechte                  |
| LDAP-Display-Name | sdrightabffective                    |
| Size              | \-                                   |
| Berechtigung aktualisieren  | \-                                   |
| Aktualisierungshäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1304              |
| System-ID-GUID    | c3dbafa6-33df-11d2-98b2-0000f87a57d4 |
| Syntax            | [**Enumeration**](s-enumeration.md) |



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
| Ist-einwertig       | Richtig                            |
| Ist indiziert             | False                           |
| Im globalen Katalog      | False                           |
| NT-Security-Descriptor | o:Bag: schlecht: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | False                           |
| Ist-einwertig       | Richtig                            |
| Ist indiziert             | False                           |
| Im globalen Katalog      | False                           |
| NT-Security-Descriptor | o:Bag: schlecht: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | False                           |
| Ist-einwertig       | Richtig                            |
| Ist indiziert             | False                           |
| Im globalen Katalog      | False                           |
| NT-Security-Descriptor | o:Bag: schlecht: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | False                           |
| Ist-einwertig       | Richtig                            |
| Ist indiziert             | False                           |
| Im globalen Katalog      | False                           |
| NT-Security-Descriptor | o:Bag: schlecht: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | False                           |
| Ist-einwertig       | Richtig                            |
| Ist indiziert             | False                           |
| Im globalen Katalog      | False                           |
| NT-Security-Descriptor | o:Bag: schlecht: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | False                           |
| Ist-einwertig       | Richtig                            |
| Ist indiziert             | False                           |
| Im globalen Katalog      | False                           |
| NT-Security-Descriptor | o:Bag: schlecht: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | False                           |
| Ist-einwertig       | Richtig                            |
| Ist indiziert             | False                           |
| Im globalen Katalog      | False                           |
| NT-Security-Descriptor | o:Bag: schlecht: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



 

 





