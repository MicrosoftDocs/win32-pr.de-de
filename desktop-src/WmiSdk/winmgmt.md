---
description: Winmgmt ist der WMI-Dienst innerhalb des SVCHOST-Prozesses, der unter der &\# 0034 ausgeführt wird. LocalSystem&\# 0034;-Konto.
ms.assetid: 3923322a-3acb-407e-8a07-09c59d252e8b
ms.tgt_platform: multiple
title: winmgmt
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
ms.openlocfilehash: 455c48cce10d048fa77cde638955899d1ab4fd33a90ee7c59e063916e2a77de0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120740"
---
# <a name="winmgmt"></a>winmgmt

Winmgmt ist der WMI-Dienst innerhalb des SVCHOST-Prozesses, der unter dem Konto "LocalSystem" ausgeführt wird.

In allen Fällen wird der WMI-Dienst automatisch gestartet, wenn die erste Verwaltungsanwendung oder das erste Skript eine Verbindung mit einem WMI-Namespace anfordert. Weitere Informationen finden Sie unter [Starten und Beenden des WMI-Diensts](starting-and-stopping-the-wmi-service.md).

> [!Note]  
> WMI ist eine Kernkomponente des Windows Betriebssystems, mit der Entwickler und IT-Administratoren Skripts und Anwendungen schreiben können, um bestimmte Aufgaben zu automatisieren. Winmgmt.exe ist der Dienst, mit dem WMI auf Ihrem lokalen Computer ausgeführt werden kann. Weitere Informationen zur Verwendung von WMI finden Sie unter [Verwenden von WMI.](using-wmi.md) Wenn Sie eine Fehlermeldung zu winmgmt.exe erhalten haben, finden Sie weitere Informationen unter [WMI-Problembehandlung.](wmi-troubleshooting.md) Weitere Informationen zu Winmgmt.exe finden Sie unter [Verwenden von WMI-Verwaltungstools.](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10))

 

Wenn der WMI-Dienst über die Eingabeaufforderung ausgeführt wird, verfügt er über die folgenden Schalter.

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

## <a name="switches"></a>Optionen

<dl> <dt>

<span id="__________backup__filename_________"></span><span id="__________BACKUP__FILENAME_________"></span>**/backup***<filename>* 
</dt> <dd>

Bewirkt, dass WMI das Repository unter dem angegebenen Dateinamen gesichert. Das *Filename-Argument* sollte den vollständigen Pfad zum Dateispeicherort enthalten. Dieser Prozess erfordert eine Schreibsperre für das Repository, damit Schreibvorgänge für das Repository angehalten werden, bis der Sicherungsvorgang abgeschlossen ist.

Wenn Sie keinen Pfad für die Datei angeben, wird sie im Verzeichnis %Windir% \\ System32 abgelegt.

</dd> <dt>

<span id="__________restore__filename____flag_____"></span><span id="__________RESTORE__FILENAME____FLAG_____"></span>**/restore** *<filename>**<flag>* 
</dt> <dd>

Stellt das WMI-Repository manuell aus der angegebenen Sicherungsdatei wieder her. Das *Filename-Argument* sollte den vollständigen Pfad zum Speicherort der Sicherungsdatei enthalten. Um den Wiederherstellungsvorgang auszuführen, speichert WMI das vorhandene Repository zum Zurückschreiben, wenn der Vorgang fehlschlägt. Anschließend wird das Repository aus der Sicherungsdatei wiederhergestellt, die im *Argument filename* angegeben ist. Wenn der exklusive Zugriff auf das Repository nicht möglich ist, werden vorhandene Clients von WMI getrennt.

Das *Flagargument* muss 1 (Erzwingen der Trennung von Benutzern und Wiederherstellung) oder 0 (Standardwiederherstellung, wenn keine Benutzer verbunden sind) sein und gibt den Wiederherstellungsmodus an.

</dd> <dt>

<span id="__________resyncperf__winmgmt-service-process-id_____"></span><span id="__________RESYNCPERF__WINMGMT-SERVICE-PROCESS-ID_____"></span>**/resyncperf** *<winmgmt-service-process-id>* 
</dt> <dd>

Registriert die Leistungsbibliotheken des Computers bei WMI. WMI PID ist die Prozess-ID für den WMI-Dienst.

Nur erforderlich, wenn die Leistungsüberwachungsklassen keine zuverlässigen Ergebnisse zurückgeben.

</dd> <dt>

<span id="_standalonehost__level_"></span><span id="_STANDALONEHOST__LEVEL_"></span>**/standalonehost**\[*<level>*\]
</dt> <dd>

Verschiebt den Winmgmt-Dienst in einen eigenständigen Svchost-Prozess mit einem festen DCOM-Endpunkt. Der Standardendpunkt ist "ncacn \_ ip \_ tcp.0.24158". Der Endpunkt kann jedoch durch Ausführen von Dcomcnfg.exe geändert werden. Weitere Informationen zum Einrichten eines festen Ports für WMI finden Sie unter [Einrichten eines festen Ports für WMI.](setting-up-a-fixed-port-for-wmi.md)

Das *level-Argument* ist die Authentifizierungsebene für den Svchost-Prozess. WMI wird normalerweise als Teil eines freigegebenen Diensthosts ausgeführt, und Sie können die Authentifizierungsebene für WMI nicht allein erhöhen. Wenn *level* nicht angegeben ist, ist der Standardwert 4 (**RPC C \_ \_ AUTHN \_ LEVEL \_ PKT** oder **WbemAuthenticationLevelPkt**).

