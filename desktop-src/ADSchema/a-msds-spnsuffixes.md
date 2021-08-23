---
title: ms-DS-SPN-Suffixes-Attribut
description: Dieses Attribut beschreibt die Suffixe von DNS-Hostnamen, die von Servern in der Gesamtstruktur verwendet werden. Diese DNS-Suffixe werden für andere Gesamtstrukturen freigegeben, die über gesamtstrukturübergreifende Vertrauensstellungen mit dieser Gesamtstruktur verfügen.
ms.assetid: 56153832-1228-419f-99d4-eb1ce3edc867
ms.tgt_platform: multiple
keywords:
- MS-DS-SPN-Suffixes-Attribut AD-Schema
- MSDS-SPNSuffixes-Attribut AD-Schema
topic_type:
- apiref
api_name:
- ms-DS-SPN-Suffixes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17c51a0805fefe9dbb8ddbeca3da89e3f5b3e66714b562af57cebc7975875cda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544420"
---
# <a name="ms-ds-spn-suffixes-attribute"></a>ms-DS-SPN-Suffixes-Attribut

Dieses Attribut beschreibt die Suffixe von DNS-Hostnamen, die von Servern in der Gesamtstruktur verwendet werden. Diese DNS-Suffixe werden für andere Gesamtstrukturen freigegeben, die über gesamtstrukturübergreifende Vertrauensstellungen mit dieser Gesamtstruktur verfügen.



| Eingabe | Wert |
|-------------------|----------------------------------------------|
| CN                | ms-DS-SPN-Suffixe                           |
| Ldap-Anzeigename | msDS-SPNSuffixes                             |
| Size              | 255 Bytes                                    |
| Aktualisieren von Berechtigungen  | Domänenadministrator                         |
| Updatehäufigkeit  | Wenn Server in der Gesamtstruktur ein neues Suffix erhalten. |
| Attribute-Id      | 1.2.840.113556.1.4.1715                      |
| System-ID-GUID    | 789ee1eb-8c8e-4e4c-8cec-79b31b7617b5         |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)  |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------|
| Link-ID                | \-                                                            |
| MAPI-Id                | \-                                                            |
| System-Only            | False                                                         |
| Ist einwertig       | False                                                         |
| Ist indiziert             | False                                                         |
| Im globalen Katalog      | False                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                  |
| Range-Lower            | \-                                                            |
| Range-Upper            | \-                                                            |
| Search-Flags           | 0x00000000                                                    |
| System-Flags           | 0x00000010                                                    |
| In verwendete Klassen        | [**Cross-Ref-Container**](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------|
| Link-ID                | \-                                                            |
| MAPI-Id                | \-                                                            |
| System-Only            | False                                                         |
| Ist einwertig       | False                                                         |
| Ist indiziert             | False                                                         |
| Im globalen Katalog      | False                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                  |
| Range-Lower            | \-                                                            |
| Range-Upper            | \-                                                            |
| Search-Flags           | 0x00000000                                                    |
| System-Flags           | 0x00000010                                                    |
| In verwendete Klassen        | [**Cross-Ref-Container**](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------|
| Link-ID                | \-                                                            |
| MAPI-Id                | \-                                                            |
| System-Only            | False                                                         |
| Ist einwertig       | False                                                         |
| Ist indiziert             | False                                                         |
| Im globalen Katalog      | False                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                  |
| Range-Lower            | \-                                                            |
| Range-Upper            | \-                                                            |
| Search-Flags           | 0x00000000                                                    |
| System-Flags           | 0x00000010                                                    |
| In verwendete Klassen        | [**Ref-übergreifender Container**](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------|
| Link-ID                | \-                                                            |
| MAPI-Id                | \-                                                            |
| System-Only            | False                                                         |
| Is-Single-Valued       | False                                                         |
| Ist indiziert             | False                                                         |
| Im globalen Katalog      | False                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                  |
| Range-Lower            | \-                                                            |
| Range-Upper            | \-                                                            |
| Search-Flags           | 0x00000000                                                    |
| System-Flags           | 0x00000010                                                    |
| In verwendete Klassen        | [**Ref-übergreifender Container**](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------|
| Link-ID                | \-                                                            |
| MAPI-Id                | \-                                                            |
| System-Only            | False                                                         |
| Is-Single-Valued       | False                                                         |
| Ist indiziert             | False                                                         |
| Im globalen Katalog      | False                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                  |
| Range-Lower            | \-                                                            |
| Range-Upper            | \-                                                            |
| Search-Flags           | 0x00000000                                                    |
| System-Flags           | 0x00000010                                                    |
| In verwendete Klassen        | [**Ref-übergreifender Container**](c-crossrefcontainer.md)<br/> |



 

 





