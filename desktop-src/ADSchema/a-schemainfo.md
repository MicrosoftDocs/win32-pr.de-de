---
title: Schema-Info-Attribut
description: Ein interner binärer Wert, der verwendet wird, um Schemaänderungen zwischen DCs zu erkennen und einen Schema-NC-Replikationszyklus zu erzwingen, bevor ein anderer NC repliziert wird. Wird verwendet, um Bindungen aufzulösen, wenn das Schema FSMO aufgelöst wird und eine Änderung an mehreren Domänencontrollern vorgenommen wird.
ms.assetid: 416cef3f-211b-439d-b177-267806c6a5d2
ms.tgt_platform: multiple
keywords:
- Schema-Info AD-Attributschema
- schemaInfo-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Schema-Info
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfa0d55dd29f207b84b0951ee448ba988d128fabfd126f38b2a4692d7cd3e0fa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119646529"
---
# <a name="schema-info-attribute"></a>Schema-Info-Attribut

Ein interner binärer Wert, der verwendet wird, um Schemaänderungen zwischen DCs zu erkennen und einen Schema-NC-Replikationszyklus zu erzwingen, bevor ein anderer NC repliziert wird. Wird verwendet, um Bindungen aufzulösen, wenn das Schema FSMO aufgelöst wird und eine Änderung an mehreren Domänencontrollern vorgenommen wird.



| Eingabe | Wert |
|-------------------|-------------------------------------------------------|
| CN                | Schema-Info                                           |
| Ldap-Anzeigename | Schemainfo                                            |
| Size              | \-                                                    |
| Aktualisieren von Berechtigungen  | Dieser Wert wird vom System festgelegt.                      |
| Updatehäufigkeit  | \-                                                    |
| Attribute-Id      | 1.2.840.113556.1.4.1358                               |
| System-ID-GUID    | f9fb64ae-93b4-11d2-9945-0000f87a57d4                  |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md) |



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
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Ist einwertig       | False                           |
| Ist indiziert             | False                           |
| Im globalen Katalog      | False                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| In verwendete Klassen        | [**Dmd**](c-dmd.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Ist einwertig       | False                           |
| Ist indiziert             | False                           |
| Im globalen Katalog      | False                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| In verwendete Klassen        | [**Dmd**](c-dmd.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Ist einwertig       | False                           |
| Ist indiziert             | False                           |
| Im globalen Katalog      | False                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| In verwendete Klassen        | [**Dmd**](c-dmd.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Is-Single-Valued       | False                           |
| Ist indiziert             | False                           |
| Im globalen Katalog      | False                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| In verwendete Klassen        | [**Dmd**](c-dmd.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Is-Single-Valued       | False                           |
| Ist indiziert             | False                           |
| Im globalen Katalog      | False                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| In verwendete Klassen        | [**Dmd**](c-dmd.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Is-Single-Valued       | False                           |
| Ist indiziert             | False                           |
| Im globalen Katalog      | False                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| In verwendete Klassen        | [**Dmd**](c-dmd.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Is-Single-Valued       | False                           |
| Ist indiziert             | False                           |
| Im globalen Katalog      | False                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| In verwendete Klassen        | [**Dmd**](c-dmd.md)<br/> |



 

 