Sie können WMI sicherer ausführen, indem Sie die Authentifizierungsebene auf Paketdatenschutz erhöhen (**RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY** oder **WbemAuthenticationLevelPktPrivacy**). Die Authentifizierungsebenen für Visual Basic und Skripts werden in [**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)beschrieben. Informationen zu C++ finden Sie unter [Festlegen der Standardprozesssicherheitsstufe mit C++](setting-the-default-process-security-level-using-c-.md). Weitere Informationen finden Sie unter [Verwalten der WMI-Sicherheit.](maintaining-wmi-security.md)

</dd> <dt>

<span id="_sharedhost"></span><span id="_SHAREDHOST"></span>**/sharedhost**
</dt> <dd>

Verschiebt den Winmgmt-Dienst in den freigegebenen Svchost-Prozess.

</dd> <dt>

<span id="__________verifyrepository__path_____"></span><span id="__________VERIFYREPOSITORY__PATH_____"></span>**/verifyrepository***<path>* 
</dt> <dd>

Führt eine Konsistenzprüfung für das WMI-Repository aus. Wenn Sie den Schalter **/verifyrepository** ohne das *<path>* -Argument hinzufügen, wird das aktuell von WMI verwendete Liverepository überprüft. Wenn Sie das *Path-Argument* angeben, können Sie jede gespeicherte Kopie des Repositorys überprüfen. In diesem Fall sollte das path-Argument den vollständigen Pfad zur gespeicherten Repositorykopie enthalten. Das gespeicherte Repository sollte eine Kopie des gesamten Repositoryordners sein. Weitere Informationen zu Fehlern, die von diesem Befehl zurückgegeben werden, finden Sie im Abschnitt Hinweise.

</dd> <dt>

<span id="_salvagerepository"></span><span id="_SALVAGEREPOSITORY"></span>**/salvagerepository**
</dt> <dd>

Führt eine Konsistenzprüfung für das WMI-Repository aus. Wenn eine Inkonsistenz erkannt wird, wird das Repository neu erstellt. Der Inhalt des inkonsistenten Repositorys wird mit dem neu erstellten Repository zusammengeführt, wenn es gelesen werden kann. Der Salvage-Vorgang funktioniert immer mit dem Repository, das der WMI-Dienst derzeit verwendet. Weitere Informationen zu Fehlern, die von diesem Befehl zurückgegeben werden, finden Sie im Abschnitt Hinweise.

% MOF-Dateien, die die Präprozessor-Anweisung [**\# pragma autorecover**](pragma-autorecover.md) enthalten, werden im Repository wiederhergestellt.

</dd> <dt>

<span id="_resetrepository"></span><span id="_RESETREPOSITORY"></span>**/resetrepository**
</dt> <dd>

Das Repository wird auf den ursprünglichen Zustand zurückgesetzt, wenn das Betriebssystem zum ersten Mal installiert wird. MOF-Dateien, die die Präprozessor-Anweisung [**\# pragma autorecover**](pragma-autorecover.md) enthalten, werden im Repository wiederhergestellt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Dieses Tool befindet sich im Verzeichnis %Windir% \\ System32 \\ wbem. Geben Sie an der Eingabeaufforderung ein, um eine Liste der verfügbaren Switches `WinMgmt /?` anzuzeigen.

Das WMI-Repository, auch als CIM-Repository bezeichnet, ist nicht nur eine einzelne Datei, sondern eine Sammlung von Dateien im Repositoryordner, die als Datenbank zusammenarbeiten. Wenn Sie den Schalter **/backup** zum Sichern des Repositorys verwenden, ist die resultierende Sicherung eine einzelne komprimierte Datei.

WMI gibt den Fehler **ERROR \_ INTERNAL DB \_ \_ CORRUPTION** (net helpmsg 1358) zurück, wenn ein Überprüfungsvorgang angibt, dass sich das Repository nicht in einem konsistenten Zustand befindet. Dieser Fehler kann von jedem Befehl zurückgegeben werden, der die Repositoryüberprüfung durchführt, z. B. **/verifyrepository** oder **/salvagerepository.**

> [!Note]
>
> Wenn WMI Fehlermeldungen zurückgibt, beachten Sie, dass sie möglicherweise keine Probleme im WMI-Dienst oder in WMI-Anbietern angeben. Fehler können aus anderen Teilen des Betriebssystems stammen und über WMI als Fehler auftreten. Löschen Sie das WMI-Repository unter keinen Umständen als erste Aktion, da das Löschen des Repositorys Schäden am System oder an installierten Anwendungen verursachen kann.
>
> Um weitere Informationen zur Ursache des Problems zu finden, laden Sie das [Befehlszeilentool für die WMI-Diagnosehilfsprogramm](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) Diagnose herunter, und führen Sie es aus. Dieses Tool erstellt einen Bericht, der in der Regel die Ursache des Problems isolieren und Anweisungen zur Behebung des Problems bereitstellen kann. Der Bericht unterstützt auch microsoft-Supportdienste bei der Unterstützung. Sie können die [WMI-Diagnosehilfsprogramm](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d)herunterladen.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WMI-Problembehandlung](wmi-troubleshooting.md)
</dt> <dt>

[Herstellen einer Remoteverbindung mit WMI ab Vista](connecting-to-wmi-remotely-starting-with-vista.md)
</dt> </dl>

 

