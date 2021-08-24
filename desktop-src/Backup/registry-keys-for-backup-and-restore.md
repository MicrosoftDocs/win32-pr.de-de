---
title: Registrierungsschlüssel und -werte für Sicherung und Wiederherstellung
ms.assetid: 83449f78-cca1-449b-8c5f-3c8a91c8b3e7
description: Weitere Informationen finden Sie unter Registrierungsschlüssel und -werte für Sicherung und Wiederherstellung.
keywords:
- Sicherungssicherung, Registrierungsschlüssel
- Sicherung von Registrierungsschlüsseln
- CustomPerformanceSettings-Sicherung
- DisableMonitoring Backup
- FilesNotToBackup-Sicherung
- FilesNotToSnapshot-Sicherung
- KeysNotToRestore-Sicherung
- LastInstance-Sicherung
- LastRestoreId-Sicherung
- MaxShadowCopies-Sicherung
- MinDiffAreaFileSize-Sicherung
- OverallPerformanceSetting Backup
- SYSVOL-Sicherung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d825c6588242dccd5df16778de9c590e51b7cdbf6696be4f1a5e40ff2d967c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702190"
---
# <a name="registry-keys-and-values-for-backup-and-restore"></a>Registrierungsschlüssel und -werte für Sicherung und Wiederherstellung

Anwendungen, die Sicherungs- und Wiederherstellungsvorgänge anfordern oder ausführen, sollten die folgenden Registrierungsschlüssel und -werte verwenden, um miteinander oder mit Features wie dem [Volumeschattenkopie-Dienst (VSS)](/windows/desktop/VSS/volume-shadow-copy-service-portal) und dem Windows-Sicherung:

