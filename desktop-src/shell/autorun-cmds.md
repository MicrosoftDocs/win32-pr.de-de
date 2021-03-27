---
description: Dieses Thema ist ein Verweis auf die Einträge, die in einer Autorun. inf-Datei verwendet werden können. Ein Eintrag besteht aus einem Schlüssel und einem Wert.
ms.assetid: 5b8fd559-b1be-4552-a7be-19ad107855af
title: Autorun. inf-Einträge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56d93244f177d107bddc720fab1d0c774fd94735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214442"
---
# <a name="autoruninf-entries"></a>Autorun. inf-Einträge

Dieses Thema ist ein Verweis auf die Einträge, die in einer Autorun. inf-Datei verwendet werden können. Ein Eintrag besteht aus einem Schlüssel und einem Wert.

-   [\[Autorun- \] Schlüssel](#autorun-keys)
    -   [action](#parameters)
    -   [CustomEvent](#customevent)
    -   [angezeigt](#parameters)
    -   [label](#parameters)
    -   [open](#parameters)
    -   [Useautoplay](#parameters)
    -   [ShellExecute](#shellexecute)
    -   [schel](#autoruninf-entries)
    -   [\\shellverb](#shellverb)
-   [\[Inhalts \] Schlüssel](#content-keys)
-   [\[Exclusivecontentpath- \] Schlüssel](#exclusivecontentpaths-keys)
-   [\[Ignorecontentpath- \] Schlüssel](#ignorecontentpaths-keys)
-   [\[Schlüssel für "de viceingestall" \]](#deviceinstall-keys)
    -   [DriverPath "](#driverpath)

## <a name="autorun-keys"></a>\[Autorun- \] Schlüssel

-   [action](#parameters)
-   [CustomEvent](#customevent)
-   [angezeigt](#parameters)
-   [label](#parameters)
-   [open](#parameters)
-   [Useautoplay](#parameters)
-   [ShellExecute](#shellexecute)
-   [schel](#autoruninf-entries)
-   [\\shellverb](#shellverb)

### <a name="action"></a>action

Der **Aktions** Eintrag gibt den Text an, der im Dialogfeld "AutoPlay" für den Handler verwendet wird, der das im [Open](#parameters) -oder [ShellExecute](#shellexecute) -Eintrag in der Datei "Autorun. inf" des Mediums angegebene Programm darstellt. Der Wert kann entweder als Text oder als Ressource ausgedrückt werden, die in einer Binärdatei gespeichert ist.


```
action=ActionText
```




```
action=@[filepath\]filename,-resourceID
```



### <a name="parameters"></a>Parameter

-   *Action Text*

    Text, der im Dialogfeld "AutoPlay" für den Handler verwendet wird, der das im Eintrag " [Open](#parameters) " oder " [ShellExecute](#shellexecute) " in der Datei "Autorun. inf" des Mediums angegebene Programm darstellt.

-   *FilePath*

    Eine Zeichenfolge, die den voll qualifizierten Pfad des Verzeichnisses enthält, das die Binärdatei enthält, die die Zeichenfolge enthält. Wenn kein Pfad angegeben wird, muss sich die Datei im Stammverzeichnis des Laufwerks befinden.

-   *filename*

    Eine Zeichenfolge, die den Namen der Binärdatei enthält.

-   *resourceID*

    Die ID der Zeichenfolge in der Binärdatei.

### <a name="remarks"></a>Bemerkungen

Der **Aktions** Schlüssel wird nur in Windows XP Service Pack 2 (SP2) oder höher verwendet. Sie wird nur für Laufwerke vom Typ "Laufwerk Wechsel" und "Laufwerk korrigiert" unterstützt \_ \_ . Im Fall einer Wechsel Datenträger \_ ist der **Aktions** Schlüssel erforderlich. Ein **Action** -Befehl in der Autorun. inf-Datei einer AudioCD oder Movie DVD wird ignoriert, und diese Medienverhalten sich weiterhin wie in Windows XP Service Pack 1 (SP1) und früher.

Die im Dialogfeld "AutoPlay" angezeigte Zeichenfolge wird erstellt, indem der im **Aktions** Eintrag angegebene Text mit hart codiertem Text benannt wird, der von der Shell bereitgestellt wird. Das [Symbol](#parameters) wird daneben angezeigt. Dieser Eintrag wird immer als erste Option im Dialogfeld "AutoPlay" angezeigt und ist standardmäßig ausgewählt. Wenn der Benutzer die Option annimmt, wird die durch den Eintrag " [Open](#parameters) " oder " [ShellExecute](#shellexecute) " in der Datei "Autorun. inf" des Mediums angegebene Anwendung gestartet. Die Option **ausgewählte Aktion immer** ausführen ist in dieser Situation nicht verfügbar.

Die [Aktions](#parameters) -und [Symbol](#parameters) Tasten definieren die Darstellung der Anwendung, die vom Endbenutzer im Dialogfeld "AutoPlay" angezeigt wird. Sie sollten so zusammengesetzt werden, dass Benutzer Sie leicht identifizieren können. Sie sollten die auszuwendende Anwendung, das Unternehmen, das Sie erstellt hat, und alle zugeordneten Branding angeben.

Aus Gründen der Abwärtskompatibilität ist der **Aktions** Eintrag für Geräte vom Typ Laufwerk \_ Fixed optional. Bei diesem Typ wird im Dialogfeld "AutoPlay" ein Standardeintrag verwendet, wenn in der Datei "Autorun. inf" kein **Aktions** Eintrag vorhanden ist.

Der **Aktions** Eintrag ist für Geräte vom Typ "Laufwerk Wechsel" obligatorisch \_ , die bis jetzt keine Unterstützung für "Autorun. inf" aufweisen. Wenn kein **Aktions** Eintrag vorhanden ist, wird das Dialogfeld "AutoPlay" angezeigt, aber ohne Option zum Starten des zusätzlichen Inhalts.

### <a name="customevent"></a>CustomEvent

Der **CustomEvent** -Eintrag gibt ein benutzerdefiniertes Ereignis zum Wiedergeben von Inhalten an.


```
CustomEvent=CustomEventName
```



### <a name="parameters"></a>Parameter

-   *CustomEventName*

    Eine Text Zeichenfolge, die den Namen des AutoPlay-Inhalts Ereignisses enthält. Der Name darf nicht mehr als 100 alphanumerische Zeichen enthalten.

### <a name="remarks"></a>Bemerkungen

Sie können einen benutzerdefinierten Ereignis Namen in die Datei Autorun. inf eines Volumes einschließen. Wenn der Benutzer von der automatischen Wiedergabe zur Verwendung mit dem Volume aufgefordert wird, werden nur Anwendungen angezeigt, die für den angegebenen benutzerdefinierten Ereignis Namen registriert sind. Informationen dazu, wie Sie eine Anwendung als Handler für das benutzerdefinierte AutoPlay-Inhalts Ereignis registrieren können, finden Sie unter [Automatisches Starten mit Autoplay](/previous-versions/windows/apps/hh452731(v=win.10)) oder [Registrieren eines Ereignis Handlers](how-to-register-an-event-handler.md).

Im folgenden Beispiel wird der Wert "mycontentonarrival" als neues AutoPlay-Inhalts Ereignis angegeben.


```
CustomEvent=MyContentOnArrival
```



### <a name="icon"></a>icon

Der **Symbol** Eintrag gibt ein Symbol an, das das Autorun-aktivierte Laufwerk in der Windows-Benutzeroberfläche darstellt.


```
icon=iconfilename[,index]
```



### <a name="parameters"></a>Parameter

-   *IconFileName*

    Der Name einer ICO-, BMP-, exe-oder DLL-Datei, die die Symbol Informationen enthält. Wenn eine Datei mehr als ein Symbol enthält, müssen Sie auch einen NULL basierten Index des Symbols angeben.

### <a name="remarks"></a>Bemerkungen

Das Symbol stellt in Verbindung mit der Bezeichnung das Autorun-aktivierte Laufwerk in der Windows-Benutzeroberfläche dar. Beispielsweise wird in Windows-Explorer das Laufwerk durch dieses Symbol anstatt durch das Standard Laufwerk Symbol dargestellt. Die Symbol Datei muss sich im gleichen Verzeichnis befinden wie die Datei, die durch den Befehl " [Öffnen](#parameters) " angegeben wird.

Im folgenden Beispiel wird das zweite Symbol in der MyProg.exe-Datei angegeben.


```
icon=MyProg.exe,1
```



### <a name="label"></a>label

Der Bezeichnungs Eintrag gibt eine Text Bezeichnung an, die das Autorun-aktivierte Laufwerk **in der Windows** -Benutzeroberfläche darstellt.


```
label=LabelText
```



### <a name="parameters"></a>Parameter

-   *LabelText*

    Eine Text Zeichenfolge, die die Bezeichnung enthält. Sie kann Leerzeichen enthalten und darf nicht länger als 32 Zeichen sein.

> [!Note]  
> Es ist möglich, einen Wert in den Parameter " **LabelText** " einzufügen, der mehr als 32 Zeichen enthält und keine Fehlermeldung empfängt. Das System zeigt jedoch nur die ersten 32 Zeichen an. Alle Zeichen nach dem 32. werden abgeschnitten und nicht angezeigt. Beispiel: " **LabelText** " lautet wie folgt: Bezeichnung = "diese CD ist als ultimative Musik-CD konzipiert." Folgendes wird angezeigt: "diese CD ist als UL konzipiert."

 

### <a name="remarks"></a>Bemerkungen

Die Bezeichnung stellt in Verbindung mit einem Symbol das Autorun-aktivierte Laufwerk in der Windows-Benutzeroberfläche dar.

Im folgenden Beispiel wird der Wert "My Drive Label" als Bezeichnung des Laufwerks angegeben.


```
label=My Drive Label
```



### <a name="open"></a>open

Der Eintrag **Öffnen** gibt den Pfad und den Dateinamen der Anwendung an, die gestartet wird, wenn ein Benutzer einen Datenträger in das Laufwerk einfügt.


```
open=[exepath\]exefile [param1 [param2] ...] 
```



### <a name="parameters"></a>Parameter

-   *exefile*

    Voll qualifizierter Pfad einer ausführbaren Datei, die beim Einfügen der CD ausgeführt wird. Wenn nur ein Dateiname angegeben wird, muss er sich im Stammverzeichnis des Laufwerks befinden. Wenn Sie die Datei in einem Unterverzeichnis suchen möchten, müssen Sie einen Pfad angeben. Sie können auch einen oder mehrere Befehlszeilenparameter einschließen, um Sie an die Start Anwendung zu übergeben.

### <a name="useautoplay"></a>Useautoplay

Unter Windows XP gibt der **useautoplay** -Eintrag an, dass AutoPlay anstelle von Autorun verwendet werden soll.

Unter Windows Vista und höher bewirkt dieser Eintrag, dass alle für Autorun angegebenen Aktionen (entweder mithilfe der Einträge " **Open** " oder " **ShellExecute** ") im Dialogfeld "AutoPlay" unterdrückt werden. Dieser Eintrag hat keine Auswirkung auf ältere Windows-Versionen als Windows XP.

Wenn Sie unter Windows 8 und höher den Wert 0 angeben, wird die automatische Wiedergabe für dieses Gerät deaktiviert.

### <a name="parameters"></a>Parameter

Um diese Option zu verwenden, fügen Sie der Datei Autorun. inf einen Eintrag für **useautoplay** hinzu, und legen Sie den Eintrag auf 1 fest. In Windows-Versionen vor Windows 8 wird kein anderer Wert unterstützt.

Geben Sie unter Windows 8 und höher den Wert 0 an, um die automatische Wiedergabe für dieses Gerät zu deaktivieren.


```
UseAutoPlay=1
```



### <a name="remarks"></a>Bemerkungen

**Useautoplay** ist derzeit nur unter Windows XP oder höher und nur auf einem Laufwerk anwendbar, das von [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea) als **Laufwerk- \_ CDROM** festgelegt wird.

Wenn **useautoplay** verwendet wird, werden alle Aktionen, die von den Einträgen " **Open** " oder " **ShellExecute** " in "Autorun. inf" angegeben werden, unter Windows XP ignoriert und im Dialogfeld "AutoPlay" unter Windows Vista ausgelassen.

Autorun wird in der Regel zum automatischen Ausführen oder Laden von auf den eingefügten Medien enthaltenen Medien verwendet, während die automatische Wiedergabe ein Dialogfeld mit einer Liste relevanter Aktionen darstellt, die durchgeführt werden können, und dem Benutzer die Auswahl der auszuführenden Aktion ermöglicht. Weitere Informationen zu den Unterschieden zwischen Autorun und AutoPlay finden Sie unter [Erstellen einer Autorun-aktivierten CD-ROM-Anwendung](autoplay.md) und [verwenden und Konfigurieren der automatischen AutoPlay](autoplay2k-using.md).

### <a name="usage-example"></a>Verwendungsbeispiel

Eine CD enthält drei Dateien: autorun. inf, Readme.txt und Music. WMA. Abhängig von der verwendeten Windows-Version und den in Autorun. inf angegebenen Optionen kann die CD beim Einfügen entweder durch Autorun oder AutoPlay verarbeitet werden (vorausgesetzt, Autorun/AutoPlay ist für das Laufwerk aktiviert, in das die CD eingefügt wird).

Nehmen Sie zunächst eine Autorun. inf-Datei mit folgendem Inhalt in Erwägung, und beachten Sie, dass **useautoplay = 1** nicht angegeben ist:


```
[AutoRun]
shellexecute="Readme.txt"
```



Die Aktion, die von der Shell durchgeführt wird, wenn diese CD eingefügt wird, hängt von der verwendeten Windows-Version ab:

-   Unter Windows XP oder früher wird diese CD von Autorun verarbeitet, wenn Sie eingefügt wird. In diesem Fall wird der Eintrag **ShellExecute** gelesen, und die Shell Ruft den Datei Handler auf, der den txt-Dateien zugeordnet ist. in der Regel würde dies Readme.txt in Notepad öffnen.
-   Unter Windows Vista bewirkt das vorhanden sein einer Autorun. inf-Datei mit einem **ShellExecute** -Eintrag, dass das Medium als AutoPlay-Typ "Software und Games" identifiziert wird. In diesem Fall wird dem Benutzer ein Dialogfeld für die automatische Wiedergabe angezeigt, in dem die durch den Eintrag **ShellExecute** angegebene Aktion (als "Load Readme.txt" im Dialogfeld dargestellt) zusammen mit den Medien vom Typ "Software und Spiele" angezeigt wird.

Um anzugeben, dass AutoPlay anstelle von Autorun unter Windows XP verwendet werden soll, und dass die vom Autorun ShellExecute-Eintrag angegebene Aktion im Dialogfeld "AutoPlay" unter Windows Vista unterdrückt werden soll, fügen Sie **useautoplay** wie folgt in die Datei Autorun. inf ein:


```
[AutoRun]
shellexecute="Readme.txt"
UseAutoPlay=1
```



Die Aktion, die von der Shell durchgeführt wird, wenn diese CD eingefügt wird, hängt von der verwendeten Windows-Version ab.

-   In früheren Windows-Versionen als Windows XP wird Autorun weiterhin verwendet, und die von **ShellExecute** angegebene Aktion wird ausgeführt, wie zuvor beschrieben. (Beachten Sie, dass nur Autorun in früheren Windows-Versionen als Windows XP verfügbar ist.)
-   Unter Windows XP bewirkt der **useautoplay** -Eintrag, dass AutoPlay anstelle von Autorun verwendet wird. In diesem Fall wird durch die automatische Wiedergabe festgelegt, dass das Medium eine Windows Media Audio Datei (. WMA) enthält, und der Inhalt wird als "Musikdateien" kategorisiert. Dem Benutzer wird ein Dialogfeld für die automatische Wiedergabe mit registrierten Handlern für den Medientyp "Musikdateien" angezeigt. der Eintrag Autorun ShellExecute wird ignoriert.

### <a name="shellexecute"></a>ShellExecute

[Version 5,0.](versions.md) Der Eintrag **ShellExecute** gibt eine Anwendung oder eine Datendatei an, die Autorun zum Aufrufen von [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)verwendet.


```
shellexecute=[filepath\]filename[param1, [param2]...] 
```



### <a name="parameters"></a>Parameter

-   *FilePath*

    Eine Zeichenfolge, die den voll qualifizierten Pfad des Verzeichnisses enthält, das die Daten oder die ausführbare Datei enthält. Wenn kein Pfad angegeben wird, muss sich die Datei im Stammverzeichnis des Laufwerks befinden.

-   *filename*

    Eine Zeichenfolge, die den Dateinamen enthält. Wenn es sich um eine ausführbare Datei handelt, wird Sie gestartet. Wenn es sich um eine Datendatei handelt, muss Sie ein Member eines [Dateityps](fa-file-types.md)sein. [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) starten Sie den Standardbefehl, der dem Dateityp zugeordnet ist.

-   *paramx*

    Enthält alle zusätzlichen Parameter, die an [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)weitergeleitet werden sollen.

### <a name="remarks"></a>Bemerkungen

Dieser Eintrag ist ähnlich wie [geöffnet](#parameters), ermöglicht Ihnen jedoch die Verwendung von [Datei](fa-intro.md) Zuordnungs Informationen, um die Anwendung auszuführen.

### <a name="shell"></a>Shell

Der **shelleintrag** gibt einen Standardbefehl für das Kontextmenü des Laufwerks an.


```
shell=verb
```



### <a name="parameters"></a>Parameter

-   *Verb*

    Das Verb, das dem Menübefehl entspricht. Das Verb und der zugehörige Menübefehl müssen in der Datei "Autorun. inf" mit [einem \\ shellverb](#shellverb) Eintrag definiert werden.

### <a name="remarks"></a>Bemerkungen

Wenn ein Benutzer mit der rechten Maustaste auf das Laufwerk Symbol klickt, wird ein Kontextmenü angezeigt. Wenn eine Autorun. inf-Datei vorhanden ist, wird der Standardkontext Menübefehl davon übernommen. Dieser Befehl wird auch ausgeführt, wenn der Benutzer auf das Laufwerk Symbol doppelklickt.

Um den Standardkontext Menübefehl anzugeben, definieren Sie zuerst das Verb, die Befehls Zeichenfolge und den Menütext mit dem [ \\ shellverb](#shellverb). Verwenden Sie dann Shell, um Sie als Standardkontext Menübefehl zu verwenden. Andernfalls ist der Standardmenü Element Text "AutoPlay", wodurch die Anwendung gestartet wird, die durch den [geöffneten](#parameters) Eintrag angegeben wird.

### <a name="shellverb"></a>\\shellverb

Mit dem Eintrag für den **\\ shellverb** wird dem Kontextmenü des Laufwerks ein benutzerdefinierter Befehl hinzugefügt.


```
shell\verb\command=Filename.exe 
shell\verb=MenuText
```



### <a name="parameters"></a>Parameter

-   *Verb*

    Das Verb des Menübefehls. Der *_\\ Befehls_* Eintrag des **\\ shellverbs** ordnet das Verb einer ausführbaren Datei zu. Verben dürfen keine eingebetteten Leerzeichen enthalten. Standardmäßig ist das *Verb* der Text, der im Kontextmenü angezeigt wird.

-   *Filename.exe*

    Der Pfad und der Dateiname der Anwendung, die die Aktion ausführt.

-   *MenuText*

    Dieser Parameter gibt den Text an, der im Kontextmenü angezeigt wird. Wenn der Wert weggelassen wird, wird das *Verb* angezeigt. *MenuText* kann gemischt und Leerzeichen enthalten. Sie können eine Tastenkombination für das Menü Element festlegen, indem Sie ein kaufmännisches und-Element (&) vor dem Buchstaben platzieren.

### <a name="remarks"></a>Bemerkungen

Wenn ein Benutzer mit der rechten Maustaste auf das Laufwerk Symbol klickt, wird ein Kontextmenü angezeigt. Durch das Hinzufügen von **\\ shellverb** Einträgen zur Autorun. inf-Datei des Laufwerks können Sie diesem Kontextmenü Befehle hinzufügen.

Dieser Eintrag besteht aus zwei Teilen, die sich in separaten Zeilen befinden müssen. Der erste Teil ist der *_\\ Befehl_* **\\ shellverb**. Sie ist erforderlich. Eine Zeichenfolge, die als *Verb* bezeichnet wird, wird mit der Anwendung verknüpft, die beim Ausführen des Befehls gestartet werden soll. Der zweite Teil ist der **\\ shellverb** Eintrag. Der Vorgang ist optional. Sie können ihn einschließen, um den Text anzugeben, der im Kontextmenü angezeigt wird.

Um einen Standardkontext Menübefehl anzugeben, definieren Sie das Verb mit dem **\\ shellverb**, und legen Sie es als Standardbefehl mit dem [shelleintrag](#autoruninf-entries) fest.

Das folgende Autorun. inf-Beispiel Fragment *ordnet das Readit* -Verb der Befehls Zeichenfolge "Notepad ABC \\readme.txt" zu. Der Menütext ist "Read Me", und "'m" ist als Tastenkombination des Elements definiert. Wenn der Benutzer diesen Befehl auswählt, wird die Datei ABCreadme.txt des Laufwerks \\ mit Microsoft Notepad geöffnet.


```
shell\readit\command=notepad abc\readme.txt 
shell\readit=Read &Me
```



## <a name="content-keys"></a>\[Inhalts \] Schlüssel

Es gibt drei Dateityp Schlüssel: " **musicfiles**", " **PictureFiles**" und " **Videofiles**".

Wenn einer dieser Inhalte durch die Werte 1, y, Yes, t oder true auf true festgelegt ist, zeigt die Autoplay-Benutzeroberfläche die diesem Inhaltstyp zugeordneten Handler an, unabhängig davon, ob Inhalt dieses Typs auf dem Medium vorhanden ist.

Wenn einer dieser Inhalte durch die Werte 0, n, Nein, f oder false auf false festgelegt ist, werden die diesem Inhaltstyp zugeordneten Handler von der Benutzeroberfläche für die automatische Wiedergabe nicht angezeigt, auch wenn Inhalt dieses Typs auf dem Medium erkannt wird.

Die Verwendung dieses Abschnitts soll Inhalts Entwicklern ermöglichen, die Absicht von Inhalten an die automatische Wiedergabe zu übermitteln. Beispielsweise kann eine CD so kategorisiert werden, dass Sie nur Musikinhalte enthält, obwohl Sie auch über Bilder und Videos verfügt und andernfalls als gemischte Inhalte angesehen werden würde.

Der Abschnitt " **\[ Inhalt \]** " wird nur unter Windows Vista und höher unterstützt.


```
[Content]
MusicFiles=Y
PictureFiles=0
VideoFiles=false
```



## <a name="exclusivecontentpaths-keys"></a>\[Exclusivecontentpath- \] Schlüssel

Die in diesem Abschnitt aufgeführten Ordner schränken die automatische Wiedergabe ein, um nur die Ordner und deren Unterordner nach Inhalt zu durchsuchen. Sie können mit oder ohne einen führenden umgekehrten Schrägstrich () angegeben werden \\ . In beiden Fällen werden Sie als absolute Pfade aus dem Stammverzeichnis des Mediums übernommen. Wenn Ordner mit Leerzeichen in ihren Namen vorliegen, dürfen diese nicht in Anführungszeichen eingeschlossen werden, da die Anführungszeichen als Teil des Pfads wörtlich genommen werden.

Die Verwendung dieses Abschnitts soll es Autoren von Inhalten ermöglichen, die Absicht von Inhalten an die automatische Wiedergabe zu übermitteln und die Überprüfungs Zeit zu verkürzen, indem die Überprüfung auf bestimmte wichtige Bereiche der Medien beschränkt wird.

Die folgenden Pfade sind gültig.


```
[ExclusiveContentPaths]
\music
\music\more music
music2
```



Der Abschnitt " **\[ exclusivecontentpath \]** " wird nur unter Windows Vista und höher unterstützt.

## <a name="ignorecontentpaths-keys"></a>\[Ignorecontentpath- \] Schlüssel

Die in diesem Abschnitt aufgeführten Ordner und deren Unterordner werden bei der Suche nach Inhalten von einem Medium ignoriert. Sie können mit oder ohne einen führenden umgekehrten Schrägstrich () angegeben werden \\ . In beiden Fällen werden Sie als absolute Pfade aus dem Stammverzeichnis des Mediums übernommen. Wenn Ordner mit Leerzeichen in ihren Namen vorliegen, dürfen diese nicht in Anführungszeichen eingeschlossen werden, da die Anführungszeichen als Teil des Pfads wörtlich genommen werden.

Die Pfade in diesem Abschnitt haben Vorrang vor Pfaden im Abschnitt **\[ exclusivecontentpath \]** . Wenn ein in **\[ ignorecontentpath \]** angegebener Pfad ein Unterordner eines in **\[ exclusivecontentpath \]** angegebenen Pfads ist, wird er weiterhin ignoriert.

Die Verwendung dieses Abschnitts soll es Autoren von Inhalten ermöglichen, die Absicht von Inhalten an die automatische Wiedergabe zu übermitteln und die Überprüfungs Zeit zu verkürzen, indem die Überprüfung auf bestimmte wichtige Bereiche der Medien beschränkt wird.

Die folgenden Pfade sind gültig.


```
[IgnoreContentPaths]
\music
\music\more music
music2
```



Der **\[ ignorecontentpath \]** -Abschnitt wird nur unter Windows Vista und höher unterstützt.

## <a name="deviceinstall-keys"></a>\[Schlüssel für "de viceingestall" \]

### <a name="driverpath"></a>DriverPath "

Der Eintrag **DriverPath** gibt ein Verzeichnis an, in dem rekursiv nach Treiberdateien gesucht werden soll. Dieser Befehl wird während einer Treiberinstallation verwendet und ist nicht Teil eines Autorun-Vorgangs. Der Abschnitt " **\[ deviceingestall \]** " wird nur unter Windows XP unterstützt.


```
[DeviceInstall]
DriverPath=directorypath
```



### <a name="parameters"></a>Parameter

-   *DirectoryPath*

    Ein Pfad zu einem Verzeichnis, in dem Windows nach Treiberdateien sucht, sowie alle zugehörigen Unterverzeichnisse.

### <a name="remarks"></a>Bemerkungen

Verwenden Sie die Laufwerk Buchstaben nicht in *Director Path* , wenn Sie von einem Computer zum nächsten wechseln.

Fügen Sie zum Durchsuchen mehrerer Verzeichnisse einen **DriverPath** -Eintrag für jedes Verzeichnis hinzu, wie in diesem Beispiel.


```
[DeviceInstall]
DriverPath=drivers\video 
DriverPath=drivers\audio
```



Wenn kein **DriverPath** -Eintrag im Abschnitt " **\[ deviceinstall \]** " bereitgestellt wird oder der Eintrag " **DriverPath** " keinen Wert aufweist, wird dieses Laufwerk bei der Suche nach Treiberdateien übersprungen.

 

 
