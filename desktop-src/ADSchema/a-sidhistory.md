---
title: SID-History-Attribut
description: Enthält vorherige SIDs, die für das Objekt verwendet wurden, wenn das Objekt aus einer anderen Domäne verschoben wurde.
ms.assetid: d738002b-fc05-4c60-aaf9-b83be61ed5a9
ms.tgt_platform: multiple
keywords:
- SID-History AD-Attributschema
- sIDHistory-Attribut AD-Schema
topic_type:
- apiref
api_name:
- SID-History
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5c2dbfb3572392bdbed3f13683adc1cbf64b70e061962975a178f8380f55f5a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119836290"
---
# <a name="sid-history-attribute"></a>SID-History-Attribut

Enthält vorherige SIDs, die für das Objekt verwendet wurden, wenn das Objekt aus einer anderen Domäne verschoben wurde. Wenn ein Objekt von einer Domäne in eine andere verschoben wird, wird eine neue SID erstellt, und diese neue SID wird zur objectSID. Die vorherige SID wird der sIDHistory-Eigenschaft hinzugefügt.



| Eingabe | Wert |
|-------------------|------------------------------------------------|
| CN                | SID-History                                    |
| Ldap-Anzeigename | Sidhistory                                     |
| Size              | \-                                             |
| Aktualisieren von Berechtigungen  | Dieser Wert wird vom System festgelegt.               |
| Updatehäufigkeit  | Jedes Mal, wenn das Objekt in eine neue Domäne verschoben wird. |
| Attribute-Id      | 1.2.840.113556.1.4.609                         |
| System-ID-GUID    | 17eb4278-d167-11d0-b002-0000f80367c1           |
| Syntax            | [**String(Sid)**](s-string-sid.md)            |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Richtig                                                         |
| Ist einwertig       | Falsch                                                        |
| Ist indiziert             | Richtig                                                         |
| Im globalen Katalog      | Richtig                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| In verwendete Klassen        | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falsch                                                        |
| Ist einwertig       | Falsch                                                        |
| Ist indiziert             | Richtig                                                         |
| Im globalen Katalog      | Richtig                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| In verwendete Klassen        | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falsch                                                        |
| Ist einwertig       | Falsch                                                        |
| Ist indiziert             | Richtig                                                         |
| Im globalen Katalog      | Richtig                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| In verwendete Klassen        | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falsch                                                        |
| Is-Single-Valued       | Falsch                                                        |
| Ist indiziert             | Richtig                                                         |
| Im globalen Katalog      | Richtig                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| In verwendete Klassen        | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falsch                                                        |
| Is-Single-Valued       | Falsch                                                        |
| Ist indiziert             | Richtig                                                         |
| Im globalen Katalog      | Richtig                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| In verwendete Klassen        | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falsch                                                        |
| Is-Single-Valued       | Falsch                                                        |
| Ist indiziert             | Richtig                                                         |
| Im globalen Katalog      | Richtig                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| In verwendete Klassen        | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> |



 

 





