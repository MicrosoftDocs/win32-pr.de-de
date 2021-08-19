---
title: ACS-Permission-Bits-Attribut
description: Ermöglicht die Multicastfluss-Origination für einen bestimmten Benutzer.
ms.assetid: c7e7866d-b906-4a64-bd51-4e9cc7b8fb86
ms.tgt_platform: multiple
keywords:
- AD-Schema des ACS-Permission-Bits-Attributs
- AD-Schema des aCSPermissionBits-Attributs
topic_type:
- apiref
api_name:
- ACS-Permission-Bits
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 332d27bb6a3be07f79a5a1c0bbefc4b5e8a6f94b88cba512f0c928995dc752a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929760"
---
# <a name="acs-permission-bits-attribute"></a>ACS-Permission-Bits-Attribut

Ermöglicht die Multicastfluss-Origination für einen bestimmten Benutzer.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | ACS-Permission-Bits                  |
| Ldap-Anzeigename | aCSPermissionBits                    |
| Size              | 8 Bytes                              |
| Aktualisieren von Berechtigungen  | \-                                   |
| Updatehäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.765               |
| System-Id-Guid    | 7f561282-5301-11d1-a9c5-0000f80367c1 |
| Syntax            | [**Intervall**](s-interval.md)       |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falsch                                        |
| Is-Single-Valued       | Richtig                                         |
| Ist indiziert             | Falsch                                        |
| Im globalen Katalog      | Falsch                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**ACS-Policy**](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falsch                                        |
| Is-Single-Valued       | Richtig                                         |
| Ist indiziert             | Falsch                                        |
| Im globalen Katalog      | Falsch                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**ACS-Policy**](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falsch                                        |
| Is-Single-Valued       | Richtig                                         |
| Ist indiziert             | Falsch                                        |
| Im globalen Katalog      | Falsch                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**ACS-Policy**](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falsch                                        |
| Ist einwertig       | Richtig                                         |
| Ist indiziert             | Falsch                                        |
| Im globalen Katalog      | Falsch                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**ACS-Policy**](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falsch                                        |
| Ist einwertig       | Richtig                                         |
| Ist indiziert             | Falsch                                        |
| Im globalen Katalog      | Falsch                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**ACS-Policy**](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falsch                                        |
| Ist einwertig       | Richtig                                         |
| Ist indiziert             | Falsch                                        |
| Im globalen Katalog      | Falsch                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**ACS-Policy**](c-acspolicy.md)<br/> |



 

 





