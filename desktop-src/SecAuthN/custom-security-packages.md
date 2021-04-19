---
description: Erläutert, wie benutzerdefinierte Sicherheitspakete mithilfe der benutzerdefinierten Sicherheitspaket-API erstellt werden.
ms.assetid: 915ef590-c427-4ac2-a2f7-aed328776cb7
title: Benutzerdefinierte Sicherheitspakete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a4c447f1a24a3edc2f25a55f83d82c174094c50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346994"
---
# <a name="custom-security-packages"></a>Benutzerdefinierte Sicherheitspakete

Verwenden Sie zum Implementieren neuer Sicherheitsprotokolle, die in die Windows Server-und Windows-Betriebssysteme integriert sind, die benutzerdefinierte Sicherheitspaket-API und die Funktionen der [*lokalen Sicherheits Autorität*](/windows/desktop/SecGloss/l-gly) (LSA).

Die benutzerdefinierte Sicherheitspaket-API unterstützt die kombinierte Entwicklung von benutzerdefinierten [*Security Support Providers*](/windows/desktop/SecGloss/s-gly) (SSPs), die [nicht interaktive Authentifizierungs](noninteractive-authentication.md) Dienste und den sicheren Nachrichtenaustausch für Client-/Serveranwendungen bereitstellen, mit der Entwicklung benutzerdefinierter [*Authentifizierungs Pakete*](/windows/desktop/SecGloss/a-gly), die Dienste für Anwendungen bereitstellen, die [interaktive Authentifizierung](interactive-authentication.md)durchführen. Diese Dienste werden, wenn Sie in einem einzelnen Paket kombiniert werden, als Security Support Provider-/Authentifizierungspaket (SSP/AP) bezeichnet.

Wie bei von Microsoft bereitgestellten Sicherheitspaketen greifen Benutzer des benutzerdefinierten Sicherheitspakets mithilfe der [LSA-Anmelde Funktionen](authentication-functions.md)auf interaktive Authentifizierungsdienste zu. Der Zugriff auf die nicht interaktive Authentifizierung und den Nachrichten Schutzdienst kann mithilfe der [Security Support Provider Interface](sspi.md) (SSPI) direkt erfolgen.

Die in SSP/APS bereitgestellten Sicherheitspakete sind vollständig in die LSA integriert. Mithilfe der LSA-Unterstützungsfunktionen, die für benutzerdefinierte Sicherheitspakete verfügbar sind, können Entwickler erweiterte Sicherheitsfunktionen implementieren, wie z. b. Tokenerstellung, Unterstützung [*zusätzlicher Anmelde*](/windows/desktop/SecGloss/s-gly) Informationen und Passthrough-Authentifizierung. Eine Liste der unterstützten Funktionen finden Sie unter [LSA-Funktionen, die von Authentifizierungs Paketen aufgerufen](authentication-functions.md)werden. Informationen zum Implementieren von benutzerdefinierten Sicherheitspaketen finden Sie unter [Erstellen benutzerdefinierter Sicherheitspakete](creating-custom-security-packages.md).

Weitere Informationen zu benutzerdefinierten Sicherheitspaketen finden Sie in den folgenden Themen.



| Thema                                                                                                                                                 | BESCHREIBUNG                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [SSP/APS im Vergleich zu SSPs](ssp-aps-versus-ssps.md)<br/>                                                                                                | Informationen dazu, wie Sie bestimmen können, ob sich ein Sicherheitspaket in einem SSP/AP oder SSP befinden sollte.<br/> |
| [LSA-Modus im Vergleich zum Benutzermodus](lsa-mode-versus-user-mode.md)<br/>                                                                                    | Details dazu, wie der LSA-Modus und der Benutzermodus unterschiedlich sind.<br/>                                      |
| [Einschränkungen bei der Registrierung und Installation eines Sicherheitspakets](restrictions-around-registering-and-installing-a-security-package.md)<br/> | Aktionen von Sicherheitspaketen, die in Windows nicht unterstützt werden.<br/>                              |



 

 

