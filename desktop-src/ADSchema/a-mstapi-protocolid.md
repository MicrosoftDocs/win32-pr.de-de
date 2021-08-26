---
title: ms-TAPI-Protocol-Id-Attribut
description: Dieses Attribut gibt den TAPI-Konferenztyp an.
ms.assetid: 6114efc3-4201-4f20-81ca-4f90a9e44f60
ms.tgt_platform: multiple
keywords:
- MS-TAPI-Protocol-Id-Attribut AD-Schema
- MSTAPI-ProtocolId-Attribut AD-Schema
topic_type:
- apiref
api_name:
- ms-TAPI-Protocol-Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6fb09579ae7c97c9a44140cf634b9fab42f257401fb00091ac74209b0a4908b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120066180"
---
# <a name="ms-tapi-protocol-id-attribute"></a>ms-TAPI-Protocol-Id-Attribut

Dieses Attribut gibt den TAPI-Konferenztyp an. Dieses Attribut wird verwendet, um zu bestimmen, wie das binäre BLOB im [**ms-TAPI-Conference-Blob-Attribut**](a-mstapi-conferenceblob.md) interpretiert werden soll. Dieses Attribut ist eine beliebige Zeichenfolge, die in der Regel weniger als 100 Zeichen lang ist.



| Eingabe | Wert |
|-------------------|------------------------------------------------------------|
| CN                | ms-TAPI-Protocol-Id                                        |
| Ldap-Anzeigename | msTAPI-ProtocolId                                          |
| Size              | \-                                                         |
| Aktualisieren von Berechtigungen  | Es sind keine besonderen Berechtigungen erforderlich.                            |
| Updatehäufigkeit  | Wird zum Zeitpunkt der Erstellung des Rt-Conference-Objekts einmal festgelegt. |
| Attribute-Id      | 1.2.840.113556.1.4.1699                                    |
| System-ID-GUID    | 89c1ebcf-7a5f-41fd-99ca-c900b32299ab                       |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------|
| Link-ID                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | Falsch                                                             |
| Ist einwertig       | Richtig                                                              |
| Ist indiziert             | Falsch                                                             |
| Im globalen Katalog      | Falsch                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| In verwendete Klassen        | [**ms-TAPI-Rt-Conference**](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------|
| Link-ID                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | Falsch                                                             |
| Ist einwertig       | Richtig                                                              |
| Ist indiziert             | Falsch                                                             |
| Im globalen Katalog      | Falsch                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| In verwendete Klassen        | [**ms-TAPI-Rt-Conference**](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------|
| Link-ID                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | Falsch                                                             |
| Ist einwertig       | Richtig                                                              |
| Ist indiziert             | Falsch                                                             |
| Im globalen Katalog      | Falsch                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| In verwendete Klassen        | [**ms-TAPI-Rt-Conference**](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------|
| Link-ID                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | Falsch                                                             |
| Ist einwertig       | Richtig                                                              |
| Ist indiziert             | Falsch                                                             |
| Im globalen Katalog      | Falsch                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| In verwendete Klassen        | [**ms-TAPI-Rt-Conference**](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------|
| Link-ID                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | Falsch                                                             |
| Ist einwertig       | Richtig                                                              |
| Ist indiziert             | Falsch                                                             |
| Im globalen Katalog      | Falsch                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| In verwendete Klassen        | [**ms-TAPI-Rt-Conference**](c-mstapi-rtconference.md)<br/> |



 

 





