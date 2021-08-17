---
title: Foreign-Identifier-Attribut
description: Die sicherheitseigenschaften, die von einem fremden System verwendet werden.
ms.assetid: f39deb69-2e3b-4494-88f0-050ad90242a5
ms.tgt_platform: multiple
keywords:
- Foreign-Identifier AD-Attributschema
- foreignIdentifier-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Foreign-Identifier
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6c2c73beda34f02594bc8de770efb672772221839fe567f07651c2c42170abc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119306910"
---
# <a name="foreign-identifier-attribute"></a>Foreign-Identifier-Attribut

Die sicherheitseigenschaften, die von einem fremden System verwendet werden.



| Eingabe | Wert |
|-------------------|-------------------------------------------------------|
| CN                | Foreign-Identifier                                    |
| Ldap-Anzeigename | foreignIdentifier                                     |
| Size              | \-                                                    |
| Aktualisieren von Berechtigungen  | \-                                                    |
| Updatehäufigkeit  | \-                                                    |
| Attribute-Id      | 1.2.840.113556.1.4.356                                |
| System-ID-GUID    | 3e97891e-8c01-11d0-afda-00c04fd930c9                  |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------|
| Link-ID                | \-                                                                          |
| MAPI-Id                | \-                                                                          |
| System-Only            | Falsch                                                                       |
| Ist einwertig       | Richtig                                                                        |
| Ist indiziert             | Falsch                                                                       |
| Im globalen Katalog      | Falsch                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                |
| Range-Lower            | \-                                                                          |
| Range-Upper            | \-                                                                          |
| Search-Flags           | 0x00000000                                                                  |
| System-Flags           | 0x00000010                                                                  |
| In verwendete Klassen        | [**Fremdsicherheitsprinzipal**](c-foreignsecurityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------|
| Link-ID                | \-                                                                          |
| MAPI-Id                | \-                                                                          |
| System-Only            | Falsch                                                                       |
| Ist einwertig       | Richtig                                                                        |
| Ist indiziert             | Falsch                                                                       |
| Im globalen Katalog      | Falsch                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                |
| Range-Lower            | \-                                                                          |
| Range-Upper            | \-                                                                          |
| Search-Flags           | 0x00000000                                                                  |
| System-Flags           | 0x00000010                                                                  |
| In verwendete Klassen        | [**Fremdsicherheitsprinzipal**](c-foreignsecurityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------|
| Link-ID                | \-                                                                          |
| MAPI-Id                | \-                                                                          |
| System-Only            | Falsch                                                                       |
| Ist einwertig       | Richtig                                                                        |
| Ist indiziert             | Falsch                                                                       |
| Im globalen Katalog      | Falsch                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                |
| Range-Lower            | \-                                                                          |
| Range-Upper            | \-                                                                          |
| Search-Flags           | 0x00000000                                                                  |
| System-Flags           | 0x00000010                                                                  |
| In verwendete Klassen        | [**Fremdsicherheitsprinzipal**](c-foreignsecurityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------|
| Link-ID                | \-                                                                          |
| MAPI-Id                | \-                                                                          |
| System-Only            | Falsch                                                                       |
| Is-Single-Valued       | Richtig                                                                        |
| Ist indiziert             | Falsch                                                                       |
| Im globalen Katalog      | Falsch                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                |
| Range-Lower            | \-                                                                          |
| Range-Upper            | \-                                                                          |
| Search-Flags           | 0x00000000                                                                  |
| System-Flags           | 0x00000010                                                                  |
| In verwendete Klassen        | [**Foreign-Security-Principal**](c-foreignsecurityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------|
| Link-ID                | \-                                                                          |
| MAPI-Id                | \-                                                                          |
| System-Only            | Falsch                                                                       |
| Is-Single-Valued       | Richtig                                                                        |
| Ist indiziert             | Falsch                                                                       |
| Im globalen Katalog      | Falsch                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                |
| Range-Lower            | \-                                                                          |
| Range-Upper            | \-                                                                          |
| Search-Flags           | 0x00000000                                                                  |
| System-Flags           | 0x00000010                                                                  |
| In verwendete Klassen        | [**Foreign-Security-Principal**](c-foreignsecurityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------|
| Link-ID                | \-                                                                          |
| MAPI-Id                | \-                                                                          |
| System-Only            | Falsch                                                                       |
| Is-Single-Valued       | Richtig                                                                        |
| Ist indiziert             | Falsch                                                                       |
| Im globalen Katalog      | Falsch                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                |
| Range-Lower            | \-                                                                          |
| Range-Upper            | \-                                                                          |
| Search-Flags           | 0x00000000                                                                  |
| System-Flags           | 0x00000010                                                                  |
| In verwendete Klassen        | [**Foreign-Security-Principal**](c-foreignsecurityprincipal.md)<br/> |



 

 





