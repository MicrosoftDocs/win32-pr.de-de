---
description: In diesem Thema werden Tipps zur Problembehandlung für die Verwendung der Webauthentifizierungsbroker-APIs für Ihre Webseiten beschrieben.
ms.assetid: 25A024AA-9A70-40A5-BF5E-452FD148D0D2
title: Webauthentifizierungsprobleme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c722aefa35849485d2c8958e17c654b5bb6477479ac1765e76e648fe15f9826
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785868"
---
# <a name="web-authentication-problems"></a>Webauthentifizierungsprobleme

In diesem Thema werden Tipps zur Problembehandlung für die Verwendung der Webauthentifizierungsbroker-APIs für Ihre Webseiten beschrieben.

-   [Betriebsprotokolle](#operational-logs)
-   [Verwenden von Fiddler mit dem Webauthentifizierungsbroker](#using-fiddler-with-web-authentication-broker)
-   [Zugehörige Themen](#related-topics)

## <a name="operational-logs"></a>Betriebsprotokolle

Häufig können Sie anhand der Betriebsprotokolle ermitteln, was nicht funktioniert. Es gibt einen dedizierten Ereignisprotokollkanal Microsoft-Windows-WebAuth Operational, mit dem Websiteentwickler verstehen können, wie ihre Webseiten vom \\ Webauthentifizierungsbroker verarbeitet werden. Starten Sie zum Aktivieren dieses eventvwr.exe, und aktivieren Sie das Betriebsprotokoll unter Anwendung und Dienste \\ Microsoft \\ Windows \\ WebAuth. Außerdem fügt der Webauthentifizierungsbroker eine eindeutige Zeichenfolge an die Benutzer-Agent-Zeichenfolge an, um sich auf dem Webserver zu identifizieren. Die Zeichenfolge lautet „MSAuthHost/1.0“. Beachten Sie, dass sich die Versionsnummer ändern kann. Verlassen Sie sich also in Ihrem Code nicht auf diese Versionsnummer. Ein Beispiel für die vollständige Benutzer-Agent-Zeichenfolge lautet wie folgt:

`User-Agent: Mozilla/5.0 (compatible; MSIE 10.0; Windows NT 6.2; Win64; x64; Trident/6.0; MSAuthHost/1.0)`

Beispiel für die Verwendung von Betriebsprotokollen

1.  Aktivieren von Betriebsprotokollen
2.  Ausführen einer Contoso-Anwendung für soziale Netzwerke![Ereignisanzeige mit webauth-Betriebsprotokollen](images/wab-figure15.png)
3.  Die generierten Protokolleinträge können verwendet werden, um das Verhalten des Webauthentifizierungsbrokers ausführlicher zu verstehen. In diesem Fall können sie Folgendes enthalten:
    -   Navigation – Starten: Protokolliert, wann AuthHost gestartet wird, und enthält Informationen zu den Start- und End-URLs.
    -   ![Veranschaulicht die Details von „Navigation – Starten“"](images/wab-figure16.png)
    -   Navigation abgeschlossen: Protokolliert den Abschluss des Ladevorgangs einer Webseite.
    -   META-Tag: Protokolliert, wann ein META-Tag auftritt (einschließlich Details).
    -   Navigation – Beenden: Die Navigation wurde vom Benutzer beendet.
    -   Navigationsfehler: AuthHost ermittelt einen Navigationsfehler bei einer URL, einschließlich HttpStatusCode.
    -   Navigationsende: End-URL liegt vor.

## <a name="using-fiddler-with-web-authentication-broker"></a>Verwenden von Fiddler mit dem Webauthentifizierungsbroker

Der Fiddler-Webdebugger kann mit Windows 8 verwendet werden.

1.  Da AuthHost in einem eigenen App-Container ausgeführt wird, um Funktionen für private Netzwerke zu ermöglichen, müssen Sie einen Registrierungsschlüssel festlegen: Windows Registry Editor Version 5.00

    **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** Image File Execution \\ **Options** \\ **authhost.exe** \\ **EnablePrivateNetwork** = 00000001<dl> <dt>

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

Weitere Informationen finden Sie im [Blog zur Verwendung des Fiddler-Webdebuggers mit Windows Store Apps.](/archive/blogs/fiddler/revisiting-fiddler-and-win8-immersive-applications)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Überlegungen für die Webseitenentwicklung](considerations-for-the-web-page-development.md)
</dt> <dt>

[Häufig gestellte Fragen zum Webauthentifizierungsbroker](faq-for-web-authentication-broker.yml)
</dt> <dt>

[Beispiel-App für das Webauthentifizierungsbroker-SDK](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web?view=winrt-19041&preserve-view=true)
</dt> </dl>

 

 
