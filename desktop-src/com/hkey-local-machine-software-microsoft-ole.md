---
title: HKEY_LOCAL_MACHINESOFTWAREMicrosoftOle
description: Die Registrierungs Werte, die der HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ OLE key zugeordnet sind, steuern die Standardeinstellungen für Start-und Zugriffsberechtigungen und Sicherheitsfunktionen auf Aufrufebene für COM-basierte Anwendungen, die nicht CoInitializeSecurity aufrufen.
ms.assetid: 871ae88f-ed2c-4078-8160-b0a490390426
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02406bca5dd69098f8cd49c2fba5f067852fcc5f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037524"
---
# <a name="hkey_local_machinesoftwaremicrosoftole"></a>HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ OLE

Die Registrierungs Werte, die der **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ OLE** key zugeordnet sind, steuern die Standardeinstellungen für Start-und Zugriffsberechtigungen und Sicherheitsfunktionen auf Aufrufebene für COM-basierte Anwendungen, die nicht [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)aufrufen.

Nur Administratoren, der Objekt Ersteller und das System verfügen über Vollzugriff auf diesen Teil der Registrierung. Alle anderen Benutzer verfügen über schreibgeschützten Zugriff.



| Registrierungswert                                                                         | BESCHREIBUNG                                                                                                                                                                   |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Activationfailurelogginglevel**](activationfailurelogginglevel.md)                 | Legt den ausführlichkeits Grad von Ereignisprotokoll Einträgen zu fehlgeschlagenen Anforderungen für das Starten und Aktivieren von Komponenten fest.                                                                            |
| [**CallFailureLoggingLevel**](callfailurelogginglevel.md)                             | Legt die Ausführlichkeit von Ereignisprotokoll Einträgen zu fehlgeschlagenen Aufrufen von-Komponenten fest.                                                                                                     |
| [**Dcomscmremotecallflags**](dcomscmremotecallflags.md)                               | Steuert das Verhalten von Aufrufen vom lokalen DCOM-Dienststeuerungs-Manager (dcomscm) zu einem Remote-dcomscm.                                                                     |
| [**DefaultAccessPermission**](defaultaccesspermission.md)                             | Definiert die Standard Zugriffs Berechtigungs Liste für den Computer.                                                                                                                      |
| [**DefaultLaunchPermission**](defaultlaunchpermission.md)                             | Definiert die standardmäßige Start-ACL für den Computer.                                                                                                                                  |
| [**EnableDCOM**](enabledcom.md)                                                       | Legt die globale Aktivierungs Richtlinie für den Computer fest.                                                                                                                           |
| [**Invalidsecuritydescriptor LoggingLevel**](invalidsecuritydescriptorlogginglevel.md) | Legt den ausführlichkeits Grad von Ereignisprotokoll Einträgen über ungültige Sicherheits Deskriptoren für die Start-und Zugriffsberechtigungen der Komponente fest.                                                       |
| [**Legacyauthenticationlevel**](legacyauthenticationlevel.md)                         | Legt die Standard Authentifizierungs Ebene fest.                                                                                                                                        |
| [**Legacyidentitäts ationlevel**](legacyimpersonationlevel.md)                           | Legt die Standard-Identitätswechsel Ebene fest.                                                                                                                                         |
| [**Legacysecurereferences**](legacysecurereferences.md)                               | Bestimmt die Sicherheitsstufe von adressaufgabeschlikationen /  .                                                                                                              |
| [**MachineAccessRestriction**](machineaccessrestriction.md)                           | Legt die Computer weite Einschränkungs Richtlinie für den Komponenten Zugriff fest.                                                                                                               |
| [**MachineLaunchRestriction**](machinelaunchrestriction.md)                           | Legt die Computer weite Einschränkungs Richtlinie für das Starten und Aktivieren von Komponenten fest.                                                                                                |
| [**NonRedist**](nonredist.md)                                                         | Fügt der Liste der Dateien Namen hinzu, die nicht exportiert werden sollen, wenn com+-Anwendungen zur Installation auf anderen Computern verpackt werden. Beachten Sie, dass dies ein Unterschlüssel und kein Wert ist. |
| [**Srpactivateasactivatorchecks**](srpactivateasactivatorchecks.md)                   | Bestimmt, ob die Richtlinien für die Software Einschränkungs Richtlinie (SRP) während der Aktivierungen von activateasactivator verwendet werden.                                                            |
| [**Srprunningobjectchecks**](srprunningobjectchecks.md)                               | Bestimmt, ob Verbindungsversuche mit ausgelaufenden Objekten auf kompatible Richtlinien für Software Einschränkungs Richtlinien (SRP) überprüft werden.                                         |



 

 

 




