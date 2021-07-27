---
description: Beim Zugriff auf lokale WMI- oder Remotedaten in einer Anwendung oder einem Skript können Fehler auftreten, die von fehlenden Klassen bis hin zu verweigertem Zugriff reichen. Anbieter verfügen auch über Debugoptionen und Problembehandlungsklassen.
ms.assetid: b0aecdf6-ec30-49be-af4e-7eac5d124057
ms.tgt_platform: multiple
title: WMI-Problembehandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58919617c663b52ffb840b3c3382b5707f0a305e
ms.sourcegitcommit: a3e96b6c9c6a3fb629e760dd6cc6327f9e4b62b6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/27/2021
ms.locfileid: "114714794"
---
# <a name="wmi-troubleshooting"></a>WMI-Problembehandlung

Beim Zugriff auf lokale WMI- oder Remotedaten in einer Anwendung oder einem Skript können Fehler auftreten, die von fehlenden Klassen bis hin zu verweigertem Zugriff reichen. Anbieter verfügen auch über Debugoptionen und Problembehandlungsklassen.

> [!Note]  
> Die folgende Dokumentation richtet sich an Entwickler und IT-Administratoren. Wenn Sie ein Endbenutzer sind, für den eine WMI-Fehlermeldung angezeigt wurde, sollten Sie [zu Microsoft-Support](https://support.microsoft.com/) wechseln und nach dem Fehlercode suchen, der in der Fehlermeldung angezeigt wird. Weitere Informationen zur Problembehandlung bei WMI-Skripts und dem WMI-Dienst finden Sie unter [WMI isn't Working!](/previous-versions/tn-archive/ff406382(v=msdn.10))

 

## <a name="wmi-diagnosis-utility"></a>WMI-Diagnosehilfsprogramm

Das WMI-Diagnosehilfsprogramm (WMIDiag.exe) wird ab Windows 8 und Windows Server 2012 nicht mehr unterstützt.

**Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008: **

Wenn WMI Fehlermeldungen zurückgibt, beachten Sie, dass sie möglicherweise keine Probleme im WMI-Dienst oder in WMI-Anbietern angeben. Fehler können aus anderen Teilen des Betriebssystems stammen und über WMI als Fehler auftreten. Löschen Sie das WMI-Repository unter keinen Umständen als erste Aktion, da das Löschen des Repositorys Schäden am System oder an installierten Anwendungen verursachen kann.

Um weitere Informationen zur Ursache des Problems zu erhalten, können Sie das [WMI-Diagnosehilfsprogramm](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) Befehlszeilentool für die Diagnose herunterladen und ausführen. Dieses Tool erstellt einen Bericht, der in der Regel die Ursache des Problems isolieren und Anweisungen zur Behebung des Problems bereitstellen kann. Der Bericht unterstützt auch microsoft-Supportdienste bei der Unterstützung. Sie können die WMI-Diagnosehilfsprogramm im [Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d)herunterladen.

Anbieterwriter können auch Debugprobleme auftreten, es sei denn, Sie schreiben einen [*entkoppelten Anbieter.*](gloss-d.md) Weitere Informationen finden Sie unter [Debuggen von Anbietern.](debugging-providers.md)

## <a name="logging-and-tracing"></a>Protokollierung und Ablaufverfolgung

Die WMI-Protokolldateien sind nicht mehr vorhanden. sie wurden durch [die Ereignisablaufverfolgung für Windows (ETW)](/windows/desktop/ETW/event-tracing-portal)ersetzt. Weitere Informationen finden Sie unter [Ablaufverfolgung der WMI-Aktivität,](tracing-wmi-activity.md) [Protokollierung der WMI-Aktivität](logging-wmi-activity.md)und [WMI-Protokolldateien.](wmi-log-files.md)

## <a name="troubleshooting-in-scripts-and-applications"></a>Problembehandlung in Skripts und Anwendungen

WMI enthält eine Reihe von Klassen für [die Problembehandlung von](wmi-troubleshooting-classes.md) Clientanwendungen, die WMI-Anbieter verwenden. Weitere Informationen finden Sie unter [Problembehandlung bei WMI-Clientanwendungen.](troubleshooting-wmi-client-applications.md)

## <a name="how-provider-writers-can-prevent-wmi-problems"></a>Verhindern von WMI-Problemen durch Anbieterwriter

Anbieterwriter können viele Probleme verhindern, die in Fehlermeldungen über WMI auftreten, indem sie die folgenden Aktionen ausführen:

-   Ordnungsgemäße Registrierung Ihres Anbieters. Weitere Informationen finden Sie unter [Registrieren eines Anbieters.](registering-a-provider.md)
-   Hinzufügen der [**\# pragma autorecover-Anweisung**](pragma-autorecover.md) zur MOF-Datei (Managed Object Format), die Ihre Anbieterklassen definiert.

Weitere Informationen finden Sie unter [Debuggen von Anbietern](debugging-providers.md), [Bereitstellen von Daten an WMI](providing-data-to-wmi.md)und [Anbieterkonfiguration und Problembehandlungsklassen.](provider-configuration-and-troubleshooting-classes.md)

## <a name="access-denied"></a>Zugriff verweigert

Zugriffsverweigerungsfehler, die von Skripts und Anwendungen gemeldet werden, die auf WMI-Namespaces und -Daten zugreifen, fallen in der Regel in drei Kategorien. In der folgenden Tabelle sind die drei Kategorien von Fehlern zusammen mit Problemen aufgeführt, die die Fehler verursachen können, und mögliche Lösungen.



| Fehler                                                                                                                        | Mögliche Probleme                                                                                                                                                                                                                                                                                                                                                                     | Lösung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x800706BA `HRESULT_FROM_WIN32(RPC_S_SERVER_UNAVAILABLE)`<br/> Firewallproblem oder Server nicht verfügbar.<br/>      | Der Computer ist tatsächlich nicht vorhanden, oder die Windows Firewall blockiert die Verbindung.<br/>                                                                                                                                                                                                                                                                                        | Herstellen einer Verbindung mit Vista: **netsh advfirewall firewall set rule group="windows management instrumentation (wmi)" new enable=yes** Connecting to downlevel: Allow the "Remote Administration" rule in Windows Firewall.<br/>                                                                                                                                                                                                                                                                                                            |
| 0x80070005 **E \_ ACCESS \_ DENIED**<br/> Zugriff durch DCOM-Sicherheit verweigert.<br/>                                       | Der Benutzer hat keinen Remotezugriff auf den Computer über DCOM. In der Regel treten DCOM-Fehler auf, wenn eine Verbindung mit einem Remotecomputer mit einer anderen Betriebssystemversion hergestellt wird.<br/>                                                                                                                                                                                          | Erteilen Sie dem Benutzer die Berechtigungen Remotestart und Remoteaktivierung in dcomcnfg. Klicken Sie mit der rechten Maustaste auf Arbeitsplatz-> Eigenschaften. Klicken Sie unter COM-Sicherheit für beide Abschnitte auf "Grenzwerte bearbeiten". Gewähren Sie dem Benutzer Remotezugriff, Remotestart und Remoteaktivierung. Wechseln Sie dann zur DCOM-Konfiguration, suchen Sie nach "Windows-Verwaltungsinstrumentation", und geben Sie dem Benutzer die Gewünschten Remotestart- und Remoteaktivierung. Weitere Informationen finden Sie unter [Herstellen einer Verbindung zwischen verschiedenen Betriebssystemen.](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection)<br/> |
| 0x80041003 **WBEM \_ E \_ ACCESS \_ DENIED**<br/> Zugriff von einem [ *Anbieter* verweigert](gloss-p.md)<br/> | Der Benutzer verfügt nicht über die Berechtigung zum Ausführen des Vorgangs in WMI. Dies kann passieren, wenn Sie bestimmte Klassen als Benutzer mit geringen Rechten abfragen, aber meistens, wenn Sie versuchen, Methoden aufzurufen oder WMI-Instanzen als Benutzer mit geringen Rechten zu ändern. Der Namespace, mit dem Sie eine Verbindung herstellen, ist verschlüsselt, und der Benutzer versucht, eine Verbindung mit einer unverschlüsselten Verbindung herzustellen.<br/> | Gewähren Sie dem Benutzer Zugriff mit der WMI-Steuerung (stellen Sie sicher, dass der \_ Remotezugriff auf TRUE festgelegt ist) Verbinden mithilfe eines Clients, der die Verschlüsselung unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                  |



 

-   In der Regel treten DCOM-Fehler auf, wenn eine Verbindung mit einem Remotecomputer mit einer anderen Betriebssystemversion hergestellt wird.

-   Anbieter können auch den Zugriff auf Daten in bestimmten Namespaces verweigern oder bestimmte Ebenen der Verbindungssicherheit erfordern. Weitere Informationen finden Sie unter [Setting Client Application Process Security](setting-client-application-process-security.md) and Provider Hosting and [Security](provider-hosting-and-security.md).

-   Zugriffsverweigerungsfehler durch ICF-Änderungen (Internet Connection Firewall).

    Weitere Informationen finden Sie unter [Herstellen einer Verbindung über Windows Firewall.](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista)

-   Ein Zugriffsverweigerungsfehler wird von der DCOM-Sicherheit zurückgegeben, wenn ein Client mit niedriger Integrität versucht, auf WMI zuzugreifen. Beispielsweise hat ein ActiveX Steuerelement, das in Internet Explorer ausgeführt wird und für das die Sicherheitsstufe auf niedrig festgelegt ist, keinen Zugriff zum Ausführen lokaler WMI-Vorgänge.

    **Windows 7:** Benutzer mit niedriger Integrität verfügen über schreibgeschützte Berechtigungen für lokale WMI-Vorgänge.

## <a name="information-on-errors"></a>Informationen zu Fehlern

Wenn Sie eine Fehlermeldung von WMI erhalten, können Sie die Meldung in [**WMI-Fehlerkonstanten**](wmi-error-constants.md) oder , für die Skripterstellung, [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum)finden. Die vom Fehler bereitgestellten Informationen allein reichen jedoch in der Regel nicht aus, um zu bestimmen, was passiert. WMI-Repositorybeschädigungen können sich als Klassen oder Instanzen "nicht gefunden" maskieren.

Weitere Informationen zu WMI-Fehlern:

-   Die WMI-Protokolle verfolgen Ereignisse innerhalb des WMI-Kerns und von Anbietern nach. Weitere Informationen finden Sie unter [Protokollieren der WMI-Aktivität.](logging-wmi-activity.md)
-   Verwenden Sie die [WMI-Problembehandlungsklassen,](wmi-troubleshooting-classes.md) um den internen WMI-Status zu überprüfen oder Benachrichtigungen über Anbieter- oder WMI-Dienstereignisse zu empfangen. Weitere Informationen finden Sie unter [Anbieterkonfigurations- und Problembehandlungsklassen](provider-configuration-and-troubleshooting-classes.md) und [Problembehandlung bei WMI-Clientanwendungen.](troubleshooting-wmi-client-applications.md)

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[WMI-Problembehandlung](wmi-troubleshooting.md)
</dt> <dt>

[Ablaufverfolgung der WMI-Aktivität](tracing-wmi-activity.md)
</dt> <dt>

[Protokollierung der WMI-Aktivität](logging-wmi-activity.md)
</dt> </dl>

 

