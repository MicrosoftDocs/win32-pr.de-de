---
description: Kontextmenühandler, auch als Kontextmenühandler oder Verbhandler bezeichnet, sind ein Typ des Dateityphandlers. Wie alle solchen Handler handelt es sich auch hierbei um IN-Process-Component Object Model (COM)-Objekte, die als DLLs implementiert werden.
ms.assetid: cff79cdc-8a01-4575-9af7-2a485c6a8e46
title: Erstellen von Kontextmenühandlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8e102833453566f42d058ff82061f34ebc65691
ms.sourcegitcommit: 9655f82be96b11258276fdefff14423c30552fbb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "109740571"
---
# <a name="creating-shortcut-menu-handlers"></a>Erstellen von Kontextmenühandlern

Kontextmenühandler, auch als Kontextmenühandler oder Verbhandler bezeichnet, sind ein Typ des Dateityphandlers. Diese Handler können auf eine Weise heraufgeschrieben werden, die dazu führt, dass sie in ihrem eigenen Prozess, im Explorer oder in anderen Prozessen von Drittanbietern geladen werden. Achten Sie beim Erstellen von In-Process-Handlern darauf, da sie dem Prozess, der sie lädt, Schaden zufügen können.

> [!Note]  
> Bei der Registrierung von Handlern, die im Kontext von 32-Bit-Anwendungen funktionieren, gibt es besondere Überlegungen für 64-Bit-basierte Versionen von Windows: Wenn sie im Kontext einer Anwendung mit unterschiedlicher Bitität aufgerufen werden, leitet das WOW64-Subsystem den Dateisystemzugriff auf einige Pfade um. Wenn Ihr EXE-Handler in einem dieser Pfade gespeichert ist, kann in diesem Kontext nicht darauf zugegriffen werden. Daher können Sie ihre EXE-Datei entweder in einem Pfad speichern, der nicht umgeleitet wird, oder eine Stubversion Ihrer EXE-Datei speichern, die die echte Version startet.

Dieses Thema ist wie folgt organisiert:

