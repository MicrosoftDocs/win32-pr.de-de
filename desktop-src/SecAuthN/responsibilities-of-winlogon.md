---
description: Listet die Zuständigkeiten von Winlogon auf und erläutert sie.
ms.assetid: 5aef4164-11bd-4acc-b851-de982e35d2b5
title: Zuständigkeiten von Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6561bea11c48eb474c0ff56c5c0aa5ebfa0c22d9d6689aa55a6a208bbbc683e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919028"
---
# <a name="responsibilities-of-winlogon"></a>Zuständigkeiten von Winlogon

[*Winlogon*](../secgloss/w-gly.md) hat die folgenden Aufgaben:

-   Fensterstation und Desktopschutz

    Winlogon legt den Schutz der Fensterstation und der entsprechenden Desktops fest, um sicherzustellen, dass auf diese ordnungsgemäß zugegriffen werden kann. Im Allgemeinen bedeutet dies, dass das lokale System vollzugriff auf diese Objekte hat und dass ein interaktiv angemeldeter Benutzer Lesezugriff auf das Fensterstationsobjekt und Vollzugriff auf das Desktopobjekt der Anwendung hat.

-   Sas-Standarderkennung

    Winlogon verfügt über spezielle Hooks in den User32-Server, die es ihm ermöglichen, SAS-Ereignisse [*(Secure Attention Sequence)*](../secgloss/s-gly.md) mit STRG+ALT+ENTF zu überwachen. Winlogon stellt diese SAS-Ereignisinformationen FÜR SAS-Aas zur Verfügung, die sie als SAS oder als Teil ihrer SAS verwenden können. Im Allgemeinen sollten EIGENSTÄNDIGEAs SAS eigenständig überwachen. Alle [*GINA-Werte,*](../secgloss/g-gly.md) die die Standard-SAS STRG+ALT+ENTF als eine der erkannten SASs haben, sollten jedoch die winlogon-Unterstützung verwenden, die für diesen Zweck bereitgestellt wird.

-   SAS-Routinedisponierung

    Wenn Winlogon auf ein SAS-Ereignis trifft oder eine SAS von der GINA an Winlogon übermittelt wird, legt Winlogon den Zustand entsprechend fest, ändert sich am Winlogon-Desktop und ruft eine der SAS-Verarbeitungsfunktionen der GINA auf.

-   Laden von Benutzerprofilen

    Wenn sich Benutzer anmelden, werden ihre Benutzerprofile in die Registrierung geladen. Auf diese Weise können die Prozesse des Benutzers den speziellen Registrierungsschlüssel HKEY \_ CURRENT \_ USER verwenden. Winlogon führt dies automatisch nach einer erfolgreichen Anmeldung, aber vor der Aktivierung der Shell für den neu angemeldeten Benutzer durch.

-   Zuweisen der Sicherheit zur Benutzershell

    Wenn sich ein Benutzer anmeldet, ist die GINA dafür verantwortlich, einen oder mehrere anfängliche Prozesse für diesen Benutzer zu erstellen. Winlogon bietet eine Unterstützungsfunktion für die GINA, um die Sicherheit des neu angemeldeten Benutzers auf diese Prozesse anzuwenden. Die bevorzugte Methode hierfür ist jedoch, dass die GINA die Windows Funktion [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)aufruft und das System den Dienst bereitstellen lässt.

-   Bildschirmschoner-Steuerelement

    Winlogon überwacht die Tastatur- und Mausaktivität, um zu bestimmen, wann Bildschirmschoner aktiviert werden sollen. Nachdem der Bildschirmschoner aktiviert wurde, überwacht Winlogon weiterhin die Tastatur- und Mausaktivität, um zu bestimmen, wann der Bildschirmschoner beendet werden soll. Wenn der Bildschirmschoner als sicher markiert ist, behandelt Winlogon die Arbeitsstation als gesperrt. Wenn Maus- oder Tastaturaktivitäten vorhanden sind, ruft Winlogon die [**WlxDisplayLockedNotice-Funktion**](/windows/desktop/api/Winwlx/nf-winwlx-wlxdisplaylockednotice) der GINA auf, und das Verhalten der gesperrten Arbeitsstation wird fortgesetzt. Wenn der Bildschirmschoner nicht sicher ist, beendet jede Tastatur- oder Mausaktivität den Bildschirmschoner ohne Benachrichtigung an die GINA.

-   Unterstützung mehrerer Netzwerkanbieter

    Mehrere Netzwerke, die auf einem Windows System installiert sind, können in den Authentifizierungsprozess und Kennwortaktualisierungsvorgänge einbezogen werden. Durch diese Einbeziehung können zusätzliche Netzwerke während der normalen Anmeldung identifikations- und Authentifizierungsinformationen auf einmal erfassen, indem sie den sicheren Desktop von Winlogon verwenden. Einige der Parameter, die in den Winlogon-Diensten erforderlich sind, die für DIE WPA-Dienste verfügbar sind, unterstützen diese zusätzlichen Netzwerkanbieter explizit.

 

 
