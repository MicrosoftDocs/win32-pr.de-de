---
title: System-Must-Contain-Attribut
description: Die Liste der obligatorischen Attribute für eine Klasse. Diese Attribute müssen angegeben werden, wenn eine Instanz der -Klasse erstellt wird. Die Liste der Attribute kann nur vom System geändert werden.
ms.assetid: 5131bd16-1a8d-4d4a-98e4-6140438c6517
ms.tgt_platform: multiple
keywords:
- AD-Schema des Attributs "System muss enthalten"
- systemMustContain-Attribut AD-Schema
topic_type:
- apiref
api_name:
- System-Must-Contain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15fd3db51b42fa825d13f420f36e116682a5b31ac6d0f5f48e590073f2f8948d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119645200"
---
# <a name="system-must-contain-attribute"></a>System-Must-Contain-Attribut

Die Liste der obligatorischen Attribute für eine Klasse. Diese Attribute müssen angegeben werden, wenn eine Instanz der -Klasse erstellt wird. Die Liste der Attribute kann nur vom System geändert werden.



| Eingabe | Wert |
|-------------------|-------------------------------------------------------------------------------|
| CN                | System muss enthalten                                                           |
| Ldap-Anzeigename | systemMustContain                                                             |
| Size              | \-                                                                            |
| Aktualisieren von Berechtigungen  | Schemaadministrator                                                          |
| Updatehäufigkeit  | Wenn die Klasse erstellt wird oder der Klasse ein neues obligatorisches Attribut hinzugefügt wird. |
| Attribute-Id      | 1.2.840.113556.1.4.197                                                        |
| System-ID-GUID    | bf967a45-0de6-11d0-a285-00aa003049e2                                          |
| Syntax            | [**String(Object-Identifier)**](s-string-object-identifier.md)               |



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
|------------------------|--------------------------------------------------|
| Link-ID                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | True                                             |
| Ist einwertig       | False                                            |
| Ist indiziert             | False                                            |
| Im globalen Katalog      | False                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| In verwendete Klassen        | [**Klassenschema**](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|--------------------------------------------------|
| Link-ID                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | True                                             |
| Ist einwertig       | False                                            |
| Ist indiziert             | False                                            |
| Im globalen Katalog      | False                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| In verwendete Klassen        | [**Klassenschema**](c-classschema.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|--------------------------------------------------|
| Link-ID                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | True                                             |
| Ist einwertig       | False                                            |
| Ist indiziert             | False                                            |
| Im globalen Katalog      | False                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| In verwendete Klassen        | [**Klassenschema**](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------------|
| Link-ID                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | True                                             |
| Is-Single-Valued       | False                                            |
| Ist indiziert             | False                                            |
| Im globalen Katalog      | False                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| In verwendete Klassen        | [**Klassenschema**](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|--------------------------------------------------|
| Link-ID                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | True                                             |
| Is-Single-Valued       | False                                            |
| Ist indiziert             | False                                            |
| Im globalen Katalog      | False                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| In verwendete Klassen        | [**Klassenschema**](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------------|
| Link-ID                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | True                                             |
| Is-Single-Valued       | False                                            |
| Ist indiziert             | False                                            |
| Im globalen Katalog      | False                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| In verwendete Klassen        | [**Klassenschema**](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|--------------------------------------------------|
| Link-ID                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | True                                             |
| Is-Single-Valued       | False                                            |
| Ist indiziert             | False                                            |
| Im globalen Katalog      | False                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| In verwendete Klassen        | [**Klassenschema**](c-classschema.md)<br/> |



 

 





