---
description: Beim Einfügen von Kontextmenü Handlern, auch als Kontextmenü Handler oder Verb Handler bezeichnet, handelt es sich um einen Dateityp Handler. Wie bei allen solchen Handlern sind Sie in-Process-Component Object Model (com)-Objekten, die als DLLs implementiert werden.
ms.assetid: cff79cdc-8a01-4575-9af7-2a485c6a8e46
title: Erstellen von Kontextmenü Handlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e8b7091483726c322a8ae18bace883af126d404
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/28/2021
ms.locfileid: "103869308"
---
# <a name="creating-shortcut-menu-handlers"></a>Erstellen von Kontextmenü Handlern

Beim Einfügen von Kontextmenü Handlern, auch als Kontextmenü Handler oder Verb Handler bezeichnet, handelt es sich um einen Dateityp Handler. Wie bei allen solchen Handlern sind Sie in-Process-Component Object Model (com)-Objekten, die als DLLs implementiert werden.

> [!Note]  
> Beim Registrieren von Handlern, die im Kontext von 32-Bit-Anwendungen funktionieren, gibt es spezielle Überlegungen für 64-Bit-Windows: Wenn Shellverben im Kontext einer 32-Bit-Anwendung aufgerufen werden, leitet das WOW64-Subsystem den Dateisystem Zugriff auf einige Pfade um. Wenn der exe-Handler in einem dieser Pfade gespeichert ist, kann in diesem Kontext nicht darauf zugegriffen werden. Als Problem Umgehung speichern Sie die exe-Datei in einem Pfad, der nicht umgeleitet wird, oder speichern Sie eine Stubversion der exe-Datei, die die tatsächliche Version gestartet hat.

 

Dieses Thema ist wie folgt organisiert:

