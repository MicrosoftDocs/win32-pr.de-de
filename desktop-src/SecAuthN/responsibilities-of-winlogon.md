---
description: Listet und erläutert die Zuständigkeiten von Winlogon.
ms.assetid: 5aef4164-11bd-4acc-b851-de982e35d2b5
title: Zuständigkeiten von Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7842df1d4194dc7086f658a13f6725af8fa0d88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959640"
---
# <a name="responsibilities-of-winlogon"></a>Zuständigkeiten von Winlogon

[*Winlogon*](../secgloss/w-gly.md) besteht aus den folgenden Zuständigkeiten:

-   Fenster Station und Desktop Schutz

    Mit Winlogon wird der Schutz der Fenster Station und der entsprechenden Desktops festgelegt, um sicherzustellen, dass jeder ordnungsgemäß verfügbar ist. Im Allgemeinen bedeutet dies, dass das lokale System Vollzugriff auf diese Objekte hat und dass ein interaktiv angemeldeter Benutzer über Lesezugriff auf das Fenster Station-Objekt und den vollständigen Zugriff auf das Anwendungs Desktop Objekt verfügt.

-   SAS-Standard Erkennung

    Winlogon verfügt über spezielle Hooks für den User32-Server, mit denen er STRG + ALT + ENTF-SAS-Ereignisse ( [*Secure Attention Sequence*](../secgloss/s-gly.md) ) überwachen kann. Mit Winlogon werden diese SAS-Ereignis Informationen für Ginas zur Verwendung als SAS oder als Teil ihrer SAS verfügbar gemacht. Im Allgemeinen sollte Ginas SASs selbst überwachen. Allerdings sollte jede [*Gina*](../secgloss/g-gly.md) mit der Standard-SAS (STRG + ALT + ENTF) als einer der von ihr erkannten SASs die Unterstützung für die Windows-Anmeldung verwenden, die zu diesem Zweck bereitgestellt wird.

-   SAS-Routine Verteilung

    Wenn Winlogon ein SAS-Ereignis findet oder eine SAS von der Gina an Winlogon übermittelt wird, wird der Status von Winlogon entsprechend festgelegt, und die Änderungen werden auf den Desktop der Windows-Anmeldung festgelegt, und eine der SAS-Verarbeitungsfunktionen der Gina wird aufgerufen.

-   Laden von Benutzerprofilen

    Wenn sich Benutzer anmelden, werden Ihre Benutzerprofile in die Registrierung geladen. Auf diese Weise können die Benutzer Prozesse den speziellen Registrierungsschlüssel HKEY \_ Current \_ User verwenden. Winlogon führt dies nach einer erfolgreichen Anmeldung, aber vor der Aktivierung der Shell für den neu angemeldeten Benutzer automatisch durch.

-   Zuweisung der Sicherheit zur Benutzershell

    Wenn sich ein Benutzer anmeldet, ist die Gina für das Erstellen eines oder mehrerer anfänglicher Prozesse für diesen Benutzer verantwortlich. Winlogon bietet eine Unterstützungsfunktion für die Gina, um die Sicherheit des neu angemeldeten Benutzers auf diese Prozesse anzuwenden. Die bevorzugte Methode hierfür ist jedoch, dass die Gina die Windows-Funktion " [**deateprocessasuser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)" aufruft und das System den Dienst bereitstellen kann.

-   Bildschirmschoner-Steuerelement

    Winlogon überwacht die Tastatur-und Maus Aktivität, um zu bestimmen, wann Bildschirmschoner aktiviert werden sollen. Nachdem der Bildschirmschoner aktiviert ist, überwacht Winlogon weiterhin die Tastatur-und Maus Aktivität, um zu bestimmen, wann der Bildschirmschoner beendet werden soll. Wenn der Bildschirmschoner als sicher markiert ist, wird die Arbeitsstation von Winlogon als gesperrt behandelt. Wenn eine Maus-oder Tastatur Aktivität vorliegt, ruft Winlogon die [**wlxdisplaylockednotice**](/windows/desktop/api/Winwlx/nf-winwlx-wlxdisplaylockednotice) -Funktion des Gina-und gesperrten Arbeitsstations Verhaltens auf. Wenn der Bildschirmschoner nicht sicher ist, beendet jede Tastatur-oder Maus Aktivität den Bildschirmschoner ohne Benachrichtigung an Gina.

-   Unterstützung mehrerer Netzwerkanbieter

    Mehrere Netzwerke, die auf einem Windows-System installiert sind, können in den Authentifizierungsprozess und in Vorgänge zur Kenn Wort Aktualisierung eingeschlossen werden. Durch diese Einbindung können zusätzliche Netzwerke Identifikations-und Authentifizierungsinformationen alle gleichzeitig während der normalen Anmeldung mithilfe des sicheren Desktops von Winlogon sammeln. Einige der Parameter, die für die für Ginas verfügbaren Winlogon-Dienste erforderlich sind, unterstützen diese zusätzlichen Netzwerkanbieter explizit.

 

 
