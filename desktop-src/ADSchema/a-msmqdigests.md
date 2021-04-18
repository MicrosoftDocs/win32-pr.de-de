---
title: MSMQ-Digests-Attribut
description: Ein Array von Digests der entsprechenden Zertifikate in Attribut MSMQ-Sign-Zertifikats. Sie werden für die Zuordnung eines Digest zu einem Zertifikat verwendet.
ms.assetid: a9b03edd-1506-4f2d-afe1-7d953977f6fa
ms.tgt_platform: multiple
keywords:
- AD-Schema für MSMQ-Digests-Attribut
- AD-Schema des msmqdigests-Attributs
topic_type:
- apiref
api_name:
- MSMQ-Digests
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06d51c607b1d99af0aed46f259513f4bcf790844
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106344900"
---
# <a name="msmq-digests-attribute"></a>MSMQ-Digests-Attribut

Ein Array von Digests der entsprechenden Zertifikate in Attribut MSMQ-Sign-Zertifikats. Sie werden für die Zuordnung eines Digest zu einem Zertifikat verwendet.



| Eingabe | Wert |
|-------------------|-------------------------------------------------------|
| CN                | MSMQ-Digests                                          |
| LDAP-Display-Name | msmqdigests                                           |
| Size              | Jeder Digest ist 16 Bytes.                              |
| Berechtigung aktualisieren  | \-                                                    |
| Aktualisierungshäufigkeit  | \-                                                    |
| Attribute-Id      | 1.2.840.113556.1.4.948                                |
| System-ID-GUID    | 9a0dc33c-C100-11d1-bbc5-0080c76670c0                  |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md) |



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
| Ist-einwertig       | False                                                                                         |
| Ist indiziert             | Richtig                                                                                          |
| Im globalen Katalog      | Richtig                                                                                          |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                  |
| Range-Lower            | 16                                                                                            |
| Range-Upper            | 16                                                                                            |
| Search-Flags           | 0x00000001                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| In verwendete Klassen        | [**MSMQ-migriert-Benutzer**](c-msmqmigrateduser.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | False                                                                                         |
| Ist-einwertig       | False                                                                                         |
| Ist indiziert             | Richtig                                                                                          |
| Im globalen Katalog      | Richtig                                                                                          |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                  |
| Range-Lower            | 16                                                                                            |
| Range-Upper            | 16                                                                                            |
| Search-Flags           | 0x00000001                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| In verwendete Klassen        | [**MSMQ-migriert-Benutzer**](c-msmqmigrateduser.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | False                                                                                         |
| Ist-einwertig       | False                                                                                         |
| Ist indiziert             | Richtig                                                                                          |
| Im globalen Katalog      | Richtig                                                                                          |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                  |
| Range-Lower            | 16                                                                                            |
| Range-Upper            | 16                                                                                            |
| Search-Flags           | 0x00000001                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| In verwendete Klassen        | [**MSMQ-migriert-Benutzer**](c-msmqmigrateduser.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | False                                                                                         |
| Ist-einwertig       | False                                                                                         |
| Ist indiziert             | Richtig                                                                                          |
| Im globalen Katalog      | Richtig                                                                                          |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                  |
| Range-Lower            | 16                                                                                            |
| Range-Upper            | 16                                                                                            |
| Search-Flags           | 0x00000001                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| In verwendete Klassen        | [**MSMQ-migriert-Benutzer**](c-msmqmigrateduser.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | False                                                                                         |
| Ist-einwertig       | False                                                                                         |
| Ist indiziert             | Richtig                                                                                          |
| Im globalen Katalog      | Richtig                                                                                          |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                  |
| Range-Lower            | 16                                                                                            |
| Range-Upper            | 16                                                                                            |
| Search-Flags           | 0x00000001                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| In verwendete Klassen        | [**MSMQ-migriert-Benutzer**](c-msmqmigrateduser.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | False                                                                                         |
| Ist-einwertig       | False                                                                                         |
| Ist indiziert             | Richtig                                                                                          |
| Im globalen Katalog      | Richtig                                                                                          |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                  |
| Range-Lower            | 16                                                                                            |
| Range-Upper            | 16                                                                                            |
| Search-Flags           | 0x00000001                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| In verwendete Klassen        | [**MSMQ-migriert-Benutzer**](c-msmqmigrateduser.md)<br/> [**Benutzer**](c-user.md)<br/> |



 

 





