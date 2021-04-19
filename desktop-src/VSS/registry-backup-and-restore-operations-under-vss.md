---
description: Der Windows-Registrierungsdienst unterstützt eine VSS Writer, die als registrierungswriter bezeichnet wird und es Anforderern ermöglicht, eine Systemregistrierung mithilfe von Daten zu sichern, die auf einem Schatten kopierten Volume gespeichert sind.
ms.assetid: 94a45b04-0bdc-4211-bed0-caeabba774af
title: Sicherungs-und Wiederherstellungs Vorgänge für die Registrierung unter VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db1a3022ec2fb08b07bcff8b28455ae7154e4c40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348933"
---
# <a name="registry-backup-and-restore-operations-under-vss"></a>Sicherungs-und Wiederherstellungs Vorgänge für die Registrierung unter VSS

Der Windows-Registrierungsdienst unterstützt eine VSS Writer, die als registrierungswriter bezeichnet wird und es Anforderern ermöglicht, eine Systemregistrierung mithilfe von Daten zu sichern, die auf einem Schatten kopierten Volume gespeichert sind. Weitere Informationen zum registrierungswriter finden Sie unter [in-Box-VSS-Writer](in-box-vss-writers.md).

Der Registrierungs Schreiber führt direkte Sicherungen und Wiederherstellungen der Registrierung aus. Außerdem meldet der Registrierungs Schreiber nur System Strukturen. Benutzer Strukturen werden nicht gemeldet.

**Windows Server 2003:** Der Registrierungs Schreiber verwendet eine zwischenrepository-Datei (auch als "spuckdatei" bezeichnet) zum Speichern von Registrierungsdaten. Außerdem meldet der Registrierungs Schreiber System Strukturen und Benutzer Strukturen.

Die Writer-ID für den Registrierungs Schreiber lautet AFBAB4A2-367D-4D15-A586-71DBB18F8485.

**Windows XP:** Es ist kein registrierungswriter vorhanden. Die Registrierungsdaten werden vom bootable State Writer berichtet, dessen Writer-ID F2436E37-09F5-41AF-9B2A-4CA2435DBFD5 lautet.

