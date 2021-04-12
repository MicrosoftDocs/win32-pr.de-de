---
title: Registrierungsschlüssel und-Werte für die Sicherung und Wiederherstellung
ms.assetid: 83449f78-cca1-449b-8c5f-3c8a91c8b3e7
description: 'Weitere Informationen finden Sie unter: Registrierungsschlüssel und-Werte für die Sicherung und Wiederherstellung.'
keywords:
- Sicherungs Sicherung, Registrierungsschlüssel
- Sicherung von Registrierungs Schlüsseln
- Customperformancesettings-Sicherung
- Deaktivieren der Sicherung
- Filesnotto Backup-Sicherung
- Filesnotblosnapshot-Sicherung
- Keysnottorestore-Sicherung
- LastInstance-Sicherung
- Lastrestoreid-Sicherung
- Maxshadowkopien-Sicherung
- MinDiffAreaFileSize-Sicherung
- Overallperformanceseup-Sicherung
- SYSVOL-Sicherung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef9796ff96efbc20ac90de6d26a0c1bac7b17633
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127660"
---
# <a name="registry-keys-and-values-for-backup-and-restore"></a>Registrierungsschlüssel und-Werte für die Sicherung und Wiederherstellung

Anwendungen, die Sicherungs-und Wiederherstellungs Vorgänge anfordern oder ausführen, sollten die folgenden Registrierungsschlüssel und-Werte verwenden, um miteinander oder mit Features wie dem [Volumeschattenkopie-Dienst (VSS)](/windows/desktop/VSS/volume-shadow-copy-service-portal) und der Windows-Sicherung zu kommunizieren:

