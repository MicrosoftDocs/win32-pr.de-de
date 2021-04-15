---
title: MS-DS-replicates-NC-Reason-Attribut
description: Das Attribut des nTDSConnection-Objekts, das angibt, warum (oder ob) die KCC anzeigt, dass die Verbindung in der Replikations Topologie nützlich ist. Ist mit mehreren Werten und verfügt über die Syntax "DISTNAME + Binary", wobei der binäre Teil ein Bitfeld mit int-Größe ist.
ms.assetid: ba66e346-d288-4c0b-b41e-599c3f8e8405
ms.tgt_platform: multiple
keywords:
- MS-DS-replicates-NC-Reason-Attribut AD-Schema
- AD-Schema des ms-DS-replitoresnkreason-Attributs
topic_type:
- apiref
api_name:
- MS-DS-Replicates-NC-Reason
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a45c587ef82773b5e7fd310e8e8591f18ad27ab
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104392252"
---
# <a name="ms-ds-replicates-nc-reason-attribute"></a>MS-DS-replicates-NC-Reason-Attribut

Das Attribut des nTDSConnection-Objekts, das angibt, warum (oder ob) die KCC anzeigt, dass die Verbindung in der Replikations Topologie nützlich ist. Ist mit mehreren Werten und verfügt über die Syntax "DISTNAME + Binary", wobei der binäre Teil ein Bitfeld mit int-Größe ist.



| Eingabe | Wert |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| CN                | MS-DS-replicates-NC-Reason                                                                                                                 |
| LDAP-Display-Name | mS-DS-replialisiesnkreason                                                                                                                   |
| Size              | Wert für binären Teil: 0 = kein \_ Grund, 1 = GC- \_ Topologie, 2 = Ring \_ Topologie, 4 = \_ \_ hoptopologie minimieren, 8 = veraltete \_ Server \_ Topologie. |
| Berechtigung aktualisieren  | Dieser Wert wird vom System festgelegt.                                                                                                           |
| Aktualisierungshäufigkeit  | Kann als Reaktion auf Änderungen in der Netzwerktopologie geändert werden.                                                                                 |
| Attribute-Id      | 1.2.840.113556.1.4.1408                                                                                                                    |
| System-ID-GUID    | 0ea12b84-08b3-11d3-91bc-0000f 87a57d4                                                                                                       |
| Syntax            | [**Object(DN-Binary)**](s-object-dn-binary.md)                                                                                            |



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
|------------------------|--------------------------------------------------------|
| Link-ID                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | False                                                  |
| Ist-einwertig       | False                                                  |
| Ist indiziert             | False                                                  |
| Im globalen Katalog      | False                                                  |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| In verwendete Klassen        | [**NTDS-Verbindung**](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|--------------------------------------------------------|
| Link-ID                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | False                                                  |
| Ist-einwertig       | False                                                  |
| Ist indiziert             | False                                                  |
| Im globalen Katalog      | False                                                  |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                           |
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
| System-Only            | False                                                  |
| Ist-einwertig       | False                                                  |
| Ist indiziert             | False                                                  |
| Im globalen Katalog      | False                                                  |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                           |
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
| System-Only            | False                                                  |
| Ist-einwertig       | False                                                  |
| Ist indiziert             | False                                                  |
| Im globalen Katalog      | False                                                  |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                           |
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
| System-Only            | False                                                  |
| Ist-einwertig       | False                                                  |
| Ist indiziert             | False                                                  |
| Im globalen Katalog      | False                                                  |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                           |
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
| System-Only            | False                                                  |
| Ist-einwertig       | False                                                  |
| Ist indiziert             | False                                                  |
| Im globalen Katalog      | False                                                  |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                           |
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
| System-Only            | False                                                  |
| Ist-einwertig       | False                                                  |
| Ist indiziert             | False                                                  |
| Im globalen Katalog      | False                                                  |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| In verwendete Klassen        | [**NTDS-Verbindung**](c-ntdsconnection.md)<br/> |



 

 





