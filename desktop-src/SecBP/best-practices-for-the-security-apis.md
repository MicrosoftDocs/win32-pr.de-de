---
description: Vorschläge für Anwendungssicherheitsbewertungen für die App-Entwicklung von Windows Sicherheitssoftware und sichere Softwareentwicklung, einschließlich Anwendungssicherheitstests.
ms.assetid: bb0ddae2-f559-4785-97c7-182fc204fa60
title: Bewährte Methoden für die Sicherheits-APIs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 934bf52d99456d599f91ec23c6e5472bb4e130565cf1acb56763f29f6396c0b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622880"
---
# <a name="best-practices-for-the-security-apis"></a>Bewährte Methoden für die Sicherheits-APIs

Um die Entwicklung sicherer Software zu unterstützen, wird empfohlen, bei der Entwicklung von Anwendungen die folgenden bewährten Methoden zu verwenden. Weitere Informationen finden Sie unter [Security Developer Center.](https://msdn.microsoft.com/security/default.aspx)

## <a name="security-development-life-cycle"></a>Lebenszyklus der Sicherheitsentwicklung

Der [Sicherheitsentwicklungslebenszyklus (Security Development Life Cycle,](/previous-versions/ms995349(v=msdn.10)) SDL) ist ein Prozess, der eine Reihe von sicherheitsorientierten Aktivitäten und Ergebnisse für jede Phase der Softwareentwicklung anpasst. Zu diesen Aktivitäten und Bereitstellungen gehören:

-   Entwickeln von Bedrohungsmodellen
-   Verwenden von Codescantools
-   Durchführen von Codeüberprüfungen und Sicherheitstests

Weitere Informationen zum SDL finden Sie im [SDL-Blog.](https://blogs.msdn.com/sdl/archive/2007/04/26/welcome-to-the-sdl-blog.aspx)

## <a name="threat-models"></a>Bedrohungsmodelle

Die Durchführung einer Bedrohungsmodellanalyse kann Ihnen helfen, potenzielle Angriffspunkte in Ihrem Code zu ermitteln. Weitere Informationen zur Analyse des Bedrohungsmodells finden Sie unter Msi, Michael und LeBlanc, David \[ 2003 \] , Writing Secure *Code*, 2d ed., ISBN 0-7356-1722-8, Microsoft Press, Redmond, Washington. (Diese Ressource ist in einigen Sprachen und Ländern möglicherweise nicht verfügbar.)

## <a name="service-packs-and-security-updates"></a>Service Packs und Sicherheitsupdates

Build- und Testumgebungen sollten die gleichen Service Packs und Sicherheitsupdates der Zielbenutzerbasis widerspiegeln. Es wird empfohlen, die neuesten Service Packs und Sicherheitsupdates für jede Microsoft-Plattform oder -Anwendung zu installieren, die Teil Ihrer Build- und Testumgebung ist, und ihre Benutzer zu bitten, dies für die fertige Anwendungsumgebung zu tun. Weitere Informationen zu Service Packs und Sicherheitsupdates finden Sie unter [Microsoft Windows Update](https://www.update.microsoft.com/microsoftupdate/v6/vistadefault.aspx?ln=en-us) und Microsoft [Security](https://www.microsoft.com/security).

## <a name="authorization"></a>Autorisierung

Sie sollten Anwendungen erstellen, die die geringstmöglichen Berechtigungen erfordern. Durch die Verwendung der geringstmöglichen Rechte wird das Risiko verringert, dass Ihr Computersystem durch schädlichen Code kompromittieren wird. Weitere Informationen zum Ausführen von Code auf der geringstmöglichen Berechtigungsebene finden Sie unter [Ausführen mit speziellen Berechtigungen.](running-with-special-privileges.md)

## <a name="more-information"></a>Weitere Informationen

Weitere Informationen zu bewährten Methoden finden Sie in den folgenden Themen.



| Thema                                                                                                                        | Beschreibung                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Ausführen mit speziellen Berechtigungen](running-with-special-privileges.md)<br/>                                            | Erläutert die Sicherheitsauswirkungen von Berechtigungen.<br/>                                                                                                                                  |
| [Vermeiden von Pufferüberläufen](avoiding-buffer-overruns.md)<br/>                                                          | Stellt Informationen zum Vermeiden von Pufferüberläufen bereit.<br/>                                                                                                                            |
| [Ablaufsteuerungsschutz (CFG, Control Flow Guard) ](control-flow-guard.md)<br/>                                                                | Erläutert Sicherheitsrisiken durch Speicherbeschädigung.<br/>                                                                                                                                    |
| [Erstellen einer DACL](creating-a-dacl.md)<br/>                                                                            | Zeigt, wie sie eine DACL (Discretionary Access Control List) mithilfe der [Sicherheitsdeskriptordefinitionssprache (SECURITY Descriptor Definition Language,](/windows/desktop/SecAuthZ/security-descriptor-definition-language) SDDL) erstellen.<br/> |
| [Behandeln von Kennwörtern](handling-passwords.md)<br/>                                                                      | Erläutert die Sicherheitsauswirkungen der Verwendung von Kennwörtern.<br/>                                                                                                                             |
| [Optimieren der MSDN Library-Suche](how-to-optimize-your-msdn-library-search.md)<br/>                          | Erläutert Optionen zum Durchsuchen von Security SDK-Inhalten in der MSDN Library.<br/>                                                                                                           |
| [Erweiterbarkeit dynamischer Access Control Entwickler](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap)<br/> | Grundlegende Ausrichtung auf einige der Entwicklererweiterbarkeitspunkte für die neuen Dynamic Access Control-Lösungen.<br/>                                                                   |



 

 