-   [Customperformancesettings](#customperformancesettings)
-   [Disablemonitoring](#disablemonitoring)
-   [Filesnotto Backup](#filesnottobackup)
-   ["Filesnotto Snapshot"](#filesnottosnapshot)
-   [IdleTimeout](#idletimeout)
-   [Keysnottorestore](#keysnottorestore)
-   [LastInstance](#lastinstance)
-   [Lastrestoreid](#lastrestoreid)
-   [MaxShadowCopies](#maxshadowcopies)
-   [MinDiffAreaFileSize](#mindiffareafilesize)
-   [Overallperformancesetts und customperformancesettings](#overallperformancesetting-and-customperformancesettings)
-   [SYSVOL](#sysvol)

## <a name="customperformancesettings"></a>Customperformancesettings

Weitere Informationen finden Sie unter [overallperformancesetts und customperformancesettings](#overallperformancesetting-and-customperformancesettings).

## <a name="disablemonitoring"></a>Disablemonitoring

Auf Windows-Client Plattformen ab Windows 7 werden Benutzer automatisch aufgefordert, das Windows-Sicherungs Feature zu konfigurieren, sofern dies nicht bereits geschehen ist. Diese Benachrichtigungen werden bei der Startzeit des Computers angezeigt, beginnend sieben Tage nach der Installation des Betriebssystems. Sie werden auch angezeigt, wenn der Benutzer ein Festplattenlaufwerk einfügt. in diesem Fall werden die Benachrichtigungen sofort angezeigt.

OEMs und Entwickler von Sicherungs Anwendungen von Drittanbietern können den Registrierungs Wert " **disablemonitoring** " verwenden, um diese automatischen Benachrichtigungen zu deaktivieren.

Dieser Wert ist standardmäßig nicht vorhanden und muss daher unter folgendem Registrierungsschlüssel erstellt werden:

**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **WindowsBackup**

Der Registrierungs Wert **disablemonitoring** weist den Datentyp reg \_ DWORD auf und wird wie folgt interpretiert:

-   Wenn die Daten des Werts auf 1 festgelegt sind und die Benutzer das Windows-Sicherungs Feature nicht bereits konfiguriert haben, werden die automatischen Benachrichtigungen deaktiviert. Wenn eine automatische Benachrichtigung bereits im Wartungs Center vorhanden ist, wird durch Festlegen dieses Registrierungs Werts die Benachrichtigung am nächsten Morgen um 10:00 entfernt.
-   Wenn der Wert nicht vorhanden ist, wenn die Daten nicht festgelegt sind oder wenn die Daten auf NULL festgelegt sind, werden die automatischen Benachrichtigungen nicht deaktiviert.

**Windows Vista und Windows XP:** Dieser Registrierungs Wert wird nicht unterstützt.

## <a name="filesnottobackup"></a>Filesnotto Backup

Mit dem Registrierungsschlüssel **FilesNotToBackup** werden die Namen der Dateien und Verzeichnisse angegeben, die von Sicherungs Anwendungen nicht gesichert oder wieder hergestellt werden sollen. Bei allen Einträgen in diesem Schlüssel handelt es sich um eine reg \_ \_ MultiSZ-Zeichenfolge im folgenden Format:

\[ \] Laufwerk \[  \] Pfad \\ *Dateiname* \[ /s\]

-   *Laufwerk* gibt das Laufwerk an und ist optional. Beispiel: c: Um alle Laufwerke anzugeben, verwenden Sie einen umgekehrten Schrägstrich ( \) es sind keine Laufwerk Buchstaben erforderlich.
-   *Path* gibt den Pfad an und ist optional. Er darf keine Platzhalter Zeichen enthalten.
-   *Dateiname* gibt die Datei oder das Verzeichnis an und ist erforderlich. Sie kann Platzhalter Zeichen enthalten.
-   /s gibt an, dass alle Unterverzeichnisse des angegebenen Pfads eingeschlossen werden sollen.
-   Umgebungsvariablen wie% SystemRoot% können die gesamte Zeichenfolge oder einen Teil davon ersetzen.

In der folgenden Tabelle sind einige typische Einträge aufgeführt.

| Eintrags Name                             | Standardwert                                                                             |
|----------------------------------------|-------------------------------------------------------------------------------------------|
| Internet Explorer                      | Temporäre Dateien                                                                           |
| Speicher Auslagerungs Datei                       | \\Pagefile.sys                                                                            |
| MS Distributed Transaction Coordinator | C: \\ Windows \\ system32 \\ MSDTC \\ MSDTC. Log C: \\ Windows \\ system32 \\ MSDTC-Ablauf \\ Verfolgung \\ dtctrace. log |
| Offlinedateien Cache                    | % Systemroot% \\ csc \\ \* /s                                                                  |
| Energieverwaltung                       | \\hiberfil.sys                                                                            |
| Einzelinstanz-Speicherung                | \\SIS Common Store \\ \* . \* /s                                                              |
| Temporäre Dateien                        | % Temp% \\ \* /s                                                                             |



 

> [!Note]  
> Anwendungen, die Sicherungen auf Volumeebene ausführen, werden in der Regel durch Kopieren des gesamten Volumes auf Blockebene durchgeführt, sodass der Registrierungsschlüssel " **FilesNotToBackup** " beim Sicherungs Zeitpunkt nicht berücksichtigt werden kann. Stattdessen warten Sie, bis die Wiederherstellungszeit zum Löschen der Dateien, die nicht gesichert werden konnten, gelöscht werden. In den meisten Fällen ist dies eine sinnvolle Strategie. Im Fall von einzelinstanzspeicherdateien dürfen die allgemeinen SIS-Speicherdateien zum Zeitpunkt der Wiederherstellung jedoch nicht gelöscht werden.

 

Bei Volumesicherungen auf Blockebene beachten Windows Server-Sicherung und das Windows Wbadmin-Hilfsprogramm den Registrierungsschlüssel **FilesNotToBackup** , indem die entsprechenden Dateien zum Zeitpunkt der Wiederherstellung gelöscht werden. Bei der Systemwiederherstellung und der Systemstatus Sicherung wird der Registrierungsschlüssel " **FilesNotToBackup** " nicht berücksichtigt.

**Windows XP:** Bei der System Wiederherstellung wird der Registrierungsschlüssel " **FilesNotToBackup** " berücksichtigt.

## <a name="filesnottosnapshot"></a>"Filesnotto Snapshot"

VSS unterstützt den Registrierungsschlüssel " **filesnottosnapshot** ". Anwendungen und Dienste können diesen Schlüssel verwenden, um Dateien anzugeben, die aus neu erstellten Schatten Kopien gelöscht werden sollen. Weitere Informationen finden Sie unter [Ausschließen von Dateien aus Schatten Kopien](/windows/desktop/VSS/excluding-files-from-shadow-copies).

**Windows Server 2003 und Windows XP:** Dieser Registrierungsschlüssel wird nicht unterstützt.

Bei Volumesicherungen auf Blockebene berücksichtigt Windows Server-Sicherung den Registrierungsschlüssel **filesnottosnapshot** , indem die entsprechenden Dateien zum Zeitpunkt der Wiederherstellung gelöscht werden.

## <a name="idletimeout"></a>IdleTimeout

Der Registrierungs Wert **IdleTimeout** gibt die Zeitspanne in Sekunden an, die der VSS-Dienst wartet, wenn er sich im Leerlauf befindet. Wenn dieser Timeout Wert erreicht wird und keine Aufgaben ausgeführt werden können, wird der VSS-Dienst heruntergefahren.

Dieser Registrierungs Wert befindet sich unter dem folgenden Registrierungsschlüssel:

**HKEY \_ Lokale \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **VSS**- \\ **Einstellungen**

Wenn dieser Registrierungs Wert nicht vorhanden ist:

-   Der tatsächliche Timeout Wert, der standardmäßig verwendet wird, beträgt 180 Sekunden (3 Minuten).
-   Sie können einen Wert mit dem Namen **IdleTimeout** und dem Typ DWORD erstellen und ihn auf den gewünschten Wert festlegen.

Wenn dieser Registrierungs Wert auf 0 Sekunden festgelegt ist:

-   Der tatsächlich verwendete Timeout Wert beträgt 180 Sekunden (3 Minuten).

Wenn Sie diesen Registrierungs Wert festlegen:

-   VSS verwendet den von Ihnen festgelegten Timeout Wert.
-   Sie können einen beliebigen Wert zwischen 1 und FFFFFFFF Sekunden angeben. Es wird jedoch empfohlen, einen Wert zwischen 1 und 180 Sekunden auszuwählen.

**Windows Server 2003 und Windows XP:** Dieser Registrierungsschlüssel wird nicht unterstützt.

## <a name="keysnottorestore"></a>Keysnottorestore

Der Registrierungsschlüssel **keysnottorestore** gibt die Namen der Registrierungs Unterschlüssel und-Werte an, die von Sicherungs Anwendungen nicht wieder hergestellt werden sollten. Weitere Informationen finden Sie unter [keysnottorestore](/previous-versions/windows/it-pro/windows-server-2003/cc737538(v=ws.10)). Der Registrierungsschlüssel **keysnottorestore** muss nicht beachtet werden.

**Windows Server 2003 und Windows XP:** Sie müssen den Registrierungsschlüssel **keysnottorestore** berücksichtigen.

Bei Volumesicherungen auf Blockebene berücksichtigt Windows Server-Sicherung den Registrierungsschlüssel **keysnottorestore** , indem die entsprechenden Dateien zum Zeitpunkt der Wiederherstellung gelöscht werden.

Bei der System Status Sicherung wird der Registrierungsschlüssel " **keysnottorestore** " berücksichtigt.

## <a name="lastinstance"></a>LastInstance

Der **LastInstance** -Registrierungs Wert gibt an, dass ein Bare-Metal-Wiederherstellungs Vorgang durchgeführt wurde und dass die Volumes überschrieben, aber nicht formatiert wurden. Weitere Informationen finden Sie unter [Verwenden der automatisierten VSS-System Wiederherstellung für die Notfall Wiederherstellung](/windows/desktop/VSS/using-vss-automated-system-recovery-for-disaster-recovery).

**Windows Server 2003 und Windows XP:** Dieser Registrierungs Wert wird nicht unterstützt.

## <a name="lastrestoreid"></a>Lastrestoreid

Wenn eine Sicherungs Anwendung eine Systemstatus Wiederherstellung ausführt, muss Sie darauf hinweisen, dass dies durch Festlegen des **lastrestoreid** -Registrierungs Werts erreicht wurde. "System Status Wiederherstellung" bezieht sich in diesem Fall auf eine beliebige Wiederherstellung, mit der Betriebs System Binärdateien und Treiber selektiv wieder hergestellt werden.

Wenn der gesamte Start-und System Volume auf der Volumeebene wieder hergestellt wird, darf dieser Wert nicht festgelegt werden.

Wenn der **lastrestoreid** -Registrierungs Wert nicht vorhanden ist, sollte die Sicherungs Anwendung ihn unter dem folgenden Registrierungsschlüssel erstellen:

**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **backuprestore** \\ **systemstaterestore**

Erstellen Sie einen Wert mit dem Namen " **lastrestoreid** " und dem Typ "reg \_ SZ". Der Wert muss ein eindeutiger, nicht transparenter Wert sein, z. b. eine GUID.

Wenn eine neue Systemstatus Wiederherstellung durchgeführt wird, sollte die Sicherungs Anwendung die Daten des **lastrestoreid** -Werts ändern.

Andere Anwendungen, die Systemstatus Wiederherstellungen überwachen müssen, sollten die Daten dieses Registrierungs Werts speichern. Diese Daten können mit den aktuellen Daten des Registrierungs Werts **lastrestoreid** verglichen werden, um zu bestimmen, ob eine neue Systemstatus Wiederherstellung durchgeführt wurde.

**Windows Vista, Windows Server 2003 und Windows XP:** Dieser Registrierungs Wert wird bis Windows Vista mit Service Pack 1 (SP1) und Windows Server 2008 nicht unterstützt.

## <a name="maxshadowcopies"></a>MaxShadowCopies

Der Registrierungs Wert **maxshadowkopien** gibt die maximale Anzahl von [*Client zugänglichen Schatten Kopien*](/windows/desktop/VSS/vssgloss-c) an, die auf jedem Volume des Computers gespeichert werden können. Eine vom Client zugängliche Schatten Kopie ist eine Schatten Kopie, die mithilfe des **VSS \_ ctx- \_ Clients \_** , auf den zugegriffen werden kann, der [**\_ VSS- \_ Momentaufnahme \_ Kontext**](/windows/desktop/api/vss/ne-vss-vss_snapshot_context) -Enumeration erstellt wird. Die über den Client zugänglichen Schattenkopien werden von Schattenkopien für freigegebene Ordner verwendet. Weitere Informationen zu Schatten Kopien finden Sie in der [VSS](/windows/desktop/VSS/volume-shadow-copy-service-portal) -Dokumentation.

Wenn der Registrierungs Wert **maxshadowkopien** nicht vorhanden ist, kann die Sicherungs Anwendung ihn unter folgendem Registrierungsschlüssel erstellen:

**HKEY \_ Lokale \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **VSS**- \\ **Einstellungen**

Erstellen Sie einen Wert mit dem Namen **maxshadowkopien** , und geben Sie DWORD ein. Die Standarddaten für diesen Wert sind 64. Der Minimalwert ist 1. Der Höchstwert ist 512.

> [!Note]  
> Für andere Typen von Schatten Kopien gibt es keinen Registrierungs Wert, der **maxshadowkopien** entspricht. Die maximale Anzahl von Schatten Kopien beträgt 512 pro Volume.

 

**Hinweis**  Die Einstellung **maxshadowkopien** wird unter Windows Server 2003 oder höher unterstützt.

**Windows Server 2003:** Auf Cluster Servern müssen die Daten des Registrierungs Werts für **maxshadowkopien** möglicherweise auf eine niedrigere Zahl festgelegt werden. Weitere Informationen finden Sie unter "Wenn Sie die Volumeschattenkopie-Dienst auf Windows Server 2003-basierten Computern verwenden, auf denen viele e/a-Vorgänge ausgeführt werden, müssen die Datenträgervolumes in der Hilfe-und Support-Wissensdatenbank unter länger online geschaltet werden [https://support.microsoft.com/kb/945058](https://support.microsoft.com/kb/945058) .

**Windows XP:** Dieser Registrierungs Wert wird nicht unterstützt.

## <a name="mindiffareafilesize"></a>MinDiffAreaFileSize

[VSS](/windows/desktop/VSS/volume-shadow-copy-service-portal) ordnet einen Schattenkopiespeicherbereich (oder einen diff-Bereich) zum Speichern von Daten für Schatten Kopien zu. Die minimale Größe des Schattenkopiespeicherbereichs ist eine Einstellung pro Computer, die mithilfe des Registrierungs Werts **MinDiffAreaFileSize** angegeben werden kann.

Wenn der Registrierungs Wert **MinDiffAreaFileSize** nicht festgelegt ist, beträgt die Mindestgröße für den Schattenkopiespeicherbereich 32 MB für Volumes, die kleiner als 500 MB sind, und 320 MB für Volumes, die größer als 500 MB sind.

**Windows Server 2008, Windows Server 2003 mit SP1 und Windows Vista:** Wenn der Registrierungs Wert **MinDiffAreaFileSize** nicht festgelegt ist, hat der Schattenkopiespeicherbereich eine Mindestgröße von 300 MB. Wenn der Registrierungs Wert **MinDiffAreaFileSize** festgelegt wird, müssen die Daten zwischen 300 MB und 3000 MB (3 GB) liegen, und es muss sich um ein Vielfaches von 300 MB handeln.

**Windows Server 2003:** Wenn der Registrierungs Wert **MinDiffAreaFileSize** nicht festgelegt ist, beträgt die Mindestgröße für den Schattenkopiespeicherbereich 100 MB.

**Windows XP:** Dieser Registrierungs Wert wird nicht unterstützt.

Wenn der Registrierungs Wert **MinDiffAreaFileSize** nicht vorhanden ist, kann die Sicherungs Anwendung ihn unter folgendem Registrierungsschlüssel erstellen:

**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **Volsnap**

Erstellen Sie einen Wert mit dem Namen **MinDiffAreaFileSize** und dem Typ reg \_ DWORD. Die Daten für diesen Schlüssel sind in Megabyte angegeben. 320 ist gleich 320 MB, und 3200 ist gleich 3,2 GB. Geben Sie eine Zahl an, die ein Vielfaches von 32 ist. Wenn Sie einen Wert angeben, der kein Vielfaches von 32 ist, wird das nächste Vielfache von 32 verwendet.

Schatten Kopien funktionieren möglicherweise nicht ordnungsgemäß, wenn der Registrierungs Wert **MinDiffAreaFileSize** eine minimale Größe angibt, die größer ist als die maximale Größe des Schattenkopiespeicherbereichs. Um die maximale Größe für den Speicherbereich für Schatten Kopien anzugeben, verwenden Sie den Befehl [vssadmin](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) Add ShadowStorage oder vssadmin Größe shadowstorage. Um die aktuelle maximale Größe anzuzeigen, verwenden Sie den Befehl [vssadmin List ShadowStorage](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) . Wenn Sie keine maximale Größe festgelegt haben, gibt es keine Beschränkung für den Speicherplatz, der verwendet werden kann.

## <a name="overallperformancesetting-and-customperformancesettings"></a>Overallperformancesetts und customperformancesettings

Die Registrierungs Werte **overallperformanceset** und **customperformancesettings** werden verwendet, um Leistungseinstellungen für Windows Server-Sicherung anzugeben. Diese Registrierungs Werte werden nur unter Windows Server-Betriebssystemen unterstützt.

**Windows Server 2003:** Diese Registrierungs Werte werden nicht unterstützt.

Wenn diese Registrierungs Werte nicht vorhanden sind, kann Sie von der Sicherungs Anwendung unter dem folgenden Registrierungsschlüssel erstellt werden:

**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Windows-Blockierungs Sicherung**

Um die Einstellungen für die Einstellungen für alle Volumes anzugeben, erstellen Sie einen Wert mit dem Namen **overallperformancesetts** , und geben Sie reg \_ DWORD ein. Die Daten des Werts sollten auf einen der folgenden Werte festgelegt werden.

| Wert | Bedeutung                                                                                                                                                                                                                                   |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Normale Sicherungsleistung (mit vollständigen Sicherungen). Diese Einstellung entspricht der normalen Sicherungs Leistungseinstellung, die unter [Optimieren der Sicherung und Server Leistung](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd759145(v=ws.11))beschrieben wird.            |
| 2     | Schnellere Sicherungsleistung (mithilfe von inkrementellen Sicherungen). Diese Einstellung entspricht der schnelleren Sicherungs Leistungseinstellung, die unter [Optimieren der Sicherung und Server Leistung](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd759145(v=ws.11))beschrieben wird.     |
| 3     | Benutzerdefinierte Sicherungsleistung (durch Angabe einer Leistungseinstellung für jedes Volume). Diese Einstellung entspricht der benutzerdefinierten Einstellung, die unter [Optimieren der Sicherung und Server Leistung](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd759145(v=ws.11))beschrieben wird. |



 

Wenn Sie **overallperformancesetts** auf 3 festlegen, müssen Sie auch die Einstellungen der Einstellungen für jedes Volume einzeln angeben. Erstellen Sie zu diesem Zweck einen Wert mit dem Namen **customperformancesettings** , und geben Sie reg \_ \_ MultiSZ ein. Die Daten dieses Werts sollten wie folgt festgelegt werden:

-   Jede Zeichenfolge in der \_ reg \_ MultiSZ-Sequenz von Zeichen folgen enthält die Einstellung für ein Volume.
-   Jede Zeichenfolge besteht aus einer Volume-GUID, gefolgt von einem Komma, gefolgt von einem DWORD-Wert.
-   Jeder der DWORD-Werte ist entweder 1 (vollständige Sicherung) oder 2 (inkrementelle Sicherung).

Nehmen Sie beispielsweise an, dass der Computer über zwei Volumes verfügt:

-   Die beiden Volumes lauten "C:" \\ und "D:" \\ .
-   Die GUID für Volume C: \\ ist 07c473ca4-2df8-11de-9d80-806e6b6e6963 und die GUID für Volume D: \\ ist 0ac22ea6c-712f-11de-adb0-00215a67606e.
-   Sie möchten eine normale Sicherungs Ausführung für Volume C: \\ und eine schnellere Sicherungsleistung für Volume D: angeben \\ .

Zu diesem Zweck legen Sie **overallperformancesetts** auf 3 und **customperformancesettings** auf "07c473ca4-2df8-11de-9d80-806e6f6e6963, 1 \\ 00ac22ea6c-712f-11de-adb0-00215a67606e, 2" fest.

Wenn Sie **overallperformancesetts** auf 1 oder 2 festlegen, werden die Daten im **customperformancesettings** -Wert ignoriert.

## <a name="sysvol"></a>SYSVOL

Der **SYSVOL** -Registrierungs Wert ist eine Möglichkeit, den DFSR-Dienst (verteiltes Dateisystem Replication) zu benachrichtigen, dass ein Vorgang zur Wiederherstellung des System Status initiiert wurde. Jede Sicherungs Anwendung, die die Systemstatus Wiederherstellung von SYSVOL ausführt, sollte diesen Wert verwenden, um anzugeben, ob der Wiederherstellungs Vorgang autorisierend oder nicht autoritativ Dieser Wert wird vom DFSR-Dienst gelesen. Wenn dieser Wert nicht festgelegt ist, wird die SYSVOL-Wiederherstellung standardmäßig nicht autoritativ ausgeführt.

Wenn der **SYSVOL** -Registrierungs Wert nicht vorhanden ist, sollte die Sicherungs Anwendung ihn unter dem folgenden Registrierungsschlüssel erstellen:

**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **DFSR**- \\ **Wiederherstellung**

Erstellen Sie einen Wert mit dem Namen **SYSVOL** , und geben Sie reg \_ SZ ein. Die Daten des Werts sollten auf der Grundlage der Anforderung des Systemadministrators entweder auf "autoritative" oder "nicht autoritativ" festgelegt werden.

**Windows Vista, Windows Server 2003 und Windows XP:** Dieser Registrierungs Wert wird nicht unterstützt.

 

 
