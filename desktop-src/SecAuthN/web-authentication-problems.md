---
description: In diesem Thema werden Tipps zur Problembehandlung für die Verwendung der Webauthentifizierungs Broker-APIs für Ihre Webseiten beschrieben.
ms.assetid: 25A024AA-9A70-40A5-BF5E-452FD148D0D2
title: Webauthentifizierungsprobleme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc4611461effd9cbc5546059e71fc8ca3f1f0be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104571199"
---
# <a name="web-authentication-problems"></a>Webauthentifizierungsprobleme

In diesem Thema werden Tipps zur Problembehandlung für die Verwendung der Webauthentifizierungs Broker-APIs für Ihre Webseiten beschrieben.

-   [Betriebs Protokolle](#operational-logs)
-   [Verwenden von "fddler" mit dem Webauthentifizierungs Broker](#using-fiddler-with-web-authentication-broker)
-   [Zugehörige Themen](#related-topics)

## <a name="operational-logs"></a>Betriebsprotokolle

Häufig können Sie anhand der Betriebsprotokolle ermitteln, was nicht funktioniert. Es gibt einen dedizierten Ereignisprotokoll Kanal Microsoft-Windows-webauth \\ Operational, mit dem Website Entwickler verstehen können, wie Ihre Webseiten vom Webauthentifizierungs Broker verarbeitet werden. Um dies zu aktivieren, starten Sie eventvwr.exe, und aktivieren Sie das Betriebsprotokoll unter den Anwendungs-und Dienstleistungen von \\ Microsoft \\ Windows \\ webauth. Außerdem fügt der Webauthentifizierungs Broker eine eindeutige Zeichenfolge an die Benutzer-Agent-Zeichenfolge an, um sich selbst auf dem Webserver zu identifizieren. Die Zeichenfolge lautet „MSAuthHost/1.0“. Beachten Sie, dass sich die Versionsnummer ändern kann. Verlassen Sie sich also in Ihrem Code nicht auf diese Versionsnummer. Ein Beispiel für die vollständige Benutzer-Agent-Zeichenfolge sieht wie folgt aus:

`User-Agent: Mozilla/5.0 (compatible; MSIE 10.0; Windows NT 6.2; Win64; x64; Trident/6.0; MSAuthHost/1.0)`

Beispiel für die Verwendung von Betriebs Protokollen

1.  Aktivieren von Betriebsprotokollen
2.  Ausführen der Anwendung "" für soziale Netzwerke![Ereignisanzeige mit webauth-Betriebsprotokollen](images/wab-figure15.png)
3.  Die generierten Protokolleinträge können verwendet werden, um das Verhalten des Webauthentifizierungs Brokers ausführlicher nachzuvollziehen. In diesem Fall können sie Folgendes enthalten:
    -   Navigation – Starten: Protokolliert, wann AuthHost gestartet wird, und enthält Informationen zu den Start- und End-URLs.
    -   ![Veranschaulicht die Details von „Navigation – Starten“"](images/wab-figure16.png)
    -   Navigation abgeschlossen: Protokolliert den Abschluss des Ladevorgangs einer Webseite.
    -   META-Tag: Protokolliert, wann ein META-Tag auftritt (einschließlich Details).
    -   Navigation – Beenden: Die Navigation wurde vom Benutzer beendet.
    -   Navigationsfehler: AuthHost ermittelt einen Navigationsfehler bei einer URL, einschließlich HttpStatusCode.
    -   Navigationsende: End-URL liegt vor.

## <a name="using-fiddler-with-web-authentication-broker"></a>Verwenden von "fddler" mit dem Webauthentifizierungs Broker

Der webdebugger von "fddler" kann mit Windows 8-Apps verwendet werden.

1.  Da AuthHost in einem eigenen App-Container ausgeführt wird, um Funktionen für private Netzwerke zu ermöglichen, müssen Sie einen Registrierungsschlüssel festlegen: Windows Registry Editor Version 5.00

    **HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Image File Execution Options** \\ **authhost.exe** \\ **enableprivatenetwork** = 00000001<dl> <dt>

                     Data type
</dt> <dd>                     DWORD</dd> </dl>

2.  Fügen Sie eine Regel für AuthHost hinzu, da darüber ausgehender Datenverkehr generiert wird.
    ```cmd
    CheckNetIsolation.exe LoopbackExempt -a -n=microsoft.windows.authhost.a.p_8wekyb3d8bbwe
    CheckNetIsolation.exe LoopbackExempt -a -n=microsoft.windows.authhost.sso.p_8wekyb3d8bbwe
    CheckNetIsolation.exe LoopbackExempt -a -n=microsoft.windows.authhost.sso.c_8wekyb3d8bbwe
    D:\Windows\System32>CheckNetIsolation.exe LoopbackExempt -s
    List Loopback Exempted AppContainers
    [1] -----------------------------------------------------------------
        Name: microsoft.windows.authhost.sso.c_8wekyb3d8bbwe
        SID:  S-1-15-2-1973105767-3975693666-32999980-3747492175-1074076486-3102532000-500629349
    [2] -----------------------------------------------------------------
        Name: microsoft.windows.authhost.sso.p_8wekyb3d8bbwe
        SID:  S-1-15-2-166260-4150837609-3669066492-3071230600-3743290616-3683681078-2492089544
    [3] -----------------------------------------------------------------
        Name: microsoft.windows.authhost.a.p_8wekyb3d8bbwe
        SID:  S-1-15-2-3506084497-1208594716-3384433646-2514033508-1838198150-1980605558-3480344935
    ```

    

3.  Fügen Sie Fiddler eine Firewallregel für eingehenden Datenverkehr hinzu.

Weitere Informationen finden Sie unter [Verwenden des webdebuggers für Windows Store-Apps mit dem webdebugger für Windows Store](/archive/blogs/fiddler/revisiting-fiddler-and-win8-immersive-applications).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Überlegungen für die Webseitenentwicklung](considerations-for-the-web-page-development.md)
</dt> <dt>

[Häufig gestellte Fragen zum Webauthentifizierungs Broker](faq-for-web-authentication-broker.md)
</dt> <dt>

[Beispiel-App für das Web Authentication Broker SDK](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web?view=winrt-19041)
</dt> </dl>

 

 
