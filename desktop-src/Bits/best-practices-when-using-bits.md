---
title: Bewährte Methoden bei der Verwendung von Bits
description: Dieser Abschnitt enthält Informationen, die Sie beim Entwerfen einer Anwendung berücksichtigen sollten, die Bits verwendet.
ms.assetid: f4a09a80-2a85-4b59-b0fd-c23c128973f7
ms.topic: article
ms.date: 7/12/2019
ms.openlocfilehash: bbf69e75b99994eea3e8986d1be9920ff1a12bc5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947485"
---
# <a name="best-practices-when-using-bits"></a>Bewährte Methoden bei der Verwendung von Bits

Dieser Abschnitt enthält Informationen, die Sie beim Entwerfen einer Anwendung berücksichtigen sollten, die Bits verwendet.

## <a name="user-context-or-service-context"></a>Benutzer Kontext oder Dienst Kontext

Bits überträgt Dateien nur, wenn der Besitzer des Auftrags auf dem Computer angemeldet ist (der Benutzer muss interaktiv angemeldet sein). Der **runas** -Befehl wird von Bits nicht unterstützt. Weitere Informationen finden Sie unter [Benutzer und Netzwerkverbindungen](users-and-network-connections.md).

Wenn Sie den Kontext eines Benutzers für Ihre Anwendung nicht benötigen, sollten Sie stattdessen einen Dienst schreiben, der als LocalSystem, LocalService oder Network Service ausgeführt wird. Diese Systemkonten sind immer angemeldet, sodass die Übertragung keinem Benutzer unterliegt, der sich abmeldet. Wenn Sie jedoch die Identität eines Benutzers annehmen, wenn Sie den Auftrag erstellen, gelten die interaktiven Anmelde Regeln. Weitere Informationen finden Sie unter [Dienst Konten und Bits](service-accounts-and-bits.md).

## <a name="jobs-are-persistent"></a>Aufträge sind persistent.

Aufträge bleiben in der Warteschlange, bis Sie die [**ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) -Methode oder die [**ibackgroundcopyjob:: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) -Methode aufgerufen haben. Die Dateien im Auftrag stehen dem Benutzer erst zur Verfügung, wenn Sie " **Complete**" aufgerufen haben. In der Regel rufen Sie " **abgeschlossen** " auf, wenn der Status des Auftrags " **BG \_ Job \_ State \_ übertragene**" ist, und rufen Sie " **Abbrechen** " auf, wenn der Auftrag den Status " **\_ \_ \_ vorübergehender Status \_ des BG-Auftragsstatus** " oder " **BG \_ Job \_ State \_ Error** " aufweist und nicht mehr

Wenn Sie die [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) -Methode oder die [**Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) -Methode nicht innerhalb von 90 Tagen aufrufen (Standardwert für [jobinactivitytimeout](group-policies.md) Gruppenrichtlinie), bricht der Dienst den Auftrag ab. Sie sollten immer die **Complete** -oder **Cancel** -Methode aufrufen und sich nicht auf die jobinactivitytimeout-Richtlinie verlassen, um die Aufträge zu bereinigen. Die in der Warteschlange verbleibenden Aufträge können verhindern, dass Benutzer andere Aufträge erstellen, wenn das Richtlinien Limit von maxjobsperuser oder maxjobspermachine erreicht wird.

## <a name="when-to-use-foreground-or-background-priority"></a>Verwendung der Vordergrund-oder Hintergrund Priorität

Wenn der Auftrag nicht Zeit kritisch ist oder der Benutzer aktiv wartet, sollten Sie immer eine Hintergrund Priorität verwenden. Es kann jedoch vorkommen, dass Sie von der Hintergrund Priorität zur Vordergrund Priorität wechseln möchten, z. b. wenn der Proxy oder Server den Content-Range-Header nicht unterstützt, oder wenn die Antivirensoftware auf dem Client die Bereichs Header Anforderung entfernt. Der Wechsel zur Vordergrund Priorität funktioniert nur für Dateien, deren Dateigröße kleiner als 2 GB ist. Ein Beispiel finden Sie in der-Implementierung für die [**ibackgroundcopycallback:: joberror**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) -Methode. Beachten Sie außerdem, dass der Auftrag fehlschlägt, wenn der Vordergrund Auftrag aufgrund einer Netzwerkverbindung unterbrochen wird oder sich der Benutzer abmeldet, weil Bits eine Bereichs Anforderung sendet, um zu versuchen, die Übertragung an der Stelle, an der er unterbrochen wurde, neu zu starten.

Ab Windows 8 sollten Sie die Download Aufträge mit den **Bits- \_ Auftrags \_ Eigenschaften \_ Dynamic \_ Content** und **BG \_ Job \_ priority \_ Vordergrund** konfigurieren, wenn Sie auf Server abzielen, die die [HTTP-Anforderungen für Bits-Downloads](http-requirements-for-bits-downloads.md)nicht erfüllen. Beachten Sie, dass dies dazu führt, dass Bits den Download von Anfang an neu starten muss (z. b. aufgrund von Konnektivitätsproblemen oder Systemneustarts).

