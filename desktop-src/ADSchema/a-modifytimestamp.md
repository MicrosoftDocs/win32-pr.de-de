---
title: Modify-Time-Stamp-Attribut
description: Ein berechnetes Attribut, das das Datum der letzten Änderung dieses Objekts darstellt. Dieser Wert wird nicht repliziert.
ms.assetid: ad8fea90-9a78-484d-9549-26d78e87ec44
ms.tgt_platform: multiple
keywords:
- AD-Schema des Modify-Time-Stamp-Attributs
- AD-Schema des modifyTimeStamp-Attributs
topic_type:
- apiref
api_name:
- Modify-Time-Stamp
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc32a0142d47f842429c3bf67d766ec708b7fc42b9f3285ee360ce3789c1a84f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119300370"
---
# <a name="modify-time-stamp-attribute"></a>Modify-Time-Stamp-Attribut

Ein berechnetes Attribut, das das Datum der letzten Änderung dieses Objekts darstellt. Dieser Wert wird nicht repliziert.



| Eingabe | Wert |
|-------------------|---------------------------------------------------------------|
| CN                | Modify-Time-Stamp                                             |
| Ldap-Anzeigename | modifyTimeStamp                                               |
| Size              | 8 Bytes                                                       |
| Aktualisieren von Berechtigungen  | Dieser Wert wird vom System festgelegt.                              |
| Updatehäufigkeit  | \-                                                            |
| Attribute-Id      | 2.5.18.2                                                      |
| System-Id-Guid    | 9a7ad94a-ca53-11d1-bbd0-0080c76670c0                          |
| Syntax            | [**String(Generalized-Time)**](s-string-generalized-time.md) |



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
|------------------------|-----------------------------------------------------------------------------|
| Link-ID                | \-                                                                          |
| MAPI-Id                | \-                                                                          |
| System-Only            | True                                                                        |
| Is-Single-Valued       | True                                                                        |
| Ist indiziert             | False                                                                       |
| Im globalen Katalog      | False                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                |
| Range-Lower            | \-                                                                          |
| Range-Upper            | \-                                                                          |
| Search-Flags           | 0x00000000                                                                  |
| System-Flags           | 0x08000014                                                                  |
| In verwendete Klassen        | [**SubSchema**](c-subschema.md)<br/> [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------|
| Link-ID                | \-                                                                          |
| MAPI-Id                | \-                                                                          |
| System-Only            | True                                                                        |
| Is-Single-Valued       | True                                                                        |
| Ist indiziert             | False                                                                       |
| Im globalen Katalog      | False                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                |
| Range-Lower            | \-                                                                          |
| Range-Upper            | \-                                                                          |
| Search-Flags           | 0x00000000                                                                  |
| System-Flags           | 0x08000014                                                                  |
| In verwendete Klassen        | [**SubSchema**](c-subschema.md)<br/> [**Nach oben**](c-top.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------|
| Link-ID                | \-                                                                          |
| MAPI-Id                | \-                                                                          |
| System-Only            | True                                                                        |
| Is-Single-Valued       | True                                                                        |
| Ist indiziert             | False                                                                       |
| Im globalen Katalog      | False                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                |
| Range-Lower            | \-                                                                          |
| Range-Upper            | \-                                                                          |
| Search-Flags           | 0x00000000                                                                  |
| System-Flags           | 0x08000014                                                                  |
| In verwendete Klassen        | [**SubSchema**](c-subschema.md)<br/> [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------|
| Link-ID                | \-                                                                          |
| MAPI-Id                | \-                                                                          |
| System-Only            | True                                                                        |
| Ist einwertig       | True                                                                        |
| Ist indiziert             | False                                                                       |
| Im globalen Katalog      | False                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                |
| Range-Lower            | \-                                                                          |
| Range-Upper            | \-                                                                          |
| Search-Flags           | 0x00000000                                                                  |
| System-Flags           | 0x08000014                                                                  |
| In verwendete Klassen        | [**SubSchema**](c-subschema.md)<br/> [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------|
| Link-ID                | \-                                                                          |
| MAPI-Id                | \-                                                                          |
| System-Only            | True                                                                        |
| Ist einwertig       | True                                                                        |
| Ist indiziert             | False                                                                       |
| Im globalen Katalog      | False                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                |
| Range-Lower            | \-                                                                          |
| Range-Upper            | \-                                                                          |
| Search-Flags           | 0x00000000                                                                  |
| System-Flags           | 0x08000014                                                                  |
| In verwendete Klassen        | [**SubSchema**](c-subschema.md)<br/> [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------|
| Link-ID                | \-                                                                          |
| MAPI-Id                | \-                                                                          |
| System-Only            | True                                                                        |
| Ist einwertig       | True                                                                        |
| Ist indiziert             | False                                                                       |
| Im globalen Katalog      | False                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                |
| Range-Lower            | \-                                                                          |
| Range-Upper            | \-                                                                          |
| Search-Flags           | 0x00000000                                                                  |
| System-Flags           | 0x08000014                                                                  |
| In verwendete Klassen        | [**SubSchema**](c-subschema.md)<br/> [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------|
| Link-ID                | \-                                                                          |
| MAPI-Id                | \-                                                                          |
| System-Only            | True                                                                        |
| Ist einwertig       | True                                                                        |
| Ist indiziert             | False                                                                       |
| Im globalen Katalog      | False                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                |
| Range-Lower            | \-                                                                          |
| Range-Upper            | \-                                                                          |
| Search-Flags           | 0x00000000                                                                  |
| System-Flags           | 0x08000014                                                                  |
| In verwendete Klassen        | [**SubSchema**](c-subschema.md)<br/> [**Nach oben**](c-top.md)<br/> |



 

 





