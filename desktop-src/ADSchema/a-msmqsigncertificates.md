---
title: MSMQ-Sign-Zertifikats-Attribut
description: Dieses Attribut enthält eine Reihe von Zertifikaten. Ein Benutzer kann ein Zertifikat pro Computer generieren. Für jedes Zertifikat wird auch ein Digest beibehalten.
ms.assetid: 70e182c7-3544-43d7-b27a-6e8d03bd2d47
ms.tgt_platform: multiple
keywords:
- AD-Schema für das Attribut "MSMQ-Sign-Zertifikats"
- AD-Schema des msmqsignzertifikats-Attributs
topic_type:
- apiref
api_name:
- MSMQ-Sign-Certificates
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd7e81cf145ac249b78e0a3e20be657df68b4af
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859648"
---
# <a name="msmq-sign-certificates-attribute"></a>MSMQ-Sign-Zertifikats-Attribut

Dieses Attribut enthält eine Reihe von Zertifikaten. Ein Benutzer kann ein Zertifikat pro Computer generieren. Für jedes Zertifikat wird auch ein Digest beibehalten.



| Eingabe | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| CN                | MSMQ-Sign-Zertifikate                                                                 |
| LDAP-Display-Name | msmqsignzertifikate                                                                   |
| Size              | Der Attributtyp ist ein BLOB, die Größe ist nicht begrenzt, und die Daten werden in unserem eigenen Format gespeichert. |
| Berechtigung aktualisieren  | \-                                                                                     |
| Aktualisierungshäufigkeit  | \-                                                                                     |
| Attribute-Id      | 1.2.840.113556.1.4.947                                                                 |
| System-ID-GUID    | 9a0dc33b-C100-11d1-bbc5-0080c76670c0                                                   |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md)                                  |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | False                                                                                         |
| Ist-einwertig       | Richtig                                                                                          |
| Ist indiziert             | False                                                                                         |
| Im globalen Katalog      | Richtig                                                                                          |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                  |
| Range-Lower            | \-                                                                                            |
| Range-Upper            | \-                                                                                            |
| Search-Flags           | 0x00000000                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| In verwendete Klassen        | [**MSMQ-migriert-Benutzer**](c-msmqmigrateduser.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | False                                                                                         |
| Ist-einwertig       | Richtig                                                                                          |
| Ist indiziert             | False                                                                                         |
| Im globalen Katalog      | Richtig                                                                                          |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                  |
| Range-Lower            | \-                                                                                            |
| Range-Upper            | \-                                                                                            |
| Search-Flags           | 0x00000000                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| In verwendete Klassen        | [**MSMQ-migriert-Benutzer**](c-msmqmigrateduser.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | False                                                                                         |
| Ist-einwertig       | Richtig                                                                                          |
| Ist indiziert             | False                                                                                         |
| Im globalen Katalog      | Richtig                                                                                          |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                  |
| Range-Lower            | \-                                                                                            |
| Range-Upper            | \-                                                                                            |
| Search-Flags           | 0x00000000                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| In verwendete Klassen        | [**MSMQ-migriert-Benutzer**](c-msmqmigrateduser.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | False                                                                                         |
| Ist-einwertig       | Richtig                                                                                          |
| Ist indiziert             | False                                                                                         |
| Im globalen Katalog      | Richtig                                                                                          |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                  |
| Range-Lower            | \-                                                                                            |
| Range-Upper            | \-                                                                                            |
| Search-Flags           | 0x00000000                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| In verwendete Klassen        | [**MSMQ-migriert-Benutzer**](c-msmqmigrateduser.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | False                                                                                         |
| Ist-einwertig       | Richtig                                                                                          |
| Ist indiziert             | False                                                                                         |
| Im globalen Katalog      | Richtig                                                                                          |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                  |
| Range-Lower            | \-                                                                                            |
| Range-Upper            | \-                                                                                            |
| Search-Flags           | 0x00000000                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| In verwendete Klassen        | [**MSMQ-migriert-Benutzer**](c-msmqmigrateduser.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | False                                                                                         |
| Ist-einwertig       | Richtig                                                                                          |
| Ist indiziert             | False                                                                                         |
| Im globalen Katalog      | Richtig                                                                                          |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                  |
| Range-Lower            | \-                                                                                            |
| Range-Upper            | \-                                                                                            |
| Search-Flags           | 0x00000000                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| In verwendete Klassen        | [**MSMQ-migriert-Benutzer**](c-msmqmigrateduser.md)<br/> [**Benutzer**](c-user.md)<br/> |



 

 





