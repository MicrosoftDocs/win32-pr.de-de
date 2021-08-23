---
description: Wenn rollenbasierte Sicherheit verwendet wird, kann das Kontextobjekt für Sicherheitsaufrufe verwendet werden, um auf Sicherheitsinformationen zum aktuellen Aufruf zu zugreifen.
ms.assetid: 9fc0a9e5-934c-4510-8fbb-1fb2817aa0ea
title: Zugreifen auf Kontextinformationen für Sicherheitsaufrufe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38e438ce3cfa137ece28bce70d2c820becede231b1b0381da38dd7c6bcc21cb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639120"
---
# <a name="accessing-security-call-context-information"></a>Zugreifen auf Kontextinformationen für Sicherheitsaufrufe

Wenn rollenbasierte Sicherheit verwendet wird, kann das Kontextobjekt für Sicherheitsaufrufe verwendet werden, um auf Sicherheitsinformationen zum aktuellen Aufruf zu zugreifen.

Die folgenden Auflistungen von Eigenschaften sind über das Kontextobjekt für Sicherheitsaufrufe verfügbar:

-   [SecurityCallContext-Sammlung](#securitycallcontext-collection)
-   [SecurityCallers-Auflistung](#securitycallers-collection)
-   [SecurityIdentity-Sammlung](#securityidentity-collection)
-   [Zugehörige Themen](#related-topics)

## <a name="securitycallcontext-collection"></a>SecurityCallContext-Sammlung



| Eigenschaft                          | Beschreibung                                                                                                                            |
|-----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| NumCallers<br/>             | Die Anzahl der Aufrufer in der Aufrufkette.<br/>                                                                                |
| MinAuthenticationLevel<br/> | Die am wenigsten sichere Authentifizierungsebene aller Aufrufer in der Kette.<br/>                                                          |
| Anrufer<br/>                | Informationen zur Identität von Upstreamaufrufern in Form einer [**SecurityCallers-Auflistung.**](securitycallers.md)<br/> |
| DirectCaller<br/>           | Der Aufrufer, der das Objekt direkt aufgerufen hat (ohne intervening-Aufrufer). <br/>                                                  |
| OriginalCaller<br/>         | Der Aufrufer, der die Kette der Aufrufe an das -Objekt ursprünglich erstellt hat. <br/>                                                               |



 

Weitere Informationen zur Verwendung dieser Sammlung finden Visual Basic Entwickler von Microsoft in der [**SecurityCallContext-Klasse.**](securitycallcontext.md) C- und C++-Entwickler sollten auf [**ISecurityCallContext verweisen.**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext)

## <a name="securitycallers-collection"></a>SecurityCallers-Auflistung

Die [**SecurityCallers-Auflistung**](securitycallers.md) stellt Aufrufer dar, die mit einem Index zwischen 0 und 1 kleiner als NumCallers (einschließlich) abgerufen werden können. Jeder Aufrufer wird durch ein [**SecurityIdentity-Objekt**](securityidentity.md) dargestellt.

Weitere Informationen zu dieser Sammlung finden Visual Basic die [**SecurityCallers-Klasse.**](securitycallers.md) C- und C++-Entwickler sollten sich auf [**ISecurityCallersColl beziehen.**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll)

## <a name="securityidentity-collection"></a>SecurityIdentity-Sammlung



| Eigenschaft                         | Beschreibung                                                                                                                                                          |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SID<br/>                   | Die Sicherheits-ID für den Aufrufer.<br/>                                                                                                                   |
| AccountName<br/>           | Der Kontoname des Aufrufers.<br/>                                                                                                                           |
| Authenticationservice<br/> | Der verwendete Authentifizierungsdienst, z. B. NTLMSSP, Kerberos oder SSL.<br/>                                                                                       |
| Authenticationlevel<br/>   | Die verwendete Authentifizierungsebene, die den Umfang des Schutzes darstellt, der bei der Kommunikation mit dem -Objekt verwendet wird.<br/>                                         |
| ImpersonationLevel<br/>    | Die Ebene des Identitätswechsels, die vom Client festgelegt wurde, wenn ein Identitätswechsel verwendet wurde. Diese Ebene gibt die Autorität an, die dem Server vom Client erteilt wird. <br/> |



 

Weitere Informationen zu dieser Sammlung finden Visual Basic die [**SecurityIdentity-Klasse.**](securityidentity.md) C- und C++-Entwickler sollten auf [**ISecurityIdentityColl verweisen.**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Überprüfen der Rollenmitgliedschaft](checking-role-membership.md)
</dt> <dt>

[Bestimmen, ob Role-Based Sicherheit aktiviert ist](determining-whether-role-based-security-is-enabled.md)
</dt> <dt>

[Programmgesteuerte Komponentensicherheit](programmatic-component-security.md)
</dt> </dl>

 

 




