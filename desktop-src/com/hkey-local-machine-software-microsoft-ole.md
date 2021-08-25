---
title: HKEY_LOCAL_MACHINESOFTWAREMicrosoftOle
description: Die Dem HKEY LOCAL MACHINE SOFTWARE Microsoft Ole-Schlüssel zugeordneten Registrierungswerte steuern die Standardeinstellungen für Start- und Zugriffsberechtigungen sowie Sicherheitsfunktionen auf Aufrufebene für COM-basierte Anwendungen, die \_ \_ \\ \\ \\ CoInitializeSecurity nicht aufrufen.
ms.assetid: 871ae88f-ed2c-4078-8160-b0a490390426
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1648f12cd3983c73f5fdae040d4b81a833cce64995d98c19ef804e2941af48e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993050"
---
# <a name="hkey_local_machinesoftwaremicrosoftole"></a>HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Ole

Die Dem **HKEY \_ LOCAL \_ MACHINE SOFTWARE Microsoft \\ \\ \\ Ole-Schlüssel** zugeordneten Registrierungswerte steuern die Standardeinstellungen für Start- und Zugriffsberechtigungen sowie Sicherheitsfunktionen auf Aufrufebene für COM-basierte Anwendungen, die [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)nicht aufrufen.

Nur Administratoren, der Objektersteller und das System haben Vollzugriff auf diesen Teil der Registrierung. Alle anderen Benutzer haben schreibgeschützten Zugriff.



| Registrierungswert                                                                         | BESCHREIBUNG                                                                                                                                                                   |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActivationFailureLoggingLevel**](activationfailurelogginglevel.md)                 | Legt die Ausführlichkeit von Ereignisprotokolleinträgen zu fehlgeschlagenen Anforderungen für komponentenstart und -aktivierung fest.                                                                            |
| [**CallFailureLoggingLevel**](callfailurelogginglevel.md)                             | Legt die Ausführlichkeit von Ereignisprotokolleinträgen zu fehlgeschlagenen Aufrufen von Komponenten fest.                                                                                                     |
| [**DCOMSCMRemoteCallFlags**](dcomscmremotecallflags.md)                               | Steuert das Verhalten von Aufrufen vom lokalen DCOM-Dienststeuerungs-Manager (DCOMSCM) an einen Remote-DCOMSCM.                                                                     |
| [**DefaultAccessPermission**](defaultaccesspermission.md)                             | Definiert die Standardliste der Zugriffsberechtigungen für den Computer.                                                                                                                      |
| [**DefaultLaunchPermission**](defaultlaunchpermission.md)                             | Definiert die Standardstart-ACL für den Computer.                                                                                                                                  |
| [**EnableDCOM**](enabledcom.md)                                                       | Legt die globale Aktivierungsrichtlinie für den Computer fest.                                                                                                                           |
| [**InvalidSecurityDescriptorLoggingLevel**](invalidsecuritydescriptorlogginglevel.md) | Legt die Ausführlichkeit von Ereignisprotokolleinträgen zu ungültigen Sicherheitsbeschreibungen für Komponentenstart- und Zugriffsberechtigungen fest.                                                       |
| [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md)                         | Legt die Standardauthentifizierungsebene fest.                                                                                                                                        |
| [**LegacyImpersonationLevel**](legacyimpersonationlevel.md)                           | Legt die Standard-Identitätswechselebene fest.                                                                                                                                         |
| [**LegacySecureReferences**](legacysecurereferences.md)                               | Bestimmt die Sicherheitsstufe von AddRef-Releaseaufrufen. /                                                                                                               |
| [**MachineAccessRestriction**](machineaccessrestriction.md)                           | Legt die computerweite Einschränkungsrichtlinie für den Komponentenzugriff fest.                                                                                                               |
| [**MachineLaunchRestriction**](machinelaunchrestriction.md)                           | Legt die computerweite Einschränkungsrichtlinie für den Komponentenstart und die -aktivierung fest.                                                                                                |
| [**NonRedist**](nonredist.md)                                                         | Fügt der Liste der Dateien Namen hinzu, die nicht exportiert werden sollen, wenn COM+-Anwendungen für die Installation auf anderen Computern gepackt werden. Beachten Sie, dass dies ein Unterschlüssel und kein Wert ist. |
| [**SRPActivateAsActivatorChecks**](srpactivateasactivatorchecks.md)                   | Bestimmt, ob die Vertrauensebenen der Softwareeinschränkungsrichtlinie (Software Restriction Policy, SRP) während der ActivateAsActivator-Aktivierungen verwendet werden.                                                            |
| [**SRPRunningObjectChecks**](srprunningobjectchecks.md)                               | Bestimmt, ob Versuche, eine Verbindung mit ausgeführten Objekten herzustellen, auf kompatible Vertrauensebenen der Softwareeinschränkungsrichtlinie (Software Restriction Policy, SRP) durchgespiegelt werden.                                         |



 

 

 




