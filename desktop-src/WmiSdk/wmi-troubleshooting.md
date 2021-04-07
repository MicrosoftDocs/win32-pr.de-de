---
description: Beim Zugriff auf lokale oder Remote Daten von WMI in einer Anwendung oder einem Skript treten möglicherweise Fehler auf, die von fehlenden Klassen für den Zugriff verweigert werden. Außerdem verfügen Anbieter über Debugoptionen und Fehler Behebungs Klassen.
ms.assetid: b0aecdf6-ec30-49be-af4e-7eac5d124057
ms.tgt_platform: multiple
title: WMI-Problembehandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94ccb8afa1af64e6eb80050c96973a9ad9456a52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864007"
---
# <a name="wmi-troubleshooting"></a>WMI-Problembehandlung

Beim Zugriff auf lokale oder Remote Daten von WMI in einer Anwendung oder einem Skript treten möglicherweise Fehler auf, die von fehlenden Klassen für den Zugriff verweigert werden. Außerdem verfügen Anbieter über Debugoptionen und Fehler Behebungs Klassen.

> [!Note]  
> Die folgende Dokumentation richtet sich an Entwickler und IT-Administratoren. Wenn Sie ein Endbenutzer sind, bei dem eine Fehlermeldung zu WMI aufgetreten ist, sollten Sie [Microsoft-Support](https://support.microsoft.com/) aufrufen und nach dem Fehlercode suchen, der in der Fehlermeldung angezeigt wird. Weitere Informationen zur Behebung von Problemen mit WMI-Skripts und dem WMI-Dienst finden Sie unter [WMI funktioniert nicht!](/previous-versions/tn-archive/ff406382(v=msdn.10))

 

## <a name="wmi-diagnosis-utility"></a>WMI-Diagnosehilfsprogramm

Das WMI-Diagnose Hilfsprogramm (WMIDiag.exe) wird ab Windows 8 und Windows Server 2012 nicht mehr unterstützt.

* * Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008: * *

Wenn WMI Fehlermeldungen zurückgibt, beachten Sie, dass Sie möglicherweise nicht auf Probleme im WMI-Dienst oder in WMI-Anbietern hinweisen. Fehler können aus anderen Teilen des Betriebssystems stammen und als Fehler über WMI auftreten. Löschen Sie das WMI-Repository unter Umständen nicht als erste Aktion, da das Löschen des Repository zu Beschädigungen des Systems oder der installierten Anwendungen führen kann.

Um weitere Informationen zur Ursache des Problems zu erhalten, können Sie das Befehlszeilen Tool [WMI-Diagnosehilfsprogramm](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) Diagnose herunterladen und ausführen. Mit diesem Tool wird ein Bericht erstellt, der in der Regel die Ursache des Problems isolieren und Anweisungen zur Behebung des Problems bereitstellen kann. Der Bericht hilft Ihnen auch bei der Unterstützung durch den Microsoft-Support. Sie können das WMI-Diagnosehilfsprogramm im [Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d)herunterladen.

Anbieterwriter können auch Debuggingprobleme erkennen, wenn Sie keinen [*entkoppelten Anbieter*](gloss-d.md)schreiben. Weitere Informationen finden Sie unter [Debuggen von Anbietern](debugging-providers.md).

## <a name="logging-and-tracing"></a>Protokollierung und Ablauf Verfolgung

Die WMI-Protokolldateien sind nicht mehr vorhanden. Sie wurden durch die [Ereignis Ablauf Verfolgung für Windows (ETW)](/windows/desktop/ETW/event-tracing-portal)ersetzt. Weitere Informationen finden Sie unter Ablauf [Verfolgung WMI-Aktivität](tracing-wmi-activity.md), [Protokollierung der WMI-Aktivität](logging-wmi-activity.md)und [WMI-Protokolldateien](wmi-log-files.md).

## <a name="troubleshooting-in-scripts-and-applications"></a>Problembehandlung in Skripts und Anwendungen

WMI enthält eine Reihe von Klassen zur [Problem](wmi-troubleshooting-classes.md) Behandlung von Client Anwendungen, die WMI-Anbieter verwenden. Weitere Informationen finden Sie unter [Problembehandlung bei WMI-Client Anwendungen](troubleshooting-wmi-client-applications.md).

## <a name="how-provider-writers-can-prevent-wmi-problems"></a>Wie Anbieter Schreiber WMI-Probleme verhindern können

Anbieterwriter können viele Probleme, die in Fehlermeldungen über WMI auftreten, durch Ausführen der folgenden Aktionen verhindern:

-   Der Anbieter wird ordnungsgemäß registriert. Weitere Informationen finden Sie unter [Registrieren eines Anbieters](registering-a-provider.md).
-   Hinzufügen der [**\# pragma Auto Wiederherstellen**](pragma-autorecover.md) -Anweisung zu der Managed Object Format (MOF)-Datei, die die Anbieter Klassen definiert.

Weitere Informationen finden Sie unter [Debuggen von Anbietern](debugging-providers.md), [Bereitstellen von Daten für WMI](providing-data-to-wmi.md)und [Anbieter Konfiguration und Problem](provider-configuration-and-troubleshooting-classes.md)Behandlung von Klassen.

## <a name="access-denied"></a>Zugriff verweigert

Zugriffs Verweigerungs Fehler, die von Skripts und Anwendungen gemeldet werden, die auf WMI-Namespaces und Daten zugreifen, werden im Allgemeinen in drei Kategorien eingeteilt. In der folgenden Tabelle werden die drei Kategorien von Fehlern zusammen mit Problemen aufgelistet, die möglicherweise die Fehler und mögliche Lösungen verursachen.



| Fehler                                                                                                                        | Mögliche Probleme                                                                                                                                                                                                                                                                                                                                                                     | Lösung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x800706ba `HRESULT_FROM_WIN32(RPC_S_SERVER_UNAVAILABLE)`<br/> Firewallproblem oder Server nicht verfügbar.<br/>      | Der Computer ist nicht vorhanden, weil die Windows-Firewall die Verbindung blockiert.<br/>                                                                                                                                                                                                                                                                                        | Herstellen einer Verbindung mit Vista: **netsh advfirewall firewall set rule Group = "Windows Management Instrumentation (WMI)" New enable = yes** Connection to Downlevel: allow the "Remote Administration" Rule in der Windows-Firewall.<br/>                                                                                                                                                                                                                                                                                                            |
| 0x80070005 **E \_ Zugriff \_ verweigert**<br/> Der Zugriff wurde durch DCOM-Sicherheit verweigert.<br/>                                       | Der Benutzer hat keinen Remote Zugriff auf den Computer über DCOM. DCOM-Fehler treten in der Regel auf, wenn eine Verbindung mit einem Remote Computer mit einer anderen Betriebssystemversion hergestellt wird.<br/>                                                                                                                                                                                          | Hiermit werden die Benutzerberechtigungen für Remote Start und Remote Aktivierung in DCOMCNFG erteilt. Klicken Sie mit der rechten Maustaste auf Arbeitsplatz-> Eigenschaften. Klicken Sie unter COM-Sicherheit für beide Abschnitte auf "Limits bearbeiten". Erhalten Sie dem Benutzer Zugriff auf Remote Zugriff, Remote Start und Remote Aktivierung. Wechseln Sie dann zur DCOM-Konfiguration, suchen Sie nach "Windows-Verwaltungsinstrumentation", und legen Sie dem Benutzer die Möglichkeit, Remote Start und Remote Aktivierung zu aktivieren. Weitere Informationen finden Sie unter [Herstellen einer Verbindung zwischen verschiedenen Betriebssystemen](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection) .<br/> |
| 0x80041003 **WBEM \_ E \_ Zugriff \_ verweigert**<br/> Zugriff verweigert von einem [ *Anbieter*](gloss-p.md)<br/> | Der Benutzer verfügt nicht über die Berechtigung zum Ausführen des Vorgangs in WMI. Dies kann der Fall sein, wenn Sie bestimmte Klassen als Benutzer mit geringen Rechten Abfragen, aber meistens, wenn Sie versuchen, Methoden aufzurufen oder WMI-Instanzen als Benutzer mit niedrigen Rechten zu ändern. Der Namespace, mit dem Sie eine Verbindung herstellen, wird verschlüsselt, und der Benutzer versucht, eine Verbindung mit einer unverschlüsselten Verbindung herzustellen.<br/> | Ermöglichen Sie dem Benutzer den Zugriff mit dem WMI-Steuerelement (stellen Sie sicher \_ , dass der Remote Zugriff auf "true" festgelegt ist) stellen Sie eine Verbindung mithilfe eines Clients her<br/>                                                                                                                                                                                                                                                                                                                                                                                  |



 

-   DCOM-Fehler treten in der Regel auf, wenn eine Verbindung mit einem Remote Computer mit einer anderen Betriebssystemversion hergestellt wird.

-   Anbieter können auch den Zugriff auf Daten in bestimmten Namespaces verweigern oder bestimmte Ebenen der Verbindungssicherheit erfordern. Weitere Informationen finden Sie unter [Festlegen der Prozesssicherheit für Client Anwendungen](setting-client-application-process-security.md) und [Anbieter Hosting und-Sicherheit](provider-hosting-and-security.md).

-   "Zugriff verweigert"-Fehler über Änderungen der Internetverbindungs Firewall (ICF).

    Weitere Informationen finden Sie unter [Herstellen einer Verbindung über die Windows-Firewall](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).

-   Ein Fehler vom Typ "Zugriff verweigert" wird von der DCOM-Sicherheit zurückgegeben, wenn ein Client mit niedriger Integrität auf WMI zugreift. Beispielsweise kann ein ActiveX-Steuerelement, das in Internet Explorer ausgeführt wird und für das die Sicherheitsstufe auf niedrig festgelegt ist, keinen Zugriff auf lokale WMI-Vorgänge haben.

    **Windows 7:** Benutzer mit niedriger Integrität verfügen über Leseberechtigungen für lokale WMI-Vorgänge.

## <a name="information-on-errors"></a>Informationen zu Fehlern

Wenn Sie eine Fehlermeldung von WMI erhalten, können Sie die Nachricht in [**WMI-Fehler Konstanten**](wmi-error-constants.md) oder, für die Skripterstellung, [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum)suchen. Die Informationen, die nur vom Fehler bereitgestellt werden, sind jedoch in der Regel unzureichend, um zu ermitteln, was passiert. WMI-Repository-Beschädigungen können maskiert werden, da Klassen oder Instanzen nicht gefunden werden.

Weitere Informationen zu WMI-Fehlern:

-   Die WMI-Protokolle verfolgen Ereignisse aus dem WMI-Kern und aus Anbietern. Weitere Informationen finden Sie unter [Protokollieren von WMI-Aktivitäten](logging-wmi-activity.md).
-   Verwenden Sie die [WMI-Fehler Behebungs Klassen](wmi-troubleshooting-classes.md) , um den internen WMI-Status zu überprüfen oder Benachrichtigungen über Anbieter-oder WMI-Dienst Ereignisse Weitere Informationen finden Sie unter [Anbieter Konfiguration und Problem](provider-configuration-and-troubleshooting-classes.md) Behandlung von Klassen und Problembehandlung bei [WMI-Client Anwendungen](troubleshooting-wmi-client-applications.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Problembehandlung](wmi-troubleshooting.md)
</dt> <dt>

[WMI-Ablauf Verfolgung](tracing-wmi-activity.md)
</dt> <dt>

[Protokollieren der WMI-Aktivität](logging-wmi-activity.md)
</dt> </dl>

 

