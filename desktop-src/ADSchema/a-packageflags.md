---
title: Package-Flags-Attribut
description: Ein Bitfeld, das die bereitstellungstatusflags für eine Anwendung enthält.
ms.assetid: 5b6cfed5-db04-438e-912b-60dce7a16409
ms.tgt_platform: multiple
keywords:
- AD-Schema für Package-Flags-Attribut
- packageflags-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Package-Flags
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7202124bdeac22347d727638dc564a145599e9c7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744969"
---
# <a name="package-flags-attribute"></a>Package-Flags-Attribut

Ein Bitfeld, das die bereitstellungstatusflags für eine Anwendung enthält.

Dieses Attribut kann NULL sein oder eine Kombination aus einem oder mehreren der folgenden Werte aufweisen.

| Wert                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x00000004<br/> | Die nicht verwaltete Version dieser Anwendung muss deinstalliert werden, bevor Sie zugewiesen wird. **Windows XP mit SP1 und höher:** Dieses Flag wird nicht unterstützt.<br/> <br/>                                                                                                                                          |
| 0x00000008<br/> | Dies ist eine veröffentlichte Anwendung.<br/>                                                                                                                                                                                                                                                                    |
| 0x00000010<br/> | Dieses Paket wurde nach der Beta Version 3 von Windows 2000 bereitgestellt.<br/>                                                                                                                                                                                                                                             |
| 0x00000020<br/> | Diese Anwendung kann mit dem Feature "Software" **in der System** Steuerung installiert werden.<br/>                                                                                                                                                                                                 |
| 0x00000040<br/> | Diese Anwendung kann bei Bedarf automatisch installiert werden.<br/>                                                                                                                                                                                                                                                   |
| 0x00000080<br/> | Diese Anwendung ist verwaist. Eine veröffentlichte Anwendung kann verwaist werden, wenn der Administrator die Anwendung aus der Liste der bereitstell baren Anwendungen entfernt.<br/>                                                                                                                                    |
| 0x00000100<br/> | Diese Anwendung sollte als deinstalliert behandelt werden.<br/>                                                                                                                                                                                                                                                  |
| 0x00000200<br/> | Diese Anwendung ist nur als Pilotprojekt verfügbar.<br/>                                                                                                                                                                                                                                                      |
| 0x00000400<br/> | Dabei handelt es sich um eine zugewiesene Anwendung. Eine zugewiesene Anwendung kann vom Benutzer nicht vollständig entfernt werden. Wenn der Benutzer versucht, die Anwendung mit dem Feature "Software" **in der System** Steuerung zu deinstallieren, wird die Anwendung beim Abschluss des Entfernens erneut dem Computer angekündigt.<br/> |
| 0x00000800<br/> | Diese Anwendung ist verwaist, wenn die Richtlinie entfernt wird. Wenn der Administrator die Richtlinie entfernt, die mit dieser Anwendung verknüpft ist, wird die Bereitstellung der Anwendung vom Administrator nicht mehr gesteuert, aber die installierte Anwendung funktioniert weiterhin.<br/>                          |
| 0x00001000<br/> | Diese Anwendung wird beim Entfernen der Bereitstellungs Richtlinie deinstalliert.<br/>                                                                                                                                                                                                                              |
| 0x00002000<br/> | Es wird eine vollständige Installation der vom Benutzer zugewiesenen Anwendungen ausgeführt.<br/>                                                                                                                                                                                                                                |
| 0x00004000<br/> | Ältere Versionen dieser Anwendung müssen auf diese Version aktualisiert werden.<br/>                                                                                                                                                                                                                                |
| 0x00008000<br/> | Dieses Paket unterstützt nur eine minimale Benutzeroberfläche mit einer Statusanzeige für den Installationsvorgang.<br/>                                                                                                                                                                                               |
| 0x00010000<br/> | Hierbei handelt es sich um ein Paket für 32-Bit-Versionen von Windows, die nicht auf Windows XP Professional x64 Edition oder 64-Bit-Versionen von Windows Server 2003 ausgeführt werden dürfen.<br/>                                                                                                                                      |
| 0x00020000<br/> | Dieses Paket eignet sich für jede Sprache.<br/>                                                                                                                                                                                                                                                          |
| 0x00040000<br/> | Dieses Paket enthält Upgrades.<br/>                                                                                                                                                                                                                                                                          |
| 0x00080000<br/> | Dieses Paket verfügt über eine vollständige Benutzeroberfläche für den Installationsvorgang.<br/>                                                                                                                                                                                                                                |
| 0x00100000<br/> | Klassen für diese Anwendung werden während eines erneuten Bereitstellungs Vorgangs beibehalten, wenn die Anwendung in einer Domänen Umbenennung erneut bereitgestellt wird.<br/>                                                                                                                                                                       |



 



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | Package-Flags                        |
| LDAP-Display-Name | packageflags                         |
| Size              | \-                                   |
| Berechtigung aktualisieren  | \-                                   |
| Aktualisierungshäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.327               |
| System-ID-GUID    | 7d6c0e99-7E20-11D0-afd6-00c04f d930c9 |
| Syntax            | [**Enumeration**](s-enumeration.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
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
| Ist-einwertig       | Richtig                                                             |
| Ist indiziert             | Richtig                                                             |
| Im globalen Katalog      | False                                                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| In verwendete Klassen        | [**Paket Registrierung**](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------|
| Link-ID                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | False                                                            |
| Ist-einwertig       | Richtig                                                             |
| Ist indiziert             | Richtig                                                             |
| Im globalen Katalog      | False                                                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| In verwendete Klassen        | [**Paket Registrierung**](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------|
| Link-ID                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | False                                                            |
| Ist-einwertig       | Richtig                                                             |
| Ist indiziert             | Richtig                                                             |
| Im globalen Katalog      | False                                                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| In verwendete Klassen        | [**Paket Registrierung**](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------|
| Link-ID                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | False                                                            |
| Ist-einwertig       | Richtig                                                             |
| Ist indiziert             | Richtig                                                             |
| Im globalen Katalog      | False                                                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| In verwendete Klassen        | [**Paket Registrierung**](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------|
| Link-ID                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | False                                                            |
| Ist-einwertig       | Richtig                                                             |
| Ist indiziert             | Richtig                                                             |
| Im globalen Katalog      | False                                                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| In verwendete Klassen        | [**Paket Registrierung**](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------|
| Link-ID                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | False                                                            |
| Ist-einwertig       | Richtig                                                             |
| Ist indiziert             | Richtig                                                             |
| Im globalen Katalog      | False                                                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| In verwendete Klassen        | [**Paket Registrierung**](c-packageregistration.md)<br/> |



 

 





