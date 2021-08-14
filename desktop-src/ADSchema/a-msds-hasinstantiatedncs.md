---
title: ms-DS-Has-Instantiated-NCs-Attribut
description: DS-Replikationsstatusinformationen, analog zu (und einer Obermenge) der vorhandenen Attribute hasMasterNCs und hasPartialReplicaNCs. Wird vom KCC beim Einrichten von Replikationspartnern verwendet.
ms.assetid: 00dda441-e382-4fb2-b735-ae547901c11f
ms.tgt_platform: multiple
keywords:
- AD-Schema des ms-DS-Has-Instantiated-NCs-Attributs
- AD-Schema des msDS-HasInstantiatedNCs-Attributs
topic_type:
- apiref
api_name:
- ms-DS-Has-Instantiated-NCs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efde9ef1cd9a7230e4493d3e542e1f5f661ed33027ad3e9a88ded9679df812c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804051"
---
# <a name="ms-ds-has-instantiated-ncs-attribute"></a>ms-DS-Has-Instantiated-NCs-Attribut

DS-Replikationsstatusinformationen, analog zu (und einer Obermenge) der vorhandenen Attribute hasMasterNCs und hasPartialReplicaNCs. Wird vom KCC beim Einrichten von Replikationspartnern verwendet.



| Eingabe | Wert |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CN                | ms-DS-Has-Instantiated-NCs                                                                                                                                                                                  |
| Ldap-Anzeigename | msDS-HasInstantiatedNCs                                                                                                                                                                                     |
| Size              | 4 Bytes                                                                                                                                                                                                     |
| Aktualisieren von Berechtigungen  | Dieser Wert wird vom System festgelegt.                                                                                                                                                                            |
| Updatehäufigkeit  | Ungefähr doppelt so oft wie hasMasterNCs/hasPartialReplicaNCs. Diese vorhandenen Attribute werden nur aktualisiert, wenn der Domänencontroller eine Partition hinzufügt oder entfernt (z. B. beim Wechsel von DC in GC oder umgekehrt). |
| Attribute-Id      | 1.2.840.113556.1.4.1709                                                                                                                                                                                     |
| System-Id-Guid    | 11e9a5bc-4517-4049-af9c-51554fb0fc09                                                                                                                                                                        |
| Syntax            | [**Object(DN-Binary)**](s-object-dn-binary.md)                                                                                                                                                             |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|------------------------------------------|
| Link-ID                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | True                                     |
| Is-Single-Valued       | False                                    |
| Ist indiziert             | False                                    |
| Im globalen Katalog      | False                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                             |
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
| System-Only            | True                                     |
| Is-Single-Valued       | False                                    |
| Ist indiziert             | False                                    |
| Im globalen Katalog      | False                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                             |
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
| System-Only            | True                                     |
| Is-Single-Valued       | False                                    |
| Ist indiziert             | False                                    |
| Im globalen Katalog      | False                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                             |
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
| System-Only            | True                                     |
| Ist einwertig       | False                                    |
| Ist indiziert             | False                                    |
| Im globalen Katalog      | False                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                             |
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
| System-Only            | True                                     |
| Ist einwertig       | False                                    |
| Ist indiziert             | False                                    |
| Im globalen Katalog      | False                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                             |
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
| System-Only            | True                                     |
| Ist einwertig       | False                                    |
| Ist indiziert             | False                                    |
| Im globalen Katalog      | False                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| In verwendete Klassen        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



 

 