-   [CustomPerformanceSettings](#customperformancesettings)
-   [DisableMonitoring](#disablemonitoring)
-   [FilesNotToBackup](#filesnottobackup)
-   [FilesNotToSnapshot](#filesnottosnapshot)
-   [IdleTimeout](#idletimeout)
-   [KeysNotToRestore](#keysnottorestore)
-   [LastInstance](#lastinstance)
-   [LastRestoreId](#lastrestoreid)
-   [MaxShadowCopies](#maxshadowcopies)
-   [MinDiffAreaFileSize](#mindiffareafilesize)
-   [OverallPerformanceSetting und CustomPerformanceSettings](#overallperformancesetting-and-customperformancesettings)
-   [SYSVOL](#sysvol)

## <a name="customperformancesettings"></a>CustomPerformanceSettings

Weitere Informationen [finden Sie unter OverallPerformanceSetting und CustomPerformanceSettings.](#overallperformancesetting-and-customperformancesettings)

## <a name="disablemonitoring"></a>DisableMonitoring

Auf Windows Clientplattformen, die mit Windows 7 beginnen, werden Benutzer automatisch aufgefordert, das Windows-Sicherung-Feature zu konfigurieren, sofern sie dies noch nicht getan haben. Diese Benachrichtigungen werden zum Startzeit des Computers angezeigt, beginnend sieben Tage nach der Installation des Betriebssystems. Sie werden auch angezeigt, wenn der Benutzer eine Festplatte einsteckt. in diesem Fall werden die Benachrichtigungen sofort angezeigt.

OEMs und Entwickler von Sicherungsanwendungen von Drittanbietern können den **Registrierungswert DisableMonitoring** verwenden, um diese automatischen Benachrichtigungen zu deaktivieren.

Dieser Wert ist standardmäßig nicht vorhanden und muss daher unter dem folgenden Registrierungsschlüssel erstellt werden:

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **WindowsBackup**

Der **Registrierungswert DisableMonitoring** hat den Datentyp REG \_ DWORD und wird wie folgt interpretiert:

-   Wenn die Daten des Werts auf 1 festgelegt sind und Benutzer die Windows-Sicherung nicht bereits konfiguriert haben, werden die automatischen Benachrichtigungen deaktiviert. Wenn bereits eine automatische Benachrichtigung im Action Center vorhanden ist, wird die Benachrichtigung am folgenden Morgen um 10:00 Uhr entfernt, wenn Sie diesen Registrierungswert festlegen.
-   Wenn der Wert nicht vorhanden ist, seine Daten nicht festgelegt sind oder seine Daten auf 0 (null) festgelegt sind, werden die automatischen Benachrichtigungen nicht deaktiviert.

**Windows Vista und Windows XP:** Dieser Registrierungswert wird nicht unterstützt.

## <a name="filesnottobackup"></a>FilesNotToBackup

Der **Registrierungsschlüssel FilesNotToBackup** gibt die Namen der Dateien und Verzeichnisse an, die von Sicherungsanwendungen nicht gesichert oder wiederhergestellt werden sollen. Jeder der Einträge in diesem Schlüssel ist eine REG \_ MULTI \_ SZ-Zeichenfolge im folgenden Format:

\[ \] Laufwerk \[  \] Pfad \\ *FileName* \[ /s\]

-   *Laufwerk* gibt das Laufwerk an und ist optional. Beispiel: c:. Um alle Laufwerke anzugeben, verwenden Sie einen zurücken Schrägstrich ( \\ ); es sind keine Laufwerkbuchstaben erforderlich.
-   *Path* gibt den Pfad an und ist optional. Er darf keine Platzhalterzeichen enthalten.
-   *FileName* gibt die Datei oder das Verzeichnis an und ist erforderlich. Er kann Platzhalterzeichen enthalten.
-   /s gibt an, dass alle Unterverzeichnisse des angegebenen Pfads eingeschlossen werden sollen.
-   Umgebungsvariablen wie %Systemroot% können für die gesamte Zeichenfolge oder einen Teil davon ersetzt werden.

In der folgenden Tabelle sind einige typische Einträge aufgeführt.

| Eintragsname                             | Standardwert                                                                             |
|----------------------------------------|-------------------------------------------------------------------------------------------|
| Internet Explorer                      | Temporäre Dateien                                                                           |
| Speicherseitendatei                       | \\Pagefile.sys                                                                            |
| MS Distributed Transaction Coordinator | C: \\ Windows \\ system32 \\ MSDtc \\ MSDTC. LOG C: \\ Windows \\ system32 \\ MSDtc \\ trace \\ dtctrace.log |
| Offlinedateien Cache                    | %Systemroot% \\ CSC \\ \* /s                                                                  |
| Energieverwaltung                       | \\hiberfil.sys                                                                            |
| Einzelinstanz-Speicherung                | \\SIS Common Store \\ \* . \* /s                                                              |
| Temporäre Dateien                        | %TEMP% \\ \* /s                                                                             |



 

> [!Note]  
> Anwendungen, die Sicherungen auf Volumeebene durchführen, kopieren in der Regel das gesamte Volume auf Blockebene, sodass der **Registrierungsschlüssel FilesNotToBackup** zum Zeitpunkt der Sicherung nicht verwendet werden kann. Stattdessen warten sie bis zur Wiederherstellungszeit, um die Dateien zu löschen, die nicht zu sichern waren. In den meisten Fällen ist dies eine sinnvolle Strategie. Im Fall von Single Instance Storage-Dateien dürfen die SIS Common Store-Dateien zum Zeitpunkt der Wiederherstellung jedoch nicht gelöscht werden.

 

Bei Volumesicherungen auf Blockebene werden Windows Serversicherung und das hilfsprogramm Windows Wbadmin den **Registrierungsschlüssel FilesNotToBackup** verwenden, indem sie die entsprechenden Dateien zur Wiederherstellungszeit löschen. Systemwiederherstellung und Systemstatussicherung verwenden den **Registrierungsschlüssel FilesNotToBackup** nicht.

**Windows XP:** Bei der Systemwiederherstellung wird der **Registrierungsschlüssel FilesNotToBackup** verwendet.

## <a name="filesnottosnapshot"></a>FilesNotToSnapshot

VSS unterstützt den **Registrierungsschlüssel FilesNotToSnapshot.** Anwendungen und Dienste können diesen Schlüssel verwenden, um Dateien anzugeben, die aus neu erstellten Schattenkopien gelöscht werden sollen. Weitere Informationen finden Sie unter [Ausschließen von Dateien aus Schattenkopien.](/windows/desktop/VSS/excluding-files-from-shadow-copies)

**Windows Server 2003 und Windows XP:** Dieser Registrierungsschlüssel wird nicht unterstützt.

Bei Volumesicherungen auf Blockebene Windows Serversicherung den **Registrierungsschlüssel FilesNotToSnapshot,** indem die entsprechenden Dateien zum Zeitpunkt der Wiederherstellung gelöscht werden.

## <a name="idletimeout"></a>IdleTimeout

Der **Registrierungswert IdleTimeout** gibt die Zeit in Sekunden an, die der VSS-Dienst wartet, wenn er sich im Leerlauf befindet. Wenn dieser Timeoutwert erreicht wird und keine Aufgaben dafür auszuführen sind, wird der VSS-Dienst heruntergefahren.

Dieser Registrierungswert finden Sie unter dem folgenden Registrierungsschlüssel:

**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **VSS** \\ **Einstellungen**

Wenn dieser Registrierungswert nicht vorhanden ist:

-   Der tatsächlich verwendete Timeoutwert beträgt standardmäßig 180 Sekunden (3 Minuten).
-   Sie können einen Wert mit dem Namen **IdleTimeout** und dem Typ DWORD erstellen und auf den gewünschten Wert festlegen.

Wenn dieser Registrierungswert auf 0 Sekunden festgelegt ist:

-   Der tatsächlich verwendete Timeoutwert beträgt 180 Sekunden (3 Minuten).

Wenn Sie diesen Registrierungswert festlegen:

-   VSS verwendet den von Ihnen festgelegten Timeoutwert.
-   Sie können einen beliebigen Wert zwischen 1 und FFFFFFFF Sekunden angeben. Es wird jedoch empfohlen, einen Wert zwischen 1 und 180 Sekunden zu wählen.

**Windows Server 2003 und Windows XP:** Dieser Registrierungsschlüssel wird nicht unterstützt.

## <a name="keysnottorestore"></a>KeysNotToRestore

Der **Registrierungsschlüssel KeysNotToRestore** gibt die Namen der Registrierungsunterschlüssel und -werte an, die von Sicherungsanwendungen nicht wiederhergestellt werden sollen. Weitere Informationen finden Sie unter [KeysNotToRestore.](/previous-versions/windows/it-pro/windows-server-2003/cc737538(v=ws.10)) Der **Registrierungsschlüssel KeysNotToRestore** muss nicht berücksichtigt werden.

**Windows Server 2003 und Windows XP:** Sie müssen den **Registrierungsschlüssel KeysNotToRestore** berücksichtigen.

Bei Volumesicherungen auf Blockebene berücksichtigt Windows Serversicherung den **Registrierungsschlüssel KeysNotToRestore,** indem die entsprechenden Dateien zum Zeitpunkt der Wiederherstellung gelöscht werden.

Die Systemstatussicherung berücksichtigt den **Registrierungsschlüssel KeysNotToRestore.**

## <a name="lastinstance"></a>LastInstance

Der **Registrierungswert LastInstance** gibt an, dass ein Bare-Metal-Wiederherstellungsvorgang ausgeführt wurde und dass die Volumes überschrieben, aber nicht formatiert wurden. Weitere Informationen finden Sie unter [Verwenden der automatisierten VSS-Systemwiederherstellung für die Notfallwiederherstellung.](/windows/desktop/VSS/using-vss-automated-system-recovery-for-disaster-recovery)

**Windows Server 2003 und Windows XP:** Dieser Registrierungswert wird nicht unterstützt.

## <a name="lastrestoreid"></a>LastRestoreId

Wenn eine Sicherungsanwendung eine Systemstatuswiederherstellung ausführt, muss sie angeben, dass dies durch Festlegen des **Registrierungswerts LastRestoreId** erfolgt ist. "Systemstatuswiederherstellung" bezieht sich in diesem Fall auf alle Wiederherstellungen, die selektiv Binärdateien und Treiber des Betriebssystems wiederherstellen.

Wenn das gesamte Start- und Systemvolume auf Volumeebene wiederhergestellt wird, darf dieser Wert nicht festgelegt werden.

Wenn der **Registrierungswert LastRestoreId** nicht vorhanden ist, sollte er von der Sicherungsanwendung unter dem folgenden Registrierungsschlüssel erstellt werden:

**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **BackupRestore** \\ **SystemStateRestore**

Erstellen Sie einen Wert mit dem Namen **LastRestoreId,** und geben Sie REG \_ SZ ein. Der Wert sollte ein eindeutiger nicht transparenter Wert sein, z. B. eine GUID.

Wenn eine neue Systemstatuswiederherstellung durchgeführt wird, sollte die Sicherungsanwendung die Daten des **LastRestoreId-Werts** ändern.

Andere Anwendungen, die Systemstatuswiederherstellungen überwachen müssen, sollten die Daten dieses Registrierungswerts speichern. Diese Daten können mit den aktuellen Daten des **LastRestoreId-Registrierungswerts** verglichen werden, um zu bestimmen, ob eine neue Systemstatuswiederherstellung durchgeführt wurde.

**Windows Vista, Windows Server 2003 und Windows XP:** Dieser Registrierungswert wird erst Windows Vista mit Service Pack 1 (SP1) und Windows Server 2008 unterstützt.

## <a name="maxshadowcopies"></a>MaxShadowCopies

Der Registrierungswert **MaxShadowCopies** gibt die maximale Anzahl von [*clientseitig zugänglichen Schattenkopien*](/windows/desktop/VSS/vssgloss-c) an, die auf jedem Volume des Computers gespeichert werden können. Eine auf den Client zugängliche Schattenkopie ist eine Schattenkopie, die mit dem **VSS \_ CTX \_ CLIENT \_ ACCESSIBLE-Wert** der [**\_ VSS \_ SNAPSHOT \_ CONTEXT-Enumeration**](/windows/desktop/api/vss/ne-vss-vss_snapshot_context) erstellt wird. Die über den Client zugänglichen Schattenkopien werden von Schattenkopien für freigegebene Ordner verwendet. Weitere Informationen zu Schattenkopien finden Sie in der [VSS-Dokumentation.](/windows/desktop/VSS/volume-shadow-copy-service-portal)

Wenn der **Registrierungswert MaxShadowCopies** nicht vorhanden ist, kann er von der Sicherungsanwendung unter dem folgenden Registrierungsschlüssel erstellt werden:

**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **VSS** \\ **Einstellungen**

Erstellen Sie einen Wert mit dem Namen **MaxShadowCopies,** und geben Sie DWORD ein. Die Standarddaten für diesen Wert sind 64. Der Mindestwert ist 1. Der Höchstwert ist 512.

> [!Note]  
> Für andere Arten von Schattenkopien gibt es keinen Registrierungswert, der **MaxShadowCopies** entspricht. Die maximale Anzahl von Schattenkopien beträgt 512 pro Volume.

 

**Hinweis**  Die Einstellung **MaxShadowCopies** wird auf Windows Server 2003 oder höher unterstützt.

**Windows Server 2003:** Auf Clusterservern müssen die Daten des **Registrierungswerts MaxShadowCopies** möglicherweise auf eine niedrigere Zahl festgelegt werden. Weitere Informationen finden Sie unter "Wenn Sie die Volumeschattenkopie-Dienst auf Windows Server 2003-basierten Computern verwenden, auf denen viele E/A-Vorgänge ausgeführt werden, dauert es länger, bis Datenträgervolumes online geschaltet sind" im Knowledge Base Hilfe und Support unter [https://support.microsoft.com/kb/945058](https://support.microsoft.com/kb/945058) .

**Windows XP:** Dieser Registrierungswert wird nicht unterstützt.

## <a name="mindiffareafilesize"></a>MinDiffAreaFileSize

[VSS](/windows/desktop/VSS/volume-shadow-copy-service-portal) weist einen Schattenkopiespeicherbereich (oder "Diffbereich") zu, um Daten für Schattenkopien zu speichern. Die Mindestgröße des Schattenkopiespeicherbereichs ist eine Computereinstellung, die mit dem Registrierungswert **MinDiffAreaFileSize** angegeben werden kann.

Wenn der Registrierungswert **MinDiffAreaFileSize** nicht festgelegt ist, beträgt die Mindestgröße des Schattenkopiespeicherbereichs 32 MB für Volumes, die kleiner als 500 MB sind, und 320 MB für Volumes, die größer als 500 MB sind.

**Windows Server 2008, Windows Server 2003 mit SP1 und Windows Vista:** Wenn der Registrierungswert **MinDiffAreaFileSize** nicht festgelegt ist, hat der Schattenkopiespeicherbereich eine Mindestgröße von 300 MB. Wenn der Registrierungswert **MinDiffAreaFileSize** festgelegt ist, müssen die Daten zwischen 300 MB und 3000 MB (3 GB) liegen, und es muss ein Vielfaches von 300 MB sein.

**Windows Server 2003:** Wenn der Registrierungswert **MinDiffAreaFileSize** nicht festgelegt ist, beträgt die Mindestgröße des Schattenkopiespeicherbereichs 100 MB.

**Windows XP:** Dieser Registrierungswert wird nicht unterstützt.

Wenn der Registrierungswert **MinDiffAreaFileSize** nicht vorhanden ist, kann er von der Sicherungsanwendung unter dem folgenden Registrierungsschlüssel erstellt werden:

**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **VolSnap**

Erstellen Sie einen Wert mit dem Namen **MinDiffAreaFileSize,** und geben Sie REG \_ DWORD ein. Die Daten für diesen Schlüssel werden in Megabyte angegeben. 320 ist gleich 320 MB und 3200 gleich 3,2 GB. Sie sollten eine Zahl angeben, die ein Vielfaches von 32 ist. Wenn Sie einen Wert angeben, der kein Vielfaches von 32 ist, wird das nächste Vielfache von 32 verwendet.

Schattenkopien funktionieren möglicherweise nicht ordnungsgemäß, wenn der Registrierungswert **MinDiffAreaFileSize** eine Mindestgröße angibt, die größer als die maximale Größe des Schattenkopiespeicherbereichs ist. Verwenden Sie vssadmin add shadowstorage oder den Befehl [Vssadmin](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) resize shadowstorage, um die maximale Größe des Schattenkopiespeicherbereichs anzugeben. Verwenden Sie den Befehl [Vssadmin list shadowstorage,](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) um die aktuelle maximale Größe anzuzeigen. Wenn Sie keine maximale Größe festgelegt haben, gibt es keine Beschränkung für den Speicherplatz, der verwendet werden kann.

## <a name="overallperformancesetting-and-customperformancesettings"></a>OverallPerformanceSetting und CustomPerformanceSettings

Die Registrierungswerte **OverallPerformanceSetting** und **CustomPerformanceSettings** werden verwendet, um Leistungseinstellungen für Windows Serversicherung anzugeben. Diese Registrierungswerte werden nur auf Windows Serverbetriebssystemen unterstützt.

**Windows Server 2003:** Diese Registrierungswerte werden nicht unterstützt.

Wenn diese Registrierungswerte nicht vorhanden sind, kann die Sicherungsanwendung sie unter dem folgenden Registrierungsschlüssel erstellen:

**HKEY \_ LOKALE \_ COMPUTERSOFTWARE** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Windows Sicherung auf Blockebene**

Um Leistungseinstellungen für alle Volumes anzugeben, erstellen Sie einen Wert mit dem Namen **OverallPerformanceSetting,** und geben Sie REG \_ DWORD ein. Die Daten des Werts sollten auf einen der folgenden Werte festgelegt werden.

| Wert | Bedeutung                                                                                                                                                                                                                                   |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Normale Sicherungsleistung (mithilfe vollständiger Sicherungen). Diese Einstellung entspricht der Leistungseinstellung Normale Sicherung, die unter [Optimieren der Sicherung und Serverleistung](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd759145(v=ws.11))beschrieben wird.            |
| 2     | Schnellere Sicherungsleistung (mit inkrementellen Sicherungen). Diese Einstellung entspricht der Leistungseinstellung Schnellere Sicherung, die unter [Optimieren der Sicherung und Serverleistung](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd759145(v=ws.11))beschrieben wird.     |
| 3     | Benutzerdefinierte Sicherungsleistung (durch Angabe einer Leistungseinstellung für jedes Volume). Diese Einstellung entspricht der benutzerdefinierten Einstellung, die unter [Optimieren der Sicherung und Serverleistung](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd759145(v=ws.11))beschrieben wird. |



 

Wenn Sie **OverallPerformanceSetting** auf 3 festlegen, müssen Sie auch einstellungen für die Leistung für jedes Volume einzeln angeben. Erstellen Sie hierzu einen Wert mit dem Namen **CustomPerformanceSettings,** und geben Sie REG \_ MULTI SZ \_ ein. Die Daten dieses Werts sollten wie folgt festgelegt werden:

-   Jede Zeichenfolge in der REG \_ MULTI \_ SZ-Zeichenfolgensequenz enthält die Einstellung für ein Volume.
-   Jede Zeichenfolge besteht aus einer Volume-GUID, gefolgt von einem Komma und einem DWORD-Wert.
-   Jeder DWORD-Wert ist entweder 1 (vollständige Sicherung) oder 2 (inkrementelle Sicherung).

Angenommen, der Computer verfügt über zwei Volumes:

-   Die beiden Volumes sind C: \\ und D: \\ .
-   Die GUID für Volume C: \\ ist 07c473ca4-2df8-11de-9d80-806e6f6e6963, und die GUID für Volume D: \\ ist 0ac22ea6c-712f-11de-adb0-00215a67606e.
-   Sie möchten die normale Sicherungsleistung für Volume C: \\ und eine schnellere Sicherungsleistung für Volume D: \\ angeben.

Hierzu legen Sie **OverallPerformanceSetting** auf 3 und **CustomPerformanceSettings** auf "07c473ca4-2df8-11de-9d80-806e6f6e6963,1 \\ 00ac22ea6c-712f-11de-adb0-00215a67606e,2" fest.

Wenn Sie **OverallPerformanceSetting** auf 1 oder 2 festlegen, werden die Daten im **CustomPerformanceSettings-Wert** ignoriert.

## <a name="sysvol"></a>SYSVOL

Der **SYSVOL-Registrierungswert** ist eine Möglichkeit, den DFSR-Dienst (verteiltes Dateisystem Replication) darüber zu informieren, dass ein Wiederherstellungsvorgang für den Systemstatus initiiert wurde. Jede Sicherungsanwendung, die die Systemstatuswiederherstellung von SYSVOL ausführt, sollte diesen Wert verwenden, um anzugeben, ob der Wiederherstellungsvorgang autoritativ oder nicht autoritativ ist. Dieser Wert wird vom DFSR-Dienst gelesen. Wenn dieser Wert nicht festgelegt ist, wird die SYSVOL-Wiederherstellung standardmäßig nicht autoritativ ausgeführt.

Wenn der **SYSVOL-Registrierungswert** nicht vorhanden ist, sollte er von der Sicherungsanwendung unter dem folgenden Registrierungsschlüssel erstellt werden:

**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **DFSR** \\ **Restore**

Erstellen Sie einen Wert mit dem Namen **SYSVOL,** und geben Sie REG \_ SZ ein. Die Daten des Werts sollten basierend auf der Anforderung des Systemadministrators entweder auf "autoritativ" oder "nicht autoritativ" festgelegt werden.

**Windows Vista, Windows Server 2003 und Windows XP:** Dieser Registrierungswert wird nicht unterstützt.

 

 
