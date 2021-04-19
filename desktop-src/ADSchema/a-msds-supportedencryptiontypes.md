---
title: ms-DS-supported-Encryption-Types-Attribut
description: Die Verschlüsselungsalgorithmen, die von Benutzer-, Computer-oder Vertrauens Konten unterstützt werden. Beachten Sie, dass der KDC diese Informationen beim Erstellen eines Dienst Tickets für dieses Konto verwendet.
ms.assetid: 6f9055a9-531e-4f4b-8703-aca5531a3bcb
ms.tgt_platform: multiple
keywords:
- von ms-DS unterstützte-Encryption-Types-Attribut AD-Schema
- adschema des msDS-supportedencryptiontypes-Attributs
topic_type:
- apiref
api_name:
- ms-DS-Supported-Encryption-Types
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ab16959d1f1cd4405cb661a6026f3734a134f8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106346578"
---
# <a name="ms-ds-supported-encryption-types-attribute"></a>ms-DS-supported-Encryption-Types-Attribut

Die Verschlüsselungsalgorithmen, die von Benutzer-, Computer-oder Vertrauens Konten unterstützt werden.

> [!Note]  
> Der KDC verwendet diese Informationen bei der Erstellung eines Dienst Tickets für dieses Konto. Dienste und Computer können dieses Attribut auf den jeweiligen Konten in Active Directory automatisch aktualisieren und benötigen daher Schreibzugriff auf dieses Attribut.

 



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | ms-DS-supported-Encryption-Types     |
| LDAP-Display-Name | MSDS-supportedencryptiontypes        |
| Size              | \-                                   |
| Berechtigung aktualisieren  | \-                                   |
| Aktualisierungshäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1963              |
| System-ID-GUID    | 20119867-1d04-4ab7-9371-cfc3d5df0afd |
| Syntax            | [**Enumeration**](s-enumeration.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                     |
| MAPI-Id                | \-                                                                                     |
| System-Only            | False                                                                                  |
| Ist-einwertig       | Richtig                                                                                   |
| Ist indiziert             | False                                                                                  |
| Im globalen Katalog      | False                                                                                  |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                           |
| Range-Lower            | \-                                                                                     |
| Range-Upper            | \-                                                                                     |
| Search-Flags           | 0x00000000                                                                             |
| System-Flags           | 0x00000010                                                                             |
| In verwendete Klassen        | [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                     |
| MAPI-Id                | \-                                                                                     |
| System-Only            | False                                                                                  |
| Ist-einwertig       | Richtig                                                                                   |
| Ist indiziert             | False                                                                                  |
| Im globalen Katalog      | False                                                                                  |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                           |
| Range-Lower            | \-                                                                                     |
| Range-Upper            | \-                                                                                     |
| Search-Flags           | 0x00000000                                                                             |
| System-Flags           | 0x00000010                                                                             |
| In verwendete Klassen        | [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                     |
| MAPI-Id                | \-                                                                                     |
| System-Only            | False                                                                                  |
| Ist-einwertig       | Richtig                                                                                   |
| Ist indiziert             | False                                                                                  |
| Im globalen Katalog      | False                                                                                  |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                           |
| Range-Lower            | \-                                                                                     |
| Range-Upper            | \-                                                                                     |
| Search-Flags           | 0x00000000                                                                             |
| System-Flags           | 0x00000010                                                                             |
| In verwendete Klassen        | [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> [**Benutzer**](c-user.md)<br/> |



 

 





