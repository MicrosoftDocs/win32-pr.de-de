---
title: Attribut "Service-Class-ID"
description: Die GUID für die Service-Klasse.
ms.assetid: 41d131cc-ef62-4937-a883-31ad6f837a76
ms.tgt_platform: multiple
keywords:
- AD-Schema des Dienstklassen-ID-Attributs
- serviceClassID-Attribut-AD-Schema
topic_type:
- apiref
api_name:
- Service-Class-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7ac3479121449ff6fc0b1bdbbb72a554d5f82a823186faa980d5c13b23253c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119836650"
---
# <a name="service-class-id-attribute"></a>Attribut "Service-Class-ID"

Die GUID für die Service-Klasse.



| Eingabe | Wert |
|-------------------|-------------------------------------------------------|
| CN                | Dienstklassen-ID                                      |
| Ldap-Anzeigename | serviceClassID                                        |
| Size              | \-                                                    |
| Aktualisieren von Berechtigungen  | \-                                                    |
| Updatehäufigkeit  | \-                                                    |
| Attribute-Id      | 1.2.840.113556.1.4.122                                |
| System-ID-GUID    | bf967a35-0de6-11d0-a285-00aa003049e2                  |
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
|------------------------|-------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                          |
| MAPI-Id                | \-                                                                                                          |
| System-Only            | Falsch                                                                                                       |
| Ist einwertig       | Richtig                                                                                                        |
| Ist indiziert             | Falsch                                                                                                       |
| Im globalen Katalog      | Richtig                                                                                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                |
| Range-Lower            | \-                                                                                                          |
| Range-Upper            | \-                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                  |
| System-Flags           | 0x00000010                                                                                                  |
| In verwendete Klassen        | [**Dienstklasse**](c-serviceclass.md)<br/> [**Dienstinstanz**](c-serviceinstance.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                          |
| MAPI-Id                | \-                                                                                                          |
| System-Only            | Falsch                                                                                                       |
| Ist einwertig       | Richtig                                                                                                        |
| Ist indiziert             | Falsch                                                                                                       |
| Im globalen Katalog      | Richtig                                                                                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                |
| Range-Lower            | \-                                                                                                          |
| Range-Upper            | \-                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                  |
| System-Flags           | 0x00000010                                                                                                  |
| In verwendete Klassen        | [**Dienstklasse**](c-serviceclass.md)<br/> [**Dienstinstanz**](c-serviceinstance.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                          |
| MAPI-Id                | \-                                                                                                          |
| System-Only            | Falsch                                                                                                       |
| Ist einwertig       | Richtig                                                                                                        |
| Ist indiziert             | Falsch                                                                                                       |
| Im globalen Katalog      | Richtig                                                                                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                |
| Range-Lower            | \-                                                                                                          |
| Range-Upper            | \-                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                  |
| System-Flags           | 0x00000010                                                                                                  |
| In verwendete Klassen        | [**Dienstklasse**](c-serviceclass.md)<br/> [**Dienstinstanz**](c-serviceinstance.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                          |
| MAPI-Id                | \-                                                                                                          |
| System-Only            | Falsch                                                                                                       |
| Is-Single-Valued       | Richtig                                                                                                        |
| Ist indiziert             | Falsch                                                                                                       |
| Im globalen Katalog      | Richtig                                                                                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                |
| Range-Lower            | \-                                                                                                          |
| Range-Upper            | \-                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                  |
| System-Flags           | 0x00000010                                                                                                  |
| In verwendete Klassen        | [**Service-Class**](c-serviceclass.md)<br/> [**Dienstinstanz**](c-serviceinstance.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                          |
| MAPI-Id                | \-                                                                                                          |
| System-Only            | Falsch                                                                                                       |
| Is-Single-Valued       | Richtig                                                                                                        |
| Ist indiziert             | Falsch                                                                                                       |
| Im globalen Katalog      | Richtig                                                                                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                |
| Range-Lower            | \-                                                                                                          |
| Range-Upper            | \-                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                  |
| System-Flags           | 0x00000010                                                                                                  |
| In verwendete Klassen        | [**Service-Class**](c-serviceclass.md)<br/> [**Dienstinstanz**](c-serviceinstance.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                          |
| MAPI-Id                | \-                                                                                                          |
| System-Only            | Falsch                                                                                                       |
| Is-Single-Valued       | Richtig                                                                                                        |
| Ist indiziert             | Falsch                                                                                                       |
| Im globalen Katalog      | Richtig                                                                                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                |
| Range-Lower            | \-                                                                                                          |
| Range-Upper            | \-                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                  |
| System-Flags           | 0x00000010                                                                                                  |
| In verwendete Klassen        | [**Service-Class**](c-serviceclass.md)<br/> [**Dienstinstanz**](c-serviceinstance.md)<br/> |



 

 





