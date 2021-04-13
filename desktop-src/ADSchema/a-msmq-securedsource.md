---
title: MSMQ-sicheres Quell Attribut
description: Dies ist Teil eines MSMQ-Objekts, das durch den Aufruf der API auf MQCreateQueue oder mqsetproperties festgelegt wird. Es steuert, ob MSMQ Nachrichten nur von einer gesicherten Quelle (z. b. HTTPS) für diese Warteschlange akzeptiert.
ms.assetid: 780d164f-c7fa-4c65-b46e-3a67ead92163
ms.tgt_platform: multiple
keywords:
- AD-Schema für MSMQ-sicheres Quell Attribut
- AD-Schema für MSMQ-SecuredSource-Attribut
topic_type:
- apiref
api_name:
- MSMQ-Secured-Source
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5dd005cedcd650aa0604a85e78a46d10f1e01b0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519767"
---
# <a name="msmq-secured-source-attribute"></a>MSMQ-sicheres Quell Attribut

Dies ist Teil eines MSMQ-Objekts, das durch den Aufruf der API auf MQCreateQueue oder mqsetproperties festgelegt wird. Es steuert, ob MSMQ Nachrichten nur von einer gesicherten Quelle (z. b. HTTPS) für diese Warteschlange akzeptiert.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | MSMQ-gesicherte Quelle                  |
| LDAP-Display-Name | MSMQ-SecuredSource                   |
| Size              | 4 Bytes                              |
| Berechtigung aktualisieren  | Der Besitzer der Warteschlange.                     |
| Aktualisierungshäufigkeit  | Wenn eine Warteschlange erstellt wird.             |
| Attribute-Id      | 1.2.840.113556.1.4.1713              |
| System-ID-GUID    | 8bf 0221b-7a06-4d63-91-Dienst-D3 |
| Syntax            | [**Booleschen**](s-boolean.md)         |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Ist-einwertig       | Richtig                                         |
| Ist indiziert             | False                                        |
| Im globalen Katalog      | Richtig                                         |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**MSMQ-Warteschlange**](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Ist-einwertig       | Richtig                                         |
| Ist indiziert             | False                                        |
| Im globalen Katalog      | Richtig                                         |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**MSMQ-Warteschlange**](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Ist-einwertig       | Richtig                                         |
| Ist indiziert             | False                                        |
| Im globalen Katalog      | Richtig                                         |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**MSMQ-Warteschlange**](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Ist-einwertig       | Richtig                                         |
| Ist indiziert             | False                                        |
| Im globalen Katalog      | Richtig                                         |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**MSMQ-Warteschlange**](c-msmqqueue.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Ist-einwertig       | Richtig                                         |
| Ist indiziert             | False                                        |
| Im globalen Katalog      | Richtig                                         |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**MSMQ-Warteschlange**](c-msmqqueue.md)<br/> |



 

 





