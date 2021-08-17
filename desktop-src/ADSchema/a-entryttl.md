---
title: Entry-TTL-Attribut
description: Dieses Betriebsattribut wird vom Server verwaltet und scheint in jedem dynamischen Eintrag vorhanden zu sein.
ms.assetid: cac0e52e-243d-4822-9419-2af8b9352cee
ms.tgt_platform: multiple
keywords:
- AD-Schema des Entry-TTL-Attributs
- AD-Schema des entryTTL-Attributs
topic_type:
- apiref
api_name:
- Entry-TTL
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbcd3e06304824ba51431b00b6a5b90d24d7719194dd84974470a101d5f6a1c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961559"
---
# <a name="entry-ttl-attribute"></a>Entry-TTL-Attribut

Dieses Betriebsattribut wird vom Server verwaltet und scheint in jedem dynamischen Eintrag vorhanden zu sein. Das -Attribut ist nicht vorhanden, wenn der Eintrag die dynamicObject-Objektklasse nicht enthält. Der Wert dieses Attributs ist die Zeit (in Sekunden), zu der der Eintrag weiterhin vorhanden ist, bevor er aus dem Verzeichnis entfernt wird. Wenn keine "Aktualisierungsvorgänge" durchgeführt werden, werden die Werte, die beim Lesen des Attributs in zwei aufeinander folgenden Suchvorgängen zurückgegeben werden, garantiert nicht inkrementiert. Der kleinste zulässige Wert ist 0 und gibt an, dass der Eintrag ohne Warnung möglicherweise nicht mehr angezeigt wird. Das Attribut ist als NO-USER-MODIFICATION gekennzeichnet, da es nur mithilfe des Aktualisierungsvorgang geändert werden kann.



| Eingabe | Wert |
|-------------------|---------------------------------------------|
| CN                | Entry-TTL                                   |
| Ldap-Anzeigename | entryTTL                                    |
| Size              | 4 Bytes. Maximum = 1 Jahr, Standardwert = 1 Tag. |
| Aktualisieren von Berechtigungen  | \-                                          |
| Updatehäufigkeit  | \-                                          |
| Attribute-Id      | 1.3.6.1.4.1.1466.101.119.3                  |
| System-Id-Guid    | d213decc-d81a-4384-aac2-dcfcfd631cf8        |
| Syntax            | [**Enumeration**](s-enumeration.md)        |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falsch                                                |
| Is-Single-Valued       | Richtig                                                 |
| Ist indiziert             | Falsch                                                |
| Im globalen Katalog      | Falsch                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
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
| System-Only            | Falsch                                                |
| Is-Single-Valued       | Richtig                                                 |
| Ist indiziert             | Falsch                                                |
| Im globalen Katalog      | Falsch                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
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
| System-Only            | Falsch                                                |
| Is-Single-Valued       | Richtig                                                 |
| Ist indiziert             | Falsch                                                |
| Im globalen Katalog      | Falsch                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
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
| System-Only            | Falsch                                                |
| Is-Single-Valued       | Richtig                                                 |
| Ist indiziert             | Falsch                                                |
| Im globalen Katalog      | Falsch                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
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
| System-Only            | Falsch                                                |
| Is-Single-Valued       | Richtig                                                 |
| Ist indiziert             | Falsch                                                |
| Im globalen Katalog      | Falsch                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
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
| System-Only            | Falsch                                                |
| Is-Single-Valued       | Richtig                                                 |
| Ist indiziert             | Falsch                                                |
| Im globalen Katalog      | Falsch                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| In verwendete Klassen        | [**Dynamic-Object**](c-dynamicobject.md)<br/> |



 

 