-   [Kanonische Verben](#canonical-verbs)
-   [Erweiterte Verben](#extended-verbs)
-   [Anpassen eines Kontextmenüs mithilfe statischer Verben](#customizing-a-shortcut-menu-using-static-verbs)
    -   [Aktivieren des Handlers mithilfe der IDropTarget-Schnittstelle](#activating-your-handler-using-the-idroptarget-interface)
    -   [Angeben der Position und Reihenfolge statischer Verben](#specifying-the-position-and-order-of-static-verbs)
    -   [Positionieren von Verben am oberen oder unteren Rand des Menüs](#positioning-verbs-at-the-top-or-bottom-of-the-menu)
    -   [Erstellen von statischen kaskadierenden Menüs](#creating-static-cascading-menus)
    -   [Erzielen von dynamischem Verhalten für statische Verben mithilfe der erweiterten Abfrage Syntax](#getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax)
    -   [Veraltet: Zuordnen von Verben zu dynamischer Datenaustausch Befehlen](#deprecated-associating-verbs-with-dynamic-data-exchange-commands)
-   [Abschließen der Verb Implementierungsaufgaben](#completing-verb-implementation-tasks)
    -   [Anpassen des Kontextmenüs für vordefinierte Shellobjekte](#customizing-the-shortcut-menu-for-predefined-shell-objects)
    -   [Erweitern eines neuen Untermenüs](#extending-a-new-submenu)
    -   [Unterdrücken von Verbs](#suppressing-verbs-and-controlling-visibility)
    -   [Verwenden des Verb Auswahl Modells](#employing-the-verb-selection-model)
    -   [Verwenden von Element Attributen](#using-item-attributes)
    -   [Implementieren von benutzerdefinierten Verben für Ordner durch Desktop.ini](#implementing-custom-verbs-for-folders-through-desktopini)
-   [Zugehörige Themen](#related-topics)

## <a name="canonical-verbs"></a>Kanonische Verben

Anwendungen sind im Allgemeinen für die Bereitstellung lokalisierter Anzeige Zeichenfolgen für die von Ihnen definierten Verben verantwortlich Um jedoch eine gewisse Sprachunabhängigkeit zu gewährleisten, definiert das System einen Standardsatz häufig verwendeter Verben, die als kanonische Verben bezeichnet werden. Dem Benutzer wird nie ein kanonisches Verb angezeigt, das in jeder Benutzeroberflächen Sprache verwendet werden kann. Das System verwendet den kanonischen Namen, um automatisch eine ordnungsgemäß lokalisierte Anzeige Zeichenfolge zu generieren. Beispielsweise wird die Anzeige Zeichenfolge des geöffneten **Verbs auf ein** englisches System und auf das deutsche Äquivalent auf einem deutschen System festgelegt.



| Kanonisches Verb | BESCHREIBUNG                                                          |
|----------------|----------------------------------------------------------------------|
| Öffnen           | Öffnet die Datei oder den Ordner.                                            |
| OpenNew        | Öffnet die Datei oder den Ordner in einem neuen Fenster.                            |
| Drucken          | Druckt die Datei.                                                     |
| Printto        | Ermöglicht dem Benutzer das Drucken einer Datei durchziehen auf ein Drucker Objekt. |
| Erkunden        | Öffnet den Windows-Explorer mit ausgewähltem Ordner.                     |
| Eigenschaften     | Öffnet das Eigenschaften Blatt des-Objekts.                                   |



 

> [!Note]  
> Das **Printto** -Verb ist auch kanonisch, wird aber nie angezeigt. Durch die Einbindung kann der Benutzer eine Datei drucken, indem er Sie auf ein Drucker Objekt zieht.

 

Kontextmenü Handler können **mithilfe von \_** [**IContextMenu:: getcommandstring**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) und **GCS \_ Verba** eigene kanonische Verben bereitstellen. Das System verwendet die kanonischen Verben als zweiten Parameter (*lpoperation*), der an [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)übergeben wird, und ist [**cminvokecommandinfo**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo). **lpverb** -Member, der an die [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) -Methode übergeben wird.

## <a name="extended-verbs"></a>Erweiterte Verben

Wenn der Benutzer mit der rechten Maustaste auf ein Objekt klickt, zeigt das Kontextmenü die Standard Verben an. Möglicherweise möchten Sie Befehle in einigen Kontextmenüs hinzufügen und unterstützen, die nicht in jedem Kontextmenü angezeigt werden. Beispielsweise können Sie über Befehle verfügen, die nicht häufig verwendet werden oder für erfahrene Benutzer gedacht sind. Aus diesem Grund können Sie auch ein oder mehrere erweiterte Verben definieren. Diese Verben ähneln normalen Verben, werden jedoch durch die Art und Weise, in der Sie registriert sind, von normalen Verben unterschieden. Um Zugriff auf Erweiterte Verben zu erhalten, muss der Benutzer mit der rechten Maustaste auf ein Objekt klicken, während er die UMSCHALTTASTE drückt. Wenn der Benutzer dies tut, werden die erweiterten Verben zusätzlich zu den Standard Verben angezeigt.

Sie können die Registrierung verwenden, um ein oder mehrere erweiterte Verben zu definieren. Die zugeordneten Befehle werden nur angezeigt, wenn der Benutzer mit der rechten Maustaste auf ein Objekt klickt, während gleichzeitig die UMSCHALTTASTE gedrückt wird. Wenn Sie ein Verb als erweitert definieren möchten, fügen Sie dem Unterschlüssel des Verbs einen "erweiterten" **reg \_ SZ** -Wert hinzu. Dem Wert dürfen keine Daten zugeordnet werden.

## <a name="customizing-a-shortcut-menu-using-static-verbs"></a>Anpassen eines Kontextmenüs mithilfe statischer Verben

Nachdem Sie [ein statisches oder dynamisches Verb für das Kontextmenü ausgewählt](shortcut-choose-method.md) haben, können Sie das Kontextmenü für einen Dateityp erweitern, indem Sie für den Dateityp ein statisches Verb registrieren. Fügen Sie hierzu unter dem Unterschlüssel für die ProgID der Anwendung, die dem Dateityp zugeordnet ist, einen **shellunterschlüssel** hinzu. Optional können Sie ein Standard-Verb für den Dateityp definieren, indem Sie es als Standardwert für den **shellunterschlüssel** festlegen.

Das Standardverb wird zuerst im Kontextmenü angezeigt. Der Zweck besteht darin, die Shell mit einem Verb zu versehen, das Sie verwenden kann, wenn die [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) -Funktion aufgerufen wird, aber kein Verb angegeben wird. Die Shell wählt nicht notwendigerweise das Standard Verb aus, wenn **ShellExecuteEx** auf diese Weise verwendet wird.

Die Shell verwendet das erste verfügbare Verb in der folgenden Reihenfolge:

1.  Das Standardverb
2.  Das erste Verb in der Registrierung, wenn die Verb Reihenfolge angegeben ist.
3.  Das **geöffnete** Verb
4.  Das **geöffnete with** -Verb

Wenn keines der aufgelisteten Verben verfügbar ist, schlägt der Vorgang fehl.

Erstellen Sie einen Unterschlüssel für jedes Verb, das Sie unter dem shellsubschlüssel hinzufügen möchten. Jeder dieser Unterschlüssel muss über einen **reg \_ SZ** -Wert verfügen, der auf die Anzeige Zeichenfolge des Verbs (lokalisierte Zeichenfolge) festgelegt ist. Erstellen Sie für jeden Verb Unterschlüssel einen Befehls Unterschlüssel, wobei der Standardwert auf die Befehlszeile zum Aktivieren der Elemente festgelegt ist. Für kanonische Verben wie z. b. **Öffnen** und **Drucken** können Sie die Anzeige Zeichenfolge weglassen, da das System automatisch eine ordnungsgemäß lokalisierte Zeichenfolge anzeigt. Wenn Sie für nicht kanonische Verben die Anzeige Zeichenfolge weglassen, wird die Verb Zeichenfolge angezeigt.

Beachten Sie im folgenden Registrierungs Beispiel Folgendes:

-   Da es sich bei **doit** nicht um ein kanonisches Verb handelt, wird ihm ein Anzeige Name zugewiesen, der durch Drücken der D-Taste ausgewählt werden kann.
-   Das **Printto** -Verb wird nicht im Kontextmenü angezeigt. Allerdings ermöglicht die Einbindung in die Registrierung dem Benutzer das Drucken von Dateien, indem Sie Sie auf einem Druckersymbol ablegen.
-   Ein Unterschlüssel wird für jedes Verb angezeigt. **%1** stellt den Dateinamen und **%2** für den Drucker Namen dar.

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

Das folgende Diagramm veranschaulicht die Erweiterung des Kontextmenüs in Übereinstimmung mit den oben aufgeführten Registrierungs Einträgen. In diesem Kontextmenü sind die Verben Open, **do**, and **Print** in Ihrem Menü **geöffnet**, wobei **es** als Standard Verb angezeigt wird.

![Screenshot des Kontextmenüs "Do it default Verb"](images/context-menu/context-doitdefaultverb.png)

### <a name="activating-your-handler-using-the-idroptarget-interface"></a>Aktivieren des Handlers mithilfe der IDropTarget-Schnittstelle

Dynamischer Datenaustausch (DDE) ist veraltet. Verwenden Sie stattdessen [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) . **IDropTarget** ist stabiler und bietet bessere Aktivierungs Unterstützung, da es die COM-Aktivierung des Handlers verwendet. Bei der Auswahl mehrerer Elemente unterliegt **IDropTarget** nicht den Einschränkungen für die Puffergröße, die sowohl in DDE als auch in der Datei " [**kreateprocess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)" gefunden werden. Außerdem werden Elemente als Datenobjekt an die Anwendung übergeben, das mithilfe der [**shkreateshellitemarrayfromdataobject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) -Funktion in ein Element Array konvertiert werden kann. Dies ist einfacher und verliert keine Namespace Informationen, die auftreten, wenn das Element in einen Pfad für Befehlszeilen-oder DDE-Protokolle konvertiert wird.

Weitere Informationen zu [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) -und Shell-Abfragen für Datei Zuordnungs Attribute finden Sie unter [wahrgenommene Typen und Anwendungs Registrierung](fa-perceivedtypes.md).

### <a name="specifying-the-position-and-order-of-static-verbs"></a>Angeben der Position und Reihenfolge statischer Verben

Verben werden normalerweise in einem Kontextmenü basierend auf der Enumeration angeordnet. die Enumeration basiert zuerst auf der Reihenfolge des Association-Arrays und dann auf der Reihenfolge der Elemente im Association-Array, wie in der Sortierreihenfolge der Registrierung definiert.

Verben können durch Angabe des Standardwerts für den shellunterschlüssel für den Zuordnungs Eintrag geordnet werden. Dieser Standardwert kann ein einzelnes Element enthalten, das an der obersten Position des Kontextmenüs angezeigt wird, oder eine Liste von Elementen, die durch Leerzeichen oder Kommas getrennt sind. Im letzteren Fall ist das erste Element in der Liste das Standardelement, und die anderen Verben werden direkt unterhalb in der angegebenen Reihenfolge angezeigt.

Der folgende Registrierungs Eintrag erzeugt z. b. Kontextmenü Verben in der folgenden Reihenfolge:

1.  Anzeige
2.  Geschenken
3.  Personalization

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell
         Display
         Gadgets
         Personalization
```

Entsprechend erzeugt der folgende Registrierungs Eintrag Kontextmenü Verben in der folgenden Reihenfolge:

1.  Personalization
2.  Geschenken
3.  Anzeige

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell = "Personalization,Gadgets"
      Display
```

### <a name="positioning-verbs-at-the-top-or-bottom-of-the-menu"></a>Positionieren von Verben am oberen oder unteren Rand des Menüs

Das folgende Registrierungs Attribut kann verwendet werden, um ein Verb am oberen oder unteren Rand des Menüs zu platzieren. Wenn mehrere Verben vorhanden sind, die dieses Attribut angeben, erhält das letzte zu diesem Zweck Priorität:

``` syntax
Position=Top | Bottom 
```

### <a name="creating-static-cascading-menus"></a>Erstellen von statischen kaskadierenden Menüs

In Windows 7 und höher wird die Cascading-Menü Implementierung durch Registrierungs Einstellungen unterstützt. Vor Windows 7 war die Erstellung von kaskadierenden Menüs nur durch die Implementierung der [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) -Schnittstelle möglich. In Windows 7 und höher sollten Sie auf com-Code basierende Lösungen nur zugreifen, wenn die statischen Methoden unzureichend sind.

Der folgende Screenshot zeigt ein Beispiel für ein Cascading-Menü.

![Screenshot mit einem Beispiel für ein Cascading-Menü](images/file-assoc/filecascademenu2ndex.png)

In Windows 7 und höher gibt es drei Möglichkeiten, Kaskadierende Menüs zu erstellen:

-   [Erstellen von kaskadierenden Menüs mit dem Registrierungs Eintrag Unterbefehle](#creating-cascading-menus-with-the-subcommands-registry-entry)
-   [Erstellen von kaskadierenden Menüs mit dem Registrierungs Eintrag "extendedsubcommandskey"](#creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry)
-   [Erstellen von kaskadierenden Menüs mit der IExplorerCommand-Schnittstelle](#creating-cascading-menus-with-the-iexplorercommand-interface)

### <a name="creating-cascading-menus-with-the-subcommands-registry-entry"></a>Erstellen von kaskadierenden Menüs mit dem Registrierungs Eintrag Unterbefehle

In Windows 7 und höher können Sie mithilfe des Eintrags Unterbefehle Cascading-Menüs erstellen, indem Sie das folgende Verfahren verwenden.

**So erstellen Sie ein Cascading-Menü mithilfe des Eintrags "Unterbefehle"**

1.  Erstellen Sie unter **HKEY \_ Classes \_ root** \\ *ProgID* \\ **Shell** einen Unterschlüssel, um Ihr Cascading-Menü darzustellen. In diesem Beispiel geben wir diesem Unterschlüssel den Namen *cascadetest*. Stellen Sie sicher, dass der Standardwert des unter Schlüssels *caskadetten Test* leer ist und als **(Wert nicht festgelegt)** angezeigt wird.

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
    ```

2.  Fügen Sie dem Unterschlüssel *caskadetten Test* einen MUIVerb-Eintrag vom Typ **reg \_ SZ** hinzu, und weisen Sie ihm den Text zu, der im Kontextmenü als Name angezeigt wird. In diesem Beispiel weisen wir ihm das Menü "Test Cascade Menu" zu.

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu
    ```

3.  Fügen Sie Ihrem *caskadetten Test* -Unterschlüssel einen Eintrag Unterbefehle des Typs **reg \_ SZ** , dem die Liste zugewiesen ist, demlimited durch Semikolons, der Verben hinzu, die im Menü angezeigt werden sollen, in der Reihenfolge der Darstellung. Hier können Sie beispielsweise eine Reihe von vom System bereitgestellten Verben zuweisen:

    ```
    HKEY_CLASSES_ROOT
       *
          Shell
             CascadeTest
                SubCommands
                Windows.delete;Windows.properties;Windows.rename;Windows.cut;Windows.copy;Windows.paste
    ```

4.  Wenn Sie benutzerdefinierte Verben verwenden, implementieren Sie Sie mit einer der statischen Verb Implementierungs Methoden, und Listen Sie diese unter dem **commandstore** -Unterschlüssel auf, wie in diesem Beispiel für ein fiktives Verb *verbname* gezeigt:

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
> Diese Methode hat den Vorteil, dass die benutzerdefinierten Verben einmalig registriert und wieder verwendet werden können, indem Sie den Verb Namen unter dem Eintrag Unterbefehle auflisten. Allerdings muss die Anwendung über die Berechtigung zum Ändern der Registrierung unter **HKEY \_ local \_ Machine** verfügen.

 

### <a name="creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry"></a>Erstellen von kaskadierenden Menüs mit dem Registrierungs Eintrag "extendedsubcommandskey"

In Windows 7 und höher können Sie den Eintrag extendedsubcommandkey verwenden, um erweiterte Cascading Menüs zu erstellen: Cascading Menüs in kaskadierenden Menüs.

Der folgende Screenshot zeigt ein Beispiel für ein erweitertes Cascading-Menü.

![Screenshot mit erweitertem Cascading-Menü für Geräte](images/file-assoc/extendedsubcommandskey.png)

Da **HKEY \_ Classes \_ root** eine Kombination aus **HKEY \_ Current \_ User** und **HKEY \_ local \_ Machine** ist, können Sie alle benutzerdefinierten Verben unter dem Unterschlüssel **HKEY \_ Current \_ User** \\ **Software** \\ **Classes** registrieren. Der Hauptvorteil besteht darin, dass keine erhöhte Berechtigung erforderlich ist. Außerdem können andere Dateizuordnungen diesen gesamten Satz von Verben wieder verwenden, indem Sie den gleichen extendedsubcommandskey-Unterschlüssel angeben. Wenn Sie diesen Versatz nicht wieder verwenden müssen, können Sie die Verben unter dem übergeordneten Element auflisten, jedoch sicherstellen, dass der Standardwert des übergeordneten Elements leer ist.

**So erstellen Sie ein Cascading-Menü mithilfe eines extendedsubcommandskey-Eintrags**

1.  Erstellen Sie unter **HKEY \_ Classes \_ root** \\ *ProgID* \\ **Shell** einen Unterschlüssel, um Ihr Cascading-Menü darzustellen. In diesem Beispiel geben wir diesem Unterschlüssel den Namen " *CascadeTest2*". Stellen Sie sicher, dass der Standardwert des unter Schlüssels *caskadetten Test* leer ist und als **(Wert nicht festgelegt)** angezeigt wird.

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest2
                (Default)
    ```

2.  Fügen Sie dem Unterschlüssel *caskadetten Test* einen MUIVerb-Eintrag vom Typ **reg \_ SZ** hinzu, und weisen Sie ihm den Text zu, der im Kontextmenü als Name angezeigt wird. In diesem Beispiel weisen wir ihm das Menü "Test Cascade Menu" zu.

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu 2
    ```

3.  Fügen Sie unter dem Unterschlüssel *caskadetten Test* , den Sie erstellt haben, einen Unterschlüssel **extendedsubcommandskey** hinzu, und fügen Sie dann die Dokument Unterbefehle (vom Typ " **reg \_ SZ** ") hinzu. Beispiel:

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

    Stellen Sie sicher, dass der Standardwert des unter Schlüssels *Test Cascade Menu 2* leer und als **(Wert nicht festgelegt)** angezeigt wird.

4.  Füllen Sie die subverben mithilfe einer der folgenden statischen Verb Implementierungen auf. Beachten Sie, dass der commandflags-Unterschlüssel expcmdflags-Werte darstellt. Wenn Sie ein Trennzeichen vor oder nach dem kaskadierenden Menü Element hinzufügen möchten, verwenden Sie ECF \_ separatorbefore (0x20) oder ECF \_ separatorafter (0x40). Eine Beschreibung dieser Flags von Windows 7 und höher finden Sie unter [**IExplorerCommand:: GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags). ECF \_ separatorbefore funktioniert nur für Menü Elemente der obersten Ebene. MUIVerb ist vom Typ **reg \_ SZ**, und commandflags ist vom Typ **reg \_ DWORD**.

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

Der folgende Screenshot zeigt eine Abbildung der vorherigen Beispiele für den Registrierungsschlüssel Eintrag.

![Screenshot mit einem Beispiel für ein kaskadieres Menü, das die Auswahl von Editor und WordPad anzeigt](images/file-assoc/testcascademenu2.png)

### <a name="creating-cascading-menus-with-the-iexplorercommand-interface"></a>Erstellen von kaskadierenden Menüs mit der IExplorerCommand-Schnittstelle

Eine weitere Option zum Hinzufügen von Verben zu einem kaskadierenden Menü ist die Verwendung von [**IExplorerCommand:: enumsubcommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands). Diese Methode ermöglicht Datenquellen, die ihre Befehls Modul Befehle über [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) bereitstellen, diese Befehle als Verben in einem Kontextmenü zu verwenden. In Windows 7 und höher können Sie die gleiche Verb-Implementierung mithilfe von [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) bereitstellen, wie Sie mit [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)möglich sind.

Die folgenden beiden Screenshots veranschaulichen die Verwendung von kaskadierenden Menüs im Ordner " **Geräte** ".

![Screenshot, der ein Beispiel für ein kaskadieres Menü im Geräte Ordner anzeigt.](images/file-assoc/filecascademenu.png)

Der folgende Screenshot veranschaulicht eine weitere Implementierung eines kaskadierenden Menüs im **Geräte** Ordner.

![Screenshot mit einem Beispiel für ein kaskadieres Menü im Geräte Ordner](images/file-assoc/cascadedevices2.png)

> [!Note]  
> Da [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) nur die Prozess interne Aktivierung unterstützt, empfiehlt es sich, von shelldatenquellen zu verwenden, die die Implementierung zwischen Befehlen und Kontextmenüs freigeben müssen.

 

### <a name="getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax"></a>Erzielen von dynamischem Verhalten für statische Verben mithilfe der erweiterten Abfrage Syntax

Mit der erweiterten Abfrage Syntax (AQS) kann eine Bedingung ausgedrückt werden, die mithilfe von Eigenschaften aus dem Element ausgewertet wird, für das das Verb instanziiert wird. Dieses System funktioniert nur mit schnellen Eigenschaften. Dies sind Eigenschaften, die die Shell-Datenquelle so schnell meldet, dass * * * [* shcolstate \_ langsam * * *](/windows/win32/api/shtypes/ne-shtypes-shcolstate) * aus [**IShellFolder2:: getdefaultcolumnstate**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdefaultcolumnstate)nicht zurückgegeben wird.

Windows 7 und höher unterstützen kanonische Werte, mit denen Probleme bei lokalisierten Builds vermieden werden. Die folgende kanonische Syntax ist für lokalisierte Builds erforderlich, um diese Windows 7-Erweiterung nutzen zu können.

``` syntax
System.StructuredQueryType.Boolean#True
```

Im folgenden Beispiel Registrierungs Eintrag:

-   Der **appliesTo** -Wert steuert, ob das Verb angezeigt oder ausgeblendet wird.
-   Der defaultappliesto-Wert steuert, welches Verb der Standardwert ist.
-   Der hasluashield-Wert steuert, ob ein Schild für die Benutzerkontensteuerung (User Account Control, UAC) angezeigt wird.

In diesem Beispiel macht der **defaultappliesto** -Wert dieses Verb als Standardwert für jede Datei mit dem Wort "exampleText1" im Dateinamen. Der **appliesTo** -Wert aktiviert das Verb für jede Datei mit dem Namen "exampleText1" im Namen. Der Wert **hasluashield** zeigt das Schild für Dateien mit dem Namen "exampleText2" im Namen an.

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            DefaultAppliesTo = System.ItemName:"exampleText1"
            HasLUAShield = System.ItemName:"exampleText2"
            AppliesTo = System.ItemName:"exampleText1"
```

Fügen Sie den **Befehls** Unterschlüssel und einen Wert hinzu:

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            Command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

Informationen zur Windows 7-Registrierung finden Sie unter Stamm Laufwerk der **HKEY- \_ Klassen \_** \\  als Beispiel für BitLocker-Verben, die die folgende Methode verwenden:

-   AppliesTo = System. Volume. bitlockerprotection: = 2
-   System. Volume. bitlockerrequirements Sadmin: = System. structuredquerytype. Boolean \# true

Weitere Informationen zu AQS finden Sie unter [Erweiterte Abfrage Syntax](../search/-search-3x-advancedquerysyntax.md).

### <a name="deprecated-associating-verbs-with-dynamic-data-exchange-commands"></a>Veraltet: Zuordnen von Verben zu dynamischer Datenaustausch Befehlen

DDE ist veraltet. Verwenden Sie stattdessen [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) . DDE ist veraltet, da es sich auf eine Übertragungs Fenster Meldung bezieht, um den DDE-Server zu ermitteln. Ein DDE-Server reagiert nicht mehr auf die Meldung des Übertragungs Fensters Es kommt häufig vor, dass eine einzelne gesteckte Anwendung alle nachfolgenden Abstürze über die Benutzeroberflächen hinweg verursacht.

Die [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) -Methode ist robuster und bietet eine bessere Aktivierungs Unterstützung, da Sie die COM-Aktivierung des Handlers verwendet. Bei der Auswahl mehrerer Elemente unterliegt **IDropTarget** nicht den Einschränkungen für die Puffergröße, die sowohl in DDE als auch in der Datei " [**kreateprocess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)" gefunden werden. Außerdem werden Elemente als Datenobjekt an die Anwendung übergeben, das mithilfe der [**shkreateshellitemarrayfromdataobject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) -Funktion in ein Element Array konvertiert werden kann. Dies ist einfacher und verliert keine Namespace Informationen, die auftreten, wenn das Element in einen Pfad für Befehlszeilen-oder DDE-Protokolle konvertiert wird.

Weitere Informationen zu [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) -und Shell-Abfragen für Datei Zuordnungs Attribute finden Sie unter [wahrgenommene Typen und Anwendungs Registrierung](fa-perceivedtypes.md).

## <a name="completing-verb-implementation-tasks"></a>Abschließen der Verb Implementierungsaufgaben

Die folgenden Aufgaben für das Implementieren von Verben sind für statische und dynamische Verb Implementierungen von Bedeutung. Weitere Informationen zu dynamischen Verben finden [Sie unter Anpassen eines Kontextmenüs mithilfe dynamischer Verben](shortcut-menu-using-dynamic-verbs.md).

### <a name="customizing-the-shortcut-menu-for-predefined-shell-objects"></a>Anpassen des Kontextmenüs für vordefinierte Shellobjekte

Viele vordefinierte Shellobjekte verfügen über Kontextmenüs, die angepasst werden können. Registrieren Sie den Befehl auf die gleiche Weise, wie Sie typische Dateitypen registrieren, aber verwenden Sie den Namen des vordefinierten Objekts als Dateityp Namen.

Eine Liste der vordefinierten Objekte finden Sie im Abschnitt mit den *vordefinierten shellobjekten* unter [Erstellen von Shellerweiterungs Handlern](handlers.md). Die vordefinierten Shellobjekte, deren Kontextmenüs durch das Hinzufügen von Verben in der Registrierung angepasst werden können, werden in der Tabelle mit dem Wort "Verb" markiert.

### <a name="extending-a-new-submenu"></a>Erweitern eines neuen Untermenüs

Wenn ein Benutzer das Menü **Datei** in Windows-Explorer öffnet, ist einer der angezeigten Befehle **neu**. Wenn Sie diesen Befehl auswählen, wird ein Untermenü angezeigt. Standardmäßig enthält das Untermenü zwei Befehle, **Ordner** und Verknüpfungen, die es Benutzern **ermöglichen, unter** Ordner und Verknüpfungen zu erstellen. Dieses Untermenü kann so erweitert werden, dass es Datei Erstellungs Befehle für einen beliebigen Dateityp einschließt.

Wenn Sie dem **neuen** Untermenü einen Befehl zum Erstellen von Dateien hinzufügen möchten, müssen die Dateien Ihrer Anwendung über einen zugeordneten Dateityp verfügen. Fügen Sie einen **ShellNew** -Unterschlüssel unter dem Dateinamen ein. Wenn der **neue** Befehl im Menü **Datei** ausgewählt ist, fügt die Shell den Dateityp dem **neuen** Untermenü hinzu. Die Anzeige Zeichenfolge des Befehls ist die beschreibende Zeichenfolge, die der ProgID des Programms zugewiesen wird.

Um die Datei Erstellungs Methode anzugeben, weisen Sie einen oder mehrere Datenwerte dem **ShellNew** -Unterschlüssel zu. In der folgenden Tabelle sind die verfügbaren Werte aufgeführt.



| ShellNew-Unterschlüssel Wert | BESCHREIBUNG                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Befehl               | Führt eine Anwendung aus. Dieser **reg \_ SZ** -Wert gibt den Pfad der Anwendung an, die ausgeführt werden soll. Beispielsweise können Sie festlegen, dass ein Assistent gestartet wird.                  |
| Daten                  | Erstellt eine Datei mit den angegebenen Daten. Dieser **reg- \_ Binär** Wert gibt die Daten der Datei an. Die **Daten** werden ignoriert, wenn entweder die **nulldatei** oder der **Dateiname** angegeben wird. |
| FileName              | Erstellt eine Datei, die eine Kopie einer angegebenen Datei ist. Dieser **reg \_ SZ** -Wert gibt den voll qualifizierten Pfad der zu kopierenden Datei an.                                   |
| Nulldatei              | Erstellt eine leere Datei. **NullFile** wurde kein Wert zugewiesen. Wenn **NullFile** angegeben ist, werden die Registrierungs Werte für den **Daten** -und **Dateinamen** ignoriert.                    |



 

Das folgende Beispiel für einen Registrierungsschlüssel und einen Screenshot veranschaulichen das **neue** Untermenü für den Dateityp. MYP-ms. Es verfügt über den Befehl **myprogram Application**.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      MyProgram.1
         ShellNew
         NullFile
```

Der Screenshot zeigt das **neue** Untermenü. Wenn ein Benutzer im Untermenü **neu** die Option **myprogram-Anwendung** auswählt, erstellt die Shell eine Datei mit dem Namen **New myprogram Application. MYP-MS** und übergibt sie an **MyProgram.exe**.

![Screenshot von Windows-Explorer mit dem neuen Befehl "myprogram Application" im Untermenü "New"](images/context-menu/context-myprogramexe.png)

### <a name="creating-drag-and-drop-handlers"></a>Erstellen von Drag & Drop-Handlern

Das grundlegende Verfahren zum Implementieren eines Drag & Drop-Handlers ist das gleiche wie bei herkömmlichen Kontextmenü Handlern. Bei Kontextmenü Handlern wird jedoch normalerweise nur der [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -Zeiger verwendet, der an die [**ishellextinit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) -Methode des Handler weitergeleitet wird, um den Namen des Objekts zu extrahieren. Ein Drag & Drop-Handler könnte einen anspruchsvolleren Daten Handler implementieren, um das Verhalten des gezogenen Objekts zu ändern.

Wenn ein Benutzer mit der rechten Maustaste auf ein Shellobjekt klickt, um ein Objekt zu ziehen, wird ein Kontextmenü angezeigt, wenn der Benutzer versucht, das Objekt zu löschen. Der folgende Screenshot zeigt ein typisches Kontextmenü für Drag & Drop.

![Screenshot des Kontextmenüs "Drag & amp; Drop"](images/context-menu/context-dragdrop.png)

Ein Drag & Drop-Handler ist ein Kontextmenü Handler, der diesem Kontextmenü Elemente hinzufügen kann. Drag & Drop-Handler werden in der Regel unter dem folgenden Unterschlüssel registriert.

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
```

Fügen Sie unter dem Unterschlüssel **dragdrophandlers** für den Drag & Drop-Handler einen Unterschlüssel mit dem Namen hinzu, und legen Sie den Standardwert des unter Schlüssels auf das Zeichen folgen Format der Klassen Bezeichner-GUID (CLSID) des Handlers fest. Im folgenden Beispiel wird der Drag & Drop-Handler von **mydd** aktiviert.

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
            MyDD
               (Default) = {MyDD CLSID GUID}
```

### <a name="suppressing-verbs-and-controlling-visibility"></a>Unterdrücken von Verbs

Sie können Windows-Richtlinien Einstellungen verwenden, um die Sichtbarkeit zu steuern. Verben können durch Richtlinien Einstellungen durch Hinzufügen eines **SuppressionPolicy** -Werts oder eines **suppressionpolicyex** -GUID-Werts zum Registrierungs Unterschlüssel des Verbs unterdrückt werden. Legen Sie den Wert des unter Schlüssels **SuppressionPolicy** auf die Richtlinien-ID fest. Wenn die Richtlinie aktiviert ist, werden das Verb und der zugehörige Kontextmenü Eintrag unterdrückt. Mögliche Richtlinien-ID-Werte finden Sie unter der [**Einschränkungs**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) Enumeration.

### <a name="employing-the-verb-selection-model"></a>Verwenden des Verb Auswahl Modells

Registrierungs Werte müssen für Verben festgelegt werden, um Situationen zu behandeln, in denen ein Benutzer ein einzelnes Element, mehrere Elemente oder eine Auswahl aus einem Element auswählen kann. Ein Verb erfordert separate Registrierungs Werte für jede dieser drei Situationen, die das Verb unterstützt. Die möglichen Werte für das Verb Auswahl Modell lauten wie folgt:

-   Geben Sie den multiselectmodel-Wert für alle Verben an. Wenn der multiselectmodel-Wert nicht angegeben wird, wird er vom Typ der Verb-Implementierung abgeleitet, den Sie ausgewählt haben. Für com- **basierte Methoden (** z. b. "DropTarget" und "ExecuteCommand") wird angenommen, und für die anderen **Methoden wird angenommen** .
-   Geben Sie **Single** für Verben an, die nur eine einzelne Auswahl unterstützen.
-   Geben Sie **Player** für Verben an, die eine beliebige Anzahl von Elementen unterstützen
-   Geben Sie ein **Dokument** für Verben an, die für jedes Element ein Fenster auf oberster Ebene erstellen. Dadurch wird die Anzahl der aktivierten Elemente beschränkt, und es wird vermieden, dass Systemressourcen nicht mehr ausgelastet sind, wenn der Benutzer zu viele Fenster öffnet.

Wenn die Anzahl der ausgewählten Elemente nicht mit dem Verb Auswahl Modell identisch ist oder größer als die in der folgenden Tabelle aufgeführten Standard Limits ist, wird das Verb nicht angezeigt.



| Typ der Verb Implementierung | Dokument | Player    |
|-----------------------------|----------|-----------|
| Alt                      | 15 Elemente | 100 Elemente |
| COM                         | 15 Elemente | Keine Begrenzung  |



 

Im folgenden finden Sie Beispiel Registrierungseinträge, die den multiselectmodel-Wert verwenden.

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

### <a name="using-item-attributes"></a>Verwenden von Element Attributen

Die [**sfgao**](sfgao.md) -Flagwerte der shellattribute für ein Element können getestet werden, um zu bestimmen, ob das Verb aktiviert oder deaktiviert werden soll.

Um dieses Attribut zu verwenden, fügen Sie die folgenden **reg \_ DWORD** -Werte unter dem Verb hinzu:

-   Der attributemask-Wert gibt den [**sfgao**](sfgao.md) -Wert der Bitwerte der Maske an, die getestet werden soll.
-   Der AttributeValue-Wert gibt den [**sfgao**](sfgao.md) -Wert der zu testenden Bits an.
-   Das impliedselectionmodel gibt 0 (null) für Element Verben oder einen Wert ungleich 0 (null) für Verben im Hintergrund Kontextmenü an.

Im folgenden Beispiel Registrierungs Eintrag wird attributemask auf [**sfgao \_**](sfgao.md) schreibgeschützt (0x40000) festgelegt.

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

### <a name="implementing-custom-verbs-for-folders-through-desktopini"></a>Implementieren von benutzerdefinierten Verben für Ordner durch Desktop.ini

In Windows 7 und höher können Sie über Desktop.ini Verben zu einem Ordner hinzufügen. Weitere Informationen zu Desktop.ini Dateien finden Sie unter [Anpassen von Ordnern mit Desktop.ini](how-to-customize-folders-with-desktop-ini.md).

> [!Note]  
> Desktop.ini Dateien sollten immer als ausgeblendet **markiert werden**  +   , damit Sie Benutzern nicht angezeigt werden.

 

**Um benutzerdefinierte Verben für Ordner über eine Desktop.ini Datei hinzuzufügen, führen Sie die folgenden Schritte aus:**

1.  Erstellen **Sie** einen Ordner, der als schreibgeschützt oder als **System** markiert ist.
2.  Erstellen Sie eine Desktop.ini-Datei, die eine enthält \[ . Shellclassinfo \] directoryclass = Ordner ProgID.
3.  Erstellen Sie in der Registrierung **HKEY- \_ Klassen \_** \\ **Stamm Ordner ProgID** mit dem Wert canusefordirectory. Der Wert von "canusefordirectory" vermeidet den Missbrauch von ProgIDs, die nicht an der Implementierung benutzerdefinierter Verben für Ordner durch Desktop.ini beteiligt sind.
4.  Fügen Sie unter dem **Ordner** ProgID Unterschlüssel Verben hinzu, z. b.:

    ```
    HKEY_CLASSES_ROOT
       CustomFolderType
          Shell
             MyVerb
                command
                   (Default) = %SystemRoot%\system32\notepad.exe %1\desktop.ini
    ```

> [!Note]  
> Diese Verben können das Standardverb sein. in diesem Fall wird das Verb durch Doppelklicken auf den Ordner aktiviert.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bewährte Methoden für Kontextmenü Handler und Mehrfachauswahl Verben](verbs-best-practices.md)
</dt> <dt>

[Auswählen eines statischen oder dynamischen Verbs für das Kontextmenü](shortcut-choose-method.md)
</dt> <dt>

[Anpassen eines Kontextmenüs mithilfe dynamischer Verben](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[Kontextmenüs und Kontextmenü Handler](context-menu.md)
</dt> <dt>

[Verben und Dateizuordnungen](fa-verbs.md)
</dt> <dt>

[Verweis auf das Kontextmenü](context-menu-reference.md)
</dt> </dl>

 

 
