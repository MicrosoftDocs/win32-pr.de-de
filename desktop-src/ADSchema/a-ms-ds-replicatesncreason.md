---
title: MS-DS-Replicates-NC-Reason-Attribut
description: Attribut des ntdsConnection-Objekts, das angibt, warum (oder ob) der KCC anzeigt, dass die Verbindung in der Replikationstopologie nützlich ist. Ist mehrwertig und verfügt über distName+Binärsyntax, wobei der binäre Teil ein Bitfeld der Int-Größe ist.
ms.assetid: ba66e346-d288-4c0b-b41e-599c3f8e8405
ms.tgt_platform: multiple
keywords:
- AD-Schema des MS-DS-Replicates-NC-Reason-Attributs
- mS-DS-ReplicatesNCReason-Attribut AD-Schema
topic_type:
- apiref
api_name:
- MS-DS-Replicates-NC-Reason
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 681105fe24584afae275a8869ad04698ff7a70daa32832140a98865318672863
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118686971"
---
# <a name="ms-ds-replicates-nc-reason-attribute"></a>MS-DS-Replicates-NC-Reason-Attribut

Attribut des ntdsConnection-Objekts, das angibt, warum (oder ob) der KCC anzeigt, dass die Verbindung in der Replikationstopologie nützlich ist. Ist mehrwertig und verfügt über distName+Binärsyntax, wobei der binäre Teil ein Bitfeld der Int-Größe ist.



| Eingabe | Wert |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| CN                | MS-DS-Replicates-NC-Reason                                                                                                                 |
| Ldap-Anzeigename | mS-DS-ReplicatesNCReason                                                                                                                   |
| Size              | Wert für binären Teil: 0 = NO \_ REASON,1 = \_ GC-TOPOLOGIE, 2 = RINGTOPOLOGIE, \_ 4 = MINIMIEREN DER \_ HOPS-TOPOLOGIE, \_ 8 = TOPOLOGIE VERALTETER \_ \_ SERVER. |
| Aktualisieren von Berechtigungen  | Dieser Wert wird vom System festgelegt.                                                                                                           |
| Updatehäufigkeit  | Kann sich als Reaktion auf Änderungen in der Netzwerktopologie ändern.                                                                                 |
| Attribute-Id      | 1.2.840.113556.1.4.1408                                                                                                                    |
| System-Id-Guid    | 0ea12b84-08b3-11d3-91bc-0000f87a57d4                                                                                                       |
| Syntax            | [**Object(DN-Binary)**](s-object-dn-binary.md)                                                                                            |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|--------------------------------------------------------|
| Link-ID                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | Falsch                                                  |
| Is-Single-Valued       | Falsch                                                  |
| Ist indiziert             | Falsch                                                  |
| Im globalen Katalog      | Falsch                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| In verwendete Klassen        | [**NTDS-Verbindung**](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|--------------------------------------------------------|
| Link-ID                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | Falsch                                                  |
| Is-Single-Valued       | Falsch                                                  |
| Ist indiziert             | Falsch                                                  |
| Im globalen Katalog      | Falsch                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| In verwendete Klassen        | [**NTDS-Verbindung**](c-ntdsconnection.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|--------------------------------------------------------|
| Link-ID                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | Falsch                                                  |
| Is-Single-Valued       | Falsch                                                  |
| Ist indiziert             | Falsch                                                  |
| Im globalen Katalog      | Falsch                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| In verwendete Klassen        | [**NTDS-Verbindung**](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------------------|
| Link-ID                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | Falsch                                                  |
| Is-Single-Valued       | Falsch                                                  |
| Ist indiziert             | Falsch                                                  |
| Im globalen Katalog      | Falsch                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| In verwendete Klassen        | [**NTDS-Verbindung**](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|--------------------------------------------------------|
| Link-ID                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | Falsch                                                  |
| Is-Single-Valued       | Falsch                                                  |
| Ist indiziert             | Falsch                                                  |
| Im globalen Katalog      | Falsch                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| In verwendete Klassen        | [**NTDS-Verbindung**](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------------------|
| Link-ID                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | Falsch                                                  |
| Is-Single-Valued       | Falsch                                                  |
| Ist indiziert             | Falsch                                                  |
| Im globalen Katalog      | Falsch                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| In verwendete Klassen        | [**NTDS-Verbindung**](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|--------------------------------------------------------|
| Link-ID                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | Falsch                                                  |
| Is-Single-Valued       | Falsch                                                  |
| Ist indiziert             | Falsch                                                  |
| Im globalen Katalog      | Falsch                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| In verwendete Klassen        | [**NTDS-Verbindung**](c-ntdsconnection.md)<br/> |



 

 





