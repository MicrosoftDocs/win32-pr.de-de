---
description: Beim Zugriff auf lokale WMI-Daten oder Remotedaten in einer Anwendung oder einem Skript können Fehler auftreten, die von fehlenden Klassen bis hin zu verweigerten Zugriffen reichen. Anbieter verfügen auch über Debugoptionen und Problembehandlungsklassen.
ms.assetid: b0aecdf6-ec30-49be-af4e-7eac5d124057
ms.tgt_platform: multiple
title: Problembehandlung bei WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40645c33da838658d66f608d672d979b38012fa855f26637f5896c4ec14c54ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794290"
---
# <a name="wmi-troubleshooting"></a>Problembehandlung bei WMI

Beim Zugriff auf lokale WMI-Daten oder Remotedaten in einer Anwendung oder einem Skript können Fehler auftreten, die von fehlenden Klassen bis hin zu verweigerten Zugriffen reichen. Anbieter verfügen auch über Debugoptionen und Problembehandlungsklassen.

> [!Note]  
> Die folgende Dokumentation richtet sich an Entwickler und IT-Administratoren. Wenn Sie ein Endbenutzer sind, bei dem eine Fehlermeldung zu WMI aufgetreten ist, sollten Sie zu [Microsoft-Support](https://support.microsoft.com/) wechseln und nach dem Fehlercode suchen, der in der Fehlermeldung angezeigt wird. Weitere Informationen zur Behandlung von Problemen mit WMI-Skripts und dem WMI-Dienst finden Sie unter [WMI Isn't Working!](/previous-versions/tn-archive/ff406382(v=msdn.10))

 

## <a name="wmi-diagnosis-utility"></a>WMI-Diagnosehilfsprogramm

Das WMI-Diagnoseprogramm (WMIDiag.exe) wird ab Windows 8 nicht mehr Windows Server 2012.

**Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008: **

Wenn WMI Fehlermeldungen zurückgibt, beachten Sie, dass sie möglicherweise nicht auf Probleme im WMI-Dienst oder in WMI-Anbietern hinweisen. Fehler können aus anderen Teilen des Betriebssystems stammen und über WMI als Fehler auftreten. Löschen Sie das WMI-Repository unter keinen Umständen als erste Aktion, da das Löschen des Repositorys schäden am System oder an installierten Anwendungen verursachen kann.

Um weitere Informationen zur Ursache des Problems zu erhalten, können Sie das WMI-Diagnosehilfsprogramm-Befehlszeilentool herunterladen und ausführen. [](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) Dieses Tool erstellt einen Bericht, der normalerweise die Ursache des Problems isolieren und Anweisungen zum Beheben des Problems bereitstellen kann. Der Bericht unterstützt Auch Microsoft-Supportdienste bei der Unterstützung. Sie können die WMI-Diagnosehilfsprogramm im [Download Center herunterladen.](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d)

Anbieterautoren können auch Debugprobleme haben, es sei denn, Sie schreiben einen [*entkoppelten Anbieter.*](gloss-d.md) Weitere Informationen finden Sie unter [Debuggen von Anbietern.](debugging-providers.md)

## <a name="logging-and-tracing"></a>Protokollierung und Ablaufverfolgung

Die WMI-Protokolldateien sind nicht mehr vorhanden. sie wurden durch die [Ereignisablaufverfolgung für Windows (ETW) ersetzt.](/windows/desktop/ETW/event-tracing-portal) Weitere Informationen finden Sie unter [Ablaufverfolgung der WMI-Aktivität,](tracing-wmi-activity.md) [Protokollierung der WMI-Aktivität](logging-wmi-activity.md)und [WMI-Protokolldateien.](wmi-log-files.md)

## <a name="troubleshooting-in-scripts-and-applications"></a>Problembehandlung in Skripts und Anwendungen

WMI enthält eine Reihe von Klassen für die [Problembehandlung von Clientanwendungen,](wmi-troubleshooting-classes.md) die WMI-Anbieter verwenden. Weitere Informationen finden Sie unter [Problembehandlung für WMI-Clientanwendungen.](troubleshooting-wmi-client-applications.md)

## <a name="how-provider-writers-can-prevent-wmi-problems"></a>Verhindern von WMI-Problemen durch Anbieterautoren

Anbieterautoren können viele Probleme verhindern, die in Fehlermeldungen über WMI auftreten, indem sie die folgenden Aktionen ausführen:

-   Registrieren Sie Ihren Anbieter ordnungsgemäß. Weitere Informationen finden Sie unter [Registrieren eines Anbieters.](registering-a-provider.md)
-   Hinzufügen der [**\# pragma autorecover-Anweisung**](pragma-autorecover.md) zur MANAGED OBJECT FORMAT (MOF)-Datei, die Ihre Anbieterklassen definiert.

Weitere Informationen finden Sie unter [Debuganbieter](debugging-providers.md), Bereitstellen von Daten [für WMI](providing-data-to-wmi.md)und [Anbieterkonfiguration und Problembehandlungsklassen](provider-configuration-and-troubleshooting-classes.md).

## <a name="access-denied"></a>Zugriff verweigert

Fehler vom Datentyp "Zugriff verweigert", die von Skripts und Anwendungen gemeldet werden, die auf WMI-Namespaces und -Daten zugreifen, sind in der Regel in drei Kategorien unterteilt. Die folgende Tabelle enthält die drei Kategorien von Fehlern sowie Probleme, die die Fehler verursachen können, und mögliche Lösungen.



| Fehler                                                                                                                        | Mögliche Probleme                                                                                                                                                                                                                                                                                                                                                                     | Lösung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x800706BA `HRESULT_FROM_WIN32(RPC_S_SERVER_UNAVAILABLE)`<br/> Firewallproblem oder Server nicht verfügbar.<br/>      | Der Computer ist tatsächlich nicht vorhanden, oder die Windows Firewall blockiert die Verbindung.<br/>                                                                                                                                                                                                                                                                                        | Herstellen einer Verbindung mit Vista: **netsh advfirewall firewall set rule group="windows management instrumentation (wmi)" new enable=yes** Connecting to downlevel: Allow the "Remote Administration" rule in Windows Firewall.<br/>                                                                                                                                                                                                                                                                                                            |
| 0x80070005 **\_ E-ZUGRIFF \_ VERWEIGERT**<br/> Zugriff durch DCOM-Sicherheit verweigert.<br/>                                       | Der Benutzer hat keinen Remotezugriff auf den Computer über DCOM. In der Regel treten DCOM-Fehler auf, wenn eine Verbindung mit einem Remotecomputer mit einer anderen Betriebssystemversion besteht.<br/>                                                                                                                                                                                          | Erteilen Sie dem Benutzer die Berechtigungen Remotestart und Remoteaktivierung in dcomcnfg. Klicken Sie mit der rechten Arbeitsplatz auf > Eigenschaften. Klicken Sie unter COM-Sicherheit für beide Abschnitte auf "Grenzwerte bearbeiten". Geben Sie dem Benutzer Remotezugriff, Remotestart und Remoteaktivierung. Wechseln Sie dann zur DCOM-Konfiguration, suchen Sie nach "Windows Verwaltungsinstrumentation", und geben Sie dem Benutzer, den Sie remote starten und remoteaktivieren möchten. Weitere Informationen finden Sie unter [Herstellen einer Verbindung zwischen verschiedenen Betriebssystemen.](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection)<br/> |
| 0x80041003 **WBEM \_ E \_ ACCESS \_ DENIED**<br/> Zugriff durch einen Anbieter [ *verweigert*](gloss-p.md)<br/> | Der Benutzer verfügt nicht über die Berechtigung zum Ausführen des Vorgangs in WMI. Dies kann passieren, wenn Sie bestimmte Klassen als Benutzer mit geringen Rechten abfragen, aber meistens, wenn Sie versuchen, Methoden auf- oder WMI-Instanzen als Benutzer mit geringen Rechten zu ändern. Der Namespace, mit dem Sie eine Verbindung herstellen, ist verschlüsselt, und der Benutzer versucht, eine Verbindung mit einer unverschlüsselten Verbindung herzustellen.<br/> | Geben Sie dem Benutzer Zugriff mit der WMI-Steuerung (stellen Sie sicher, dass der Remotezugriff auf TRUE festgelegt ist), Verbinden client, der Verschlüsselung \_ unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                  |



 

-   In der Regel treten DCOM-Fehler auf, wenn eine Verbindung mit einem Remotecomputer mit einer anderen Betriebssystemversion besteht.

-   Anbieter können auch den Zugriff auf Daten in bestimmten Namespaces verweigern oder bestimmte Ebenen der Verbindungssicherheit erfordern. Weitere Informationen finden Sie unter [Setting Client Application Process Security](setting-client-application-process-security.md) and Provider Hosting and [Security](provider-hosting-and-security.md).

-   Fehler "Zugriff verweigert" von ICF-Änderungen (Internet Connection Firewall).

    Weitere Informationen finden Sie unter [Herstellen einer Verbindung über Windows Firewall.](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista)

-   Ein Zugriffs verweigerter Fehler wird von der DCOM-Sicherheit zurückgegeben, wenn ein Client mit niedriger Integrität versucht, auf WMI zu zugreifen. Beispielsweise hat ein ActiveX-Steuerelement, das in Internet Explorer ausgeführt wird und dessen Sicherheitsstufe auf niedrig festgelegt ist, keinen Zugriff zum Ausführen lokaler WMI-Vorgänge.

    **Windows 7:** Benutzer mit niedriger Integrität verfügen über schreibgeschützte Berechtigungen für lokale WMI-Vorgänge.

## <a name="information-on-errors"></a>Informationen zu Fehlern

Wenn Sie eine Fehlermeldung von WMI erhalten, finden Sie die Meldung unter [**WMI-Fehlerkonst constants (WMI-Fehlerkonst constants)**](wmi-error-constants.md) oder bei der Skripterstellung [**unter WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum)( ). Die vom Fehler allein bereitgestellten Informationen reichen jedoch in der Regel nicht aus, um zu bestimmen, was passiert. Eine Beschädigung des WMI-Repositorys kann sich als Klassen oder Instanzen "nicht gefunden" maskieren.

Weitere Informationen zu WMI-Fehlern:

-   Die WMI-Protokolle verfolgen Ereignisse innerhalb des WMI-Kerns und von Anbietern nach. Weitere Informationen finden Sie unter [Protokollierung der WMI-Aktivität](logging-wmi-activity.md).
-   Verwenden Sie [die WMI-Problembehandlungsklassen,](wmi-troubleshooting-classes.md) um den internen WMI-Status zu überprüfen oder Benachrichtigungen über Anbieter- oder WMI-Dienstereignisse zu empfangen. Weitere Informationen finden Sie unter [Anbieterkonfiguration und Problembehandlungsklassen und](provider-configuration-and-troubleshooting-classes.md) [Problembehandlung bei WMI-Clientanwendungen.](troubleshooting-wmi-client-applications.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Problembehandlung bei WMI](wmi-troubleshooting.md)
</dt> <dt>

[Nachverfolgen der WMI-Aktivität](tracing-wmi-activity.md)
</dt> <dt>

[Protokollieren der WMI-Aktivität](logging-wmi-activity.md)
</dt> </dl>

 

