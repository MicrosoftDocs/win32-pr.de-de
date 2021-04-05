---
description: 'Weitere Informationen: Beispiele für den vshadow-Tool'
ms.assetid: 6a69b75b-ee4a-4613-ba05-d2deb42759b7
title: Beispiele für den vshadow-Tool
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b65fd2bfa1c390b1bd5310cd80f02e029dbf935f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751569"
---
# <a name="vshadow-tool-examples"></a>Beispiele für den vshadow-Tool

In den folgenden Beispielen wird veranschaulicht, wie das vshadow-Tool verwendet wird, um die gängigsten Aufgaben auszuführen:

-   [Zugreifen auf schattenkopieeigenschaften aus einem cmd-Skript](#accessing-shadow-copy-properties-from-a-cmd-script)
-   [Zugreifen auf nicht persistente Schatten Kopien](#accessing-nonpersistent-shadow-copies)
-   [Kopieren einer Datei aus einer Schatten Kopie](#copying-a-file-from-a-shadow-copy)
-   [Auflisten aller Dateien auf einem schattenkopiespeichergerät](#enumerating-all-files-on-a-shadow-copy-device)
-   [Importieren einer transportable-Schatten Kopie](#importing-a-transportable-shadow-copy)
-   [Einschließen von Writern oder Komponenten](#including-writers-or-components)
-   [Ausschließen von Writern oder Komponenten](#excluding-writers-or-components)
-   [Unterbrechen von schattenkopiesätzen mithilfe der breaksnapshotsetex-Methode](#breaking-shadow-copy-sets-using-the-breaksnapshotsetex-method)

Eine umfassende Liste der Befehlszeilenoptionen und deren Verwendung finden Sie unter [vshadow-Tool und-Beispiel](vshadow-tool-and-sample.md).

## <a name="accessing-shadow-copy-properties-from-a-cmd-script"></a>Zugreifen auf schattenkopieeigenschaften aus einem cmd-Skript

Wenn Sie das optionale Flag **-Script** verwenden, wenn Sie Schatten Kopien erstellen, erstellt vshadow eine cmd-Skriptdatei, die Umgebungsvariablen enthält, die sich auf die neu erstellten Schatten Kopien beziehen, wie z. b. die folgenden:

-   Die ID des schattenkopiesatzes, der in der% vshadow \_ Set \_ ID%-Umgebungsvariablen gespeichert ist.
-   Die schattenkopienids, die in Variablen der Form% vshadow \_ ID \_ *nnn*% gespeichert sind, wobei *nnn* den Index des Quell Volumens in der vshadow-Befehlszeile darstellt.
-   Die Namen der Schatten Kopie-Geräte, die in Variablen der Form% vshadow- \_ Gerät \_ *nnn*% gespeichert sind, wobei *nnn* der Index des Quell Volumens in der vshadow-Befehlszeile ist.

Mit der generierten cmd-Datei können Sie eingeschränkte Verwaltungsvorgänge für die Schatten Kopien durchführen.

> [!Note]  
> Das [**BackupComplete**](/windows/win32/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) Writer-Ereignis wird gesendet, nachdem das **-exec-** Skript ausgeführt wurde. VSS ruft die **IVssBackupComponents:: BackupComplete** -Methode auf, um den Writern zu signalisieren, dass die Sicherung abgeschlossen ist, und die Writer können an diesem Punkt möglicherweise Protokolle abschneiden. Daher ist es wichtig, zu überprüfen, ob der Schatten/die Sicherung tatsächlich abgeschlossen wurde. Wenn bei der Sicherung ein Fehler aufgetreten ist, können Sie den Erstellungs Prozess Abbrechen, indem Sie einen Exitcode ungleich NULL im ausgeführten Skript/Befehl zurückgeben. (Weitere Informationen finden Sie in der Dokumentation für den Exit-Befehl in der [Windows-Befehlszeilen Referenz](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754340(v=ws.11)).) Wenn der benutzerdefinierte Befehl mit einem Exitcode ungleich 0 (null) zurückgegeben wird, wird die Erstellung der Schatten Kopie abgebrochen, und **IVssBackupComponents:: BackupComplete** wird nicht aufgerufen.

 

Im folgenden Beispiel wird gezeigt, wie Sie eine persistente Schatten Kopie in der Befehlszeile erstellen und das cmd-Skript verwenden, um Sie verfügbar zu machen.

1.  **vshadow-p-NW-Script = SETVAR1. cmd c:**
2.  **SETVAR1. cmd aufzurufen**
3.  **C: \\>vshadow-El =% vshadow- \_ ID \_ 1%, c: \\ directory1**

## <a name="accessing-nonpersistent-shadow-copies"></a>Zugreifen auf nicht persistente Schatten Kopien

Nicht persistente Schatten Kopien werden automatisch gelöscht, wenn das Programm, das Sie erstellt, (in diesem Fall vshadow) beendet wird. Für den Zugriff auf den Inhalt dieser Schatten Kopien ermöglicht vshadow das Ausführen eines Skripts, nachdem die Schatten Kopien erstellt wurden, aber bevor das vshadow-Programm beendet wird.

Im folgenden Beispiel wird gezeigt, wie die Befehlszeilenoption-Exec zum Ausführen eines Skripts mit dem Namen "Enum. cmd" verwendet wird:

**vshadow-NW-Exec = Aufzählung. cmd c:**

Im ausgeführten Skript können Sie auch das generierte SETVAR-Skript in diesem benutzerdefinierten Befehl ausführen. Dadurch kann das Skript direkt auf den Inhalt der Schatten Kopien zugreifen. Beachten Sie, dass das Schatten Gerät von der \_ nnn-Umgebungsvariable des vshadow-Geräts abgerufen werden kann \_ .

Im folgenden finden Sie ein Beispielskript für "cmd":

``` syntax
call SETVAR1.cmd
for /R %VSHADOW_DEVICE_1%\ %%i in (*.*) do @echo %%i
```

Hier ist die Befehlszeile zum Ausführen des Skripts "Enum. cmd":

**vshadow-NW-Exec = c: \\ Umum. CMD-Script = setvar1. cmd c:**

## <a name="copying-a-file-from-a-shadow-copy"></a>Kopieren einer Datei aus einer Schatten Kopie

Im folgenden Beispiel wird gezeigt, wie eine Datei aus einer Schatten Kopie kopiert wird.

1.  **dir > c: \\somefile.txt**
2.  **vshadow-p-NW-Script = SETVAR1. cmd c:**
3.  **SETVAR1. cmd aufzurufen**
4.  **Kopieren Sie% vshadow- \_ Gerät \_ 1% \\somefile.txt c: \\ somefile \_bak.txt**

## <a name="enumerating-all-files-on-a-shadow-copy-device"></a>Auflisten aller Dateien auf einem schattenkopiespeichergerät

Im folgenden Beispiel wird gezeigt, wie alle Dateien auf einem schattenkopiesgerät aus einer Batchdatei aufgelistet werden.

1.  **dir > c: \\somefile.txt**
2.  **vshadow-p-NW-Script = SETVAR1. cmd c:**
3.  **SETVAR1. cmd aufzurufen**
4.  **für/R% vshadow- \_ Gerät \_ 1% \\ %% i in ( \* ) führen Sie @echo %% i aus.**

## <a name="importing-a-transportable-shadow-copy"></a>Importieren einer transportable-Schatten Kopie

Um eine austauschen-Schatten Kopie auf einem Computer zu erstellen und auf einen anderen Computer zu importieren, müssen Sie über zwei Computer verfügen, die (über eine SAN-Konfiguration) mit einem Speicher Array verbunden sind, das VSS-Hardware Schatten Kopien unterstützt. Ein VSS-Hardware Anbieter muss auf jedem Computer installiert sein.

Im folgenden Beispiel wird gezeigt, wie die Schatten Kopie erstellt und importiert wird.

1.  Erstellen Sie die auf Computer A (dem Produktionsserver) festgelegte Schatten Kopie, indem Sie den folgenden Befehl nach der Eingabeaufforderung eingeben:

    **vshadow-p-t =bc1.xml**

    Dadurch werden keine schattenkopiegeräte auf Computer A verfügbar gemacht.

2.  Kopieren Sie das Dokument mit den Sicherungs Komponenten (bc1.xml) von Computer A auf Computer B.
3.  Importieren Sie den Schatten Satz auf Computer B, indem Sie den folgenden Befehl eingeben:

    **vshadow-i =bc1.xml**

Optional können Sie diese Schatten Kopien als Laufwerksbuchstaben oder eingebundene Ordner verfügbar machen. Außerdem könnten Sie den Schatten Satz möglicherweise unterbrechen, damit die neuen Schattenkopievolumes Lese-/Schreibzugriff erhalten.

Zum Automatisieren des Schattensatz-Verwaltungsprozesses können Sie die Befehlszeilenoption " **-Script** " verwenden, um das cmd-Skript zu generieren, das die schattenkopieids enthält. Anschließend können Sie das generierte Skript zusammen mit den Sicherungs Komponenten auf den anderen Computer kopieren.

Im folgenden Beispiel wird gezeigt, wie Sie mithilfe von CMD-Skripts austauschen-Schatten Kopien erstellen, verfügbar machen und unterbrechen können.

1.  Erstellen Sie die auf Computer A (dem Produktionsserver) festgelegte Schatten Kopie wie folgt über die Befehlszeile:

    **vshadow-p-t =bc1.xml-Script = SC1. cmd**

    Geben Sie die Option **-Script** an, um das Skript zu generieren, das die entsprechenden Umgebungsvariablen Definitionen enthält. Beachten Sie, dass dadurch keine schattenkopiegeräte auf Computer A verfügbar gemacht werden.

2.  Kopieren Sie das Dokument mit den Sicherungs Komponenten (bc1.xml) und das generierte Skript (SC1. cmd) von Computer A auf Computer B.
3.  Importieren Sie den Schatten Satz auf Computer B, indem Sie den folgenden Befehl eingeben:

    **vshadow-i =bc1.xml**

    Hierdurch werden die erstellten Geräte auf Computer B angezeigt.

4.  Führen Sie das generierte Skript aus, um die Umgebungsvariablen für den Schattenkopiesatz festzulegen, indem Sie den Dateinamen an der Eingabeaufforderung eingeben, wie im folgenden Beispiel gezeigt:

    **SC1. cmd**

    Dadurch werden die relevanten Umgebungsvariablen festgelegt, wie unter Zugreifen auf Schatten Kopier Eigenschaften aus einem cmd-Skript beschrieben.

5.  Machen Sie die Schatten Kopien auf Computer B verfügbar, indem Sie die folgenden Befehle eingeben:
    1.  **rmdir/s c: \\ \_ Einfügepunkt**
    2.  **mkdir c: \\ \_ Einfügepunkt**
    3.  **vshadow – El =% vshadow- \_ ID \_ 1%, c: Einfügepunkt \\ \_**

    Hierdurch werden die erstellten schattenkopiegeräte auf Computer B angezeigt.
6.  Unterbrechen Sie den Schattenkopiesatz, damit die Volumes beschreibbar sind, indem Sie den folgenden Befehl eingeben:**C: \\>vshadow – BW =% vshadow \_ Set \_ ID%**

Beachten Sie, dass nicht persistente austauschen-Schatten Kopien ebenfalls importiert werden können, aber Sie werden automatisch gelöscht, wenn der **vshadow** **-i-** Prozess beendet wird. Wenn Sie die Schatten Kopien vor dem Löschen importieren möchten, müssen Sie die Befehlszeilenoption **-exec** verwenden, wie unter Zugriff auf nicht persistente Schatten Kopien beschrieben.

## <a name="including-writers-or-components"></a>Einschließen von Writern oder Komponenten

Standardmäßig nehmen alle Writer an der Erstellung von Schatten Kopien Teil. Wenn Sie bestimmen möchten, welche Writer und Komponenten in einen Schattenkopiesatz eingeschlossen werden sollen, verwenden Sie die Befehlszeilenoption **-WM** oder **-wm2** , wie in [Auflisten von Writer-Status und-Metadaten](vshadow-tool-and-sample.md)beschrieben.

Um sicherzustellen, dass alle Komponenten eines Writers enthalten sind, verwenden Sie das optionale **-Wi-** Flag in einem der folgenden Formate:

-   **vshadow** **-Wi-** *beschreibname*
-   **vshadow** **-Wi** **"**_Writer-namens Zeichenfolge_*_"_*
-   **vshadow** **-Wi** **{**_beschreiterid_*_}_*
-   **vshadow** **-Wi** **{**_InstanceId_*_}_*

Verwenden Sie das optionale **-Wi-** Flag in einem der folgenden Formate, um zu überprüfen, ob bestimmte Komponenten eingeschlossen sind:

-   **vshadow** **-Wi-** *Schreib Name ***: \\**_LogicalPath_* _\\_ * _componentname_
-   **vshadow** **-Wi** **"**_Writer-namens Zeichenfolge_*_": \\_*_LogicalPath_ *_\\_* _componentname_
-   **vshadow** **-Wi** **{**_beschreiterid_*_}: \\_*_LogicalPath_ *_\\_* _componentname_
-   **vshadow** **-Wi** **{**_InstanceId_*_}: \\_*_LogicalPath_ *_\\_* _componentname_

In den folgenden Beispielen wird gezeigt, wie das optionale **-Flag-Wi** verwendet wird.

-   Angeben von " *Write Name*: \\ *LogicalPath* \\ *componentname*":

    **vshadow-Wi = "registrierungswriter: \\ Registrierung"**

-   Angeben von {*Write ID*}:

    **vshadow-Wi = {BE000CBE-11FE-4426-9C58-531AA6355FC4}**

-   Angeben von mehr als einem Writer oder einer Komponente:

    **vshadow-Wi = "Registry Writer: \\ Registry"-Wi = "com+ RegDB Writer"**

## <a name="excluding-writers-or-components"></a>Ausschließen von Writern oder Komponenten

Um alle Writer auszuschließen, verwenden Sie das optionale Flag **-NW** , wenn Sie die Schatten Kopie erstellen.

Um alle Komponenten eines Writers auszuschließen, verwenden Sie das optionale **-WX-** Flag in einem der folgenden Formate:

-   **vshadow** **-WX-** *beschreitername*
-   **vshadow** **-WX** **"**_Writer-namens Zeichenfolge_*_"_*
-   **vshadow** **-WX** **{**_beschreiterid_*_}_*
-   **vshadow** **-WX** **{**_InstanceId_*_}_*

Um bestimmte Komponenten auszuschließen, verwenden Sie das optionale **-WX-** Flag in einem der folgenden Formate:

-   **vshadow** **-WX-** *Schreib Name ***: \\**_LogicalPath_* _\\_ * _componentname_
-   **vshadow** **-WX** **"**_Writer-namens Zeichenfolge_*_": \\_*_LogicalPath_ *_\\_* _componentname_
-   **vshadow** **-WX** **{**_beschreiterid_*_}: \\_*_LogicalPath_ *_\\_* _componentname_
-   **vshadow** **-WX** **{**_InstanceId_*_}: \\_*_LogicalPath_ *_\\_* _componentname_

In den folgenden Beispielen wird gezeigt, wie Sie das optionale Flag **-WX** verwenden.

-   Angeben von " *Write Name*: \\ *LogicalPath* \\ *componentname*":

    **vshadow-WX = "registrierungswriter: \\ Registrierung"**

-   Angeben von {*Write ID*}:

    **vshadow-WX = {BE000CBE-11FE-4426-9C58-531AA6355FC4}**

-   Angeben von mehr als einem Writer oder einer Komponente:

    **vshadow-WX = "Registry Writer: \\ Registry"-WX = "com+ RegDB Writer"**

## <a name="breaking-shadow-copy-sets-using-the-breaksnapshotsetex-method"></a>Unterbrechen von schattenkopiesätzen mithilfe der breaksnapshotsetex-Methode

In den folgenden Beispielen wird gezeigt, wie die Befehlszeilenoption **-BEx** verwendet wird.

-   Angeben, dass die LUN der Schatten Kopie vom Host maskiert werden soll:

    **vshadow** **-BEx** **-Mask**

-   Angeben, dass die LUN der Schatten Kopie als Lese-/schreibvolume für den Host verfügbar gemacht werden soll:

    **vshadow** **-BEx** **-RW**

-   Angeben, dass die LUN der Schatten Kopie als Lese-/schreibvolume für den Host verfügbar gemacht wird, und dass keine der Datenträger Signaturen in den schattenkopieluns auf die der ursprünglichen LUNs zurückgesetzt werden:

    **vshadow** **-BEx** **-norevert**

 

 
