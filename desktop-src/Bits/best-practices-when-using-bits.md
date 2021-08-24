---
title: Bewährte Methoden bei der Verwendung von BITS
description: Dieser Abschnitt enthält Informationen, die Sie beim Entwerfen einer Anwendung berücksichtigen sollten, die BITS verwendet.
ms.assetid: f4a09a80-2a85-4b59-b0fd-c23c128973f7
ms.topic: article
ms.date: 7/12/2019
ms.openlocfilehash: cbc11365cde74e092ae179c8b41562a16de9a6c36f0d85e51787a979c9332863
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702090"
---
# <a name="best-practices-when-using-bits"></a>Bewährte Methoden bei der Verwendung von BITS

Dieser Abschnitt enthält Informationen, die Sie beim Entwerfen einer Anwendung berücksichtigen sollten, die BITS verwendet.

## <a name="user-context-or-service-context"></a>Benutzerkontext oder Dienstkontext

BITS überträgt Dateien nur, wenn der Besitzer des Auftrags am Computer angemeldet ist (der Benutzer muss sich interaktiv angemeldet haben). BITS unterstützt den **RunAs-Befehl** nicht. Weitere Informationen finden Sie unter [Benutzer und Netzwerkverbindungen.](users-and-network-connections.md)

Wenn Sie den Kontext eines Benutzers für Ihre Anwendung nicht benötigen, sollten Sie stattdessen einen Dienst schreiben, der als LocalSystem, LocalService oder NetworkService ausgeführt wird. Diese Systemkonten sind immer angemeldet, sodass die Übertragung nicht von einem Benutzer abgemelgt wird. Wenn Sie jedoch beim Erstellen des Auftrags die Identität eines Benutzers übernehmen, gelten die Regeln für die interaktive Anmeldung. Weitere Informationen finden Sie unter [Dienstkonten und BITS](service-accounts-and-bits.md).

## <a name="jobs-are-persistent"></a>Aufträge sind persistent

Aufträge verbleiben in der Warteschlange, bis Sie die [**IBackgroundCopyJob::Complete-**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) oder [**IBackgroundCopyJob::Cancel-Methode**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) aufrufen. Die Dateien im Auftrag sind für den Benutzer erst verfügbar, wenn Sie **Abschließen aufrufen.** In der Regel  rufen Sie Complete auf, wenn der Status des  Auftrags **BG JOB STATE \_ \_ \_ TRANSFERD** ist, und Sie rufen Abbrechen auf, wenn sich der Auftrag im **Status BG JOB STATE TRANSIENT \_ \_ \_ \_ ERROR** oder **BG JOB STATE \_ \_ \_ ERROR** befindet und keinen Fortschritt mehr erzielen kann.

Wenn Sie die [**Complete-Methode**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) oder die [**Cancel-Methode**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) nicht innerhalb von 90 Tagen aufrufen (standardeinstellung [JobInactivityTimeout](group-policies.md) Gruppenrichtlinie), bricht der Dienst den Auftrag ab. Sie sollten immer die **Complete- oder** **Cancel-Methode** aufrufen und sich nicht auf die JobInactivityTimeout-Richtlinie verlassen, um Ihre Aufträge zu bereinigten. Aufträge, die in der Warteschlange übrig bleiben, können Benutzer daran hindern, andere Aufträge zu erstellen, wenn das Richtlinienlimit für MaxJobsPerUser oder MaxJobsPerMachine erreicht wird.

## <a name="when-to-use-foreground-or-background-priority"></a>Verwendung von Vordergrund- oder Hintergrundpriorität

Wenn der Auftrag nicht zeitkritisch ist oder der Benutzer aktiv wartet, sollten Sie immer eine Hintergrundpriorität verwenden. Es gibt jedoch Zeiten, in denen Sie möglicherweise von der Hintergrundpriorität zur Vordergrundpriorität wechseln möchten, z. B. wenn der Proxy oder Server den Content-Range-Header nicht unterstützt oder Antivirensoftware auf dem Client die Bereichsheaderanforderung entfernt. Der Wechsel zur Vordergrundpriorität funktioniert nur für Dateien, deren Dateigröße kleiner als 2 GB ist. Ein Beispiel finden Sie in der Implementierung für die [**IBackgroundCopyCallback::JobError-Methode.**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) Beachten Sie außerdem, dass der Auftrag fehlschlägt, wenn der Vordergrundauftrag dann aufgrund einer Netzwerkverbindung unterbrochen wird oder sich der Benutzer abmeldet, da BITS eine Bereichsanforderung sendet, um zu versuchen, die Übertragung von der Stelle, an der sie unterbrochen wurde, neu zu starten.

Ab Windows 8 sollten Sie Downloadaufträge mit **BITS \_ JOB PROPERTY DYNAMIC \_ \_ \_ CONTENT** und **BG JOB PRIORITY \_ \_ \_ FOREGROUND** konfigurieren, wenn Sie Server als Ziel verwenden, die die HTTP-Anforderungen für [BITS-Downloads nicht erfüllen.](http-requirements-for-bits-downloads.md) Beachten Sie, dass DIEs dazu führt, dass BITS den Download von Anfang an neu starten muss, wenn er unterbrochen wird (z. B. aufgrund von Konnektivitätsproblemen oder Systemneustart).

