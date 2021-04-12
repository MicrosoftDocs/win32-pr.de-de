---
title: ms-DS-has-instantiated-NCS-Attribut
description: DS-Replikations Zustandsinformationen, analog zu (und einer übergeordneten Menge) der vorhandenen Attribute hasmasterncs und haspartialreplicancs. Für die Verwendung durch die KCC beim Einrichten von Replikations Partnern.
ms.assetid: 00dda441-e382-4fb2-b735-ae547901c11f
ms.tgt_platform: multiple
keywords:
- 'ms-DS-has-instanziiert: AD-Schema des NCS-Attributs'
- AD-Schema des msDS-hasinstantiatedncs-Attributs
topic_type:
- apiref
api_name:
- ms-DS-Has-Instantiated-NCs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2900d68f82e859bac7ce1dabbfea2d28fd8998b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480095"
---
# <a name="ms-ds-has-instantiated-ncs-attribute"></a>ms-DS-has-instantiated-NCS-Attribut

DS-Replikations Zustandsinformationen, analog zu (und einer übergeordneten Menge) der vorhandenen Attribute hasmasterncs und haspartialreplicancs. Für die Verwendung durch die KCC beim Einrichten von Replikations Partnern.



| Eingabe | Wert |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CN                | ms-DS-has-instantiated-NCS                                                                                                                                                                                  |
| LDAP-Display-Name | MSDS-hasinstantiatedncs                                                                                                                                                                                     |
| Size              | 4 Bytes                                                                                                                                                                                                     |
| Berechtigung aktualisieren  | Dieser Wert wird vom System festgelegt.                                                                                                                                                                            |
| Aktualisierungshäufigkeit  | Ungefähr doppelt so oft wie hasmasterncs/haspartialreplicancs. Diese vorhandenen Attribute werden nur aktualisiert, wenn der Domänen Controller eine Partition hinzufügt oder entfernt (z. b. bei Wechsel von DC in GC oder umgekehrt). |
| Attribute-Id      | 1.2.840.113556.1.4.1709                                                                                                                                                                                     |
| System-ID-GUID    | 11e9a5bc-4517-4049-af9c-51554, b0fc09                                                                                                                                                                        |
| Syntax            | [**Object(DN-Binary)**](s-object-dn-binary.md)                                                                                                                                                             |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|------------------------------------------|
| Link-ID                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | Richtig                                     |
| Ist-einwertig       | False                                    |
| Ist indiziert             | False                                    |
| Im globalen Katalog      | False                                    |
| NT-Security-Descriptor | o:Bag: schlecht: S:                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| In verwendete Klassen        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|------------------------------------------|
| Link-ID                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | Richtig                                     |
| Ist-einwertig       | False                                    |
| Ist indiziert             | False                                    |
| Im globalen Katalog      | False                                    |
| NT-Security-Descriptor | o:Bag: schlecht: S:                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| In verwendete Klassen        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|------------------------------------------|
| Link-ID                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | Richtig                                     |
| Ist-einwertig       | False                                    |
| Ist indiziert             | False                                    |
| Im globalen Katalog      | False                                    |
| NT-Security-Descriptor | o:Bag: schlecht: S:                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| In verwendete Klassen        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|------------------------------------------|
| Link-ID                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | Richtig                                     |
| Ist-einwertig       | False                                    |
| Ist indiziert             | False                                    |
| Im globalen Katalog      | False                                    |
| NT-Security-Descriptor | o:Bag: schlecht: S:                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| In verwendete Klassen        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|------------------------------------------|
| Link-ID                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | Richtig                                     |
| Ist-einwertig       | False                                    |
| Ist indiziert             | False                                    |
| Im globalen Katalog      | False                                    |
| NT-Security-Descriptor | o:Bag: schlecht: S:                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| In verwendete Klassen        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|------------------------------------------|
| Link-ID                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | Richtig                                     |
| Ist-einwertig       | False                                    |
| Ist indiziert             | False                                    |
| Im globalen Katalog      | False                                    |
| NT-Security-Descriptor | o:Bag: schlecht: S:                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| In verwendete Klassen        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



 

 





