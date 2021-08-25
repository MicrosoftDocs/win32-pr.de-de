---
title: System-Only-Attribut
description: Ein boolescher Wert, der angibt, ob nur Active Directory die Klasse ändern kann. Nur-Systemklassen können nur vom Verzeichnissystem-Agent erstellt oder gelöscht werden.
ms.assetid: 78d2da1f-bdf1-452b-bc64-78088f3630dd
ms.tgt_platform: multiple
keywords:
- System-Only AD-Attributschema
- systemOnly-Attribut AD-Schema
topic_type:
- apiref
api_name:
- System-Only
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e03c28707c2cc2d9070ff639dd9c9e9d934a0a5569e32ae40b067e639e6a21e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119835861"
---
# <a name="system-only-attribute"></a>System-Only-Attribut

Ein boolescher Wert, der angibt, ob nur Active Directory die Klasse ändern kann. Nur-Systemklassen können nur vom Verzeichnissystem-Agent erstellt oder gelöscht werden.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | System-Only                          |
| Ldap-Anzeigename | systemOnly                           |
| Size              | 4 Bytes                              |
| Aktualisieren von Berechtigungen  | \-                                   |
| Updatehäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.170               |
| System-ID-GUID    | bf967a46-0de6-11d0-a285-00aa003049e2 |
| Syntax            | [**Boolean**](s-boolean.md)         |



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
|------------------------|-----------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Richtig                                                                                                      |
| Ist einwertig       | Richtig                                                                                                      |
| Ist indiziert             | Falsch                                                                                                     |
| Im globalen Katalog      | Falsch                                                                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                              |
| Range-Lower            | \-                                                                                                        |
| Range-Upper            | \-                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| In verwendete Klassen        | [**Attributschema**](c-attributeschema.md)<br/> [**Klassenschema**](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Richtig                                                                                                      |
| Ist einwertig       | Richtig                                                                                                      |
| Ist indiziert             | Falsch                                                                                                     |
| Im globalen Katalog      | Falsch                                                                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                              |
| Range-Lower            | \-                                                                                                        |
| Range-Upper            | \-                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| In verwendete Klassen        | [**Attributschema**](c-attributeschema.md)<br/> [**Klassenschema**](c-classschema.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Richtig                                                                                                      |
| Ist einwertig       | Richtig                                                                                                      |
| Ist indiziert             | Falsch                                                                                                     |
| Im globalen Katalog      | Falsch                                                                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                              |
| Range-Lower            | \-                                                                                                        |
| Range-Upper            | \-                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| In verwendete Klassen        | [**Attributschema**](c-attributeschema.md)<br/> [**Klassenschema**](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Richtig                                                                                                      |
| Is-Single-Valued       | Richtig                                                                                                      |
| Ist indiziert             | Falsch                                                                                                     |
| Im globalen Katalog      | Falsch                                                                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                              |
| Range-Lower            | \-                                                                                                        |
| Range-Upper            | \-                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| In verwendete Klassen        | [**Attributschema**](c-attributeschema.md)<br/> [**Klassenschema**](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Richtig                                                                                                      |
| Is-Single-Valued       | Richtig                                                                                                      |
| Ist indiziert             | Falsch                                                                                                     |
| Im globalen Katalog      | Falsch                                                                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                              |
| Range-Lower            | \-                                                                                                        |
| Range-Upper            | \-                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| In verwendete Klassen        | [**Attributschema**](c-attributeschema.md)<br/> [**Klassenschema**](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Richtig                                                                                                      |
| Is-Single-Valued       | Richtig                                                                                                      |
| Ist indiziert             | Falsch                                                                                                     |
| Im globalen Katalog      | Falsch                                                                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                              |
| Range-Lower            | \-                                                                                                        |
| Range-Upper            | \-                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| In verwendete Klassen        | [**Attributschema**](c-attributeschema.md)<br/> [**Klassenschema**](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Richtig                                                                                                      |
| Is-Single-Valued       | Richtig                                                                                                      |
| Ist indiziert             | Falsch                                                                                                     |
| Im globalen Katalog      | Falsch                                                                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                              |
| Range-Lower            | \-                                                                                                        |
| Range-Upper            | \-                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| In verwendete Klassen        | [**Attributschema**](c-attributeschema.md)<br/> [**Klassenschema**](c-classschema.md)<br/> |



 

 





