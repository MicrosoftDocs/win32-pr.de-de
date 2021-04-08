---
title: System-Only-Attribut
description: Ein boolescher Wert, der angibt, ob nur Active Directory die Klasse ändern können. Reine System Klassen können nur vom Verzeichnis System-Agent erstellt oder gelöscht werden.
ms.assetid: 78d2da1f-bdf1-452b-bc64-78088f3630dd
ms.tgt_platform: multiple
keywords:
- AD-Schema für System-Only-Attribut
- System only-Attribut AD-Schema
topic_type:
- apiref
api_name:
- System-Only
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1310eb5f13da3c17c20ac9c01f337ff2a018a545
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859565"
---
# <a name="system-only-attribute"></a>System-Only-Attribut

Ein boolescher Wert, der angibt, ob nur Active Directory die Klasse ändern können. Reine System Klassen können nur vom Verzeichnis System-Agent erstellt oder gelöscht werden.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | System-Only                          |
| LDAP-Display-Name | systemOnly                           |
| Size              | 4 Bytes                              |
| Berechtigung aktualisieren  | \-                                   |
| Aktualisierungshäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.170               |
| System-ID-GUID    | bf967a46-0de6-11d0-a285-00aa003049e2 |
| Syntax            | [**Booleschen**](s-boolean.md)         |



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
|------------------------|-----------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Richtig                                                                                                      |
| Ist-einwertig       | Richtig                                                                                                      |
| Ist indiziert             | False                                                                                                     |
| Im globalen Katalog      | False                                                                                                     |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                              |
| Range-Lower            | \-                                                                                                        |
| Range-Upper            | \-                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| In verwendete Klassen        | [**Attribut-Schema**](c-attributeschema.md)<br/> [**Class-Schema**](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Richtig                                                                                                      |
| Ist-einwertig       | Richtig                                                                                                      |
| Ist indiziert             | False                                                                                                     |
| Im globalen Katalog      | False                                                                                                     |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                              |
| Range-Lower            | \-                                                                                                        |
| Range-Upper            | \-                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| In verwendete Klassen        | [**Attribut-Schema**](c-attributeschema.md)<br/> [**Class-Schema**](c-classschema.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Richtig                                                                                                      |
| Ist-einwertig       | Richtig                                                                                                      |
| Ist indiziert             | False                                                                                                     |
| Im globalen Katalog      | False                                                                                                     |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                              |
| Range-Lower            | \-                                                                                                        |
| Range-Upper            | \-                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| In verwendete Klassen        | [**Attribut-Schema**](c-attributeschema.md)<br/> [**Class-Schema**](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Richtig                                                                                                      |
| Ist-einwertig       | Richtig                                                                                                      |
| Ist indiziert             | False                                                                                                     |
| Im globalen Katalog      | False                                                                                                     |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                              |
| Range-Lower            | \-                                                                                                        |
| Range-Upper            | \-                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| In verwendete Klassen        | [**Attribut-Schema**](c-attributeschema.md)<br/> [**Class-Schema**](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Richtig                                                                                                      |
| Ist-einwertig       | Richtig                                                                                                      |
| Ist indiziert             | False                                                                                                     |
| Im globalen Katalog      | False                                                                                                     |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                              |
| Range-Lower            | \-                                                                                                        |
| Range-Upper            | \-                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| In verwendete Klassen        | [**Attribut-Schema**](c-attributeschema.md)<br/> [**Class-Schema**](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Richtig                                                                                                      |
| Ist-einwertig       | Richtig                                                                                                      |
| Ist indiziert             | False                                                                                                     |
| Im globalen Katalog      | False                                                                                                     |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                              |
| Range-Lower            | \-                                                                                                        |
| Range-Upper            | \-                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| In verwendete Klassen        | [**Attribut-Schema**](c-attributeschema.md)<br/> [**Class-Schema**](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Richtig                                                                                                      |
| Ist-einwertig       | Richtig                                                                                                      |
| Ist indiziert             | False                                                                                                     |
| Im globalen Katalog      | False                                                                                                     |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                              |
| Range-Lower            | \-                                                                                                        |
| Range-Upper            | \-                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| In verwendete Klassen        | [**Attribut-Schema**](c-attributeschema.md)<br/> [**Class-Schema**](c-classschema.md)<br/> |



 

 