-   [Kanonische Verben](#canonical-verbs)
-   [Erweiterte Verben](#extended-verbs)
-   [Nur Verben für programmgesteuerten Zugriff](#programmaticaccessonly-verbs)
-   [Anpassen eines Kontextmenüs mit statischen Verben](#customizing-a-shortcut-menu-using-static-verbs)
    -   [Aktivieren des Handlers mithilfe der IDropTarget-Schnittstelle](#activating-your-handler-using-the-idroptarget-interface)
    -   [Angeben der Position und Reihenfolge statischer Verben](#specifying-the-position-and-order-of-static-verbs)
    -   [Positionieren von Verben am oberen oder unteren Rand des Menüs](#positioning-verbs-at-the-top-or-bottom-of-the-menu)
    -   [Erstellen statischer kaskadierender Menüs](#creating-static-cascading-menus)
    -   [Abrufen von dynamischem Verhalten für statische Verben mithilfe der erweiterten Abfragesyntax](#getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax)
    -   [Veraltet: Zuordnen von Verben zu dynamischer Datenaustausch Befehlen](#deprecated-associating-verbs-with-dynamic-data-exchange-commands)
-   [Abschließen von Verbimplementierungsaufgaben](#completing-verb-implementation-tasks)
    -   [Anpassen des Kontextmenüs für vordefinierte Shellobjekte](#customizing-the-shortcut-menu-for-predefined-shell-objects)
    -   [Erweitern eines neuen Untermenüs](#extending-a-new-submenu)
    -   [Unterdrücken von Verben und Steuern der Sichtbarkeit](#suppressing-verbs-and-controlling-visibility)
    -   [Verwenden des Verbauswahlmodells](#employing-the-verb-selection-model)
    -   [Verwenden von Elementattributen](#using-item-attributes)
    -   [Implementieren von benutzerdefinierten Verben für Ordner Desktop.ini](#implementing-custom-verbs-for-folders-through-desktopini)
-   [Zugehörige Themen](#related-topics)

## <a name="canonical-verbs"></a>Kanonische Verben

Anwendungen sind im Allgemeinen dafür verantwortlich, lokalisierte Anzeigezeichenfolgen für die von ihnen definierten Verben zur Verfügung zu stellen. Um jedoch einen gewissen Grad an Sprachunabhängigkeit zu gewährleisten, definiert das System einen Standardsatz häufig verwendeter Verben, die als kanonische Verben bezeichnet werden. Ein kanonisches Verb wird dem Benutzer nie angezeigt und kann mit jeder beliebigen Benutzeroberflächensprache verwendet werden. Das System verwendet den kanonischen Namen, um automatisch eine ordnungsgemäß lokalisierte Anzeigezeichenfolge zu generieren. Beispielsweise ist die Anzeigezeichenfolge des geöffneten Verbs auf **Einem** englischen System auf Öffnen und auf das deutsche Äquivalent auf einem deutschen System festgelegt.


| Kanonisches Verb | BESCHREIBUNG                                                          |
|----------------|----------------------------------------------------------------------|
| Öffnen           | Öffnet die Datei oder den Ordner.                                            |
| Opennew        | Öffnet die Datei oder den Ordner in einem neuen Fenster.                            |
| Drucken          | Gibt die Datei aus.                                                     |
| Printto        | Ermöglicht dem Benutzer das Drucken einer Datei durch Ziehen auf ein Druckerobjekt. |
| Erkunden        | Öffnet Windows-Explorer mit dem ausgewählten Ordner.                     |
| Eigenschaften     | Öffnet das Eigenschaftenblatt des Objekts.                                   |

> [!Note]  
> Das **Printto-Verb** ist ebenfalls kanonisch, wird aber nie angezeigt. Durch das Einschließen kann der Benutzer eine Datei drucken, indem er sie auf ein Druckerobjekt zieht.

Kontextmenühandler können ihre eigenen kanonischen Verben über [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) mit **GCS \_ VERBW** oder **GCS \_ VERBA** bereitstellen. Das System verwendet die kanonischen Verben als zweiten Parameter (*lpOperation*), der an [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)übergeben wird, und ist [**cminvokecommandinfo**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo). **lpVerb-Member,** der an die [**IContextMenu::InvokeCommand-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) übergeben wird.

## <a name="extended-verbs"></a>Erweiterte Verben

Wenn der Benutzer mit der rechten Maustaste auf ein Objekt klickt, werden im Kontextmenü die Standardverben angezeigt. Möglicherweise möchten Sie Befehle in einigen Kontextmenüs hinzufügen und unterstützen, die nicht in jedem Kontextmenü angezeigt werden. Beispielsweise können Sie Befehle verwenden, die nicht häufig verwendet werden oder für erfahrene Benutzer vorgesehen sind. Aus diesem Grund können Sie auch ein oder mehrere erweiterte Verben definieren. Diese Verben ähneln normalen Verben, unterscheiden sich jedoch durch ihre Registrierung von normalen Verben. Um Zugriff auf erweiterte Verben zu erhalten, muss der Benutzer beim Drücken der UMSCHALTTASTE mit der rechten Maustaste auf ein Objekt klicken. Wenn der Benutzer dies tut, werden die erweiterten Verben zusätzlich zu den Standardverben angezeigt.

Sie können die Registrierung verwenden, um ein oder mehrere erweiterte Verben zu definieren. Die zugeordneten Befehle werden nur angezeigt, wenn der Benutzer mit der rechten Maustaste auf ein Objekt klickt und gleichzeitig die UMSCHALTTASTE drückt. Um ein Verb als erweitert zu definieren, fügen Sie dem Unterschlüssel des Verbs einen "erweiterten" **REG \_ SZ-Wert** hinzu. Dem Wert dürfen keine Daten zugeordnet sein.

## <a name="programmatic-access-only"></a>Nur programmgesteuerter Zugriff

Diese Verben werden nie in einem Kontextmenü angezeigt. Sie können auf diese zugreifen, indem [**Sie ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) verwenden und das **lpVerb-Feld** des *pExecInfo-Parameters* (ein [SHELLEXECUTEINFO-Objekt)](/windows/win32/api/shellapi/ns-shellapi-shellexecuteinfoa) angeben. Um ein Verb nur als programmgesteuerten Zugriff zu definieren, fügen Sie dem Unterschlüssel des Verbs den **REG \_ SZ-Wert** "ProgrammaticAccessOnly" hinzu. Dem Wert sollten keine Daten zugeordnet sein.

Sie können die Registrierung verwenden, um ein oder mehrere erweiterte Verben zu definieren. Die zugeordneten Befehle werden nur angezeigt, wenn der Benutzer mit der rechten Maustaste auf ein Objekt klickt und gleichzeitig die UMSCHALTTASTE drückt. Um ein Verb als erweitert zu definieren, fügen Sie dem Unterschlüssel des Verbs einen "erweiterten" **REG \_ SZ-Wert** hinzu. Dem Wert sollten keine Daten zugeordnet sein.

## <a name="customizing-a-shortcut-menu-using-static-verbs"></a>Anpassen eines Kontextmenüs mit statischen Verben

Nach [dem Auswählen eines statischen oder](shortcut-choose-method.md) dynamischen Verbs für das Kontextmenü können Sie das Kontextmenü für einen Dateityp erweitern, indem Sie ein statisches Verb für den Dateityp registrieren. Fügen Sie dazu  einen Shell-Unterschlüssel unterhalb des Unterschlüssels für die ProgID der Anwendung hinzu, die dem Dateityp zugeordnet ist. Optional können Sie ein Standardverb für den Dateityp definieren,  indem Sie es zum Standardwert des Shell-Unterschlüssels machen.

Das Standardverb wird zuerst im Kontextmenü angezeigt. Der Zweck besteht in der Bereitstellung eines Verbs für die Shell, das beim Aufruf der [**ShellExecuteEx-Funktion verwendet**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) werden kann, aber es wird kein Verb angegeben. Die Shell wählt nicht unbedingt das Standardverb aus, wenn **ShellExecuteEx** auf diese Weise verwendet wird.

Die Shell verwendet das erste verfügbare Verb in der folgenden Reihenfolge:

1.  Das Standardverb
2.  Das erste Verb in der Registrierung, wenn die Verb reihenfolge angegeben ist
3.  Das **Verb "Öffnen"**
4.  Das **Verb "Öffnen mit"**

Wenn keines der aufgeführten Verben verfügbar ist, schlägt der Vorgang fehl.

Erstellen Sie einen Unterschlüssel für jedes Verb, das Sie unter dem Shell-Unterschlüssel hinzufügen möchten. Für jeden dieser Unterschlüssel muss ein **REG \_ SZ-Wert** auf die Anzeigezeichenfolge des Verbs (lokalisierte Zeichenfolge) festgelegt sein. Erstellen Sie für jeden Verbunterschlüssel einen Befehlsunterschlüssel mit dem Standardwert, der auf die Befehlszeile zum Aktivieren der Elemente festgelegt ist. Bei kanonischen Verben wie **Öffnen** und **Drucken** können Sie die Anzeigezeichenfolge weglassen, da das System automatisch eine ordnungsgemäß lokalisierte Zeichenfolge anzeigt. Bei nicht kanonischen Verben wird die Verbzeichenfolge angezeigt, wenn Sie die Anzeigezeichenfolge weglassen.

Beachten Sie im folgenden Registrierungsbeispiel Folgendes:

-   Da **Doit** kein kanonisches Verb ist, wird ihm ein Anzeigename zugewiesen, der durch Drücken der D-Taste ausgewählt werden kann.
-   Das **Printto-Verb** wird nicht im Kontextmenü angezeigt. Durch die Einbindung in die Registrierung kann der Benutzer jedoch Dateien drucken, indem er sie auf einem Druckersymbol ablegen kann.
-   Für jedes Verb wird ein Unterschlüssel angezeigt. **%1** stellt den Dateinamen und **%2** den Druckernamen dar.

```
HKEY_CLASSES_ROOT
   .myp-ms
      (Default) = MyProgram.1
      MyProgram.1
         (Default) = My Program Application
         Shell
            (Default) = doit
            doit
               (Default) = &Do It
               command
                  (Default) = c:\MyDir\MyProgram.exe /d "%1"
            open
               command
                  (Default) = c:\MyDir\MyProgram.exe /d "%1"
            print
               command
                  (Default) = c:\MyDir\MyProgram.exe /p "%1"
            printto
               command
                  (Default) = c:\MyDir\MyProgram.exe /p "%1" "%2"
```

Das folgende Diagramm veranschaulicht die Erweiterung des Kontextmenüs in Übereinstimmung mit den obigen Registrierungseinträgen. Dieses Kontextmenü enthält die Verben **Öffnen**, Do **It** und **Drucken** im Menü, wobei **Do It** als Standardverb verwendet wird.

![Screenshot des Kontextmenüs für das Standardverb "Do it"](images/context-menu/context-doitdefaultverb.png)

### <a name="activating-your-handler-using-the-idroptarget-interface"></a>Aktivieren des Handlers mithilfe der IDropTarget-Schnittstelle

dynamischer Datenaustausch (DDE) ist veraltet. Verwenden Sie stattdessen [**IDropTarget.**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) **IDropTarget** ist robuster und bietet eine bessere Aktivierungsunterstützung, da die COM-Aktivierung des Handlers verwendet wird. Im Fall der Auswahl mehrerer Elemente unterliegt **IDropTarget** nicht den Puffergrößenbeschränkungen, die sowohl in DDE als auch im [**CreateProcess-Element**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)gefunden werden. Außerdem werden Elemente als Datenobjekt an die Anwendung übergeben, das mithilfe der [**SHCreateShellItemArrayFromDataObject-Funktion**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) in ein Elementarray konvertiert werden kann. Dies ist einfacher, und namespace-Informationen gehen nicht verloren, wenn das Element in einen Pfad für Befehlszeilen- oder DDE-Protokolle konvertiert wird.

Weitere Informationen zu [**IDropTarget-**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) und Shell-Abfragen für Dateiassozattribute finden Sie unter [Wahrgenommene Typen und Anwendungsregistrierung.](fa-perceivedtypes.md)

### <a name="specifying-the-position-and-order-of-static-verbs"></a>Angeben der Position und Reihenfolge statischer Verben

Normalerweise werden Verben in einem Kontextmenü basierend darauf geordnet, wie sie aufzählen. -Enumeration basiert zuerst auf der Reihenfolge des Zuordnungsarrays und dann auf der Reihenfolge der Elemente im Zuordnungsarray, wie durch die Sortierreihenfolge der Registrierung definiert.

Verben können durch Angabe des Standardwerts des Shell-Unterschlüssels für den Zuordnungseintrag geordnet werden. Dieser Standardwert kann ein einzelnes Element enthalten, das an der oberen Position des Kontextmenüs angezeigt wird, oder eine Liste von Elementen, die durch Leerzeichen oder Kommas getrennt sind. Im letzteren Fall ist das erste Element in der Liste das Standardelement, und die anderen Verben werden direkt darunter in der angegebenen Reihenfolge angezeigt.

Beispielsweise erzeugt der folgende Registrierungseintrag Kontextmenüverben in der folgenden Reihenfolge:

1.  Anzeige
2.  Gadgets
3.  Personalisierung

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell
         Display
         Gadgets
         Personalization
```

Entsprechend erzeugt der folgende Registrierungseintrag Kontextmenüverben in der folgenden Reihenfolge:

1.  Personalisierung
2.  Gadgets
3.  Anzeige

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell = "Personalization,Gadgets"
      Display
```

### <a name="positioning-verbs-at-the-top-or-bottom-of-the-menu"></a>Positionieren von Verben am oberen oder unteren Rand des Menüs

Das folgende Registrierungsattribut kann verwendet werden, um ein Verb am oberen oder unteren Rand des Menüs zu platzieren. Wenn es mehrere Verben gibt, die dieses Attribut angeben, erhält der letzte, der dies tun soll, Priorität:

``` syntax
Position=Top | Bottom 
```

### <a name="creating-static-cascading-menus"></a>Erstellen von statischen kaskadierenden Menüs

In Windows 7 und höher wird die Implementierung des kaskadierenden Menüs über Registrierungseinstellungen unterstützt. Vor Windows 7 war die Erstellung von kaskadierenden Menüs nur über die Implementierung der [**IContextMenu-Schnittstelle**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) möglich. In Windows 7 und höher sollten Sie nur dann auf COM-codebasierte Lösungen zurück greifen, wenn die statischen Methoden nicht ausreichen.

Der folgende Screenshot enthält ein Beispiel für ein kaskadiertes Menü.

![Screenshot, der ein Beispiel für ein kaskadiertes Menü zeigt](images/file-assoc/filecascademenu2ndex.png)

In Windows 7 und höher gibt es drei Möglichkeiten, kaskadierende Menüs zu erstellen:

-   [Erstellen von kaskadierenden Menüs mit dem Registrierungseintrag "SubCommands"](#creating-cascading-menus-with-the-subcommands-registry-entry)
-   [Erstellen von kaskadierenden Menüs mit dem Registrierungseintrag ExtendedSubCommandsKey](#creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry)
-   [Erstellen von kaskadierenden Menüs mit der IExplorerCommand-Schnittstelle](#creating-cascading-menus-with-the-iexplorercommand-interface)

### <a name="creating-cascading-menus-with-the-subcommands-registry-entry"></a>Erstellen von kaskadierenden Menüs mit dem Registrierungseintrag "SubCommands"

In Windows 7 und höher können Sie den Eintrag Unterbefehle verwenden, um kaskadierende Menüs mithilfe des folgenden Verfahrens zu erstellen.

**So erstellen Sie ein kaskadierendes Menü mithilfe des Eintrags "SubCommands"**

1.  Erstellen Sie unter **HKEY \_ CLASSES \_ ROOT** \\ *ProgID* shell einen \\  Unterschlüssel, um Ihr kaskadierendes Menü darzustellen. In diesem Beispiel geben wir diesem Unterschlüssel den Namen *CascadeTest*. Stellen Sie sicher, dass der Standardwert des *CascadeTest-Unterschlüssels* leer ist und als **(Wert nicht festgelegt)** angezeigt wird.

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
    ```

2.  Fügen Sie Ihrem *CascadeTest-Unterschlüssel* einen ENTRYVerb-Eintrag vom Typ **REG \_ SZ** hinzu, und weisen Sie ihm den Text zu, der im Kontextmenü als Name angezeigt wird. In diesem Beispiel weisen wir ihm "Test Cascade Menu" zu.

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu
    ```

3.  Fügen Sie Ihrem *CascadeTest-Unterschlüssel* einen SubCommands-Eintrag vom Typ **REG \_ SZ** hinzu, dem die Liste der Verben, die im Menü angezeigt werden sollen, durch Semikolons getrennt in der Reihenfolge der Darstellung zugewiesen wird. Hier weisen wir beispielsweise eine Reihe von vom System bereitgestellten Verben zu:

    ```
    HKEY_CLASSES_ROOT
       *
          Shell
             CascadeTest
                SubCommands
                Windows.delete;Windows.properties;Windows.rename;Windows.cut;Windows.copy;Windows.paste
    ```

4.  Implementieren Sie bei benutzerdefinierten Verben diese mit einer der statischen Verbimplementierungen, und listen Sie sie unter dem **CommandStore-Unterschlüssel** auf, wie in diesem Beispiel für ein fiktives Verb *VerbName* gezeigt:

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      CommandStore
                         Shell
                            VerbName
                            command
                               (Default) = notepad.exe %1
    ```

> [!Note]  
> Diese Methode hat den Vorteil, dass die benutzerdefinierten Verben einmal registriert und wiederverwendet werden können, indem der Verbname unter dem Eintrag SubCommands aufgelistet wird. Die Anwendung muss jedoch über die Berechtigung verfügen, die Registrierung unter **HKEY \_ LOCAL \_ MACHINE** zu ändern.

 

### <a name="creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry"></a>Erstellen von kaskadierenden Menüs mit dem Registrierungseintrag ExtendedSubCommandsKey

In Windows 7 und höher können Sie den Eintrag ExtendedSubCommandKey verwenden, um erweiterte kaskadierenden Menüs zu erstellen: kaskadierenden Menüs in kaskadierenden Menüs.

Der folgende Screenshot ist ein Beispiel für ein erweitertes kaskadierenden Menü.

![Screenshot mit erweitertem Kaskadierungsmenü für Geräte](images/file-assoc/extendedsubcommandskey.png)

Da **HKEY \_ CLASSES \_ ROOT** eine Kombination aus **HKEY CURRENT \_ \_ USER** und **HKEY LOCAL \_ \_ MACHINE** ist, können Sie alle benutzerdefinierten Verben unter dem **Unterschlüssel HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Classes** registrieren. Der Hauptvorteil ist, dass erhöhte Berechtigungen nicht erforderlich sind. Außerdem können andere Dateizuordnungen diesen gesamten Satz von Verben wiederverwenden, indem sie denselben ExtendedSubCommandsKey-Unterschlüssel angeben. Wenn Sie diesen Satz von Verben nicht wiederverwenden müssen, können Sie die Verben unter dem übergeordneten Element auflisten, aber sicherstellen, dass der Standardwert des übergeordneten Elements leer ist.

**So erstellen Sie ein kaskadierenden Menü mithilfe eines ExtendedSubCommandsKey-Eintrags**

1.  Erstellen Sie unter HKEY CLASSES ROOT ProgID shell **(HKEY \_ CLASSES \_ ROOT** \\ *ProgID-Shell)* einen Unterschlüssel, \\  um Ihr kaskadiertes Menü zu darstellen. In diesem Beispiel geben wir diesem Unterschlüssel den Namen *CascadeTest2*. Stellen Sie sicher, dass der Standardwert des *CascadeTest-Unterschlüssels* leer ist und **als (Wert nicht festgelegt) angezeigt wird.**

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest2
                (Default)
    ```

2.  Fügen Sie *ihrem CascadeTest-Unterschlüssel* einen EINTRAG VOM TYP **REG \_ SZ** hinzu, und weisen Sie ihm den Text zu, der als Name im Kontextmenü angezeigt wird. In diesem Beispiel weisen wir ihm "Test Cascade Menu" zu.

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu 2
    ```

3.  Fügen Sie unter dem von Ihnen erstellten *CascadeTest-Unterschlüssel* einen **ExtendedSubCommandsKey-Unterschlüssel** hinzu, und fügen Sie dann die Dokumentunterschlüssel (des **REG \_ SZ-Typs)** hinzu. Beispiel:

    ```
    HKEY_CLASSES_ROOT
       txtfile
          Shell
             Test Cascade Menu 2
                (Default)
                ExtendedSubCommandsKey
                   Layout
                   Properties
                   Select all
    ```

    Stellen Sie sicher, dass der Standardwert des *Unterschlüssels Test Cascade Menu 2* leer und als **(Wert nicht festgelegt) angezeigt wird.**

4.  Füllen Sie die Unterverben mithilfe einer der folgenden statischen Verbimplementierungen auf. Beachten Sie, dass der CommandFlags-Unterschlüssel EXPCMDFLAGS-Werte darstellt. Wenn Sie vor oder nach dem kaskadierten Menüelement ein Trennzeichen hinzufügen möchten, verwenden Sie ECF \_ SEPARATORBEFORE (0x20) oder ECF \_ SEPARATORAFTER (0x40). Eine Beschreibung dieser Windows 7- und höher-Flags finden Sie unter [**IExplorerCommand::GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags). ECF \_ SEPARATORBEFORE funktioniert nur für die Menüelemente der obersten Ebene. CABVerb ist vom Typ **REG \_ SZ,** und CommandFlags ist vom Typ **REG \_ DWORD**.

    ```
    HKEY_CLASSES_ROOT
       txtile
          Shell
             Test Cascade Menu 2
                (Default)
                ExtendedSubCommandsKey
                   Shell
                      cmd1
                         MUIVerb = Notepad
                         command
                            (Default) = %SystemRoot%\system32\notepad.exe %1
                      cmd2
                         MUIVerb = Wordpad
                         CommandFlags = 0x20
                         command
                            (Default) = "C:\Program Files\Windows NT\Accessories\wordpad.exe" %1
    ```

Der folgende Screenshot zeigt die vorherigen Beispiele für Registrierungsschlüsseleinträge.

![Screenshot eines Beispiels für ein kaskadierendes Menü mit Auswahlmöglichkeiten für Editor und Wordpad](images/file-assoc/testcascademenu2.png)

### <a name="creating-cascading-menus-with-the-iexplorercommand-interface"></a>Erstellen von kaskadierenden Menüs mit der IExplorerCommand-Schnittstelle

Eine weitere Option zum Hinzufügen von Verben zu einem kaskadierenden Menü ist [**IExplorerCommand::EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands). Diese Methode ermöglicht Datenquellen, die ihre Befehlsmodulbefehle über [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) bereitstellen, diese Befehle als Verben in einem Kontextmenü zu verwenden. Unter Windows 7 und höher können Sie [**mithilfe von IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) die gleiche Verbimplementierungen wie mit [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)bereitstellen.

Die folgenden beiden Screenshots veranschaulichen die Verwendung von kaskadierenden Menüs im Ordner **Geräte.**

![Screenshot: Beispiel für ein kaskadierendes Menü im Ordner "devices"](images/file-assoc/filecascademenu.png)

Der folgende Screenshot veranschaulicht eine weitere Implementierung eines kaskadierenden Menüs im Ordner **Geräte.**

![Screenshot eines Beispiels für ein kaskadierendes Menü im Ordner "devices"](images/file-assoc/cascadedevices2.png)

> [!Note]  
> Da [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) nur die Prozessaktivierung unterstützt, wird die Verwendung durch Shell-Datenquellen empfohlen, die die Implementierung zwischen Befehlen und Kontextmenüs freigeben müssen.

 

### <a name="getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax"></a>Abrufen von dynamischem Verhalten für statische Verben mithilfe der erweiterten Abfragesyntax

Advanced Query Syntax (AQS) kann eine Bedingung ausdrücken, die mithilfe von Eigenschaften aus dem Element ausgewertet wird, für das das Verb instanziiert wird. Dieses System funktioniert nur mit schnellen Eigenschaften. Dies sind Eigenschaften, die die Shell-Datenquelle als schnell meldet, indem [sie nicht "SHCOLSTATE \_ SLOW"](/windows/win32/api/shtypes/ne-shtypes-shcolstate) aus [**IShellFolder2::GetDefaultColumnState zurücksendet.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdefaultcolumnstate)

Windows 7 und höher unterstützen kanonische Werte, die Probleme bei lokalisierten Builds vermeiden. Die folgende kanonische Syntax ist für lokalisierte Builds erforderlich, um diese Windows 7-Erweiterung nutzen zu können.

``` syntax
System.StructuredQueryType.Boolean#True
```

Im folgenden Beispielregistrierungseintrag:

-   Der **AppliesTo-Wert** steuert, ob das Verb angezeigt oder ausgeblendet wird.
-   Der DefaultAppliesTo-Wert steuert, welches Verb der Standardwert ist.
-   Der HasLUAShield-Wert steuert, ob ein UAC-Schutz (User Account Control) angezeigt wird.

In diesem Beispiel macht **der DefaultAppliesTo-Wert** dieses Verb zum Standard für jede Datei mit dem Wort "exampleText1" im Dateinamen. Der **AppliesTo-Wert** aktiviert das Verb für jede Datei mit "exampleText1" im Namen. Der **HasLUAShield-Wert** zeigt den Schutz für Dateien mit "exampleText2" im Namen an.

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            DefaultAppliesTo = System.ItemName:"exampleText1"
            HasLUAShield = System.ItemName:"exampleText2"
            AppliesTo = System.ItemName:"exampleText1"
```

Fügen Sie **den Unterschlüssel Befehl** und einen Wert hinzu:

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            Command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

In der Windows 7-Registrierung finden Sie **unter HKEY CLASSES ROOT drive (HKEY \_ CLASSES \_ ROOT-Laufwerk)** ein Beispiel für \\  BitLocker-Verben, die den folgenden Ansatz verwenden:

-   AppliesTo = System.Volume.BitlockerProtection:=2
-   System.Volume.BitlockerRequiresAdmin:=System.StructuredQueryType.Boolean \# True

Weitere Informationen zu AQS finden Sie unter [Erweiterte Abfragesyntax](../search/-search-3x-advancedquerysyntax.md).

### <a name="deprecated-associating-verbs-with-dynamic-data-exchange-commands"></a>Veraltet: Zuordnen von Verben zu dynamischer Datenaustausch Befehlen

DDE ist veraltet. verwenden [**Sie stattdessen IDropTarget.**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) DDE ist veraltet, da er auf einer Broadcastfensternachricht basiert, um den DDE-Server zu finden. Ein DDE-Server hängt die Broadcastfensternachricht und hängt daher DDE-Konversationen für andere Anwendungen. Es ist üblich, dass eine einzelne hängende Anwendung nachfolgende Hängen in der gesamten Benutzererfahrung verursacht.

Die [**IDropTarget-Methode**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) ist robuster und bietet eine bessere Aktivierungsunterstützung, da sie die COM-Aktivierung des Handlers verwendet. Im Fall der Auswahl mehrerer Elemente unterliegt **IDropTarget** nicht den Puffergrößenbeschränkungen, die sowohl in DDE als auch im [**CreateProcess-Element**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)gefunden werden. Außerdem werden Elemente als Datenobjekt an die Anwendung übergeben, das mithilfe der [**SHCreateShellItemArrayFromDataObject-Funktion**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) in ein Elementarray konvertiert werden kann. Dies ist einfacher und verliert keine Namespaceinformationen wie beim Konvertieren des Elements in einen Pfad für Befehlszeilen- oder DDE-Protokolle.

Weitere Informationen zu [**IDropTarget-**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) und Shell-Abfragen für Dateizuordnungsattribute finden Sie unter [Wahrgenommene Typen und Anwendungsregistrierung.](fa-perceivedtypes.md)

## <a name="completing-verb-implementation-tasks"></a>Abschließen von Verbimplementierungsaufgaben

Die folgenden Aufgaben zum Implementieren von Verben sind sowohl für statische als auch dynamische Verbimplementierungen relevant. Weitere Informationen zu dynamischen Verben finden Sie unter [Anpassen eines Kontextmenüs mit dynamischen Verben.](shortcut-menu-using-dynamic-verbs.md)

### <a name="customizing-the-shortcut-menu-for-predefined-shell-objects"></a>Anpassen des Kontextmenüs für vordefinierte Shellobjekte

Viele vordefinierte Shell-Objekte verfügen über Kontextmenüs, die angepasst werden können. Registrieren Sie den Befehl auf die gleiche Weise wie typische Dateitypen, verwenden Sie jedoch den Namen des vordefinierten Objekts als Dateitypnamen.

Eine Liste vordefinierter Objekte finden Sie im Abschnitt *Vordefinierte Shellobjekte* unter [Erstellen von Shellerweiterungshandlern.](handlers.md) Vordefinierte Shell-Objekte, deren Kontextmenüs durch Hinzufügen von Verben in der Registrierung angepasst werden können, werden in der Tabelle mit dem Wort Verb markiert.

### <a name="extending-a-new-submenu"></a>Erweitern eines neuen Untermenüs

Wenn ein Benutzer das Menü **Datei** in Windows-Explorer öffnet, ist einer der angezeigten Befehle **Neu.** Wenn Sie diesen Befehl auswählen, wird ein Untermenü angezeigt. Standardmäßig enthält das Untermenü zwei Befehle: **Ordner** und **Verknüpfung,** mit denen Benutzer Unterordner und Verknüpfungen erstellen können. Dieses Untermenü kann erweitert werden, um Dateierstellungsbefehle für jeden Dateityp einzuschließt.

Um dem Untermenü Neu  einen Dateierstellungsbefehl hinzuzufügen, müssen die Dateien Ihrer Anwendung über einen zugeordneten Dateityp verfügen. Fügen Sie unter dem Dateinamen einen **ShellNeuen** Unterschlüssel ein. Wenn der **Befehl** Neu im Menü Datei **ausgewählt** ist, fügt die Shell dem Untermenü Neu den **Dateityp** hinzu. Die Anzeigezeichenfolge des Befehls ist die beschreibende Zeichenfolge, die der ProgID des Programms zugewiesen ist.

Um die Dateierstellungsmethode anzugeben, weisen Sie dem **Unterschlüssel ShellNeu** einen oder mehrere Datenwerte zu. Die verfügbaren Werte sind in der folgenden Tabelle aufgeführt.



| ShellNeuer Unterschlüsselwert | BESCHREIBUNG                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Befehl               | Führt eine Anwendung aus. Dieser **REG \_ SZ-Wert** gibt den Pfad der auszuführenden Anwendung an. Sie können z. B. festlegen, dass ein Assistent gestartet wird.                  |
| Daten                  | Erstellt eine Datei mit angegebenen Daten. Dieser **REG \_ BINARY-Wert** gibt die Daten der Datei an. **Daten** werden ignoriert, wenn **nullFile** oder **FileName** angegeben wird. |
| FileName              | Erstellt eine Datei, die eine Kopie einer angegebenen Datei ist. Dieser **REG \_ SZ-Wert** gibt den vollqualifizierten Pfad der zu kopierenden Datei an.                                   |
| NullFile              | Erstellt eine leere Datei. **NullFile** wurde kein Wert zugewiesen. Wenn **NullFile** angegeben wird, werden die **Registrierungswerte Data** und **FileName** ignoriert.                    |



 

Das folgende Registrierungsschlüsselbeispiel und der Screenshot veranschaulichen das **Untermenü New** für den Dateityp .myp-ms. Sie verfügt über den Befehl **MyProgram Application**.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      MyProgram.1
         ShellNew
         NullFile
```

Der Screenshot veranschaulicht das Untermenü **"Neu".** Wenn ein Benutzer im Untermenü **Neu** die Option **MyProgram-Anwendung** auswählt, erstellt die Shell eine Datei mit dem Namen **New MyProgram Application.myp-ms** und übergibt sie an **MyProgram.exe**.

![Screenshot des Windows-Explorers mit einem neuen Befehl "myprogram application" im Untermenü "new"](images/context-menu/context-myprogramexe.png)

### <a name="creating-drag-and-drop-handlers"></a>Erstellen von Drag & Drop-Handlern

Das grundlegende Verfahren zum Implementieren eines Drag & Drop-Handlers ist das gleiche wie bei herkömmlichen Kontextmenühandlern. Kontextmenühandler verwenden jedoch normalerweise nur den [**IDataObject-Zeiger,**](/windows/win32/api/objidl/nn-objidl-idataobject) der an die [**IShellExtInit::Initialize-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) des Handlers übergeben wird, um den Namen des Objekts zu extrahieren. Ein Drag & Drop-Handler könnte einen komplexeren Datenhandler implementieren, um das Verhalten des gezogenen Objekts zu ändern.

Wenn ein Benutzer mit der rechten Maustaste auf ein Shell-Objekt klickt, um ein Objekt zu ziehen, wird ein Kontextmenü angezeigt, wenn der Benutzer versucht, das Objekt zu löschen. Der folgende Screenshot veranschaulicht ein typisches Drag & Drop-Kontextmenü.

![Screenshot des Drag & Drop-Kontextmenüs](images/context-menu/context-dragdrop.png)

Ein Drag & Drop-Handler ist ein Kontextmenühandler, der diesem Kontextmenü Elemente hinzufügen kann. Drag & Drop-Handler werden in der Regel unter dem folgenden Unterschlüssel registriert.

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
```

Fügen Sie unter dem Unterschlüssel **DragDropHandlers** einen Unterschlüssel mit dem Namen für den Drag & Drop-Handler hinzu, und legen Sie den Standardwert des Unterschlüssels auf die Zeichenfolgenform der CLSID-GUID (Class Identifier) des Handlers fest. Im folgenden Beispiel wird der Drag & Drop-Handler **MyDD** aktiviert.

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
            MyDD
               (Default) = {MyDD CLSID GUID}
```

### <a name="suppressing-verbs-and-controlling-visibility"></a>Unterdrücken von Verben und Steuern der Sichtbarkeit

Sie können Windows-Richtlinieneinstellungen verwenden, um die Sichtbarkeit von Verben zu steuern. Verben können durch Richtlinieneinstellungen unterdrückt werden, indem dem Registrierungsunterschlüssel des Verbs ein **SuppressPolicy-Wert** oder ein **SuppressionPolicyEx-GUID-Wert** hinzugefügt wird. Legen Sie den Wert des **Unterschlüssels SuppressionPolicy** auf die Richtlinien-ID fest. Wenn die Richtlinie aktiviert ist, werden das Verb und der zugehörige Kontextmenüeintrag unterdrückt. Mögliche Richtlinien-ID-Werte finden Sie in der [**RESTRICTIONS-Enumeration.**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions)

### <a name="employing-the-verb-selection-model"></a>Verwenden des Verbauswahlmodells

Registrierungswerte müssen für Verben festgelegt werden, um Situationen zu behandeln, in denen ein Benutzer ein einzelnes Element, mehrere Elemente oder eine Auswahl aus einem Element auswählen kann. Ein Verb erfordert separate Registrierungswerte für jede dieser drei Situationen, die das Verb unterstützt. Die möglichen Werte für das Verbauswahlmodell lauten wie folgt:

-   Geben Sie den MultiSelectModel-Wert für alle Verben an. Wenn der MultiSelectModel-Wert nicht angegeben ist, wird er von dem Typ der von Ihnen gewählten Verbimplementierung abgeleitet. Für COM-basierte Methoden (z. B. DropTarget und ExecuteCommand) wird **der Player** und für die anderen Methoden **document** angenommen.
-   Geben **Sie Single** für Verben an, die nur eine einzelne Auswahl unterstützen.
-   Geben **Sie Player** für Verben an, die eine beliebige Anzahl von Elementen unterstützen.
-   Geben **Sie Dokument** für Verben an, die ein Fenster der obersten Ebene für jedes Element erstellen. Dadurch wird die Anzahl der aktivierten Elemente beschränkt, und es wird verhindert, dass die Systemressourcen knapp werden, wenn der Benutzer zu viele Fenster öffnet.

Wenn die Anzahl der ausgewählten Elemente nicht mit dem Verbauswahlmodell oder größer als die in der folgenden Tabelle beschriebenen Standardgrenzwerte ist, wird das Verb nicht angezeigt.



| Typ der Verbimplementierung | Dokument | Player    |
|-----------------------------|----------|-----------|
| Alt                      | 15 Elemente | 100 Elemente |
| COM                         | 15 Elemente | Keine Begrenzung  |



 

Im Folgenden finden Sie Beispielregistrierungseinträge mit dem MultiSelectModel-Wert.

```
HKEY_CLASSES_ROOT
   Folder
      shell
         open
             = MultiSelectModel = Document
```

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         verb
             = MultiSelectModel = Single | Document | Player
```

### <a name="using-item-attributes"></a>Verwenden von Elementattributen

Die [**SFGAO-Flagwerte**](sfgao.md) der Shellattribute für ein Element können getestet werden, um zu bestimmen, ob das Verb aktiviert oder deaktiviert werden soll.

Um dieses Attributfeature zu verwenden, fügen Sie die folgenden **REG \_ DWORD-Werte** unter dem Verb hinzu:

-   Der AttributeMask-Wert gibt den [**SFGAO-Wert**](sfgao.md) der Bitwerte der Maske an, mit der getestet werden soll.
-   Der AttributeValue-Wert gibt den [**SFGAO-Wert**](sfgao.md) der getesteten Bits an.
-   Das ImpliedSelectionModel gibt 0 (null) für Elementverben oder ungleich 0 (null) für Verben im Kontextmenü im Hintergrund an.

Im folgenden Beispielregistrierungseintrag ist AttributeMask auf [**SFGAO \_ READONLY**](sfgao.md) (0x40000) festgelegt.

```
HKEY_CLASSES_ROOT
   txtfile
      Shell
         test.verb2
            AttributeMask = 0x40000
            AttributeValue = 0x0
            ImpliedSelectionModel = 0x0
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

### <a name="implementing-custom-verbs-for-folders-through-desktopini"></a>Implementieren von benutzerdefinierten Verben für Ordner über Desktop.ini

In Windows 7 und höher können Sie einem Ordner verbs über Desktop.ini hinzufügen. Weitere Informationen zu Desktop.ini-Dateien finden Sie unter [Anpassen von Ordnern mit Desktop.ini](how-to-customize-folders-with-desktop-ini.md).

> [!Note]  
> Desktop.ini Dateien sollten immer als **System** ausgeblendet gekennzeichnet  +   werden, damit sie benutzern nicht angezeigt werden.

 

**Führen Sie die folgenden Schritte aus, um benutzerdefinierte Verben für Ordner über eine Desktop.ini-Datei hinzuzufügen:**

1.  Erstellen Sie einen Ordner, der als **Schreibgeschützt** oder **System** gekennzeichnet ist.
2.  Erstellen Sie eine Desktop.ini-Datei, die \[ enthält. ShellClassInfo \] DirectoryClass=Folder ProgID.
3.  Erstellen Sie in der Registrierung **HKEY \_ CLASSES \_ ROOT** \\ **Folder ProgID** mit dem Wert CanUseForDirectory. Der CanUseForDirectory-Wert vermeidet den Missbrauch von ProgIDs, die so festgelegt sind, dass sie nicht an der Implementierung benutzerdefinierter Verben für Ordner über Desktop.ini teilnehmen.
4.  Fügen Sie Verben unter dem Unterschlüssel **Folder** ProgID hinzu, z. B.:

    ```
    HKEY_CLASSES_ROOT
       CustomFolderType
          Shell
             MyVerb
                command
                   (Default) = %SystemRoot%\system32\notepad.exe %1\desktop.ini
    ```

> [!Note]  
> Diese Verben können das Standardverb sein. In diesem Fall wird das Verb durch Doppelklicken auf den Ordner aktiviert.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bewährte Methoden für Kontextmenühandler und Verben für mehrfache Auswahl](verbs-best-practices.md)
</dt> <dt>

[Auswählen eines statischen oder dynamischen Verbs für das Kontextmenü](shortcut-choose-method.md)
</dt> <dt>

[Anpassen eines Kontextmenüs mit dynamischen Verben](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[Kontextmenüs und Kontextmenühandler](context-menu.md)
</dt> <dt>

[Verben und Dateizuordnungen](fa-verbs.md)
</dt> <dt>

[Kontextmenüreferenz](context-menu-reference.md)
</dt> </dl>

 

 