Informationen zu den verfügbaren Prioritäten und zur Verwendung der Prioritätsstufe durch Bits zum Planen von Aufträgen finden Sie unter [**BG- \_ Auftrags \_ Priorität**](/windows/desktop/api/Bits/ne-bits-bg_job_priority).

## <a name="transient-and-fatal-errors"></a>Vorübergehende und schwerwiegende Fehler

Einige Fehler sind wiederherstellbar, andere nicht. Beispielsweise ist der Fehler "der Server ist nicht verfügbar" ein BEHEB barer Fehler, und der Fehler "Zugriff verweigert" ist ein schwerwiegender Fehler. Bits versetzt wiederherstellbare Fehler in einen vorübergehenden Fehlerzustand und versucht den Auftrag nach einem bestimmten Intervall erneut. Wenn der Auftrag nicht fortgesetzt werden kann, verschiebt Bits den Auftrag in einen schwerwiegenden Fehlerzustand. Verwenden Sie die [**ibackgroundcopyjob:: setminimumretrydelay**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay) -Methode und die [**ibackgroundcopyjob:: setnoprogresstimeout**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout) -Methode, um zu steuern, wie Bits vorübergehende Fehler verarbeitet.

Für Vordergrund Aufträge sollten Sie die Zeitspanne beschränken, die ein Auftrag im vorübergehenden Fehlerzustand verbleibt, und eine Wiederherstellung versuchen. Verwenden Sie die [**setnoprogresstimeout**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout) -Methode, um die Zeitspanne zu begrenzen, in der ein Auftrag im vorübergehenden Fehlerzustand verbleibt, oder um einen schwerwiegenden Fehlerzustand zu erzwingen. Wenn Sie versuchen, eine Wiederherstellung durchzuführen, sollten Sie die [**setminimumretrydelay**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay) -Methode verwenden, um die minimale Wiederholungs Verzögerung auf 60 Sekunden festzulegen, oder Sie können die [**ibackgroundcopyjob:: Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) -Methode aufrufen, um den Auftrag erneut zu aktivieren.

Weitere Informationen finden Sie unter [**BG- \_ Auftrags \_ Status**](/windows/desktop/api/Bits/ne-bits-bg_job_state), [Lebenszyklus eines Bits-Auftrags](life-cycle-of-a-bits-job.md)und [Behandeln von Fehlern](handling-errors.md).

## <a name="measuring-network-bandwidth-usage"></a>Messen der Auslastung der Netzwerkbandbreite

Bits kann den Netzwerkadapter des Clients verwenden, um die verfügbare Netzwerkbandbreite zu schätzen. Da Bits die Bandbreite nicht über den Client hinaus messen kann, kann Bits die WAN-Verbindung erfassen. Zum Reduzieren der Überlastung der WAN-Verbindung können Sie die Gruppenrichtlinie " **MaxInternetBandwidth** " verwenden, um die vom Client verwendete Bandbreite einzuschränken. Weitere Informationen finden Sie unter [Netzwerkbandbreite](network-bandwidth.md) und [Gruppenrichtlinien](group-policies.md).

Wenn Sie eine Anwendung schreiben, die von vielen Clients zum Herunterladen von Dateien von einem bestimmten Server verwendet wird, sollten Sie ein Schema in Erwägung nehmen, das die Download Anforderungen abgleicht, sodass Sie den Server nicht mit Anforderungen überladen.

## <a name="setting-credentials-for-proxy-and-server-authentication"></a>Festlegen von Anmelde Informationen für die Proxy-und Server Authentifizierung

Wenn Sie davon ausgehen, dass der Proxy oder der Server Benutzer Anmelde Informationen erfordert, müssen Sie die Anmelde Informationen für Bits angeben. Um die Anmelde Informationen anzugeben, müssen Sie die [**IBackgroundCopyJob2:: Set-Anmelde**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) Informationen-Methode aufrufen. Bits unterstützt die Authentifizierungs Schemas Basic, Digest, Aushandlung, NTLM und Passport.

Weitere Informationen zur Authentifizierung finden Sie unter [Authentifizierung](authentication.md).

## <a name="specifying-proxy-settings-for-user-accounts-and-service-accounts"></a>Angeben von Proxy Einstellungen für Benutzerkonten und Dienst Konten

Standardmäßig verwendet Bits die Internet Explorer-Proxy Einstellungen des Benutzers. Um die Internet Explorer-Proxy Einstellungen des Benutzers außer Kraft zu setzen, müssen Sie die [**ibackgroundcopyjob:: setproxysettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) -Methode aufrufen.

