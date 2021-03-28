---
description: In diesem Thema wird erläutert, wie Anwendungen Informationen über sich selbst verfügbar machen können, um bestimmte Szenarien zu ermöglichen.
ms.assetid: F88AA3E6-6F7B-442d-935A-7D2CB4958E6B
title: Anwendungs Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 857e96893d2fe717f1a4939d06c77af043ead318
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958777"
---
# <a name="application-registration"></a>Anwendungs Registrierung

In diesem Thema wird erläutert, wie Anwendungen Informationen über sich selbst verfügbar machen können, um bestimmte Szenarien zu ermöglichen. Dies umfasst Informationen, die erforderlich sind, um die Anwendung zu finden, die von der Anwendung unterstützten Verben und die Dateitypen, die von einer Anwendung verarbeitet werden können.

Dieses Thema ist wie folgt organisiert:

-   [Suchen einer ausführbaren Datei der Anwendung](#finding-an-application-executable)
-   [Anwendungen werden registriert](#registering-applications)
    -   [Verwenden des unter Schlüssels für App-Pfade](#using-the-app-paths-subkey)
    -   [Verwenden des unter Schlüssels "Anwendungen"](#using-the-applications-subkey)
-   [Registrieren von Verben und anderen Datei Zuordnungs Informationen](#registering-verbs-and-other-file-association-information)
-   [Registrieren eines erkannten Typs](#registering-a-perceived-type)
-   [Zugehörige Themen](#related-topics)

> [!Note]  
> Anwendungen können auch in den Einstellungen "Programm Zugriff und Computer Standards festlegen" (SPAD) registriert und die System Steuerungsanwendungen für die Standardprogramme (SYDP) festgelegt werden. Informationen zur Registrierung von SPAD-und SYDP-Anwendungen finden Sie unter [Richtlinien für Dateizuordnungen und Standardprogramme](appguide-fa-defpro.md)und [Festlegen des Programm Zugriffs und der Computer Standards (SPAD)](cpl-setprogramaccess.md).

 

## <a name="finding-an-application-executable"></a>Suchen einer ausführbaren Datei der Anwendung

Wenn die [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) -Funktion mit dem Namen einer ausführbaren Datei im *lpfile* -Parameter aufgerufen wird, gibt es mehrere Stellen, an denen die Funktion nach der Datei sucht. Es wird empfohlen, die Anwendung im Registrierungs Unterschlüssel **App-Pfade** zu registrieren. Dadurch entfällt die Notwendigkeit, dass Anwendungen die Systempfad-Umgebungsvariable ändern.

Die Datei wird an den folgenden Speicherorten gesucht:

-   Das aktuelle Arbeitsverzeichnis
-   Nur das **Windows** -Verzeichnis (es werden keine Unterverzeichnisse durchsucht).
-   Das **Windows \\ system32** -Verzeichnis.
-   Verzeichnisse, die in der PATH-Umgebungsvariablen aufgelistet sind.
-   Empfohlen: **HKEY \_ local \_ Machine** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion**- \\ **App-Pfade**

## <a name="registering-applications"></a>Anwendungen werden registriert

Die Registrierungs Unterschlüssel **App-Pfade** und **Anwendungen** werden verwendet, um das Verhalten des Systems im Auftrag von Anwendungen zu registrieren und zu steuern. Der Unterschlüssel für **App-Pfade** ist der bevorzugte Speicherort.

### <a name="using-the-app-paths-subkey"></a>Verwenden des unter Schlüssels für App-Pfade

In Windows 7 und höher wird dringend empfohlen, Anwendungen pro Benutzer anstatt pro Computer zu installieren. Eine Anwendung, die für pro Benutzer installiert wird, kann unter **HKEY \_ Current \_ User** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **app path** registriert werden. Eine Anwendung, die für alle Benutzer des Computers installiert ist, kann unter **HKEY \_ local \_ Machine** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **app path** registriert werden.

Die unter APP- **Pfade** gefundenen Einträge werden hauptsächlich für folgende Zwecke verwendet:

-   , Um den Namen der ausführbaren Datei einer Anwendung dem voll qualifizierten Pfad der Datei zuzuordnen.
-   , Um der Umgebungsvariablen "Path" pro Anwendung, pro Prozess, Informationen vorab hinzufügen zu können.

Wenn der Name eines unter Schlüssels von **App-Pfaden** mit dem Dateinamen übereinstimmt, führt die Shell zwei Aktionen aus:

-   Der (standardmäßige) Eintrag wird als voll qualifizierter Pfad der Datei verwendet.
-   Der Pfad Eintrag für diesen Unterschlüssel wird der PATH-Umgebungsvariablen dieses Prozesses vorausgeht. Wenn dies nicht erforderlich ist, kann der Pfadwert weggelassen werden.

Folgende mögliche Probleme sind zu beachten:

-   Die Shell schränkt die Länge einer Befehlszeile auf Max \_ . Pfad \* 2 Zeichen ein. Wenn viele Dateien als Registrierungseinträge aufgeführt sind oder die Pfade lang sind, können die Dateinamen später in der Liste verloren gehen, wenn die Befehlszeile abgeschnitten wird.
-   Einige Anwendungen akzeptieren nicht mehrere Dateinamen in einer Befehlszeile.
-   Einige Anwendungen, die mehrere Dateinamen akzeptieren, erkennen nicht das Format, in dem Sie von der Shell bereitgestellt werden. Die Shell stellt die Parameterliste als Zeichenfolge in Anführungszeichen bereit, aber einige Anwendungen erfordern möglicherweise Zeichen folgen ohne Anführungszeichen.
-   Nicht alle Elemente, die gezogen werden können, sind Teil des Dateisystems. beispielsweise Drucker. Diese Elemente verfügen über keinen standardmäßigen Win32-Pfad. Daher gibt es keine Möglichkeit, für [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)einen sinnvollen *lpparameter* -Wert bereitzustellen.

Die Verwendung des DropTarget-Eintrags vermeidet diese potenziellen Probleme durch die Bereitstellung des Zugriffs auf alle Zwischenablage Formate, einschließlich [cfstr \_ shellidlist](clipboard.md) (für lange Dateilisten) und [cfstr \_ File Content](clipboard.md) (für nicht-Dateisystem Objekte).

So **registrieren und Steuern Sie das Verhalten Ihrer Anwendungen mit dem Unterschlüssel für App-Pfade**:

1.  Fügen Sie dem Unterschlüssel für **App-Pfade** einen Unterschlüssel mit dem gleichen Namen wie die ausführbare Datei hinzu, wie im folgenden Registrierungs Eintrag gezeigt.

    ```
    HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
       SOFTWARE
          Microsoft
             Windows
                CurrentVersion
                   App Paths
                      file.exe
                         (Default)
                         DontUseDesktopChangeRouter
                         DropTarget
                         Path
                         UseUrl
    ```

2.  In der folgenden Tabelle finden Sie Details zu den Unterschlüssel Einträgen für **App-Pfade** . 

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Registrierungseintrag</th>
    <th>Details</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>(Standardwert)</td>
    <td>Der voll qualifizierte Pfad der Anwendung. Der im (Standard-) Eintrag angegebene Anwendungsname kann mit oder ohne Erweiterung. exe angegeben werden. Bei Bedarf fügt die <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> -Funktion beim Durchsuchen des unter Schlüssels der <strong>App-Pfade</strong> die Erweiterung hinzu. Der Eintrag ist vom <strong>REG_SZ</strong> Typ.</td>
    </tr>
    <tr class="even">
    <td>Dontusedesktopchangerouter</td>
    <td>Ist für Debugger-Anwendungen obligatorisch, um beim Debuggen des Windows-Explorer-Prozesses Datei Dialogfelder zu vermeiden. Das Festlegen des "dontusedesktopchangerouter"-Eintrags führt jedoch zu einer etwas weniger effizienten Behandlung der Änderungs Benachrichtigungen. Der Eintrag ist vom <strong>REG_DWORD</strong> Typ, und der Wert ist 0x1.</td>
    </tr>
    <tr class="odd">
    <td>DropTarget</td>
    <td>Ist ein Klassen Bezeichner (CLSID). Der DropTarget-Eintrag enthält die CLSID eines Objekts (in der Regel ein lokaler Server anstelle eines in-Process-Servers), der <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a>implementiert. Wenn das Ablage Ziel eine ausführbare Datei ist und kein DropTarget-Wert bereitgestellt wird, konvertiert die Shell standardmäßig die Liste der gelöschten Dateien in einen Befehlszeilenparameter und übergibt Sie mithilfe von <em>lpparameters</em>an <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> .</td>
    </tr>
    <tr class="even">
    <td>`Path`</td>
    <td>Stellt eine Zeichenfolge (in Form einer durch Semikolons getrennten Liste von Verzeichnissen) bereit, die an die PATH-Umgebungsvariable angehängt werden soll, wenn eine Anwendung durch den Aufruf von <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a>aufgerufen wird. Dabei handelt es sich um den voll qualifizierten Pfad der exe-Datei. Es ist <strong>REG_SZ</strong>. In <strong>Windows 7 und</strong>höher kann der Typ <strong>REG_EXPAND_SZ</strong>werden und ist häufig <strong>REG_EXPAND_SZ</strong> % Program Files%.
    <blockquote>
    [!Note]<br />
Zusätzlich zu den (Standard), Pfad-und DropTarget-Einträgen, die von der Shell erkannt werden, kann eine Anwendung auch benutzerdefinierte Werte dem <strong>App-Pfad</strong> -Unterschlüssel der ausführbaren Datei hinzufügen. Wir empfehlen Anwendungsentwicklern, den <strong>App</strong> -Pfad-Unterschlüssel zu verwenden, um einen anwendungsspezifischen Pfad bereitzustellen, anstatt Erweiterungen zum globalen Systempfad zu erstellen.
    </blockquote>
    <br/></td>
    </tr>
    <tr class="odd">
    <td>SupportedProtocols</td>
    <td>Erstellt eine Zeichenfolge, die die URL-Protokoll Schemas für einen angegebenen Schlüssel enthält. Dies kann mehrere Registrierungs Werte enthalten, um anzugeben, welche Schemas unterstützt werden. Diese Zeichenfolge folgt dem Format von <strong>scheme1: scheme2</strong>. Wenn diese Liste nicht leer ist, wird die <strong>Datei:</strong> der Zeichenfolge hinzugefügt. Dieses Protokoll wird implizit unterstützt, wenn " <em>supportedprotokolls</em> " definiert ist. <br/></td>
    </tr>
    <tr class="even">
    <td>UseUrl</td>
    <td>Gibt an, dass die Anwendung eine URL (anstelle eines Datei namens) in der Befehlszeile annehmen kann. Anwendungen, die Dokumente direkt aus dem Internet öffnen können, wie Webbrowser und Medien Player, sollten diesen Eintrag festlegen. <br/> Wenn die <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> -Funktion eine Anwendung startet und der Wert useurl = 1 nicht festgelegt ist, lädt <strong>ShellExecuteEx</strong> das Dokument in eine lokale Datei herunter und ruft den Handler für die lokale Kopie auf.<br/> Wenn für die Anwendung z. b. dieser Eintrag festgelegt ist und ein Benutzer mit der rechten Maustaste auf eine auf einem Webserver gespeicherte Datei klickt, wird das geöffnete Verb verfügbar gemacht. Wenn dies nicht der Fall ist, muss der Benutzer die Datei herunterladen und die lokale Kopie öffnen. <br/> Der useurl-Eintrag hat <strong>REG_DWORD</strong> Typ, und der Wert ist 0x1.<br/> In Windows Vista und früheren Versionen hat dieser Eintrag angegeben, dass die URL zusammen mit einem lokalen Dateinamen an die Anwendung weitergegeben werden soll, wenn Sie über ShellExecuteEx aufgerufen wird. In Windows 7 deutet dies darauf hin, dass die Anwendung jede HTTP-oder HTTPS-URL, die an Sie übergeben wird, verstehen kann, ohne auch den Cache Dateinamen angeben zu müssen. Dieser Registrierungsschlüssel ist mit dem <em>supportedprotokolls</em> -Schlüssel verknüpft.<br/></td>
    </tr>
    </tbody>
    </table>

    

     

### <a name="using-the-applications-subkey"></a>Verwenden des unter Schlüssels "Anwendungen"

Durch die Einbindung von Registrierungs Einträgen unter den **HKEY \_ - \_ Klassen** Stamm \\ **Anwendungen** \\ *ApplicationName.exe* Unterschlüssel können Anwendungen die anwendungsspezifischen Informationen bereitstellen, die in der folgenden Tabelle aufgeführt sind.



| Registrierungseintrag                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \\shellverb                      | Stellt die Verb Methode zum Aufrufen der Anwendung aus openWith bereit. Ohne eine hier angegebene Verb Definition geht das System davon aus, dass die Anwendung "up [**Process**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)" unterstützt, und übergibt den Dateinamen in der Befehlszeile. Diese Funktion gilt für alle Verb-Methoden, einschließlich DropTarget, ExecuteCommand und dynamischer Datenaustausch (DDE).                                                                                                                                                                                                                                                                                                                            |
| DefaultIcon                      | Ermöglicht es einer Anwendung, ein bestimmtes Symbol zur Darstellung der Anwendung bereitzustellen, anstatt das erste Symbol, das in der exe-Datei gespeichert ist.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Friendlyappname                  | Bietet eine Möglichkeit, einen lokalisierbaren Namen für eine Anwendung zu erhalten, anstatt nur die angezeigten Versionsinformationen anzuzeigen, die möglicherweise nicht lokalisierbar sind. Die Association-Abfrage [**assocstr**](/windows/desktop/api/Shlwapi/ne-shlwapi-assocstr) liest diesen Registrierungs Eintrags Wert und greift auf den FileDescription-Namen in den Versionsinformationen zurück. Wenn dieser Name fehlt, wird für die Zuordnungs Abfrage standardmäßig der Anzeige Name der Datei verwendet. Anwendungen sollten mithilfe von **assocstr \_ friendlyappname** diese Informationen abrufen, um das richtige Verhalten zu erhalten.                                                                                                                                                                        |
| SupportedTypes                   | Listet die Dateitypen auf, die von der Anwendung unterstützt werden. Dadurch kann die Anwendung im Dialogfeld **Öffnen mit** im Menü Cascade aufgeführt werden.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Noopenwith                       | Gibt an, dass keine Anwendung zum Öffnen dieses Dateityps angegeben wird. Beachten Sie, dass, wenn ein OpenWithProgIds-Unterschlüssel für eine Anwendung nach Dateityp festgelegt wurde und der ProgID-Unterschlüssel selbst nicht auch über einen noopenwith-Eintrag verfügt, diese Anwendung in der Liste der empfohlenen oder verfügbaren Anwendungen angezeigt wird, auch wenn Sie den Eintrag noopenwith angegeben hat. Weitere Informationen finden Sie unter Gewusst wie: [Einschließen einer Anwendung im Dialogfeld "Öffnen mit](how-to-include-an-application-on-the-open-with-dialog-box.md) " und [ausschließen einer Anwendung aus dem Dialogfeld Öffnen mit](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md).<br/> |
| Ishostapp                        | Gibt an, dass es sich bei dem Prozess um einen Host Prozess handelt, z. b. Rundll32.exe oder Dllhost.exe, und sollte nicht für das **anheten des Start** Menüs oder das einschließen in die Liste der am häufigsten verwendeten (MFU-) Anforderungen Beim Start mit einer Verknüpfung, die eine Argumentliste ungleich NULL oder eine explizite [Anwendungs Benutzer Modell-ID (appusermudelids)](appids.md)enthält, kann der Prozess fixiert werden. Solche Verknüpfungen sind Kandidaten für die Einbindung in die MFU-Liste.                                                                                                                                                                                                                                                  |
| NoStartPage                      | Gibt an, dass die ausführbare Datei der Anwendung und Verknüpfungen aus dem **Startmenü** ausgeschlossen und in der MFU-Liste fixiert oder eingeschlossen werden sollen. Dieser Eintrag wird normalerweise verwendet, um System Tools, Installationsprogramme und Uninstaller sowie Info Dateien auszuschließen.                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Useexecutablefortaskbargroupicon | Bewirkt, dass die Taskleiste das Standard Symbol dieser ausführbaren Datei verwendet, wenn für diese Anwendung keine Einfügbare Verknüpfung vorhanden ist, und nicht das Symbol des Fensters, das zuerst gefunden wurde.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Taskbargroupicon                 | Gibt das Symbol an, das zum Überschreiben des Task leisten Symbols verwendet wird. Das Fenster Symbol wird normalerweise für die Taskleiste verwendet. Wenn Sie den Eintrag taskbargroupicon festlegen, verwendet das System stattdessen das Symbol aus der exe-Anwendung für die Anwendung.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

### <a name="examples"></a>Beispiele

Einige Beispiele für Anwendungs Registrierungen über die **HKEY- \_ Klassen \_** Stamm \\ **Anwendungen** \\ *ApplicationName.exe* Unterschlüssel lauten wie folgt. Alle Registrierungs Eintrags Werte sind vom Typ " **reg \_ SZ** ", mit Ausnahme von " **DefaultIcon** " mit dem Typ " **reg \_ Expand \_ SZ** ".

```
HKEY_CLASSES_ROOT
   Applications
      wordpad.exe
         FriendlyAppName = @%SystemRoot%\System32\shell32.dll,-22069
```

```
HKEY_CLASSES_ROOT
   Applications
      wmplayer.exe
         SupportedTypes
            .3gp2
```

```
HKEY_CLASSES_ROOT
   Applications
      wmplayer.exe
         DefaultIcon
            (Default) = %SystemRoot%\system32\wmploc.dll,-730
```

```
HKEY_CLASSES_ROOT
   Applications
      WScript.exe
         NoOpenWith
```

```
HKEY_CLASSES_ROOT
   Applications
      photoviewer.dll
         shell
            open
               DropTarget
                  Clsid = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
```

```
HKEY_CLASSES_ROOT
   Applications
      mspaint.exe
         SupportedTypes
            .bmp
            .dib
            .rle
            .jpg
            .jpeg
            .jpe
            .jfif
            .gif
            .emf
            .wmf
            .tif
            .tiff
            .png
            .ico
```

## <a name="registering-verbs-and-other-file-association-information"></a>Registrieren von Verben und anderen Datei Zuordnungs Informationen

Unterschlüssel, die unter den **HKEY- \_ Klassen " \_ root** \\ **systemfilezuordnungen** " registriert sind, ermöglichen der Shell, das Standardverhalten von Attributen für Dateitypen zu definieren und freigegebene Dateizuordnungen Wenn Benutzer die Standardanwendung für einen Dateityp ändern, hat die ProgID der neuen Standardanwendung eine Priorität bei der Bereitstellung von Verben und anderen Zuordnungs Informationen. Diese Priorität ist darauf zurückzuführen, dass es sich um den ersten Eintrag im Association-Array handelt. Wenn das Standardprogramm geändert wird, sind die Informationen unter der vorherigen ProgID nicht mehr verfügbar.

Wenn Sie proaktiv mit den Folgen einer Änderung an Standardprogrammen umgehen möchten, können Sie die **HKEY- \_ Klassen " \_ root** \\ **systemfileassociation** " verwenden, um Verben und andere Zuordnungs Informationen zu registrieren. Aufgrund ihrer Position nach der ProgID im Association-Array haben diese Registrierungen eine niedrigere Priorität. Diese systemfileassociationsregistrierungen sind auch dann stabil, wenn Benutzer die Standardprogramme ändern, und geben einen Speicherort zum Registrieren sekundärer Verben an, die für einen bestimmten Dateityp immer verfügbar sein werden. Ein Beispiel für die Registrierung finden Sie unter [Registrieren eines erkannten Typs](#registering-a-perceived-type) weiter unten in diesem Thema.

Das folgende Registrierungs Beispiel zeigt, was geschieht, wenn der Benutzer das Element " **Standardprogramme** " in der Systemsteuerung ausführt, um die Standardeinstellung für. MP3-Dateien in App2ProgID zu ändern. Nach dem Ändern der Standardeinstellung ist Verb1 nicht mehr verfügbar, und Verb2 wird zum Standard.

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = App1ProgID
```

```
HKEY_CLASSES_ROOT
   App1ProgID
      shell
         Verb1
```

```
HKEY_CLASSES_ROOT
   App2ProgID
      shell
         Verb2
```

## <a name="registering-a-perceived-type"></a>Registrieren eines erkannten Typs

Registrierungs Werte für wahrgenommene Typen werden als Unterschlüssel des Stamm **\_ \_** \\ **systemfileassociations** -Registrierungs unter Schlüssels der HKEY-Klassen definiert. Beispielsweise wird der erkannte **Typtext** wie folgt registriert:

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      text
         shell
            edit
               command
                  (Default) = "%SystemRoot%\system32\NOTEPAD.EXE" "%1"
            open
               command
                  (Default) = "%SystemRoot%\system32\NOTEPAD.EXE" "%1"
```

Der wahrgenommene Typ eines Dateityps wird durch Einschließen eines "wahrnehmvedtype"-Werts in den Unterschlüssel des Dateityps angegeben. Der Wert "wahrnehmvedtype" wird auf den Namen des erkannten Typs festgelegt, der unter **HKEY \_ Classes \_ root** \\ **systemfileassociations** -Registrierungs Unterschlüssel registriert ist, wie im vorherigen Registrierungs Beispiel gezeigt. Fügen Sie beispielsweise den folgenden Registrierungs Eintrag hinzu, um cpp-Dateien als den wahrgenommenen Typ "Text" zu deklarieren:

```
HKEY_CLASSES_ROOT
   .cpp
      PerceivedType = text
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dateitypen](fa-file-types.md)
</dt> <dt>

[Funktionsweise von Dateizuordnungen](fa-how-work.md)
</dt> <dt>

[Inhaltsansicht nach Dateityp oder-Art](prophand-content-view.md)
</dt> <dt>

[Dateityp Überprüfung](file-type-verifier.md)
</dt> <dt>

[Dateityp Handler](fa-file-extensions.md)
</dt> <dt>

[Programmgesteuerte Bezeichner](fa-progids.md)
</dt> <dt>

[Wahrgenommene Typen](fa-perceivedtypes.md)
</dt> <dt>

[Zuordnungs Arrays](fa-associationarray.md)
</dt> </dl>

