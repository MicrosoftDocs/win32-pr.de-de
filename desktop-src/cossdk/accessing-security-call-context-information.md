---
description: Wenn die rollenbasierte Sicherheit verwendet wird, kann das Kontext Objekt für den Sicherheits Rückruf verwendet werden, um auf Sicherheitsinformationen zum aktuellen-Befehl zuzugreifen.
ms.assetid: 9fc0a9e5-934c-4510-8fbb-1fb2817aa0ea
title: Aufrufen von Kontextinformationen für den Sicherheitskontext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6d7e5160c766783b6d43822571d624e0a595c9e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214222"
---
# <a name="accessing-security-call-context-information"></a>Aufrufen von Kontextinformationen für den Sicherheitskontext

Wenn die rollenbasierte Sicherheit verwendet wird, kann das Kontext Objekt für den Sicherheits Rückruf verwendet werden, um auf Sicherheitsinformationen zum aktuellen-Befehl zuzugreifen.

Die folgenden Auflistungen von Eigenschaften sind im Kontext Objekt für den Sicherheits Rückruf verfügbar:

-   [SecurityCallContext-Auflistung](#securitycallcontext-collection)
-   [SecurityCaller-Sammlung](#securitycallers-collection)
-   [SecurityIdentity-Sammlung](#securityidentity-collection)
-   [Zugehörige Themen](#related-topics)

## <a name="securitycallcontext-collection"></a>SecurityCallContext-Auflistung



| Eigenschaft                          | BESCHREIBUNG                                                                                                                            |
|-----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Numaufrufer<br/>             | Die Anzahl der Aufrufer in der Aufruf Kette.<br/>                                                                                |
| MinAuthenticationLevel<br/> | Die am wenigsten sichere Authentifizierungs Ebene aller Aufrufer in der Kette.<br/>                                                          |
| Anrufer<br/>                | Informationen zur Identität von upstreamaufrufern in Form einer [**SecurityCaller**](securitycallers.md) -Auflistung.<br/> |
| DirectCaller<br/>           | Der Aufrufer, der das Objekt direkt aufgerufen hat (ohne dazwischen liegende Aufrufer). <br/>                                                  |
| OriginalCaller<br/>         | Der Aufrufer, der die Kette der Aufrufe des-Objekts ausgelöst hat. <br/>                                                               |



 

Um weitere Informationen zur Verwendung dieser Sammlung zu erhalten, sollte Microsoft Visual Basic-Entwicklern die [**SecurityCallContext**](securitycallcontext.md) -Klasse angezeigt werden. C-und C++-Entwickler sollten auf [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext)verweisen.

## <a name="securitycallers-collection"></a>SecurityCaller-Sammlung

Die [**SecurityCaller**](securitycallers.md) -Auflistung stellt Aufrufer dar, die mithilfe eines Indexes zwischen 0 und 1 weniger als numcaller, einschließlich, abgerufen werden können. Jeder Aufrufer wird durch ein [**SecurityIdentity**](securityidentity.md) -Objekt dargestellt.

Weitere Informationen zu dieser Sammlung finden Visual Basic Entwicklern die [**SecurityCaller**](securitycallers.md) -Klasse. C-und C++-Entwickler sollten auf [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll)verweisen.

## <a name="securityidentity-collection"></a>SecurityIdentity-Sammlung



| Eigenschaft                         | BESCHREIBUNG                                                                                                                                                          |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SID<br/>                   | Die Sicherheits-ID für den Aufrufer.<br/>                                                                                                                   |
| AccountName<br/>           | Der Kontoname des Aufrufers.<br/>                                                                                                                           |
| AuthenticationService<br/> | Der verwendete Authentifizierungsdienst, z. b. NTLMSSP, Kerberos oder SSL.<br/>                                                                                       |
| AuthenticationLevel<br/>   | Die verwendete Authentifizierungs Ebene, die die für die Kommunikation mit dem-Objekt verwendete Menge an Schutz darstellt.<br/>                                         |
| ImpersonationLevel<br/>    | Die vom Client festgelegte Ebene des Identitäts Wechsels, wenn der Identitätswechsel verwendet wurde. Diese Ebene gibt die Menge an Autorität an, die vom Client an den Server übergeben wird. <br/> |



 

Weitere Informationen zu dieser Sammlung finden Visual Basic Entwicklern die [**SecurityIdentity**](securityidentity.md) -Klasse. C-und C++-Entwickler sollten sich auf [**isecurityidentitycoll**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll)beziehen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Überprüfen der Rollen Mitgliedschaft](checking-role-membership.md)
</dt> <dt>

[Bestimmen, ob Role-Based Sicherheit aktiviert ist](determining-whether-role-based-security-is-enabled.md)
</dt> <dt>

[Sicherheit für programmgesteuerte Komponenten](programmatic-component-security.md)
</dt> </dl>

 

 




