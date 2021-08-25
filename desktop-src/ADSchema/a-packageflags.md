---
title: Package-Flags-Attribut
description: Ein Bitfeld, das die Bereitstellungszustandsflags für eine Anwendung enthält.
ms.assetid: 5b6cfed5-db04-438e-912b-60dce7a16409
ms.tgt_platform: multiple
keywords:
- Package-Flags AD-Attributschema
- packageFlags-Attribut-AD-Schema
topic_type:
- apiref
api_name:
- Package-Flags
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd6965b5c39603032bdb673df10026b0eed2a5d5ae838aeb094013d9a5e95dff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119923940"
---
# <a name="package-flags-attribute"></a>Package-Flags-Attribut

Ein Bitfeld, das die Bereitstellungszustandsflags für eine Anwendung enthält.

Dieses Attribut kann 0 (null) oder eine Kombination aus einem oder mehreren der folgenden Werte sein.

| Wert                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x00000004<br/> | Die nicht verwaltete Version dieser Anwendung muss vor der Zuweisung deinstalliert werden. **Windows XP mit SP1 und höher:** Dieses Flag wird nicht unterstützt.<br/> <br/>                                                                                                                                          |
| 0x00000008<br/> | Dies ist eine veröffentlichte Anwendung.<br/>                                                                                                                                                                                                                                                                    |
| 0x00000010<br/> | Dieses Paket wurde nach Beta 3 von Windows 2000 bereitgestellt.<br/>                                                                                                                                                                                                                                             |
| 0x00000020<br/> | Diese Anwendung kann mit dem Feature **Software** der Systemsteuerung installiert werden.<br/>                                                                                                                                                                                                 |
| 0x00000040<br/> | Diese Anwendung kann bei Bedarf automatisch installiert werden.<br/>                                                                                                                                                                                                                                                   |
| 0x00000080<br/> | Diese Anwendung ist verwaist. Eine veröffentlichte Anwendung kann verwaist werden, wenn der Administrator die Anwendung aus der Liste der bereitstellbaren Anwendungen entfernt.<br/>                                                                                                                                    |
| 0x00000100<br/> | Diese Anwendung sollte als deinstalliert behandelt werden.<br/>                                                                                                                                                                                                                                                  |
| 0x00000200<br/> | Diese Anwendung ist nur als Pilot verfügbar.<br/>                                                                                                                                                                                                                                                      |
| 0x00000400<br/> | Dies ist eine zugewiesene Anwendung. Eine zugewiesene Anwendung kann vom Benutzer nicht vollständig entfernt werden. Wenn der Benutzer versucht, die Anwendung mit dem Feature **Programme hinzufügen oder entfernen** des Systemsteuerung zu deinstallieren, wird die Anwendung dem Computer nach Abschluss der Entfernung erneut angekündigt.<br/> |
| 0x00000800<br/> | Diese Anwendung ist verwaist, wenn die Richtlinie entfernt wird. Wenn der Administrator die Richtlinie entfernt, die sich auf diese Anwendung bezieht, steuert der Administrator die Bereitstellung der Anwendung nicht mehr, aber die installierte Anwendung funktioniert weiterhin.<br/>                          |
| 0x00001000<br/> | Diese Anwendung wird deinstalliert, wenn die Bereitstellungsrichtlinie entfernt wird.<br/>                                                                                                                                                                                                                              |
| 0x00002000<br/> | Eine vollständige Installation von vom Benutzer zugewiesenen Anwendungen wird ausgeführt.<br/>                                                                                                                                                                                                                                |
| 0x00004000<br/> | Ältere Versionen dieser Anwendung müssen auf diese Version aktualisiert werden.<br/>                                                                                                                                                                                                                                |
| 0x00008000<br/> | Dieses Paket unterstützt nur eine minimale Benutzeroberfläche mit einer Statusanzeige für den Installationsvorgang.<br/>                                                                                                                                                                                               |
| 0x00010000<br/> | Dies ist ein Paket für 32-Bit-Versionen von Windows, das nicht auf Windows XP Professional x64 Edition oder 64-Bit-Versionen von Windows Server 2003 ausgeführt werden sollte.<br/>                                                                                                                                      |
| 0x00020000<br/> | Dieses Paket eignet sich für jede Sprache.<br/>                                                                                                                                                                                                                                                          |
| 0x00040000<br/> | Dieses Paket verfügt über Upgrades.<br/>                                                                                                                                                                                                                                                                          |
| 0x00080000<br/> | Dieses Paket verfügt über eine vollständige Benutzeroberfläche für den Installationsvorgang.<br/>                                                                                                                                                                                                                                |
| 0x00100000<br/> | Klassen für diese Anwendung werden während eines erneuten Bereitstellungsvorgangs beibehalten, wenn die Anwendung in einer Domänenumbenennung erneut bereitgestellt wird.<br/>                                                                                                                                                                       |



 



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | Package-Flags                        |
| Ldap-Anzeigename | packageFlags                         |
| Size              | \-                                   |
| Aktualisieren von Berechtigungen  | \-                                   |
| Updatehäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.327               |
| System-ID-GUID    | 7d6c0e99-7e20-11d0-afd6-00c04fd930c9 |
| Syntax            | [**Enumeration**](s-enumeration.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------|
| Link-ID                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | False                                                            |
| Ist einwertig       | True                                                             |
| Ist indiziert             | True                                                             |
| Im globalen Katalog      | False                                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| In verwendete Klassen        | [**Paketregistrierung**](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------|
| Link-ID                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | False                                                            |
| Is-Single-Valued       | True                                                             |
| Ist indiziert             | True                                                             |
| Im globalen Katalog      | False                                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| In verwendete Klassen        | [**Paketregistrierung**](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------|
| Link-ID                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | False                                                            |
| Is-Single-Valued       | True                                                             |
| Ist indiziert             | True                                                             |
| Im globalen Katalog      | False                                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| In verwendete Klassen        | [**Paketregistrierung**](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------|
| Link-ID                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | False                                                            |
| Is-Single-Valued       | True                                                             |
| Ist indiziert             | True                                                             |
| Im globalen Katalog      | False                                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| In verwendete Klassen        | [**Paketregistrierung**](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------|
| Link-ID                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | False                                                            |
| Is-Single-Valued       | True                                                             |
| Ist indiziert             | True                                                             |
| Im globalen Katalog      | False                                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| In verwendete Klassen        | [**Paketregistrierung**](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------|
| Link-ID                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | False                                                            |
| Is-Single-Valued       | True                                                             |
| Ist indiziert             | True                                                             |
| Im globalen Katalog      | False                                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| In verwendete Klassen        | [**Paketregistrierung**](c-packageregistration.md)<br/> |



 

 





