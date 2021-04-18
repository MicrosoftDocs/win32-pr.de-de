---
description: WinMgmt ist der WMI-Dienst innerhalb des svchost-Prozesses, der unter dem &\# 0034; ausgeführt wird. LocalSystem&\# 0034; Konto.
ms.assetid: 3923322a-3acb-407e-8a07-09c59d252e8b
ms.tgt_platform: multiple
title: WinMgmt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- winmgmt
api_type:
- NA
api_location: ''
ms.openlocfilehash: 090fe71edbb00bd7964e5dcc1d518f57179af943
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351536"
---
# <a name="winmgmt"></a>WinMgmt

WinMgmt ist der WMI-Dienst innerhalb des svchost-Prozesses, der unter dem Konto "LocalSystem" ausgeführt wird.

In jedem Fall wird der WMI-Dienst automatisch gestartet, wenn die erste Verwaltungs Anwendung oder das erste Skript eine Verbindung mit einem WMI-Namespace anfordert. Weitere Informationen finden Sie unter [Starten und Beenden des WMI-Diensts](starting-and-stopping-the-wmi-service.md).

> [!Note]  
> WMI ist eine Kernkomponente des Windows-Betriebssystems, mit der Entwickler und IT-Administratoren Skripts und Anwendungen schreiben können, um bestimmte Aufgaben zu automatisieren. Winmgmt.exe ist der Dienst, mit dem WMI auf dem lokalen Computer ausgeführt werden kann. Weitere Informationen zur Verwendung von WMI finden Sie unter [Verwenden von WMI](using-wmi.md). Wenn Sie eine Fehlermeldung bezüglich winmgmt.exe erhalten haben, finden Sie weitere Informationen unter [WMI-Problem](wmi-troubleshooting.md)Behandlung. Weitere Informationen zu Winmgmt.exe finden Sie unter [Verwenden von WMI-Verwaltungs Tools](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10)).

 

Wenn der WMI-Dienst von der Eingabeaufforderung aus ausgeführt wird, verfügt er über die folgenden Schalter.

``` syntax
winmgmt 
  [/backup <filename>] 
  [/restore <filename> <mode>] 
  [/resyncperf <winmgmt service process id>] 
  [/standalonehost <level>]
  [/sharedhost]
  [/verifyrepository <path>]
  [/salvagerepository] 
  [/resetrepository]
```

## <a name="switches"></a>Switches

<dl> <dt>

<span id="__________backup__filename_________"></span><span id="__________BACKUP__FILENAME_________"></span>**/Backup***<filename>* 
</dt> <dd>

Bewirkt, dass WMI das Repository im angegebenen Dateinamen sichert. Das *filename* -Argument sollte den vollständigen Pfad zum Speicherort der Datei enthalten. Dieser Vorgang erfordert eine Schreibsperre für das Repository, damit Schreibvorgänge in das Repository angehalten werden, bis der Sicherungs Vorgang abgeschlossen ist.

Wenn Sie keinen Pfad für die Datei angeben, wird diese im Verzeichnis% windir% \\ system32 abgelegt.

</dd> <dt>

<span id="__________restore__filename____flag_____"></span><span id="__________RESTORE__FILENAME____FLAG_____"></span>**/Restore** *<filename>**<flag>* 
</dt> <dd>

Stellt das WMI-Repository manuell aus der angegebenen Sicherungsdatei wieder her. Das *filename* -Argument sollte den vollständigen Pfad zum Speicherort der Sicherungsdatei enthalten. Um den Wiederherstellungs Vorgang auszuführen, speichert WMI das vorhandene Repository, um zurückschreiben, wenn der Vorgang fehlschlägt. Anschließend wird das Repository aus der Sicherungsdatei wieder hergestellt, die im *filename* -Argument angegeben ist. Wenn exklusiver Zugriff auf das Repository nicht möglich ist, werden vorhandene Clients von WMI getrennt.

Das *Flag* -Argument muss 1 (die Trennung von Benutzern und Wiederherstellung erzwingen) oder 0 (Standard Wiederherstellung, wenn keine Benutzer verbunden sind) und der Wiederherstellungs Modus sein.

</dd> <dt>

<span id="__________resyncperf__winmgmt-service-process-id_____"></span><span id="__________RESYNCPERF__WINMGMT-SERVICE-PROCESS-ID_____"></span>**/resyncperf** *<WinMgmt-Service-Process-ID>* 
</dt> <dd>

Registriert die Leistungs Bibliotheken des Computers bei WMI. WMI-PID ist die Prozess-ID für den WMI-Dienst.

Nur erforderlich, wenn die System Monitor Klassen keine zuverlässigen Ergebnisse zurückgeben.

</dd> <dt>

<span id="_standalonehost__level_"></span><span id="_STANDALONEHOST__LEVEL_"></span>**/standalonehost**\[*<level>*\]
</dt> <dd>

Verschiebt den WinMgmt-Dienst in einen eigenständigen Svchost-Prozess, der über einen DCOM-Endpunkt mit fester Größe verfügt. Der Standard Endpunkt ist "ncacn \_ IP \_ TCP. 0.24158". Der Endpunkt kann jedoch durch Ausführen von Dcomcnfg.exe geändert werden. Weitere Informationen zum Einrichten eines festgelegten Ports für WMI finden Sie unter [Einrichten eines Fixed-Ports für WMI](setting-up-a-fixed-port-for-wmi.md).

Das *Level* -Argument ist die Authentifizierungs Ebene für den Svchost-Prozess. WMI wird normalerweise als Teil eines Hosts für gemeinsame Dienste ausgeführt, und Sie können die Authentifizierungs Ebene für WMI nicht allein erhöhen. Wenn *Level* nicht angegeben wird, lautet der Standardwert 4 (**RPC-C- \_ \_ authn- \_ Ebene \_ Pkt** oder **wbemauthenticationlevelpkt**).

