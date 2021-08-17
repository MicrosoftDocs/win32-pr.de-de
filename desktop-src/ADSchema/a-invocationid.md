---
title: Invocation-Id-Attribut
description: Wird verwendet, um jedes Microsoft Exchange Server Verzeichnis in der Organisation eindeutig zu identifizieren.
ms.assetid: c069a57c-b9d0-49e9-8096-39b43f378573
ms.tgt_platform: multiple
keywords:
- Invocation-Id AD-Attributschema
- INVOCATIONID-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Invocation-Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 345b6f23ff4a6f4d2640c2d388f5505126400bab364bf5a3cf199047e06e4e16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119322900"
---
# <a name="invocation-id-attribute"></a>Invocation-Id-Attribut

Wird verwendet, um jedes Microsoft Exchange Server Verzeichnis in der Organisation eindeutig zu identifizieren.



| Eingabe | Wert |
|-------------------|-------------------------------------------------------|
| CN                | Invocation-Id                                         |
| Ldap-Anzeigename | invocationId                                          |
| Size              | \-                                                    |
| Aktualisieren von Berechtigungen  | \-                                                    |
| Updatehäufigkeit  | Wenn die Exchange Server installiert ist.                |
| Attribute-Id      | 1.2.840.113556.1.2.115                                |
| System-ID-GUID    | bf96798e-0de6-11d0-a285-00aa003049e2                  |
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
|------------------------|------------------------------------------|
| Link-ID                | \-                                       |
| MAPI-Id                | 0x80BF                                   |
| System-Only            | Richtig                                     |
| Ist einwertig       | Richtig                                     |
| Ist indiziert             | Falsch                                    |
| Im globalen Katalog      | Falsch                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| In verwendete Klassen        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|------------------------------------------|
| Link-ID                | \-                                       |
| MAPI-Id                | 0x80BF                                   |
| System-Only            | Richtig                                     |
| Ist einwertig       | Richtig                                     |
| Ist indiziert             | Richtig                                     |
| Im globalen Katalog      | Falsch                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000001                               |
| System-Flags           | 0x00000010                               |
| In verwendete Klassen        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|------------------------------------------|
| Link-ID                | \-                                       |
| MAPI-Id                | 0x80BF                                   |
| System-Only            | Richtig                                     |
| Ist einwertig       | Richtig                                     |
| Ist indiziert             | Richtig                                     |
| Im globalen Katalog      | Falsch                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000001                               |
| System-Flags           | 0x00000010                               |
| In verwendete Klassen        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|------------------------------------------|
| Link-ID                | \-                                       |
| MAPI-Id                | 0x80BF                                   |
| System-Only            | Richtig                                     |
| Ist einwertig       | Richtig                                     |
| Ist indiziert             | Richtig                                     |
| Im globalen Katalog      | Falsch                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000001                               |
| System-Flags           | 0x00000010                               |
| In verwendete Klassen        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|------------------------------------------|
| Link-ID                | \-                                       |
| MAPI-Id                | 0x80BF                                   |
| System-Only            | Richtig                                     |
| Ist einwertig       | Richtig                                     |
| Ist indiziert             | Richtig                                     |
| Im globalen Katalog      | Falsch                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000001                               |
| System-Flags           | 0x00000010                               |
| In verwendete Klassen        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|------------------------------------------|
| Link-ID                | \-                                       |
| MAPI-Id                | 0x80BF                                   |
| System-Only            | Richtig                                     |
| Ist einwertig       | Richtig                                     |
| Ist indiziert             | Richtig                                     |
| Im globalen Katalog      | Falsch                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000001                               |
| System-Flags           | 0x00000010                               |
| In verwendete Klassen        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|------------------------------------------|
| Link-ID                | \-                                       |
| MAPI-Id                | 0x80BF                                   |
| System-Only            | Richtig                                     |
| Ist einwertig       | Richtig                                     |
| Ist indiziert             | Richtig                                     |
| Im globalen Katalog      | Falsch                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000001                               |
| System-Flags           | 0x00000010                               |
| In verwendete Klassen        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



 

 