Informationen zu den verfügbaren Prioritäten und dazu, wie BITS die Prioritätsebene zum Planen von Aufträgen verwendet, finden Sie unter [**BG \_ JOB \_ PRIORITY**](/windows/desktop/api/Bits/ne-bits-bg_job_priority).

## <a name="transient-and-fatal-errors"></a>Vorübergehende und schwerwiegende Fehler

Einige Fehler können wiederhergestellt werden, andere nicht. Beispielsweise ist der Fehler "Server ist nicht verfügbar" ein wiederherstellbarer Fehler, und der Fehler "Zugriff verweigert" ist ein schwerwiegender Fehler. BITS versetzt wiederherstellbare Fehler in einen vorübergehenden Fehlerzustand und versucht den Auftrag nach einem angegebenen Intervall erneut. Wenn der Auftrag nicht weiterkommen kann, verschiebt BITS den Auftrag in einen schwerwiegenden Fehlerzustand. Verwenden Sie die [**Methoden IBackgroundCopyJob::SetMinimumRetryDelay**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay) und [**IBackgroundCopyJob::SetNoProgressTimeout,**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout) um zu steuern, wie BITS vorübergehende Fehler verarbeitet.

Bei Vordergrundaufträgen sollten Sie die Zeit begrenzen, für die ein Auftrag im vorübergehenden Fehlerzustand bleiben soll, und versuchen, eine Wiederherstellung zu versuchen. Verwenden Sie [**die SetNoProgressTimeout-Methode,**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout) um die Zeit zu begrenzen, die ein Auftrag im vorübergehenden Fehlerzustand bleibt, oder um den Auftrag in den schwerwiegenden Fehlerzustand zu zwingen. Wenn Sie den Auftrag wiederherstellen lassen, sollten Sie die [**SetMinimumRetryDelay-Methode**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay) verwenden, um die minimale Wiederholungsverzögerung auf 60 Sekunden zu setzen, oder die [**IBackgroundCopyJob::Resume-Methode**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) aufrufen, um den Auftrag erneut zu aktivieren.

Weitere Informationen finden Sie unter [**BG \_ JOB \_ STATE**](/windows/desktop/api/Bits/ne-bits-bg_job_state), [Lebenszyklus eines BITS-Auftrags](life-cycle-of-a-bits-job.md)und [Behandeln von Fehlern](handling-errors.md).

## <a name="measuring-network-bandwidth-usage"></a>Messen der Netzwerkbandbreitennutzung

BITS kann den Netzwerkadapter des Clients verwenden, um die verfügbare Netzwerkbandbreite zu schätzen. Da BITS die Bandbreite nicht über den Client hinaus messen kann, kann BITS die WAN-Verbindung überlasten. Um die Überlastung der WAN-Verbindung zu reduzieren, können Sie die **Gruppenrichtlinie MaxInternetBandwidth** verwenden, um die Bandbreite zu begrenzen, die der Client verwendet. Weitere Informationen finden Sie unter [Netzwerkbandbreite und](network-bandwidth.md) [Gruppenrichtlinien.](group-policies.md)

Wenn Sie eine Anwendung schreiben, die viele Clients zum Herunterladen von Dateien von einem bestimmten Server verwenden, sollten Sie ein Schema in Betracht ziehen, das die Downloadanforderungen staffelt, damit Sie den Server nicht mit Anforderungen überladen.

## <a name="setting-credentials-for-proxy-and-server-authentication"></a>Festlegen von Anmeldeinformationen für die Proxy- und Serverauthentifizierung

Wenn Sie erwarten, dass der Proxy oder Server Benutzeranmeldeinformationen erfordert, müssen Sie die Anmeldeinformationen für BITS angeben. Um die Anmeldeinformationen anzugeben, rufen Sie die [**IBackgroundCopyJob2::SetCredentials-Methode**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) auf. BITS unterstützt Standard-, Digest-, Negotiate-, NTLM- und Passport-Authentifizierungsschemas.

Weitere Informationen zur Authentifizierung finden Sie unter [Authentifizierung.](authentication.md)

## <a name="specifying-proxy-settings-for-user-accounts-and-service-accounts"></a>Angeben von Proxyeinstellungen für Benutzerkonten und Dienstkonten

Standardmäßig verwendet BITS die Internet Explorer Proxyeinstellungen des Benutzers. Um die Proxyeinstellungen des Benutzers Internet Explorer, rufen Sie die [**IBackgroundCopyJob::SetProxySettings-Methode**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) auf.

