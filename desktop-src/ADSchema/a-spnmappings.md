---
title: SPN-Mappings-Attribut
description: Dieses mehrwertige Attribut enthält eine Liste von Dienstprinzipalnamen (Service Principal Names, SPN), um die Äquivalenz von SPN-Typen zu zeigen.
ms.assetid: 6d37618d-426d-4e7b-8475-c912adb595ee
ms.tgt_platform: multiple
keywords:
- SPN-Mappings AD-Schema
- AD-Schema des sPNMappings-Attributs
topic_type:
- apiref
api_name:
- SPN-Mappings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 451f8d3f98984f725915410e964e39a66905f29c1ccbcf9156b55d7ba51d3e5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118960049"
---
# <a name="spn-mappings-attribute"></a>SPN-Mappings-Attribut

Dieses mehrwertige Attribut enthält eine Liste von Dienstprinzipalnamen (Service Principal Names, SPN), um die Äquivalenz von SPN-Typen zu zeigen. Der SPN ist der Name, den ein Client verwendet, um eine Instanz eines Diensts eindeutig zu identifizieren. Wenn Sie mehrere Instanzen eines Diensts auf Computern innerhalb einer Gesamtstruktur installieren, muss jede Instanz über einen eigenen SPN verfügen. Eine Dienstinstanz kann mehrere SPNs aufweisen, falls mehrere Namen vorhanden sind, die von den Clients zur Authentifizierung verwendet werden können. Beispiel: "ldap/..." SPNs könnten zugeordnet werden, sodass sie "host/..." entsprechen. Spns.



| Eingabe | Wert |
|-------------------|--------------------------------------------------------------------------------------------------------------------|
| CN                | SPN-Mappings                                                                                                       |
| Ldap-Anzeigename | sPNMappings                                                                                                        |
| Size              | \-                                                                                                                 |
| Aktualisieren von Berechtigungen  | Dieser Wert wird während der Produktinstallation festgelegt. Sie kann vom Systemadministrator zu einem späteren Zeitpunkt geändert werden. |
| Updatehäufigkeit  | \-                                                                                                                 |
| Attribute-Id      | 1.2.840.113556.1.4.1347                                                                                            |
| System-Id-Guid    | 2ab0e76c-7041-11d2-9905-0000f87a57d4                                                                               |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                                                        |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|--------------------------------------------------|
| Link-ID                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Falsch                                            |
| Is-Single-Valued       | Falsch                                            |
| Ist indiziert             | Falsch                                            |
| Im globalen Katalog      | Falsch                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| In verwendete Klassen        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|--------------------------------------------------|
| Link-ID                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Falsch                                            |
| Is-Single-Valued       | Falsch                                            |
| Ist indiziert             | Falsch                                            |
| Im globalen Katalog      | Falsch                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| In verwendete Klassen        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------------|
| Link-ID                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Falsch                                            |
| Is-Single-Valued       | Falsch                                            |
| Ist indiziert             | Falsch                                            |
| Im globalen Katalog      | Falsch                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| In verwendete Klassen        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|--------------------------------------------------|
| Link-ID                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Falsch                                            |
| Is-Single-Valued       | Falsch                                            |
| Ist indiziert             | Falsch                                            |
| Im globalen Katalog      | Falsch                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| In verwendete Klassen        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------------|
| Link-ID                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Falsch                                            |
| Is-Single-Valued       | Falsch                                            |
| Ist indiziert             | Falsch                                            |
| Im globalen Katalog      | Falsch                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| In verwendete Klassen        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|--------------------------------------------------|
| Link-ID                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Falsch                                            |
| Is-Single-Valued       | Falsch                                            |
| Ist indiziert             | Falsch                                            |
| Im globalen Katalog      | Falsch                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| In verwendete Klassen        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



 

 