Sie können WMI sicherer ausführen, indem Sie die Authentifizierungs Ebene auf Paket Datenschutz (**RPC- \_ C- \_ authn- \_ Ebene \_ Pkt \_ Privacy** oder **wbemauthenticationlevelpktprivacy**) erhöhen. Die Authentifizierungs Ebenen für Visual Basic und Skripts werden in [**wbemauthenticationlevelerum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)beschrieben. Informationen zu C++ finden [Sie unter Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von C++](setting-the-default-process-security-level-using-c-.md). Weitere Informationen finden Sie unter Verwalten der [WMI-Sicherheit](maintaining-wmi-security.md).

</dd> <dt>

<span id="_sharedhost"></span><span id="_SHAREDHOST"></span>**/sharedhost**
</dt> <dd>

Verschiebt den WinMgmt-Dienst in den freigegebenen Svchost-Prozess.

</dd> <dt>

<span id="__________verifyrepository__path_____"></span><span id="__________VERIFYREPOSITORY__PATH_____"></span>**/verifyrepository***<path>* 
</dt> <dd>

Führt eine Konsistenzprüfung für das WMI-Repository aus. Wenn Sie den Schalter **/verifyrepository** ohne das- *<path>* Argument hinzufügen, wird das liverepository überprüft, das zurzeit von WMI verwendet wird. Wenn Sie das *path* -Argument angeben, können Sie eine beliebige gespeicherte Kopie des Repository überprüfen. In diesem Fall sollte das path-Argument den vollständigen Pfad zur gespeicherten Repository-Kopie enthalten. Beim gespeicherten Repository sollte es sich um eine Kopie des gesamten Repository-Ordners handeln. Weitere Informationen zu den von diesem Befehl zurückgegebenen Fehlern finden Sie im Abschnitt "Hinweise".

</dd> <dt>

<span id="_salvagerepository"></span><span id="_SALVAGEREPOSITORY"></span>**/salvagerepository**
</dt> <dd>

Führt eine Konsistenzprüfung für das WMI-Repository aus. Wenn eine Inkonsistenz festgestellt wird, wird das Repository neu erstellt. Der Inhalt des inkonsistenten Repository wird in das neu erstellte Repository zusammengeführt, wenn es gelesen werden kann. Der Vorgang "retten" funktioniert immer mit dem Repository, das vom WMI-Dienst zurzeit verwendet wird. Weitere Informationen zu den von diesem Befehl zurückgegebenen Fehlern finden Sie im Abschnitt "Hinweise".

% MOF-Dateien, die die " [**\# pragma Auto Wiederherstellen**](pragma-autorecover.md) "-Präprozessoranweisung enthalten, werden im Repository wieder hergestellt.

</dd> <dt>

<span id="_resetrepository"></span><span id="_RESETREPOSITORY"></span>**/resetrepository**
</dt> <dd>

Das Repository wird bei der Erstinstallation des Betriebssystems auf den ursprünglichen Zustand zurückgesetzt. MOF-Dateien, die die " [**\# pragma Auto Wiederherstellen**](pragma-autorecover.md) "-Präprozessoranweisung enthalten, werden im Repository wieder hergestellt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Dieses Tool befindet sich im Verzeichnis% windir% \\ system32 \\ WBEM. Geben Sie `WinMgmt /?` an der Eingabeaufforderung ein, um eine Liste der verfügbaren Switches zu erhalten.

Das WMI-Repository, das auch als CIM-Repository bezeichnet wird, ist nicht nur eine einzelne Datei, sondern eine Sammlung von Dateien im Repository-Ordner, die als Datenbank zusammenarbeiten. Wenn Sie den **/Backup** -Schalter verwenden, um das Repository zu sichern, ist die resultierende Sicherung eine einzelne komprimierte Datei.

WMI gibt die Fehler **Meldung \_ interner \_ \_** Daten Bank Beschädigung (net helpmsg 1358) zurück, wenn bei einem Überprüfungs Vorgang angegeben ist, dass sich das Repository nicht in einem konsistenten Zustand befindet. Dieser Fehler kann von jedem Befehl zurückgegeben werden, der die Repository-Überprüfung ausführt, z. b. **/verifyrepository** oder **/salvagerepository**.

> [!Note]
>
> Wenn WMI Fehlermeldungen zurückgibt, beachten Sie, dass Sie möglicherweise nicht auf Probleme im WMI-Dienst oder in WMI-Anbietern hinweisen. Fehler können aus anderen Teilen des Betriebssystems stammen und als Fehler über WMI auftreten. Löschen Sie das WMI-Repository unter Umständen nicht als erste Aktion, da das Löschen des Repository zu Beschädigungen des Systems oder der installierten Anwendungen führen kann.
>
> Weitere Informationen zur Ursache des Problems erhalten Sie, indem Sie das Befehlszeilen Tool [WMI-Diagnosehilfsprogramm](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) Diagnose herunterladen und ausführen. Mit diesem Tool wird ein Bericht erstellt, der in der Regel die Ursache des Problems isolieren und Anweisungen zur Behebung des Problems bereitstellen kann. Der Bericht hilft Ihnen auch bei der Unterstützung durch den Microsoft-Support. Sie können den [WMI-Diagnosehilfsprogramm](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d)herunterladen.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WMI-Problembehandlung](wmi-troubleshooting.md)
</dt> <dt>

[Remote Verbindung mit WMI ab Vista](connecting-to-wmi-remotely-starting-with-vista.md)
</dt> </dl>

 