Die Internet Explorer-Proxyeinstellungen gelten nicht für Systemkonten, sodass das Standardproxyverhalten (**BG JOB PROXY USAGE \_ \_ \_ \_ PRECONFIG**) nur in WPAD-Bereitstellungen (Web Proxy Auto-Discovery Protocol) ordnungsgemäß funktioniert, es sei denn, es werden zusätzliche Konfigurationsschritte ausgeführt. Wenn Ihre Anwendung ein Dienst ist, der als LocalSystem, LocalService oder NetworkService ausgeführt wird, sollten Sie ein Hilfstoken für Ihre BITS-Aufträge konfigurieren oder explizit die richtigen Proxyeinstellungen festlegen, indem Sie [**IBackgroundCopyJob::SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) mit **BG JOB PROXY USAGE OVERRIDE \_ \_ \_ \_ aufrufen.** Alternativ können Sie die Schalter **/Util /SetIEProxy** von BitsAdmin.exe verwenden, um Internet Explorer-Proxyeinstellungen für das Systemkonto LocalSystem, LocalService oder NetworkService festlegen. Weitere Informationen finden Sie unter [BitsAdmin Tool](bitsadmin-tool.md).

BITS erkennt nicht die Proxyeinstellungen, die mithilfe der Proxycfg.exe werden.

Ab dem Windows 10 October 2018 Update (10.0; Build 17763) verwendet BITS die gleiche Proxy reihenfolge wie WinHttp mit AUTOMATIC_PROXY. BITS verwendet diese kompatiblere Reihenfolge, wenn BG_JOB_PROXY_USAGE_PRECONFIG angegeben wird. BG_JOB_PROXY_USAGE_PRECONFIG ist der Standardwert für die Angabe des HTTP-Proxys.

## <a name="specifying-user-specific-settings-for-authenticating-proxies"></a>Angeben von benutzerspezifischen Einstellungen für die Authentifizierung von Proxys

Wenn Sie BITS in einer Umgebung verwenden, die eine Proxyauthentifizierung erfordert, während sie als Konto ohne nutzbare NTLM- oder Kerberos-Anmeldeinformationen in der Netzwerkdomäne des Computers ausgeführt wird, müssen Sie zusätzliche Schritte ausführen, um sich ordnungsgemäß mit den Anmeldeinformationen eines anderen Benutzerkontos zu authentifizieren, das über Anmeldeinformationen für die Domäne verfügt. Dies ist ein typisches Szenario, wenn Ihr BITS-Code als Systemdienst wie LocalService, NetworkService oder LocalSystem ausgeführt wird, da diese Konten nicht über nutzbare NTLM- oder Kerberos-Anmeldeinformationen verfügen.

Weitere Informationen zur Funktionsweise der Authentifizierung in diesem Szenario finden Sie unter [Authentifizierung.](authentication.md)

## <a name="scalability"></a>Skalierbarkeit

Wenn sich mehr als 100 Aufträge in der Warteschlange befinden, kann die Leistung je nach Zusammensetzung des Auftrags abnehmen. BITS verwendet die [Richtlinieneinstellung MaxJobsPerMachine,](group-policies.md) um eine harte Grenze für die Anzahl von Aufträgen in der Warteschlange zu erzwingen. Anwendungen sollten die Anzahl ihrer Aufträge auf etwa 10 beschränken, damit mehrere Anwendungen weniger Wahrscheinlichkeit haben, die Richtlinie für 100 Aufträge zu überschreiten. In der Regel übermittelt eine Anwendung mit einer großen Anzahl von zu übermittelnden Aufträgen zunächst 10 Aufträge und dann nach Abschluss jedes Auftrags jeweils einen Auftrag.

Die Anzahl der Dateien im Auftrag sollte ebenfalls auf maximal 10 Dateien beschränkt werden. Wenn Sie eine große Anzahl von Dateien für einen Auftrag übertragen möchten, sollten Sie stattdessen eine CAB-Datei erstellen, die alle Dateien enthält.

## <a name="http-headers-can-be-in-any-case"></a>HTTP-Header können in jedem Fall sein.

Die HTTP-Standards haben immer gesagt, dass HTTP-Header ohne Unterscheidung nach Groß-/Kleinschreibung behandelt werden müssen (RFC 7230, Abschnitt 3.2). Der neueste HTTP-Standard, RFC 7540, geht noch weiter und besagt, dass http/2-Datenverkehr die Header als nicht großschreibungsunabhängig vergleichen und Header in Kleinschreibung (RFC 6540, Abschnitt 8.1.2) präsentieren muss. Auch wenn Datenverkehr mit Nicht-Klein-Headern gesendet wird, können Proxys entscheiden, ob die Header in Klein-/Kleinschrift erzwingen werden.

## <a name="avoiding-personally-identifiable-information-pii"></a>Vermeiden personenbezogener Informationen (Personally Identifiable Information, PII)

BITS-Aufträge, einschließlich des Auftragsanzeigenamens, der Beschreibung und der Dateinamen, sind für alle Benutzer mit Administratorrechten sichtbar. Sie können auch der Telemetrie Windows hinzugefügt werden. Vermeiden Sie es, vertrauliche Daten (z. B. den eigenen Namen des Benutzers) in die Auftragsdetails zu setzen.
