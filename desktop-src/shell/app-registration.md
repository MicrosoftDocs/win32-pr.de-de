---
description: In diesem Thema wird erläutert, wie Anwendungen Informationen über sich selbst verfügbar machen können, die für bestimmte Szenarien erforderlich sind.
ms.assetid: F88AA3E6-6F7B-442d-935A-7D2CB4958E6B
title: Anwendungsregistrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0b9647809f46c2147ab6ed464f0e8de1d7ef0df
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122464857"
---
# <a name="application-registration"></a>Anwendungsregistrierung

In diesem Thema wird erläutert, wie Anwendungen Informationen über sich selbst verfügbar machen können, die für bestimmte Szenarien erforderlich sind. Dies schließt Informationen ein, die zum Suchen der Anwendung erforderlich sind, die von der Anwendung unterstützten Verben und die Dateitypen, die eine Anwendung verarbeiten kann.

Dieses Thema ist wie folgt organisiert:

-   [Suchen einer ausführbaren Anwendungsdatei](#finding-an-application-executable)
-   [Registrieren von Anwendungen](#registering-applications)
    -   [Verwenden des Unterschlüssels "App Paths"](#using-the-app-paths-subkey)
    -   [Verwenden des Unterschlüssels "Anwendungen"](#using-the-applications-subkey)
-   [Registrieren von Verben und anderen Dateiassozinformationen](#registering-verbs-and-other-file-association-information)
-   [Registrieren eines wahrgenommenen Typs](#registering-a-perceived-type)
-   [Zugehörige Themen](#related-topics)

> [!Note]  
> Anwendungen können auch in den Systemsteuerungsanwendungen Set Program Access and Computer Defaults (SPAD) und Set Your Default Programs (SYDP) registriert werden. Informationen zur SPAD- und SYDP-Anwendungsregistrierung finden Sie unter [Richtlinien](appguide-fa-defpro.md)für Dateizuordnungen und Standardprogramme und Festlegen von Programmzugriff und [Computereinstellungen (SPAD).](cpl-setprogramaccess.md)

 

## <a name="finding-an-application-executable"></a>Suchen einer ausführbaren Anwendungsdatei

Wenn die [**ShellExecuteEx-Funktion**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) mit dem Namen einer ausführbaren Datei im *lpFile-Parameter* aufgerufen wird, gibt es mehrere Stellen, an denen die Funktion nach der Datei sucht. Es wird empfohlen, Ihre Anwendung im **Registrierungsunterschlüssel App Paths** zu registrieren. Dadurch wird vermieden, dass Anwendungen die Path-Umgebungsvariable des Systems ändern müssen.

Die Datei wird an den folgenden Speicherorten gesucht:

-   Das aktuelle Arbeitsverzeichnis
-   Das **Windows** verzeichnis (es werden keine Unterverzeichnisse durchsucht).
-   Das **Windows \\ System32-Verzeichnis.**
-   Verzeichnisse, die in der PATH-Umgebungsvariablen aufgeführt sind.
-   Empfohlen: **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion-App-Pfade** \\ 

## <a name="registering-applications"></a>Registrieren von Anwendungen

Sowohl die **Registrierungsunterschlüssel "App Paths"** als auch **"Applications"** werden verwendet, um das Verhalten des Systems im Auftrag von Anwendungen zu registrieren und zu steuern. Der **Unterschlüssel App Paths** ist der bevorzugte Speicherort.

### <a name="using-the-app-paths-subkey"></a>Verwenden des Unterschlüssels "App Paths"

In Windows 7 und höher wird dringend empfohlen, Anwendungen pro Benutzer und nicht pro Computer zu installieren. Eine Anwendung, die für pro Benutzer installiert wird, kann unter **HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion App** Paths registriert \\ **werden.** Eine Anwendung, die für alle Benutzer des Computers installiert ist, kann unter **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **App Paths registriert werden.**

Die Einträge unter **App-Pfade** werden hauptsächlich für die folgenden Zwecke verwendet:

-   So ordnen Sie den Namen der ausführbaren Datei einer Anwendung dem vollqualifizierten Pfad dieser Datei zu.
-   Um Informationen pro Anwendung und pro Prozess in die PATH-Umgebungsvariable vorab zu pendieren.

Wenn der Name eines Unterschlüssels von **App Paths** dem Dateinamen entspricht, führt die Shell zwei Aktionen aus:

-   Der Eintrag (Standard) wird als vollqualifizierter Pfad der Datei verwendet.
-   Der Path-Eintrag für diesen Unterschlüssel ist in die PATH-Umgebungsvariable dieses Prozesses vorgefertigt. Wenn dies nicht erforderlich ist, kann der Path-Wert weggelassen werden.

Mögliche Zu beachtende Probleme:

-   Die Shell beschränkt die Länge einer Befehlszeile auf MAX \_ PATH \* 2 Zeichen. Wenn viele Dateien als Registrierungseinträge aufgeführt sind oder ihre Pfade lang sind, können Dateinamen später in der Liste verloren gehen, wenn die Befehlszeile abgeschnitten wird.
-   Einige Anwendungen akzeptieren nicht mehrere Dateinamen in einer Befehlszeile.
-   Einige Anwendungen, die mehrere Dateinamen akzeptieren, erkennen nicht das Format, in dem die Shell sie zur Verfügung stellt. Die Shell stellt die Parameterliste als Zeichenfolge in Anführungszeichen zur Verfügung, aber einige Anwendungen erfordern möglicherweise Zeichenfolgen ohne Anführungszeichen.
-   Nicht alle Elemente, die gezogen werden können, sind Teil des Dateisystems. z. B. Drucker. Diese Elemente haben keinen Win32-Standardpfad, daher gibt es keine Möglichkeit, [**shellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)einen *aussagekräftigen lpParameters-Wert* zur Verfügung zu stellen.

Die Verwendung des DropTarget-Eintrags vermeidet diese potenziellen Probleme, indem zugriff auf alle Zwischenablageformate ermöglicht wird, einschließlich [CFSTR \_ SHELLIDLIST](clipboard.md) (für lange Dateilisten) und [CFSTR \_ FILECONTENTS](clipboard.md) (für Nichtdateisystemobjekte).

**So registrieren und steuern Sie das Verhalten Ihrer Anwendungen mit dem App Paths-Unterschlüssel:**

1.  Fügen Sie dem Unterschlüssel **App Paths** einen Unterschlüssel mit dem gleichen Namen wie die ausführbare Datei hinzu, wie im folgenden Registrierungseintrag gezeigt.

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

2.  Details zu den Unterschlüsseleinträgen für **App-Pfade** finden Sie in der folgenden Tabelle. 

    
| Registrierungseintrag | Details | 
|----------------|---------|
| (Standardwert) | Der vollqualifizierte Pfad zur Anwendung. Der im Eintrag (Standard) angegebene Anwendungsname kann mit oder ohne die .exe werden. Bei Bedarf fügt die <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx-Funktion</strong></a> die Erweiterung beim Durchsuchen des <strong>Unterschlüssels App Paths</strong> hinzu. Der Eintrag ist vom typ <strong>REG_SZ</strong> Typ. | 
| DontUseDesktopChangeRouter | Ist für Debuggeranwendungen obligatorisch, um Deadlocks im Dateidialogfeld beim Debuggen des Windows Explorer-Prozesses zu vermeiden. Das Festlegen des Eintrags DontUseDesktopChangeRouter führt jedoch zu einer etwas weniger effizienten Behandlung der Änderungsbenachrichtigungen. Der Eintrag ist vom Typ <strong>REG_DWORD,</strong> und der Wert ist 0x1. | 
| DropTarget | Ein Klassenbezeichner (CLSID). Der DropTarget-Eintrag enthält die CLSID eines Objekts (in der Regel ein lokaler Server statt eines Prozessservers), das <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget implementiert.</strong></a> Wenn das Abbruchziel eine ausführbare Datei ist und kein DropTarget-Wert angegeben wird, konvertiert die Shell die Liste der gelöschten Dateien standardmäßig in einen Befehlszeilenparameter und übergibt sie über <em>lpParameters</em>an <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx.</strong></a> | 
| Pfad | Stellt eine Zeichenfolge (in Form einer durch Semikolons getrennten Liste von Verzeichnissen) zum Anfügen an die PATH-Umgebungsvariable bei, wenn eine Anwendung durch Aufrufen von <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx gestartet wird.</strong></a> Dies ist der vollqualifizierte Pfad zum .exe. Sie ist <strong>REG_SZ</strong>. In <strong>Windows 7 und höher</strong>kann der Typ REG_EXPAND_SZ werden, und wird <strong>REG_EXPAND_SZ</strong> %ProgramFiles% verwendet. <strong></strong>    <blockquote>    [!Note]<br />    Zusätzlich zu den Einträgen (Standard), Path und DropTarget, die von der Shell erkannt werden, kann eine Anwendung dem Unterschlüssel <strong>App Paths</strong> ihrer ausführbaren Datei auch benutzerdefinierte Werte hinzufügen. Wir empfehlen Anwendungsentwicklern, den <strong>Unterschlüssel App Paths</strong> zu verwenden, um einen anwendungsspezifischen Pfad zur Verfügung zu stellen, anstatt dem globalen Systempfad Ergänzungen zu machen.    </blockquote><br /> | 
| SupportedProtocols | Erstellt eine Zeichenfolge, die die URL-Protokollschemas für einen bestimmten Schlüssel enthält. Dies kann mehrere Registrierungswerte enthalten, um anzugeben, welche Schemas unterstützt werden. Diese Zeichenfolge folgt dem Format <strong>scheme1:scheme2</strong>. Wenn diese Liste nicht leer ist, <strong>wird file:</strong> der Zeichenfolge hinzugefügt. Dieses Protokoll wird implizit unterstützt, wenn <em>SupportedProtocols</em> definiert ist. <br /> | 
| UseUrl | Gibt an, dass Ihre Anwendung eine URL (anstelle eines Dateinamens) in der Befehlszeile akzeptieren kann. Anwendungen, die Dokumente direkt aus dem Internet öffnen können, z. B. Webbrowser und Media Player, sollten diesen Eintrag festlegen. <br /> Wenn die <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx-Funktion</strong></a> eine Anwendung startet und der UseUrl=1-Wert nicht festgelegt ist, lädt <strong>ShellExecuteEx</strong> das Dokument in eine lokale Datei herunter und ruft den Handler für die lokale Kopie auf.<br /> Wenn die Anwendung beispielsweise über diesen Eintragssatz verfügt und ein Benutzer mit der rechten Maustaste auf eine Datei klickt, die auf einem Webserver gespeichert ist, wird das Verb Öffnen verfügbar gemacht. Falls nicht, muss der Benutzer die Datei herunterladen und die lokale Kopie öffnen. <br /> Der UseUrl-Eintrag ist vom <strong>REG_DWORD,</strong> und der Wert ist 0x1.<br /> In Windows Vista und früher hat dieser Eintrag angegeben, dass die URL zusammen mit einem lokalen Dateinamen an die Anwendung übergeben werden soll, wenn sie über ShellExecuteEx aufgerufen wird. In Windows 7 gibt dies an, dass die Anwendung jede http- oder https-URL verstehen kann, die an sie übergeben wird, ohne auch den Namen der Cachedatei angeben zu müssen. Dieser Registrierungsschlüssel ist dem <em>Schlüssel SupportedProtocols</em> zugeordnet.<br /> | 


    

     

### <a name="using-the-applications-subkey"></a>Verwenden des Unterschlüssels "Anwendungen"

Durch das Einschluss von Registrierungseinträgen unter dem **Unterschlüssel HKEY \_ CLASSES \_ ROOT** ApplicationsApplicationName.exekönnen Anwendungen die anwendungsspezifischen Informationen bereitstellen, die in der \\  \\ ** folgenden Tabelle gezeigt werden.



| Registrierungseintrag                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \\Shellverb                      | Stellt die Verbmethode zum Aufrufen der Anwendung von OpenWith aus zur Anwendung zur Anwendung. Ohne hier angegebene Verbdefinition geht das System davon aus, dass die Anwendung [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)unterstützt, und übergibt den Dateinamen an die Befehlszeile. Diese Funktion gilt für alle Verbmethoden, einschließlich DropTarget, ExecuteCommand und dynamische Daten Exchange (DDE).                                                                                                                                                                                                                                                                                                                            |
| DefaultIcon                      | Ermöglicht es einer Anwendung, ein bestimmtes Symbol für die Darstellung der Anwendung anstelle des ersten Symbols in der .exe bereitstellen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| FriendlyAppName                  | Bietet eine Möglichkeit, einen lokalisierbaren Namen für eine Anwendung anzuzeigen, anstatt nur die angezeigten Versionsinformationen anzuzeigen, die möglicherweise nicht lokalisierbar sind. Die Zuordnungsabfrage [**ASSOCSTR**](/windows/desktop/api/Shlwapi/ne-shlwapi-assocstr) liest diesen Registrierungseintragswert und greift zurück, um den FileDescription-Namen in den Versionsinformationen zu verwenden. Wenn dieser Name fehlt, wird in der Zuordnungsabfrage standardmäßig der Anzeigename der Datei verwendet. Anwendungen sollten **ASSOCSTR \_ FRIENDLYAPPNAME** verwenden, um diese Informationen abzurufen, um das richtige Verhalten zu erhalten.                                                                                                                                                                        |
| SupportedTypes                   | Listet die Dateitypen auf, die von der Anwendung unterstützt werden. Auf diese Weise kann die Anwendung im kaskadierten Menü des Dialogfelds **Öffnen mit** aufgeführt werden.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| NoOpenWith                       | Gibt an, dass keine Anwendung zum Öffnen dieses Dateityps angegeben ist. Beachten Sie Folgendes: Wenn ein OpenWithProgIDs-Unterschlüssel für eine Anwendung nach Dateityp festgelegt wurde und der ProgID-Unterschlüssel selbst nicht auch über einen NoOpenWith-Eintrag verfügt, wird diese Anwendung in der Liste der empfohlenen oder verfügbaren Anwendungen angezeigt, auch wenn sie den Eintrag NoOpenWith angegeben hat. Weitere Informationen finden Sie unter [How to Include an Application in the Open With Dialog Box](how-to-include-an-application-on-the-open-with-dialog-box.md) und How to exclude an Application from the Öffnen mit Dialog [Box](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md).<br/> |
| IsHostApp                        | Gibt an, dass es sich bei dem Prozess um einen Hostprozess handelt, z. B. Rundll32.exe oder Dllhost.exe, und sollte nicht für das Anheften oder Einschließen des **Startmenüs** in die Liste der am häufigsten verwendeten (MFU) berücksichtigt werden. Beim Starten mit einer Verknüpfung, die eine Nicht-NULL-Argumentliste oder eine explizite [Anwendungsbenutzermodell-IDs (AppUserModelIDs)](appids.md)enthält, kann der Prozess angeheftet werden (als diese Verknüpfung). Solche Tastenkombinationen sind Kandidaten für die Aufnahme in die MFU-Liste.                                                                                                                                                                                                                                                  |
| NoStartPage                      | Gibt an, dass die ausführbare Datei der Anwendung und Die Verknüpfungen aus dem **Startmenü** und aus dem Anheften oder Einschließen in die MFU-Liste ausgeschlossen werden sollen. Dieser Eintrag wird in der Regel verwendet, um Systemtools, Installationsprogramme und Deinstallationsprogramme sowie Readmedateien auszuschließen.                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| UseExecutableForTaskbarGroupIcon | Bewirkt, dass die Taskleiste das Standardsymbol dieser ausführbaren Datei verwendet, wenn keine anheftbare Verknüpfung für diese Anwendung vorhanden ist, und nicht das Symbol des Fensters, das zum ersten Mal gefunden wurde.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| TaskbarGroupIcon                 | Gibt das Symbol an, das zum Überschreiben des Taskleistensymbols verwendet wird. Das Fenstersymbol wird normalerweise für die Taskleiste verwendet. Wenn Sie den Eintrag TaskbarGroupIcon festlegen, verwendet das System stattdessen das Symbol aus dem .exe für die Anwendung.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

### <a name="examples"></a>Beispiele

Einige Beispiele für Anwendungsregistrierungen über den **HKEY \_ CLASSES ROOT \_ Applications** \\  \\ *ApplicationName.exe* Unterschlüssel sind: Alle Registrierungseintragswerte sind vom **REG \_ SZ-Typ,** mit Ausnahme von **DefaultIcon,** das vom **REG EXPAND \_ \_ SZ-Typ** ist.

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

## <a name="registering-verbs-and-other-file-association-information"></a>Registrieren von Verben und anderen Dateizuordnungsinformationen

Unterschlüssel, die unter **HKEY \_ CLASSES \_ ROOT** \\ **SystemFileAssociations** registriert sind, ermöglichen es der Shell, das Standardverhalten von Attributen für Dateitypen zu definieren und freigegebene Dateizuordnungen zu aktivieren. Wenn Benutzer die Standardanwendung für einen Dateityp ändern, hat die ProgID der neuen Standardanwendung Priorität beim Bereitstellen von Verben und anderen Zuordnungsinformationen. Diese Priorität ist darauf zurückzuführen, dass es sich um den ersten Eintrag im Zuordnungsarray handelt. Wenn das Standardprogramm geändert wird, sind die Informationen unter der vorherigen ProgID nicht mehr verfügbar.

Um proaktiv mit den Folgen einer Änderung an Standardprogrammen umzugehen, können Sie **HKEY \_ CLASSES \_ ROOT** \\ **SystemFileAssociations** verwenden, um Verben und andere Zuordnungsinformationen zu registrieren. Aufgrund ihres Speicherorts nach der ProgID im Zuordnungsarray haben diese Registrierungen eine niedrigere Priorität. Diese SystemFileAssociationsregistrations sind auch dann stabil, wenn Benutzer die Standardprogramme ändern, und stellen einen Speicherort zum Registrieren sekundärer Verben bereit, die immer für einen bestimmten Dateityp verfügbar sind. Ein Registrierungsbeispiel finden Sie weiter unten in diesem Thema unter [Registrieren eines wahrgenommenen Typs.](#registering-a-perceived-type)

Das folgende Registrierungsbeispiel zeigt, was geschieht, wenn der Benutzer das Element **Standardprogramme** in Systemsteuerung ausführt, um die Standardeinstellung für .mp3 Dateien in App2ProgID zu ändern. Nach dem Ändern des Standardwerts ist Verb1 nicht mehr verfügbar, und Verb2 wird zur Standardeinstellung.

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

## <a name="registering-a-perceived-type"></a>Registrieren eines wahrgenommenen Typs

Registrierungswerte für wahrgenommene Typen werden als Unterschlüssel des Registrierungsunterschlüssels **HKEY \_ CLASSES \_ ROOT** \\ **SystemFileAssociations** definiert. Beispielsweise wird der wahrgenommene **Typtext** wie folgt registriert:

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

Der wahrgenommene Typ eines Dateityps wird durch Einschließen eines PerceivedType-Werts in den Unterschlüssel des Dateityps angegeben. Der PerceivedType-Wert wird auf den Namen des wahrgenommenen Typs festgelegt, der unter dem Registrierungsunterschlüssel **HKEY \_ CLASSES \_ ROOT** \\ **SystemFileAssociations** registriert ist, wie im vorherigen Registrierungsbeispiel gezeigt. Fügen Sie beispielsweise den folgenden Registrierungseintrag hinzu, um CPP-Dateien als "text"-Typ zu deklarieren:

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

[Inhaltsansicht nach Dateityp oder Art](prophand-content-view.md)
</dt> <dt>

[Dateitypüberprüfung](file-type-verifier.md)
</dt> <dt>

[Dateityphandler](fa-file-extensions.md)
</dt> <dt>

[Programmgesteuerte Bezeichner](fa-progids.md)
</dt> <dt>

[Wahrgenommene Typen](fa-perceivedtypes.md)
</dt> <dt>

[Zuordnungsarrays](fa-associationarray.md)
</dt> </dl>