Die Internet Explorer-Proxy Einstellungen gelten nicht für Systemkonten. Daher funktioniert das standardmäßige Proxy Verhalten (**preconfig für die Verwendung von BG- \_ Auftrags \_ Proxys \_ \_**) nur ordnungsgemäß in WPAD-bereit Stellungen (Web Proxy Auto-Discovery Protocol), es sei denn, es werden zusätzliche Konfigurationsschritte ausgeführt. Wenn es sich bei Ihrer Anwendung um einen Dienst handelt, der als "LocalSystem", "LocalService" oder "Network Service" ausgeführt wird, sollten Sie ein Hilfsobjekt für ihre Bits-Aufträge konfigurieren oder die korrekten Proxy Einstellungen explizit festlegen, indem Sie [**ibackgroundcopyjob:: setproxysettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) mit der **\_ \_ \_ \_ außer Kraft** setzung der Als Alternative können Sie die **/util/SetIEProxy** -Schalter von BitsAdmin.exe verwenden, um Internet Explorer-Proxy Einstellungen für das Systemkonto "LocalSystem", "LocalService" oder "Network Service" festzulegen. Weitere Informationen finden Sie unter [bitadmin-Tool](bitsadmin-tool.md).

Bits erkennt die Proxy Einstellungen nicht, die mithilfe der Proxycfg.exe Datei festgelegt werden.

Beginnend mit dem Windows 10-Update vom Oktober 2018 (10,0; Build 17763), Bits verwendet dieselbe Proxy Reihenfolge, die WinHTTP mit AUTOMATIC_PROXY verwendet. Bits verwendet diese kompatibler Reihenfolge, wenn BG_JOB_PROXY_USAGE_PRECONFIG angegeben wird. BG_JOB_PROXY_USAGE_PRECONFIG ist der Standardwert für die Angabe des HTTP-Proxys.

## <a name="specifying-user-specific-settings-for-authenticating-proxies"></a>Angeben von benutzerspezifischen Einstellungen für das Authentifizieren von Proxys

Wenn Sie Bits in einer Umgebung verwenden, die bei Ausführung als Konto ohne verwendbare NTLM-oder Kerberos-Anmelde Informationen in der Netzwerk Domäne des Computers eine Proxy Authentifizierung erfordert, müssen Sie zusätzliche Schritte ausführen, um die Authentifizierung mithilfe der Anmelde Informationen eines anderen Benutzerkontos, das über Anmelde Informationen für die Domäne verfügt, ordnungsgemäß durchführen zu können. Dies ist ein typisches Szenario, wenn Ihr Bits-Code als Systemdienst wie LocalService, Network Service oder LocalSystem ausgeführt wird, da diese Konten keine verwendbaren NTLM-oder Kerberos-Anmelde Informationen aufweisen.

Ausführliche Informationen zur Funktionsweise der Authentifizierung in diesem Szenario finden Sie unter [Authentifizierung.](authentication.md)

## <a name="scalability"></a>Skalierbarkeit

Wenn sich mehr als 100 Aufträge in der Warteschlange befinden, kann die Leistung ggf. in Abhängigkeit von der Zusammensetzung des Auftrags gesenkt werden. Bits verwendet die Richtlinien Einstellung " [maxjobspermachine](group-policies.md) ", um einen festen Grenzwert für die Anzahl der Aufträge in der Warteschlange festzulegen. Anwendungen sollten die Anzahl ihrer Aufträge auf ungefähr 10 beschränken, sodass mehrere Anwendungen die 100-Job-Richtlinie nicht überschreiten können. In der Regel würde eine Anwendung mit einer großen Anzahl von zu über mittelenden Aufträgen zunächst 10 Aufträge übermitteln und diese dann einzeln einreichen, sobald jeder Auftrag abgeschlossen ist.

Die Anzahl der Dateien im Auftrag sollte auch auf maximal 10 Dateien beschränkt sein. Wenn Sie eine große Anzahl von Dateien für einen Auftrag übertragen möchten, sollten Sie stattdessen eine CAB-Datei erstellen, die alle Dateien enthält.

## <a name="http-headers-can-be-in-any-case"></a>HTTP-Header können in jedem Fall vorhanden sein.

Die HTTP-Standards haben immer gesagt, dass HTTP-Header bei der Groß-/Kleinschreibung nicht beachtet werden müssen (RFC 7230, Abschnitt 3,2). Der neueste http-Standard RFC 7540 geht weiter und besagt, dass http/2-Datenverkehr die Header als groß-und Kleinschreibung vergleichen muss und Header in Kleinbuchstaben (RFC 6540, Abschnitt 8.1.2) enthalten muss. Auch wenn Datenverkehr mit nicht in Kleinbuchstaben gesendeten Headern gesendet wird, können Proxys die Groß-/Kleinschreibung der Header erzwingen.

## <a name="avoiding-personally-identifiable-information-pii"></a>Vermeiden von personenbezogenen Informationen (PII)

BITS-Aufträge einschließlich Auftrags Anzeige Name, Beschreibung und Dateinamen sind für alle Benutzer mit Administratorrechten sichtbar. Sie können auch Windows-Telemetriedaten hinzugefügt werden. Vermeiden Sie es, vertrauliche Daten (z. b. den Namen des Benutzers) in den Auftragsdetails zu platzieren.
