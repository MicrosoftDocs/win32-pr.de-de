---
title: SPN-Mappings-Attribut
description: Dieses Attribut mit mehreren Werten enthält eine Liste von Dienst Prinzipal Namen (SPN), um die Äquivalenz von SPN-Typen anzuzeigen.
ms.assetid: 6d37618d-426d-4e7b-8475-c912adb595ee
ms.tgt_platform: multiple
keywords:
- AD-Schema für SPN-Mappings-Attribut
- spnmappings-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- SPN-Mappings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3ccb07e068a22d0a85928832890f0b66ebda016
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519983"
---
# <a name="spn-mappings-attribute"></a>SPN-Mappings-Attribut

Dieses Attribut mit mehreren Werten enthält eine Liste von Dienst Prinzipal Namen (SPN), um die Äquivalenz von SPN-Typen anzuzeigen. Der SPN ist der Name, den ein Client zum eindeutigen Identifizieren einer Instanz eines Dienstanbieter verwendet. Wenn Sie mehrere Instanzen eines Diensts auf Computern innerhalb einer Gesamtstruktur installieren, muss jede Instanz über einen eigenen SPN verfügen. Eine Dienstinstanz kann mehrere SPNs aufweisen, falls mehrere Namen vorhanden sind, die von den Clients zur Authentifizierung verwendet werden können. Beispiel: "LDAP/..." SPNs können zugeordnet werden, damit Sie "Host/..." entsprechen. SPNs.



| Eingabe | Wert |
|-------------------|--------------------------------------------------------------------------------------------------------------------|
| CN                | SPN-Mappings                                                                                                       |
| LDAP-Display-Name | spnmappings                                                                                                        |
| Size              | \-                                                                                                                 |
| Berechtigung aktualisieren  | Dieser Wert wird während der Produktinstallation festgelegt. Diese kann vom Systemadministrator zu einem späteren Zeitpunkt geändert werden. |
| Aktualisierungshäufigkeit  | \-                                                                                                                 |
| Attribute-Id      | 1.2.840.113556.1.4.1347                                                                                            |
| System-ID-GUID    | 2ab0e76c-7041-11d2-9905-0000f 87a57d4                                                                               |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                                                        |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|--------------------------------------------------|
| Link-ID                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | False                                            |
| Ist-einwertig       | False                                            |
| Ist indiziert             | False                                            |
| Im globalen Katalog      | False                                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| In verwendete Klassen        | [**NTDS-Dienst**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|--------------------------------------------------|
| Link-ID                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | False                                            |
| Ist-einwertig       | False                                            |
| Ist indiziert             | False                                            |
| Im globalen Katalog      | False                                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| In verwendete Klassen        | [**NTDS-Dienst**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------------|
| Link-ID                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | False                                            |
| Ist-einwertig       | False                                            |
| Ist indiziert             | False                                            |
| Im globalen Katalog      | False                                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| In verwendete Klassen        | [**NTDS-Dienst**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|--------------------------------------------------|
| Link-ID                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | False                                            |
| Ist-einwertig       | False                                            |
| Ist indiziert             | False                                            |
| Im globalen Katalog      | False                                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| In verwendete Klassen        | [**NTDS-Dienst**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------------|
| Link-ID                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | False                                            |
| Ist-einwertig       | False                                            |
| Ist indiziert             | False                                            |
| Im globalen Katalog      | False                                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| In verwendete Klassen        | [**NTDS-Dienst**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|--------------------------------------------------|
| Link-ID                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | False                                            |
| Ist-einwertig       | False                                            |
| Ist indiziert             | False                                            |
| Im globalen Katalog      | False                                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| In verwendete Klassen        | [**NTDS-Dienst**](c-ntdsservice.md)<br/> |



 

 





