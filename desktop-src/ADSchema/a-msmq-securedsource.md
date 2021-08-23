---
title: MSMQ-Secured-Source-Attribut
description: Dies ist Teil eines MSMQ-Objekts und wird durch Aufrufen der API auf MQCreateQueue oder MQSetProperties festgelegt. Sie steuert, ob MSMQ nur Nachrichten von einer gesicherten Quelle (z. B. HTTPS) für diese Warteschlange akzeptiert.
ms.assetid: 780d164f-c7fa-4c65-b46e-3a67ead92163
ms.tgt_platform: multiple
keywords:
- AD-Schema des MSMQ-Secured-Source-Attributs
- MSMQ-SecuredSource AD-Attributschema
topic_type:
- apiref
api_name:
- MSMQ-Secured-Source
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23785fd626debe61981185561b3b1ea243d93ff870fc2e025777488e1d898c16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119762750"
---
# <a name="msmq-secured-source-attribute"></a>MSMQ-Secured-Source-Attribut

Dies ist Teil eines MSMQ-Objekts und wird durch Aufrufen der API auf MQCreateQueue oder MQSetProperties festgelegt. Sie steuert, ob MSMQ nur Nachrichten von einer gesicherten Quelle (z. B. HTTPS) für diese Warteschlange akzeptiert.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | MSMQ-gesicherte Quelle                  |
| Ldap-Anzeigename | MSMQ-SecuredSource                   |
| Size              | 4 Bytes                              |
| Aktualisieren von Berechtigungen  | Der Besitzer der Warteschlange.                     |
| Updatehäufigkeit  | Wenn eine Warteschlange erstellt wird.             |
| Attribute-Id      | 1.2.840.113556.1.4.1713              |
| System-ID-GUID    | 8bf0221b-7a06-4d63-91f0-1499941813d3 |
| Syntax            | [**Boolean**](s-boolean.md)         |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falsch                                        |
| Ist einwertig       | Richtig                                         |
| Ist indiziert             | Falsch                                        |
| Im globalen Katalog      | Richtig                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**MSMQ-Queue**](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falsch                                        |
| Ist einwertig       | Richtig                                         |
| Ist indiziert             | Falsch                                        |
| Im globalen Katalog      | Richtig                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**MSMQ-Queue**](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falsch                                        |
| Ist einwertig       | Richtig                                         |
| Ist indiziert             | Falsch                                        |
| Im globalen Katalog      | Richtig                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**MSMQ-Queue**](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falsch                                        |
| Ist einwertig       | Richtig                                         |
| Ist indiziert             | Falsch                                        |
| Im globalen Katalog      | Richtig                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**MSMQ-Queue**](c-msmqqueue.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falsch                                        |
| Ist einwertig       | Richtig                                         |
| Ist indiziert             | Falsch                                        |
| Im globalen Katalog      | Richtig                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**MSMQ-Queue**](c-msmqqueue.md)<br/> |



 

 





