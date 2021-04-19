---
description: Vorschläge für Anwendungs Sicherheitsbewertungen für die APP-Entwicklung von Windows-Sicherheitssoftware und sichere Softwareentwicklung, einschließlich Anwendungs Sicherheitstests.
ms.assetid: bb0ddae2-f559-4785-97c7-182fc204fa60
title: Bewährte Methoden für die Sicherheits-APIs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa821cfbaa9874d17559ad0e81f636fbaddd14f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363365"
---
# <a name="best-practices-for-the-security-apis"></a>Bewährte Methoden für die Sicherheits-APIs

Zur Unterstützung der Entwicklung sicherer Software empfiehlt es sich, beim Entwickeln von Anwendungen die folgenden bewährten Methoden zu verwenden. Weitere Informationen finden Sie im [Security Developer Center](https://msdn.microsoft.com/security/default.aspx).

## <a name="security-development-life-cycle"></a>Lebenszyklus der Sicherheitsentwicklung

Beim [Security Development](/previous-versions/ms995349(v=msdn.10)) Lifecycle (SDL) handelt es sich um einen Prozess, der eine Reihe von sicherheitsorientierten Aktivitäten und Lieferleistungen für jede Phase der Softwareentwicklung anpasst. Folgende Aktivitäten und Ergebnisse sind verfügbar:

-   Entwickeln von Bedrohungs Modellen
-   Verwenden von Code Scan Tools
-   Durchführen von Code Überprüfungen und Sicherheitstests

Weitere Informationen zu SDL finden Sie im SDL- [Blog](https://blogs.msdn.com/sdl/archive/2007/04/26/welcome-to-the-sdl-blog.aspx).

## <a name="threat-models"></a>Bedrohungs Modelle

Das Durchführen einer Bedrohungs Modellanalyse kann Ihnen helfen, potenzielle Angriffspunkte in Ihrem Code zu ermitteln. Weitere Informationen zur Bedrohungs Modellanalyse finden Sie unter Howard, Michael und LeBlanc, David \[ 2003 \] , Schreiben von *sicherem Code*, 2D Ed., ISBN 0-7356-1722-8, Microsoft Press, Redmond, Washington. (Diese Ressource ist möglicherweise nicht in einigen Sprachen und Ländern verfügbar.)

## <a name="service-packs-and-security-updates"></a>Service Packs und Sicherheits Updates

Build-und Testumgebungen sollten die gleichen Ebenen von Service Packs und Sicherheitsupdates der Ziel Benutzerbasis widerspiegeln. Es wird empfohlen, dass Sie die neuesten Service Packs und Sicherheitsupdates für alle Microsoft-Plattformen oder-Anwendungen installieren, die Teil ihrer Build-und Testumgebung sind, und die Benutzer dazu auffordern, die gleichen Schritte für die fertige Anwendungsumgebung durchzuführen. Weitere Informationen zu Service Packs und Sicherheitsupdates finden Sie unter [Microsoft Windows Update](https://www.update.microsoft.com/microsoftupdate/v6/vistadefault.aspx?ln=en-us) und [Microsoft-Sicherheit](https://www.microsoft.com/security).

## <a name="authorization"></a>Autorisierung

Sie sollten Anwendungen erstellen, die die geringstmöglichen Berechtigungen erfordern. Wenn Sie die geringstmöglichen Berechtigungen verwenden, verringern Sie das Risiko, dass bösartiger Code Ihr Computersystem beeinträchtigt. Weitere Informationen zum Ausführen von Code mit geringstmöglichen Berechtigungsstufen finden Sie unter [Ausführen mit speziellen Berechtigungen](running-with-special-privileges.md).

## <a name="more-information"></a>Weitere Informationen

Weitere Informationen zu bewährten Methoden finden Sie in den folgenden Themen.



| Thema                                                                                                                        | BESCHREIBUNG                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Ausführen mit besonderen Berechtigungen](running-with-special-privileges.md)<br/>                                            | Erläutert Sicherheitsauswirkungen von Berechtigungen.<br/>                                                                                                                                  |
| [Vermeiden von Pufferüberläufen](avoiding-buffer-overruns.md)<br/>                                                          | Bietet Informationen zum Vermeiden von Pufferüberläufen.<br/>                                                                                                                            |
| [Ablaufsteuerungsschutz (CFG, Control Flow Guard) ](control-flow-guard.md)<br/>                                                                | Erläutert Sicherheitsrisiken bei der Speicher Beschädigung.<br/>                                                                                                                                    |
| [Erstellen einer DACL](creating-a-dacl.md)<br/>                                                                            | Zeigt, wie eine freigegebene Zugriffs Steuerungs Liste (DACL) mithilfe der [Sicherheits Deskriptor-Definitions Sprache](/windows/desktop/SecAuthZ/security-descriptor-definition-language) (SDDL) erstellt wird.<br/> |
| [Behandeln von Kenn Wörtern](handling-passwords.md)<br/>                                                                      | Erläutert die Auswirkungen der Verwendung von Kenn Wörtern auf die Sicherheit.<br/>                                                                                                                             |
| [Optimieren der MSDN Library-Suche](how-to-optimize-your-msdn-library-search.md)<br/>                          | Erläutert Optionen zum Durchsuchen von Sicherheits-SDK-Inhalten in der MSDN Library.<br/>                                                                                                           |
| [Dynamische Access Control Developer-Erweiterbarkeit](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap)<br/> | Grundlegende Ausrichtung auf einige Entwickler Erweiterbarkeits Punkte für die neuen dynamischen Access Control Lösungen.<br/>                                                                   |



 

 

