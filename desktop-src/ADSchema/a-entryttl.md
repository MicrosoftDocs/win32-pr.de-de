---
title: Entry-TTL-Attribut
description: Dieses Betriebs Attribut wird vom Server verwaltet und ist anscheinend in jedem dynamischen Eintrag vorhanden.
ms.assetid: cac0e52e-243d-4822-9419-2af8b9352cee
ms.tgt_platform: multiple
keywords:
- AD-Schema für Entry-TTL-Attribut
- entryttl-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Entry-TTL
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab2dd5e38b22731fee7f957ee8f817537e32c645
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479711"
---
# <a name="entry-ttl-attribute"></a>Entry-TTL-Attribut

Dieses Betriebs Attribut wird vom Server verwaltet und ist anscheinend in jedem dynamischen Eintrag vorhanden. Das-Attribut ist nicht vorhanden, wenn der Eintrag nicht die DynamicObject-Objektklasse enthält. Der Wert dieses Attributs ist die Zeit (in Sekunden), in der der Eintrag weiterhin vorhanden ist, bevor er aus dem Verzeichnis verschwindet. Wenn keine dazwischenliegenden "Refresh"-Vorgänge vorhanden sind, werden die Werte, die durch das Lesen des Attributs in zwei aufeinander folgenden suchen zurückgegeben werden, garantiert nicht zunehmen. Der kleinste zulässige Wert ist 0 (null) und gibt an, dass der Eintrag ohne Warnung verschwinden kann. Das Attribut ist als "keine Benutzer Änderung" gekennzeichnet, da es nur mit dem Aktualisierungs Vorgang geändert werden kann.



| Eingabe | Wert |
|-------------------|---------------------------------------------|
| CN                | Entry-TTL                                   |
| LDAP-Display-Name | entryttl                                    |
| Size              | 4 Bytes. Maximum = 1 Jahr, Standardwert = 1 Tag. |
| Berechtigung aktualisieren  | \-                                          |
| Aktualisierungshäufigkeit  | \-                                          |
| Attribute-Id      | 1.3.6.1.4.1.1466.101.119.3                  |
| System-ID-GUID    | d213decc-d81a-4384-aac2-dcfcfd631cf8        |
| Syntax            | [**Enumeration**](s-enumeration.md)        |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Ist-einwertig       | Richtig                                                 |
| Ist indiziert             | False                                                |
| Im globalen Katalog      | False                                                |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| In verwendete Klassen        | [**Dynamic-Object**](c-dynamicobject.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Ist-einwertig       | Richtig                                                 |
| Ist indiziert             | False                                                |
| Im globalen Katalog      | False                                                |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| In verwendete Klassen        | [**Dynamic-Object**](c-dynamicobject.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Ist-einwertig       | Richtig                                                 |
| Ist indiziert             | False                                                |
| Im globalen Katalog      | False                                                |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| In verwendete Klassen        | [**Dynamic-Object**](c-dynamicobject.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Ist-einwertig       | Richtig                                                 |
| Ist indiziert             | False                                                |
| Im globalen Katalog      | False                                                |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| In verwendete Klassen        | [**Dynamic-Object**](c-dynamicobject.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Ist-einwertig       | Richtig                                                 |
| Ist indiziert             | False                                                |
| Im globalen Katalog      | False                                                |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| In verwendete Klassen        | [**Dynamic-Object**](c-dynamicobject.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Ist-einwertig       | Richtig                                                 |
| Ist indiziert             | False                                                |
| Im globalen Katalog      | False                                                |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| In verwendete Klassen        | [**Dynamic-Object**](c-dynamicobject.md)<br/> |



 

 





