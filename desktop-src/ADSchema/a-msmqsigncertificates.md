---
title: MSMQ-Sign-Certificates-Attribut
description: Dieses Attribut enthält eine Reihe von Zertifikaten. Ein Benutzer kann ein Zertifikat pro Computer generieren. Für jedes Zertifikat wird auch ein Digest beibehalten.
ms.assetid: 70e182c7-3544-43d7-b27a-6e8d03bd2d47
ms.tgt_platform: multiple
keywords:
- AD-Schema des MSMQ-Sign-Certificates-Attributs
- mSMQSignCertificates-Attribut-AD-Schema
topic_type:
- apiref
api_name:
- MSMQ-Sign-Certificates
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89ee82a5a2bf64acc315dfb535ca6897261ef0cb26f5e249a8c8593cc492b53c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119081744"
---
# <a name="msmq-sign-certificates-attribute"></a>MSMQ-Sign-Certificates-Attribut

Dieses Attribut enthält eine Reihe von Zertifikaten. Ein Benutzer kann ein Zertifikat pro Computer generieren. Für jedes Zertifikat wird auch ein Digest beibehalten.



| Eingabe | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| CN                | MSMQ-Sign-Certificates                                                                 |
| Ldap-Anzeigename | mSMQSignCertificates                                                                   |
| Size              | Der Attributtyp ist ein BLOB, die Größe ist nicht beschränkt, und Die Daten werden in unserem eigenen Format gespeichert. |
| Aktualisieren von Berechtigungen  | \-                                                                                     |
| Updatehäufigkeit  | \-                                                                                     |
| Attribute-Id      | 1.2.840.113556.1.4.947                                                                 |
| System-ID-GUID    | 9a0dc33b-c100-11d1-sender5-0080c76670c0                                                   |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md)                                  |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
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
| Ist einwertig       | True                                                                                          |
| Ist indiziert             | False                                                                                         |
| Im globalen Katalog      | True                                                                                          |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                  |
| Range-Lower            | \-                                                                                            |
| Range-Upper            | \-                                                                                            |
| Search-Flags           | 0x00000000                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| In verwendete Klassen        | [**MSMQ-Migrated-User**](c-msmqmigrateduser.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | False                                                                                         |
| Ist einwertig       | True                                                                                          |
| Ist indiziert             | False                                                                                         |
| Im globalen Katalog      | True                                                                                          |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                  |
| Range-Lower            | \-                                                                                            |
| Range-Upper            | \-                                                                                            |
| Search-Flags           | 0x00000000                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| In verwendete Klassen        | [**MSMQ-Migrated-User**](c-msmqmigrateduser.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | False                                                                                         |
| Ist einwertig       | True                                                                                          |
| Ist indiziert             | False                                                                                         |
| Im globalen Katalog      | True                                                                                          |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                  |
| Range-Lower            | \-                                                                                            |
| Range-Upper            | \-                                                                                            |
| Search-Flags           | 0x00000000                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| In verwendete Klassen        | [**MSMQ-Migrated-User**](c-msmqmigrateduser.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | False                                                                                         |
| Is-Single-Valued       | True                                                                                          |
| Ist indiziert             | False                                                                                         |
| Im globalen Katalog      | True                                                                                          |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                  |
| Range-Lower            | \-                                                                                            |
| Range-Upper            | \-                                                                                            |
| Search-Flags           | 0x00000000                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| In verwendete Klassen        | [**MSMQ-Migrated-User**](c-msmqmigrateduser.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | False                                                                                         |
| Is-Single-Valued       | True                                                                                          |
| Ist indiziert             | False                                                                                         |
| Im globalen Katalog      | True                                                                                          |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                  |
| Range-Lower            | \-                                                                                            |
| Range-Upper            | \-                                                                                            |
| Search-Flags           | 0x00000000                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| In verwendete Klassen        | [**MSMQ-Migrated-User**](c-msmqmigrateduser.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | False                                                                                         |
| Is-Single-Valued       | True                                                                                          |
| Ist indiziert             | False                                                                                         |
| Im globalen Katalog      | True                                                                                          |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                  |
| Range-Lower            | \-                                                                                            |
| Range-Upper            | \-                                                                                            |
| Search-Flags           | 0x00000000                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| In verwendete Klassen        | [**MSMQ-Migrated-User**](c-msmqmigrateduser.md)<br/> [**Benutzer**](c-user.md)<br/> |



 

 