> [!Note]  
> Microsoft bietet keinen technischen Support für Entwickler oder IT-Experten für die Implementierung von Online-Systemstatus Wiederherstellungen unter Windows (alle Versionen). Weitere Informationen zur Verwendung von von Microsoft bereitgestellten APIs und Prozeduren zum Implementieren von Online-Systemstatus Wiederherstellungen finden Sie in den Communityressourcen im [MSDN Community Center](https://msdn.microsoft.com/community/default.aspx).

 

> [!Note]  
> Die folgenden Informationen gelten nur für Windows Server 2003 und Windows XP.

 

## <a name="registry-backup-using-vss"></a>Registrierungs Sicherung mithilfe von VSS

Der registrierungswriter exportiert und speichert aktive Registrierungsdateien an den Speicherorten, die vom Schlüssel **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **hivelist** definiert werden.

Die Namen der Werte unter diesem Registrierungs Eintrag identifizieren die zu speichernde Registrierungs Struktur, und die Daten des Werts enthalten die Datei, die die Datei enthält (die Hive-Datei). Die Hive-Dateien werden im folgenden Format angegeben: \\ Device \\ *harddiskvolumex* \\ *Pfad* \\ *Dateiname*.

Beispielsweise wird unter **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **hivelist** möglicherweise die Geräte **\\ \\ \\ Software**  =  \\ Device \\ HarddiskVolume1 \\ Windows \\ system32 \\ config Software angezeigt \\ .

Der Registrierungs Schreiber stellt sicher, dass Hive-Dateien vor der Schatten Kopie auf dem Datenträger gespeichert werden.

Beim Sichern der Registrierungs Strukturen ersetzt ein Anforderer das \\ Gerät \\ *harddiskvolumex* durch die [*Geräte Objekt*](vssgloss-d.md) Zeichenfolge der Schatten Kopie des Volumes.

> [!Note]  
> Sie können den \\ \\ *harddiskvolumex* -Pfad des Geräts mithilfe der [**querydosdevice**](/windows/win32/api/fileapi/nf-fileapi-querydosdevicew) -Funktion in einen entsprechenden Win32-Pfad konvertieren. Weitere Informationen finden Sie unter Abrufen [eines Datei namens von einem Datei Handle](../memory/obtaining-a-file-name-from-a-file-handle.md) oder [Anzeigen von volumepfadnamen](../fileio/displaying-volume-paths.md).

 

## <a name="registry-restore-using-non-vss-win32-apis"></a>Registrierungs Wiederherstellung mit nicht-VSS-Win32-APIs

Bei einer Online Wiederherstellung (Abgesicherter Modus oder vollständiges Betriebssystem) müssen die untergeordneten Schlüssel im **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Session Manager**" \\ **pdingfilerenameoperations** " gespeichert werden.

Die Funktionen " [**fivefileex**](/windows/win32/api/winbase/nf-winbase-movefileexa) " und " [**muvefiletransall**](/windows/win32/api/winbase/nf-winbase-movefiletransacteda) " verwenden diesen Registrierungsschlüssel zum Speichern von Informationen zu Dateien, die mit dem \_ Wert "verzögerten verzögerten Datei Verzögerung" \_ \_ im Parameter " *dwFlags* " umbenannt wurden.

Um den Inhalt des Registrierungsschlüssels " **pdingfilerenameoperations** " beizubehalten, sollte die Sicherungs Anwendung die [**RegLoadKey**](/windows/win32/api/winreg/nf-winreg-regloadkeya) -Funktion aufrufen, um die wieder herzustellende Registrierungsdatei in der aktiven Registrierung zu verbinden. Die Sicherungs Anwendung kann dann die verschiedenen Registrierungsfunktionen verwenden, um die gewünschten Schlüssel und Werte in die geladene Struktur zu kopieren. Nachdem der Kopiervorgang beendet wurde, sollten die Funktionen [**regflushkey**](/windows/win32/api/winreg/nf-winreg-regflushkey) und [**regunloadkey**](/windows/win32/api/winreg/nf-winreg-regunloadkeya) aufgerufen werden.

Bei einer Offline Wiederherstellung (Windows Recovery Environment oder Windows PE) ist es nicht notwendig, den Registrierungsschlüssel " **pdingfilerenameoperations** " einzuhalten.

## <a name="registry-restore-using-non-vss-win32-apis-in-windows-server-2003"></a>Wiederherstellung der Registrierung mithilfe von nicht-VSS-Win32-APIs in Windows Server 2003

> [!Note]  
> Die folgenden Informationen gelten nur für Wiederherstellungs Vorgänge im Zusammenhang mit der Notfall Wiederherstellung (auch als Bare-Metal-Recovery bezeichnet), die in Windows Server 2003 ausgeführt werden.

 

Beim Wiederherstellen der Registrierung muss eine Sicherungs Anwendung einige der Unterschlüssel aus der aktuellen Registrierung in die wieder herzustellende Registrierung verschieben.

Zu diesem Zweck kann eine Sicherungs Anwendung **RegLoadKey** zum Verbinden der Registrierungsdatei verwenden, die mit der aktuell aktiven Registrierung wieder hergestellt werden soll. Anschließend können die verschiedenen Registrierungsfunktionen verwendet werden, um die gewünschten Schlüssel und Werte in die geladene Struktur zu kopieren. Nachdem der Kopiervorgang beendet wurde, werden **regflushkey** und **regunloadkey** aufgerufen.

Es gibt einen Registrierungsschlüssel, der einer Wiederherstellungs Anwendung (Anforderer) die Registrierungsschlüssel unter **HKEY \_ local \_ Machine \\ System** anzeigt, die zum Zeitpunkt der Wiederherstellung nicht überschrieben werden sollen:

**HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ backuprestore \\ keysnottorestore**

Ein Teil der Wiederherstellung des Systemstatus ist das Wiederherstellen einer zuvor gesicherten Registrierung.

Sicherungs Anwendungen müssen bei der Wiederherstellung der Systemstruktur des **lokalen HKEY \_ \_ \\** -Computers besondere Sorgfalt walten lassen, da bei der Installation einer temporären Version des Windows-Betriebssystems Schlüssel in der neu installierten System Struktur eingerichtet werden, deren Werte den Wiederherstellungs Vorgang überstehen müssen.

Wenn sich beispielsweise das Ersatzsystem eine Netzwerkschnittstellenkarte vom ursprünglichen System unterscheidet, führt das Wiederherstellen der ursprünglichen Schlüssel für die vorherige Karte zu unvorhersehbaren Ergebnissen. Dies liegt daran, dass der Plug & Play Dienst die ordnungsgemäßen Dienst-und Treiber Registrierungseinträge in der Registrierung erkannt und abgelegt hat. Diese Werte müssen beibehalten werden, damit Sie nach der Systemwiederherstellung ordnungsgemäß gestartet werden.

In diesem Abschnitt wird beschrieben, wie Sicherungs Anwendungen ermitteln können, welche Schlüssel und Dateien bei der Ausführung einer Wiederherstellung der **\_ \_ \\ System Struktur des lokalen HKEY** -Computers beibehalten werden müssen. In einigen Fällen umfasst dies Programm gesteuertes Kopieren der Schlüssel aus der neu installierten Installations Struktur in die wieder herzustellende Hive-Struktur. In anderen Fällen ist die Sicherstellung, dass die Registrierungsschlüssel eines Produkts nicht ersetzt werden, so einfach wie das Angeben dieser Schlüssel in der INF-Konfigurationsdatei des Produkts.

Schlüssel (und Schlüsseldaten), die beibehalten werden sollen, werden in der **HKEY- \_ \_ \\ System** Struktur des lokalen Computers aufgelistet.

**HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ backuprestore \\ keysnottorestore**

Schlüssel als Sätze von reg \_ MultiSZ-Zeichen folgen \_ (in diesem Dokument als *Schlüssel* Zeichenfolgen bezeichnet).

Eine Sicherungs Anwendung (Anforderer) muss die Werte dieser Schlüssel in der aktiven Registrierung und der neu wiederhergestellten Registrierung untersuchen, da jede Anwendung oder jeder Dienst Werte jederzeit hinzufügen kann.

Wie Schlüssel Zeichenfolgen von Sicherungs Anwendungen interpretiert werden sollen, hängt von Ihrem Endzeichen ab:

1.  Schlüssel Zeichenfolgen, die mit einem umgekehrten Schrägstrich (" \\ ") beendet werden, werden als Unterschlüssel interpretiert. Wenn eine solche Teil Zeichenfolge gefunden wird, muss die Sicherungs Anwendung alle Daten und alle untergeordneten Schlüssel beibehalten.

    Im folgenden Beispiel wird angegeben, dass alle untergeordneten Schlüssel und Daten bei einem Wiederherstellungs Vorgang beibehalten werden sollen:

    **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services \\ Dmio \\ Boot Info\\**

    Zu diesem Zweck müssen dieser Schlüssel und alle untergeordneten Schlüssel und Daten aus der vorhandenen Registrierung (d. h. der von der Windows-Installation erstellten) in die neu wiederhergestellte Registrierung kopiert werden. Dies wird als *Schlüssel Ersetzungs* Vorgang bezeichnet. Dieser Vorgang ersetzt den entsprechenden Schlüssel in der wiederhergestellten Registrierung.

2.  Schlüssel Zeichenfolgen, deren Beendigungs Zeichen ein Sternchen (" \* ") ist, gibt an, dass alle Unterschlüssel zusammengeführt werden sollen. Beispielsweise ist die Schlüssel Zeichenfolge:

    **HKEY \_ Lokales \_ Computer \\ System \\ CurrentControlSet \\ Services \\ \** _

    Gibt an, dass der Dienst Schlüssel in der vorhandenen Registrierung (z. b. die von der Installation von Windows erstellten) in der wiederhergestellten Registrierung zusammengeführt werden muss. Dies wird als _Key Merge *-Vorgang bezeichnet, und wenn ein Unterschlüssel sowohl in der vorhandenen Hive als auch in der wiederhergestellten Hive vorhanden ist, wird der Schlüssel im wiederhergestellten Verzeichnis mit den folgenden Ausnahmen beibehalten:

    -   , Wenn der Unterschlüssel in der vorhandenen Struktur einen Wert mit dem Namen "Start" enthält und der Unterschlüssel in der wiederhergestellten nicht.
    -   Wenn der Unterschlüssel sowohl in der vorhandenen als auch in der wiederhergestellten Hive einen Wert mit dem Namen "Start" enthält und der numerische Wert in der vorhandenen Hive kleiner ist.

    Der "Start"-Wert in der Registrierung gibt an, wann ein Dienst oder Treiber gestartet wird und einen numerischen Wert von 0-4 aufweisen kann. Je niedriger der Wert ist, desto früher wird der Dienst gestartet.

    Wenn dieser Schlüssel sowohl für das vorhandene als auch das wiederhergestellte Verzeichnis vorhanden ist, müssen Sie den Wert der Start Taste in jeder Hive überprüfen. Wenn der Wert in der vorhandenen Hive niedriger als der Wert im wiederhergestellten Verzeichnis ist, muss der niedrigere Wert beibehalten werden.

    Der Schlüssel wird erneut verwendet, um zu bestimmen, ob ein Dienst oder Treiber bei der Systemzeit, manuell, automatisch oder deaktiviert gestartet werden soll. Der niedrigere Wert stellt eine frühere Startzeit dar. Die frühere Startzeit muss auf die neue Registrierung angewendet werden, um sicherzustellen, dass der Dienst oder die Treiber beim nächsten Start ordnungsgemäß gestartet werden.

3.  Schlüssel Zeichenfolgen, deren Beendigungs Zeichen weder ein umgekehrter Schrägstrich noch ein Sternchen ist, werden als zu erhaltene Registrierungs Werte interpretiert.

    Beispielsweise ist die Schlüssel Zeichenfolge:

    **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ Session Manager \\ pdingfilerenameoperations**

    Der Mechanismus, mit dem Schlüsselprogramm gesteuert aufbewahrt werden können, umfasst die Win32-Registrierungs-API. Beispielsweise ist ein Algorithmus unten aufgeführt:

    1.  Stellen Sie die gesicherte Systemstruktur Datei in einer Datei wieder her. Nennen Sie in diesem Beispiel den Namen System. reg.
    2.  Verwenden Sie **RegLoadKey** , um System. reg unter einem temporären Namen in **den lokalen HKEY- \_ \_ Computer** zu laden. Ein solcher Name könnte z. b. lauten.

        **\_ \_ \\ tmp-System des lokalen \_ HKEY-Computers**

    3.  Zählen Sie die Werte im Unterschlüssel **keysnottorestore** aus beiden Registrierungs Kopien auf, und erstellen Sie eine übergeordnete Gruppe der Listen. Jeden solchen Schlüssel aus dem vorhandenen kopieren

        **lokales HKEY- \_ \_ Computer \\ System**

        Schlüssel in den

        **\_ \_ \\ tmp-System des lokalen \_ HKEY-Computers**

        Schlüssel gemäß der oben beschriebenen Semantik.

    4.  Wenn Sie fertig sind, verwenden Sie die Einstiegspunkte für **regflushkey**  &  **regunloadkey** , um das

        **\_ \_ \\ tmp-System des lokalen \_ HKEY-Computers**

        der Schlüssel wird zurück zu "System. reg".

    5.  Verwenden Sie abschließend **RegReplaceKey** , um anzugeben, dass System. reg das

        **lokales HKEY- \_ \_ Computer \\ System**

        Hive-Datei, System.

 

 
