---
description: Weitere Informationen finden Sie unter Beispiele für VShadow-Tools.
ms.assetid: 6a69b75b-ee4a-4613-ba05-d2deb42759b7
title: Beispiele für das VShadow-Tool
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86ec0a753f2865be98cfed76cd192a73cfc785b3fcdc487f7685c9f4ae7d52e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056348"
---
# <a name="vshadow-tool-examples"></a>Beispiele für das VShadow-Tool

In den folgenden Beispielen wird gezeigt, wie Sie das VShadow-Tool verwenden, um die gängigsten Aufgaben auszuführen:

-   [Zugreifen auf Schattenkopieeigenschaften über ein CMD-Skript](#accessing-shadow-copy-properties-from-a-cmd-script)
-   [Zugreifen auf nichtpersistente Schattenkopien](#accessing-nonpersistent-shadow-copies)
-   [Kopieren einer Datei aus einer Schattenkopie](#copying-a-file-from-a-shadow-copy)
-   [Aufzählen aller Dateien auf einem Schattenkopiegerät](#enumerating-all-files-on-a-shadow-copy-device)
-   [Importieren einer transportierbaren Schattenkopie](#importing-a-transportable-shadow-copy)
-   [Einschließlich Writer oder Komponenten](#including-writers-or-components)
-   [Ausschließen von Writern oder Komponenten](#excluding-writers-or-components)
-   [Breaking Shadow Copy Sets Using the BreakSnapshotSetEx Method](#breaking-shadow-copy-sets-using-the-breaksnapshotsetex-method)

Eine vollständige Liste der Befehlszeilenoptionen und deren Verwendung finden Sie unter [VShadow-Tool und Beispiel](vshadow-tool-and-sample.md).

## <a name="accessing-shadow-copy-properties-from-a-cmd-script"></a>Zugreifen auf Schattenkopieeigenschaften über ein CMD-Skript

Wenn Sie beim Erstellen von Schattenkopien das optionale Flag **-script** verwenden, erstellt VShadow eine CMD-Skriptdatei mit Umgebungsvariablen, die mit den neu erstellten Schattenkopien verknüpft sind, z. B.:

-   Die ID des Schattenkopiesets, die in der Umgebungsvariablen %VSHADOW \_ SET \_ ID% gespeichert ist
-   Die Schattenkopie-IDs, die in Variablen der Form %VSHADOW \_ ID \_ *NNN*% gespeichert werden, wobei *NNN* den Index des Quellvolumens in der VShadow-Befehlszeile darstellt
-   Die Schattenkopiegerätenamen, die in Variablen der Form %VSHADOW \_ DEVICE \_ *NNN*% gespeichert werden, wobei *NNN* der Index des Quellvolumens in der VShadow-Befehlszeile ist

Sie können die generierte CMD-Datei verwenden, um eingeschränkte Verwaltungsvorgänge für die Schattenkopien durchzuführen.

> [!Note]  
> Das [**BackupComplete**](/windows/win32/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) Writer-Ereignis wird gesendet, nachdem **das Skript -exec** ausgeführt wurde. VSS ruft die **IVssBackupComponents::BackupComplete-Methode** auf, um den Writern zu signalisieren, dass die Sicherung abgeschlossen ist, und die Writer können protokolle zu diesem Zeitpunkt möglicherweise abschneiden. Daher ist es wichtig zu überprüfen, ob die Schatten-/Sicherungskopie tatsächlich abgeschlossen wurde. Wenn bei der Sicherung ein Fehler auft ist, können Sie den Erstellungsprozess abbrechen, indem Sie im ausgeführten Skript/Befehl einen Exitcode ungleich 0 (null) zurückgeben. (Weitere Informationen finden Sie in der Dokumentation zum Exitbefehl in Windows [Befehlszeilenreferenz.)](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754340(v=ws.11)) Wenn der benutzerdefinierte Befehl mit einem Exitcode ungleich 0 (null) zurückgegeben wird, wird die Erstellung der Schattenkopie abgebrochen, und **IVssBackupComponents::BackupComplete** wird nicht aufgerufen.

 

Das folgende Beispiel zeigt, wie Sie eine persistente Schattenkopie über die Befehlszeile erstellen und das CMD-Skript verwenden, um sie verfügbar zu machen.

1.  **vshadow -p -nw -script=SETVAR1.cmd c:**
2.  **Aufrufen von SETVAR1.cmd**
3.  **C: \\>vshadow -el=%VSHADOW \_ ID \_ 1%,c: \\ directory1**

## <a name="accessing-nonpersistent-shadow-copies"></a>Zugreifen auf nichtpersistente Schattenkopien

Nichtpersistente Schattenkopien werden automatisch gelöscht, wenn das Programm, das sie erstellt (in diesem Fall VShadow), beendet wird. Um auf den Inhalt dieser Schattenkopien zu zugreifen, können Sie mit VShadow ein Skript ausführen, nachdem die Schattenkopien erstellt wurden, aber bevor das VShadow-Programm beendet wird.

Das folgende Beispiel zeigt, wie Sie die Befehlszeilenoption -exec verwenden, um ein Skript namens "enum.cmd" auszuführen:

**vshadow -nw -exec=enum.cmd c:**

Im ausgeführten Skript können Sie auch das generierte SETVAR-Skript in diesem benutzerdefinierten Befehl ausführen. Dadurch kann das Skript direkt auf den Inhalt der Schattenkopien zugreifen. Denken Sie daran, dass das Schattengerät aus der Umgebungsvariablen VSHADOW \_ DEVICE \_ NNN abgerufen werden kann.

Hier sehen Sie ein Beispielskript für "enum.cmd":

``` syntax
call SETVAR1.cmd
for /R %VSHADOW_DEVICE_1%\ %%i in (*.*) do @echo %%i
```

Dies ist die Befehlszeile zum Ausführen des Skripts "enum.cmd":

**vshadow -nw -exec=c: \\ enum.cmd -script=setvar1.cmd c:**

## <a name="copying-a-file-from-a-shadow-copy"></a>Kopieren einer Datei aus einer Schattenkopie

Das folgende Beispiel zeigt, wie eine Datei aus einer Schattenkopie kopiert wird.

1.  **dir > c: \\somefile.txt**
2.  **vshadow -p -nw -script=SETVAR1.cmd c:**
3.  **Aufrufen von SETVAR1.cmd**
4.  **copy %VSHADOW \_ DEVICE \_ 1% \\somefile.txt c: \\ somefile \_bak.txt**

## <a name="enumerating-all-files-on-a-shadow-copy-device"></a>Aufzählen aller Dateien auf einem Schattenkopiegerät

Das folgende Beispiel zeigt, wie sie alle Dateien auf einem Schattenkopiegerät aus einer Batchdatei aufzählen.

1.  **dir > c: \\somefile.txt**
2.  **vshadow -p -nw -script=SETVAR1.cmd c:**
3.  **Aufrufen von SETVAR1.cmd**
4.  **für /R %VSHADOW \_ DEVICE \_ 1% \\ %%i in ( \* ) do @echo %%i**

## <a name="importing-a-transportable-shadow-copy"></a>Importieren einer transportierbaren Schattenkopie

Um eine transportierbare Schattenkopie auf einem Computer zu erstellen und auf einen anderen Computer zu importieren, müssen Sie über zwei Computer verfügen, die (über eine SAN-Konfiguration) mit einem Speicherarray verbunden sind, das VSS-Hardwareschattenkopien unterstützt. Auf jedem Computer muss ein VSS-Hardwareanbieter installiert sein.

Das folgende Beispiel zeigt, wie die Schattenkopie erstellt und importiert wird.

1.  Erstellen Sie den Schattenkopiesatz auf Computer A (dem Produktionsserver), indem Sie nach der Eingabeaufforderung den folgenden Befehl eingeben:

    **vshadow -p -t=bc1.xml**

    Dadurch werden keine Schattenkopiegeräte auf Computer A verfügbar.

2.  Kopieren Sie das Sicherungskomponentendokument (bc1.xml) von Computer A auf Computer B.
3.  Importieren Sie das Schattenset auf Computer B, indem Sie den folgenden Befehl eingeben:

    **vshadow -i=bc1.xml**

Optional können Sie diese Schattenkopien als Laufwerkbuchstaben oder bereitgestellte Ordner verfügbar machen. Außerdem könnten Sie den Schattensatz möglicherweise durchbrechen, um die neuen Schattenkopievolumes mit Lese-/Schreibzugriff zu beschriften.

Um den Schattensetverwaltungsprozess zu automatisieren, können Sie die Befehlszeilenoption **-script** verwenden, um das CMD-Skript mit den Schattenkopie-IDs zu generieren. Anschließend können Sie das generierte Skript zusammen mit den Sicherungskomponenten auf den anderen Computer kopieren.

Das folgende Beispiel zeigt, wie transportable Schattenkopien mithilfe von CMD-Skripts erstellt, verfügbar und unterbricht werden.

1.  Erstellen Sie den Schattenkopiesatz auf Computer A (dem Produktionsserver) wie folgt über die Befehlszeile:

    **vshadow -p -t=bc1.xml -script=sc1.cmd**

    Geben Sie die **Option -script** an, um das Skript zu generieren, das die richtigen Umgebungsvariablendefinitionen enthält. Beachten Sie, dass dadurch keine Schattenkopiegeräte auf Computer A verfügbar sind.

2.  Kopieren Sie das Sicherungskomponentendokument (bc1.xml) und das generierte Skript (sc1.cmd) von Computer A auf Computer B.
3.  Importieren Sie das Schattenset auf Computer B, indem Sie den folgenden Befehl eingeben:

    **vshadow -i=bc1.xml**

    Dadurch werden die erstellten Geräte auf Computer B verfügbar.

4.  Führen Sie das generierte Skript aus, um die Umgebungsvariablen für den Schattenkopiesatz zu legen, indem Sie den Dateinamen wie im folgenden Beispiel an der Eingabeaufforderung eingeben:

    **sc1.cmd**

    Dadurch werden die relevanten Umgebungsvariablen wie unter Access Shadow Copy Properties from a CMD Script (Zugriffsschattenkopieeigenschaften aus einem CMD-Skript) beschrieben festgelegt.

5.  Machen Sie die Schattenkopien auf Computer B verfügbar, indem Sie die folgenden Befehle eingeben:
    1.  **rmdir /s c: \\ \_ Bereitstellungspunkt**
    2.  **mkdir c: \\ \_ Bereitstellungspunkt**
    3.  **vshadow –el=%VSHADOW \_ ID \_ 1%,c: \\ \_ Bereitstellungspunkt**

    Dadurch werden die erstellten Schattenkopiegeräte auf Computer B verfügbar.
6.  Brechen Sie den Schattenkopiesatz auf, um die Volumes schreibbar zu machen, indem Sie den folgenden Befehl eingeben:**C: \\>vshadow –bw=%VSHADOW \_ SET \_ ID%**

Beachten Sie, dass nichtpersistente transportierbare Schattenkopien ebenfalls importiert, aber automatisch gelöscht werden, wenn der **vshadow** **-i-Prozess** beendet wird. Um die Schattenkopien zu importieren, bevor sie gelöscht werden, müssen Sie die Befehlszeilenoption **-exec** verwenden, wie unter Zugreifen auf nicht vorhandene Schattenkopien beschrieben.

## <a name="including-writers-or-components"></a>Einschließlich Writer oder Komponenten

Standardmäßig nehmen alle Writer an der Erstellung von Schattenkopien teil. Um zu bestimmen, welche Writer und Komponenten in einem Schattenkopiesatz enthalten sein werden, verwenden Sie die Befehlszeilenoption **-wm** oder **-wm2,** wie unter Listing Writer Status and Metadata (Auflisten des Writerstatus und der [Metadaten) beschrieben.](vshadow-tool-and-sample.md)

Um sicherzustellen, dass alle Komponenten eines Writers enthalten sind, verwenden Sie das optionale **Flag -wi** in einem der folgenden Formate:

-   **vshadow** **-wi** *WriterName*
-   **vshadow** **-wi** **"** Writer Name _String_*_"_*
-   **vshadow** **-wi** **{**_WriterID_*_}_*
-   **vshadow** **-wi** **{**_InstanceID_*_}_*

Um zu überprüfen, ob bestimmte Komponenten enthalten sind, verwenden Sie das optionale **Flag -wi** in einem der folgenden Formate:

-   **vshadow** **-wi** *WriterName***: \\**_LogicalPath_* _\\_ * _ComponentName_
-   **vshadow** **-wi** **"** Writer Name _String_*_": \\_*_LogicalPath_ *_\\_* _ComponentName_
-   **vshadow** **-wi** **{**_WriterID_*_}: \\_*_LogicalPath_ *_\\_* _ComponentName_
-   **vshadow** **-wi** **{**_InstanceID_*_}: \\_*_LogicalPath_ *_\\_* _ComponentName_

In den folgenden Beispielen wird die Verwendung des optionalen **Flags -wi** gezeigt.

-   Angeben von *WriterName:* \\ *LogicalPath* \\ *ComponentName:*

    **vshadow -wi="Registry Writer: \\ Registry"**

-   Angeben von {*WriterID*}:

    **vshadow -wi={BE000CBE-11FE-4426-9C58-531AA6355FC4}**

-   Angeben mehrerer Writer oder Komponenten:

    **vshadow -wi="Registry Writer: \\ Registry" -wi="COM+ REGDB Writer"**

## <a name="excluding-writers-or-components"></a>Ausschließen von Writern oder Komponenten

Um alle Writer auszuschließen, verwenden Sie das optionale Flag **-nw** beim Erstellen der Schattenkopie.

Um alle Komponenten eines Writers auszuschließen, verwenden Sie das optionale Flag **-wx** in einem der folgenden Formate:

-   **vshadow** **-wx** *WriterName*
-   **vshadow** **-wx** **"** Writer Name _String_*_"_*
-   **vshadow** **-wx** **{**_WriterID_*_}_*
-   **vshadow** **-wx** **{**_InstanceID_*_}_*

Um bestimmte Komponenten auszuschließen, verwenden Sie das optionale Flag **-wx** in einem der folgenden Formate:

-   **vshadow** **-wx** *WriterName***: \\**_LogicalPath_* _\\_ * _ComponentName_
-   **vshadow** **-wx** **"** Writer Name _String_*_": \\_*_LogicalPath_ *_\\_* _ComponentName_
-   **vshadow** **-wx** **{**_WriterID_*_}: \\_*_LogicalPath_ *_\\_* _ComponentName_
-   **vshadow** **-wx** **{**_InstanceID_*_}: \\_*_LogicalPath_ *_\\_* _ComponentName_

In den folgenden Beispielen wird die Verwendung des optionalen Flags **-wx** veranschaulicht.

-   Angeben von *WriterName:* \\ *LogicalPath* \\ *ComponentName*:

    **vshadow -wx="Registry Writer: \\ Registry"**

-   Angeben von {*WriterID*}:

    **vshadow -wx={BE000CBE-11FE-4426-9C58-531AA6355FC4}**

-   Angeben mehrerer Writer oder Komponenten:

    **vshadow -wx="Registry Writer: \\ Registry" -wx="COM+ REGDB Writer"**

## <a name="breaking-shadow-copy-sets-using-the-breaksnapshotsetex-method"></a>Breaking Shadow Copy Sets mithilfe der BreakSnapshotSetEx-Methode

In den folgenden Beispielen wird die Verwendung der Befehlszeilenoption **-bex** veranschaulicht.

-   Geben Sie an, dass die Schattenkopie-LUN vom Host maskiert wird:

    **vshadow** **-bex** **-mask**

-   Geben Sie an, dass die Schattenkopie-LUN für den Host als Lese-/Schreibvolume verfügbar gemacht wird:

    **vshadow** **-bex** **-rw**

-   Geben Sie an, dass die Schattenkopie-LUN für den Host als Lese-/Schreibvolume verfügbar gemacht wird und dass keine der Datenträgersignaturen auf den Schattenkopie-LUNs auf die der ursprünglichen LUNs zurückgesetzt wird:

    **vshadow** **-bex** **-norevert**

 

 
