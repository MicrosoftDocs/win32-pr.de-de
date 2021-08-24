---
title: Schema-ID-GUID-Attribut
description: Der eindeutige Bezeichner für ein Attribut.
ms.assetid: 50f0a4b6-dded-42db-9ac5-123f2885c658
ms.tgt_platform: multiple
keywords:
- AD-Schema des Schema-ID-GUID-Attributs
- SCHEMAIDGUID-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Schema-ID-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afbf6f45b2c4518c0140eaf3188447740849ad79933d4e4eb71fe57f769f0455
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119837043"
---
# <a name="schema-id-guid-attribute"></a>Schema-ID-GUID-Attribut

Der eindeutige Bezeichner für ein Attribut.



| Eingabe | Wert |
|-------------------|---------------------------------------------------------------------|
| CN                | Schema-ID-GUID                                                      |
| Ldap-Anzeigename | schemaIDGUID                                                        |
| Size              | 16 Bytes                                                            |
| Aktualisieren von Berechtigungen  | Dieser Wert wird vom System festgelegt.                                    |
| Updatehäufigkeit  | Dieser Wert wird beim Erstellen des Objekts festgelegt und kann nicht geändert werden. |
| Attribute-Id      | 1.2.840.113556.1.4.148                                              |
| System-Id-Guid    | bf967923-0de6-11d0-a285-00aa003049e2                                |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md)               |



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
| Is-Single-Valued       | Richtig                                                                                                      |
| Ist indiziert             | Falsch                                                                                                     |
| Im globalen Katalog      | Falsch                                                                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                              |
| Range-Lower            | 16                                                                                                        |
| Range-Upper            | 16                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| In verwendete Klassen        | [**Attributschema**](c-attributeschema.md)<br/> [**Klassenschema**](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Richtig                                                                                                      |
| Is-Single-Valued       | Richtig                                                                                                      |
| Ist indiziert             | Falsch                                                                                                     |
| Im globalen Katalog      | Falsch                                                                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                              |
| Range-Lower            | 16                                                                                                        |
| Range-Upper            | 16                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| In verwendete Klassen        | [**Attributschema**](c-attributeschema.md)<br/> [**Klassenschema**](c-classschema.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Richtig                                                                                                      |
| Is-Single-Valued       | Richtig                                                                                                      |
| Ist indiziert             | Falsch                                                                                                     |
| Im globalen Katalog      | Falsch                                                                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                              |
| Range-Lower            | 16                                                                                                        |
| Range-Upper            | 16                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| In verwendete Klassen        | [**Attributschema**](c-attributeschema.md)<br/> [**Klassenschema**](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Richtig                                                                                                      |
| Ist einwertig       | Richtig                                                                                                      |
| Ist indiziert             | Falsch                                                                                                     |
| Im globalen Katalog      | Falsch                                                                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                              |
| Range-Lower            | 16                                                                                                        |
| Range-Upper            | 16                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| In verwendete Klassen        | [**Attributschema**](c-attributeschema.md)<br/> [**Klassenschema**](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Richtig                                                                                                      |
| Ist einwertig       | Richtig                                                                                                      |
| Ist indiziert             | Falsch                                                                                                     |
| Im globalen Katalog      | Falsch                                                                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                              |
| Range-Lower            | 16                                                                                                        |
| Range-Upper            | 16                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| In verwendete Klassen        | [**Attributschema**](c-attributeschema.md)<br/> [**Klassenschema**](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Richtig                                                                                                      |
| Ist einwertig       | Richtig                                                                                                      |
| Ist indiziert             | Falsch                                                                                                     |
| Im globalen Katalog      | Falsch                                                                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                              |
| Range-Lower            | 16                                                                                                        |
| Range-Upper            | 16                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| In verwendete Klassen        | [**Attributschema**](c-attributeschema.md)<br/> [**Klassenschema**](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Richtig                                                                                                      |
| Ist einwertig       | Richtig                                                                                                      |
| Ist indiziert             | Falsch                                                                                                     |
| Im globalen Katalog      | Falsch                                                                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                              |
| Range-Lower            | 16                                                                                                        |
| Range-Upper            | 16                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| In verwendete Klassen        | [**Attributschema**](c-attributeschema.md)<br/> [**Klassenschema**](c-classschema.md)<br/> |



 

 





