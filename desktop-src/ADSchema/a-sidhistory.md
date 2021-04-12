---
title: SID-History-Attribut
description: Enthält vorherige SIDs, die für das-Objekt verwendet werden, wenn das Objekt aus einer anderen Domäne verschoben wurde.
ms.assetid: d738002b-fc05-4c60-aaf9-b83be61ed5a9
ms.tgt_platform: multiple
keywords:
- AD-Schema für SID-History-Attribut
- SIDHistory-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- SID-History
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16474a6463fc99e7ed2c1d2b1a2cdbf6ea9b6614
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479922"
---
# <a name="sid-history-attribute"></a>SID-History-Attribut

Enthält vorherige SIDs, die für das-Objekt verwendet werden, wenn das Objekt aus einer anderen Domäne verschoben wurde. Wenn ein Objekt von einer Domäne in eine andere verschoben wird, wird eine neue SID erstellt, und diese neue SID wird zur objectSID. Die vorherige sid wird der SIDHistory-Eigenschaft hinzugefügt.



| Eingabe | Wert |
|-------------------|------------------------------------------------|
| CN                | SID-History                                    |
| LDAP-Display-Name | SIDHistory                                     |
| Size              | \-                                             |
| Berechtigung aktualisieren  | Dieser Wert wird vom System festgelegt.               |
| Aktualisierungshäufigkeit  | Jedes Mal, wenn das Objekt in eine neue Domäne verschoben wird. |
| Attribute-Id      | 1.2.840.113556.1.4.609                         |
| System-ID-GUID    | 17eb4278-D167-11D0-B002-0000,           |
| Syntax            | [**Zeichenfolge (SID)**](s-string-sid.md)            |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
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
| Ist-einwertig       | False                                                        |
| Ist indiziert             | Richtig                                                         |
| Im globalen Katalog      | Richtig                                                         |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| In verwendete Klassen        | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Ist-einwertig       | False                                                        |
| Ist indiziert             | Richtig                                                         |
| Im globalen Katalog      | Richtig                                                         |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| In verwendete Klassen        | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Ist-einwertig       | False                                                        |
| Ist indiziert             | Richtig                                                         |
| Im globalen Katalog      | Richtig                                                         |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| In verwendete Klassen        | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Ist-einwertig       | False                                                        |
| Ist indiziert             | Richtig                                                         |
| Im globalen Katalog      | Richtig                                                         |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| In verwendete Klassen        | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Ist-einwertig       | False                                                        |
| Ist indiziert             | Richtig                                                         |
| Im globalen Katalog      | Richtig                                                         |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| In verwendete Klassen        | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Ist-einwertig       | False                                                        |
| Ist indiziert             | Richtig                                                         |
| Im globalen Katalog      | Richtig                                                         |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| In verwendete Klassen        | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> |



 

 





