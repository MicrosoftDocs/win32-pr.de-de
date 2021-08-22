---
description: Erläutert, wie benutzerdefinierte Sicherheitspakete mithilfe der benutzerdefinierten Sicherheitspaket-API erstellt werden.
ms.assetid: 915ef590-c427-4ac2-a2f7-aed328776cb7
title: Benutzerdefinierte Sicherheitspakete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3799edb3eb8e0551afe7d7f7bcdc54924228445d6ffb28cb4773af843b5c2d9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008668"
---
# <a name="custom-security-packages"></a>Benutzerdefinierte Sicherheitspakete

Verwenden Sie die benutzerdefinierte Sicherheitspaket-API und die Funktionen der [*lokalen Sicherheitsautorität (Local Security Authority,*](/windows/desktop/SecGloss/l-gly) LSA), um neue Sicherheitsprotokolle zu implementieren, die in die Betriebssysteme Windows Server und Windows integriert sind.

Die API für benutzerdefinierte Sicherheitspakete unterstützt die kombinierte Entwicklung von benutzerdefinierten [*Sicherheitsunterstützungsanbietern*](/windows/desktop/SecGloss/s-gly) (SSPs), die [nicht interaktive Authentifizierungsdienste](noninteractive-authentication.md) und den sicheren Nachrichtenaustausch für Client-/Serveranwendungen bereitstellen, mit der Entwicklung von benutzerdefinierten [*Authentifizierungspaketen,*](/windows/desktop/SecGloss/a-gly)die Dienste für Anwendungen bereitstellen, die [die interaktive Authentifizierung](interactive-authentication.md)ausführen. Diese Dienste werden, wenn sie in einem einzelnen Paket kombiniert werden, als Sicherheitsunterstützungsanbieter/-authentifizierungspaket (SSP/AP) bezeichnet.

Wie bei von Microsoft bereitgestellten Sicherheitspaketen greifen Benutzer des benutzerdefinierten Sicherheitspakets mithilfe der [LSA-Anmeldefunktionen](authentication-functions.md)auf interaktive Authentifizierungsdienste zu. Nichtinteraktive Authentifizierungs- und Nachrichtenschutzdienste können direkt über [SSPI (Security Support Provider Interface)](sspi.md) aufgerufen werden.

Die in SSP/APs bereitgestellten Sicherheitspakete sind vollständig in das LSA integriert. Mithilfe der LSA-Supportfunktionen, die für benutzerdefinierte Sicherheitspakete verfügbar sind, können Entwickler erweiterte Sicherheitsfeatures wie die Tokenerstellung, [*zusätzliche Unterstützung von Anmeldeinformationen*](/windows/desktop/SecGloss/s-gly) und pass-through-Authentifizierung implementieren. Eine Liste dieser Unterstützungsfunktionen finden Sie unter [Von Authentifizierungspaketen aufgerufene LSA-Funktionen.](authentication-functions.md) Informationen zum Implementieren von benutzerdefinierten Sicherheitspaketen finden Sie unter [Erstellen von benutzerdefinierten Sicherheitspaketen.](creating-custom-security-packages.md)

Weitere Informationen zu benutzerdefinierten Sicherheitspaketen finden Sie in den folgenden Themen.



| Thema                                                                                                                                                 | BESCHREIBUNG                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [SSP/APs im Vergleich zu SSPs](ssp-aps-versus-ssps.md)<br/>                                                                                                | Informationen zum Bestimmen, ob ein Sicherheitspaket in einem SSP/AP oder SSP enthalten sein soll.<br/> |
| [LSA-Modus im Vergleich zum Benutzermodus](lsa-mode-versus-user-mode.md)<br/>                                                                                    | Details dazu, wie sich der LSA-Modus und der Benutzermodus unterscheiden.<br/>                                      |
| [Einschränkungen beim Registrieren und Installieren eines Sicherheitspakets](restrictions-around-registering-and-installing-a-security-package.md)<br/> | Aktionen von Sicherheitspaketen, die in Windows nicht unterstützt werden.<br/>                              |



 

 

