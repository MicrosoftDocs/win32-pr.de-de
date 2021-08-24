---
title: Object-Classes-Attribut
description: Eine mehrwertige Eigenschaft, die Zeichenfolgen enthält, die jede Klasse im Schema darstellen. Jeder Wert enthält governsID, lDAPDisplayName, mustContain, mayContain usw.
ms.assetid: 7e3eda48-8e64-4a52-8d92-7a0d37e513ef
ms.tgt_platform: multiple
keywords:
- Object-Classes AD-Attributschema
- objectClasses-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Object-Classes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c20c11ff547c24b37edab7f88a2854c9bc26ff133e7acba3a381971ededc3d90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119925190"
---
# <a name="object-classes-attribute"></a>Object-Classes-Attribut

Eine mehrwertige Eigenschaft, die Zeichenfolgen enthält, die jede Klasse im Schema darstellen. Jeder Wert enthält governsID, lDAPDisplayName, mustContain, mayContain usw.



| Eingabe | Wert |
|-------------------|--------------------------------------------------|
| CN                | Object-Classes                                   |
| Ldap-Anzeigename | objectClasses                                    |
| Size              | Durchschnittlich ca. 20 Bytes pro Klassenname.        |
| Aktualisieren von Berechtigungen  | Der Designer des -Objekts würde diesen Wert festlegen. |
| Updatehäufigkeit  | Immer dann, wenn sich der Entwurf der Klasse ändert.        |
| Attribute-Id      | 2.5.21.6                                         |
| System-ID-GUID    | 9a7ad94b-ca53-11d1-bbd0-0080c76670c0             |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)      |



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
|------------------------|---------------------------------------------|
| Link-ID                | \-                                          |
| MAPI-Id                | \-                                          |
| System-Only            | Richtig                                        |
| Ist einwertig       | Falsch                                       |
| Ist indiziert             | Falsch                                       |
| Im globalen Katalog      | Falsch                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                |
| Range-Lower            | \-                                          |
| Range-Upper            | \-                                          |
| Search-Flags           | 0x00000000                                  |
| System-Flags           | 0x08000014                                  |
| In verwendete Klassen        | [**SubSchema**](c-subschema.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|---------------------------------------------|
| Link-ID                | \-                                          |
| MAPI-Id                | \-                                          |
| System-Only            | Richtig                                        |
| Ist einwertig       | Falsch                                       |
| Ist indiziert             | Falsch                                       |
| Im globalen Katalog      | Falsch                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                |
| Range-Lower            | \-                                          |
| Range-Upper            | \-                                          |
| Search-Flags           | 0x00000000                                  |
| System-Flags           | 0x08000014                                  |
| In verwendete Klassen        | [**SubSchema**](c-subschema.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|---------------------------------------------|
| Link-ID                | \-                                          |
| MAPI-Id                | \-                                          |
| System-Only            | Richtig                                        |
| Ist einwertig       | Falsch                                       |
| Ist indiziert             | Falsch                                       |
| Im globalen Katalog      | Falsch                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                |
| Range-Lower            | \-                                          |
| Range-Upper            | \-                                          |
| Search-Flags           | 0x00000000                                  |
| System-Flags           | 0x08000014                                  |
| In verwendete Klassen        | [**SubSchema**](c-subschema.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|---------------------------------------------|
| Link-ID                | \-                                          |
| MAPI-Id                | \-                                          |
| System-Only            | Richtig                                        |
| Is-Single-Valued       | Falsch                                       |
| Ist indiziert             | Falsch                                       |
| Im globalen Katalog      | Falsch                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                |
| Range-Lower            | \-                                          |
| Range-Upper            | \-                                          |
| Search-Flags           | 0x00000000                                  |
| System-Flags           | 0x08000014                                  |
| In verwendete Klassen        | [**SubSchema**](c-subschema.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|---------------------------------------------|
| Link-ID                | \-                                          |
| MAPI-Id                | \-                                          |
| System-Only            | Richtig                                        |
| Is-Single-Valued       | Falsch                                       |
| Ist indiziert             | Falsch                                       |
| Im globalen Katalog      | Falsch                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                |
| Range-Lower            | \-                                          |
| Range-Upper            | \-                                          |
| Search-Flags           | 0x00000000                                  |
| System-Flags           | 0x08000014                                  |
| In verwendete Klassen        | [**SubSchema**](c-subschema.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|---------------------------------------------|
| Link-ID                | \-                                          |
| MAPI-Id                | \-                                          |
| System-Only            | Richtig                                        |
| Is-Single-Valued       | Falsch                                       |
| Ist indiziert             | Falsch                                       |
| Im globalen Katalog      | Falsch                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                |
| Range-Lower            | \-                                          |
| Range-Upper            | \-                                          |
| Search-Flags           | 0x00000000                                  |
| System-Flags           | 0x08000014                                  |
| In verwendete Klassen        | [**SubSchema**](c-subschema.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|---------------------------------------------|
| Link-ID                | \-                                          |
| MAPI-Id                | \-                                          |
| System-Only            | Richtig                                        |
| Is-Single-Valued       | Falsch                                       |
| Ist indiziert             | Falsch                                       |
| Im globalen Katalog      | Falsch                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                |
| Range-Lower            | \-                                          |
| Range-Upper            | \-                                          |
| Search-Flags           | 0x00000000                                  |
| System-Flags           | 0x08000014                                  |
| In verwendete Klassen        | [**SubSchema**](c-subschema.md)<br/> |



 

 





