---
description: Anwendungsbenutzermodell-IDs (AppUserModelIDs) werden von der Taskleiste in systemen mit Windows 7 und höher umfassend verwendet, um Prozesse, Dateien und Fenster einer bestimmten Anwendung zuzuordnen.
ms.assetid: ebce2d99-6f20-4545-9f12-d79cd8d0828f
title: Anwendungsbenutzermodell-IDs (AppUserModelIDs)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd0835af241a36e4d9c95237890cb63790f7fe9031476dfa8ec21254266ffd7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119351470"
---
# <a name="application-user-model-ids-appusermodelids"></a>Anwendungsbenutzermodell-IDs (AppUserModelIDs)

Anwendungsbenutzermodell-IDs (AppUserModelIDs) werden von der Taskleiste in systemen mit Windows 7 und höher umfassend verwendet, um Prozesse, Dateien und Fenster einer bestimmten Anwendung zuzuordnen. In einigen Fällen ist es ausreichend, sich auf die interne AppUserModelID zu verlassen, die einem Prozess vom System zugewiesen wird. Eine Anwendung, die mehrere Prozesse besitzt, oder eine Anwendung, die in einem Hostprozess ausgeführt wird, muss sich jedoch möglicherweise explizit identifizieren, damit sie ihre ansonsten unterschiedlichen Fenster unter einer einzigen Taskleistenschaltfläche gruppieren und den Inhalt der Sprungliste der Anwendung steuern kann.

-   [Anwendungsdefiniert und System-Defined AppUserModelIDs](#application-defined-and-system-defined-appusermodelids)
-   [Erstellen einer Application-Defined AppUserModelID](#how-to-form-an-application-defined-appusermodelid)
-   [Zuweisen einer AppUserModelID](#where-to-assign-an-appusermodelid)
-   [Registrieren einer Anwendung als Hostprozess](#registering-an-application-as-a-host-process)
-   [Ausschlusslisten für Taskleisten-Anheften und Zuletzt durchgeführte/häufige Listen](#exclusion-lists-for-taskbar-pinning-and-recentfrequent-lists)
-   [Zugehörige Themen](#related-topics)

## <a name="application-defined-and-system-defined-appusermodelids"></a>Application-Defined und System-Defined AppUserModelIDs

Einige Anwendungen deklarieren keine explizite AppUserModelID. Sie sind optional. In diesem Fall verwendet das System eine Reihe von Heuristiken, um eine interne AppUserModelID zuzuweisen. Es gibt jedoch einen Leistungsvorteil bei der Vermeidung dieser Berechnungen, und eine explizite AppUserModelID ist die einzige Möglichkeit, eine genaue Benutzererfahrung zu gewährleisten. Daher wird dringend empfohlen, eine explizite ID festzulegen. Anwendungen können keine vom System zugewiesene AppUserModelID abrufen.

Wenn eine Anwendung eine explizite AppUserModelID verwendet, muss sie allen ausgeführten Fenstern oder Prozessen, Verknüpfungen und Dateizuordnungen dieselbe AppUserModelID zuweisen. Sie muss diese AppUserModelID auch beim Anpassen der Sprungliste über [**ICustomDestinationList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist)und in allen Aufrufen von [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs)verwenden.

> [!Note]  
> Wenn Anwendungen nicht über eine explizite AppUserModelID verfügen, müssen sie die Methoden [**IApplicationDestinations**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdestinations), [**IApplicationDocumentLists**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdocumentlists)und [**ICustomDestinationList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist) sowie [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) aus der Anwendung aufrufen. Wenn diese Methoden von einem anderen Prozess wie einem Installationsprogramm oder Deinstallationsprogramm aufgerufen werden, kann das System nicht die richtige AppUserModelID generieren, und diese Aufrufe haben keine Auswirkungen.

 

Die folgenden Elemente beschreiben häufige Szenarien, die eine explizite AppUserModelID erfordern. Sie verweisen auch auf Fälle, in denen mehrere explizite AppUserModelIDs verwendet werden sollten.

-   Eine einzelne ausführbare Datei mit einer Benutzeroberfläche mit mehreren Modi, die dem Benutzer als separate Anwendungen angezeigt werden, sollte jedem Modus unterschiedliche AppUserModelIDs zuweisen. Beispielsweise sollte ein Teil einer Anwendung, den Benutzer als unabhängige Benutzeroberfläche betrachten, an die sie sich anheften und von der Taskleiste getrennt von der restlichen Anwendung starten können, über eine eigene AppUserModelID verfügen, die von der Haupterfahrung getrennt ist.
-   Mehrere Verknüpfungen mit unterschiedlichen Argumenten, die alle zu dem führen, was der Benutzer als dieselbe Anwendung betrachtet, sollten eine AppUserModelID für alle Verknüpfungen verwenden. Beispielsweise verfügt Windows Internet Explorer über unterschiedliche Tastenkombinationen für verschiedene Modi (z. B. das Starten ohne Add-Ons), aber alle sollten dem Benutzer als einzelne Internet Explorer-Instanz angezeigt werden.
-   Eine ausführbare Datei, die als Hostprozess fungiert und Zielinhalte als Anwendung ausführt, muss [sich als Hostanwendung registrieren.](#registering-an-application-as-a-host-process)Danach kann sie jeder wahrgenommenen Benutzeroberfläche, die sie hostet, unterschiedliche AppUserModelIDs zuweisen. Alternativ kann der Hostprozess dem gehosteten Programm erlauben, seine AppUserModelIDs festzulegen. In beiden Fällen muss der Hostprozess die Quelle der AppUserModelIDs aufzeichnen, entweder sich selbst oder die gehostete Anwendung. In diesem Fall gibt es keine primäre Benutzeroberfläche des Hostprozesses ohne den Zielinhalt. Beispiele sind Windows Lokal integrierte Remoteanwendungen (RAIL), die Java-Runtime, RunDLL32.exe oder DLLHost.exe.

    Bei vorhandenen gehosteten Anwendungen versucht das System, einzelne Benutzeroberflächen zu identifizieren, neue Anwendungen sollten jedoch explizite AppUserModelIDs verwenden, um die gewünschte Benutzererfahrung zu gewährleisten.

-   Kooperative oder verkettete Prozesse, die für den Benutzer Teil derselben Anwendung sind, sollten auf jeden Prozess die gleiche AppUserModelID anwenden. Beispiele hierfür sind Spiele mit einem Startprogrammprozess (verkettet) und Microsoft Windows Media Player, die über eine Erste-Ausführungs-/Setuperfahrung verfügen, die in einem Prozess ausgeführt wird, und die Hauptanwendung, die in einem anderen Prozess ausgeführt wird (kooperativ).
-   Eine Shellnamespaceerweiterung, die als separate Anwendung für mehr als das Durchsuchen und Verwalten von Inhalten in Windows Explorer fungiert, sollte eine AppUserModelID in ihren Ordnereigenschaften zuweisen. Ein Beispiel ist die Systemsteuerung.
-   In einer Virtualisierungsumgebung wie einem Bereitstellungsframework sollte die Virtualisierungsumgebung jeder verwalteten Anwendung unterschiedliche AppUserModelIDs zuweisen. In diesen Fällen verwendet ein Anwendungsstarter einen Zwischenprozess, um die Umgebung einzurichten, und übergibt den Vorgang dann an einen anderen Prozess, um die Anwendung auszuführen. Beachten Sie, dass das System dadurch nicht in der Lage ist, den ausgeführten Zielprozess mit der Verknüpfung in Beziehung zu setzen, da die Verknüpfung auf den Zwischenprozess verweist.

    Wenn eine Anwendung über mehrere Fenster, Verknüpfungen oder Prozesse verfügt, sollte die zugewiesene AppUserModelID dieser Anwendung auch von der Virtualisierungsumgebung auf jedes dieser Teile angewendet werden.

    Ein Beispiel für diese Situation ist das ClickOnce Framework, das AppUserModelIDs ordnungsgemäß im Namen der von ihm verwalteten Anwendungen zuweist. Wie in allen umgebungen sollten anwendungen, die von ClickOnce bereitgestellt und verwaltet werden, selbst keine expliziten AppUserModelIDs zuweisen, da dies zu Konflikten mit den appUserModelIDs führt, die von ClickOnce zugewiesen werden, und zu unerwarteten Ergebnissen führen.

## <a name="how-to-form-an-application-defined-appusermodelid"></a>Erstellen einer Application-Defined AppUserModelID

Eine Anwendung muss ihre AppUserModelID im folgenden Format angeben. Er darf nicht mehr als 128 Zeichen enthalten und darf keine Leerzeichen enthalten. Jeder Abschnitt sollte in Pascal-Fall sein.

`CompanyName.ProductName.SubProduct.VersionInformation`

`CompanyName` und `ProductName` sollten immer verwendet werden, während die Teile und optional sind und von den Anforderungen der Anwendung `SubProduct` `VersionInformation` abhängen. `SubProduct` ermöglicht einer Hauptanwendung, die aus mehreren Unteranwendungen besteht, eine separate Taskleistenschaltfläche für jede Unteranwendung und die zugehörigen Fenster bereitzustellen. `VersionInformation` ermöglicht, dass zwei Versionen einer Anwendung gleichzeitig vorhanden sind, während sie als diskrete Entitäten betrachtet werden. Wenn eine Anwendung nicht auf diese Weise verwendet werden soll, `VersionInformation` sollte ausgelassen werden, damit eine aktualisierte Version dieselbe AppUserModelID wie die version verwenden kann, die sie ersetzt hat.

## <a name="where-to-assign-an-appusermodelid"></a>Zuweisen einer AppUserModelID

Wenn eine Anwendung eine oder mehrere explizite AppUserModelIDs verwendet, sollte sie diese AppUserModelIDs an den folgenden Speicherorten und Situationen anwenden:

-   In der [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) Eigenschaft der Verknüpfungsdatei der Anwendung. Eine Verknüpfung (als [**IShellLink,**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka)CLSID \_ ShellLink oder LNK-Datei) unterstützt Eigenschaften über [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) und andere Eigenschafteneinstellungsmechanismen, die in der gesamten Shell verwendet werden. Dadurch kann die Taskleiste die richtige Verknüpfung zum Anheften identifizieren und sicherstellen, dass die zum Prozess gehörenden Fenster dieser Taskleistenschaltfläche entsprechend zugeordnet sind.
    > [!Note]  
    > Die [System.AppUserModel.ID-Eigenschaft](../properties/props-system-appusermodel-id.md) sollte auf eine Verknüpfung angewendet werden, wenn diese Verknüpfung erstellt wird. Wenn Sie den Microsoft Windows Installer (MSI) zum Installieren der Anwendung verwenden, ermöglicht die [MsiShortcutProperty-Tabelle,](../msi/msishortcutproperty-table.md) dass die AppUserModelID auf die Verknüpfung angewendet wird, wenn sie während der Installation erstellt wird.

     

-   Als Eigenschaft eines der ausgeführten Fenster der Anwendung. Dies kann auf zwei Arten festgelegt werden:

    1.  Wenn verschiedene Fenster im Besitz eines Prozesses unterschiedliche AppUserModelIDs zum Steuern der Taskleistengruppierung erfordern, verwenden Sie [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow)), um den Eigenschaftenspeicher des Fensters abzurufen und appUserModelID als Fenstereigenschaft festzulegen.
    2.  Wenn alle Fenster im Prozess dieselbe AppUserModelID verwenden, legen Sie die AppUserModelID für den Prozess über [**SetCurrentProcessExplicitAppUserModelID fest.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-setcurrentprocessexplicitappusermodelid) Eine Anwendung muss **SetCurrentProcessExplicitAppUserModelID** aufrufen, um ihre AppUserModelID während der anfänglichen Startroutine einer Anwendung festzulegen, bevor die Anwendung eine Benutzeroberfläche präsentiert, änderungen ihrer Sprunglisten vornimmt oder einen Aufruf von [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs)vornimmt (oder bewirkt, dass das System dies bewirkt).

    Eine AppUserModelID auf Fensterebene überschreibt eine AppUserModelID auf Prozessebene.

    Wenn eine Anwendung eine explizite AppUserModelID auf Fensterebene festlegt, kann die Anwendung die Besonderheiten ihres Neustartbefehls für die Taskleistenschaltfläche angeben. Um diese Informationen zur Verfügung zu stellen, werden die folgenden Eigenschaften verwendet:

    -   [System.AppUserModel.CsvCommand](../properties/props-system-appusermodel-relaunchcommand.md)
    -   [System.AppUserModel.CsvDisplayNameResource](../properties/props-system-appusermodel-relaunchdisplaynameresource.md)
    -   [System.AppUserModel.IconResource](../properties/props-system-appusermodel-relaunchiconresource.md)

    > [!Note]  
    > Wenn eine Verknüpfung zum Starten der Anwendung vorhanden ist, sollte eine Anwendung die AppUserModelID als Eigenschaft der Verknüpfung anwenden, anstatt die Neustarteigenschaften zu verwenden. In diesem Fall werden die Befehlszeile, das Symbol und der Text der Verknüpfung verwendet, um die gleichen Informationen wie die Neustarteigenschaften zu liefern.

     

    Eine explizite AppUserModelID auf Fensterebene kann auch die [System.AppUserModel.PreventPinning-Eigenschaft](../properties/props-system-appusermodel-preventpinning.md) verwenden, um anzugeben, dass sie nicht zum Anheften oder Neustarten verfügbar sein soll.

-   Rufen Sie in einem Aufruf zum Anpassen oder Aktualisieren ([**ICustomDestinationList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist)) ([**IApplicationDocumentLists**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdocumentlists)) ab, oder löschen Sie ([**IApplicationDestinations**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdestinations)) die Sprungliste der Anwendung.
-   Bei der Dateizuordnungsregistrierung (über ihre [ProgID),](fa-progids.md)wenn die Anwendung die automatisch generierten Ziellisten **Zuletzt verwendet** oder **Häufig** verwendet. Auf diese Zuordnungsinformationen wird von [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs)verwiesen. Diese Informationen werden auch beim Hinzufügen von [**IShellItem-Zielen**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) zu benutzerdefinierten Sprunglisten über [**ICustomDestinationList::AppendCategory**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-appendcategory)verwendet.
-   Bei jedem Aufruf übergibt die Anwendung direkt an [**SHAddToRecentDocs.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) Wenn die Anwendung vom allgemeinen Dateidialogfeld abhängig ist, um AUFRUFE an **SHAddToRecentDocs** in ihrem Namen durchzuführen, können diese Aufrufe die explizite AppUserModelID nur dann ableiten, wenn die AppUserModelID für den gesamten Prozess festgelegt ist. Wenn die Anwendung AppUserModelIDs in ihren Fenstern und nicht im Prozess festlegt, muss die Anwendung alle Aufrufe von **SHAddToRecentDocs** selbst mit ihrer expliziten AppUserModelID ausführen und verhindern, dass der allgemeine Dateidialog eigene Aufrufe vornimmt. Dies muss jedes Mal erfolgen, wenn ein Element geöffnet wird, um sicherzustellen, dass die Abschnitte **Recent (Zuletzt)** oder **Frequent (Häufig)** der Sprungliste der Anwendung korrekt sind.

Die folgenden Elemente beschreiben häufige Szenarien und die Anwendung expliziter AppUserModelIDs in diesen Szenarien.

-   Wenn ein einzelner Prozess mehrere Anwendungen enthält, verwenden Sie [**SHGetPropertyStoreForWindow,**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow) um den Eigenschaftenspeicher des Fensters abzurufen und appUserModelID als Fenstereigenschaft festzulegen.
-   Wenn eine Anwendung mehrere Prozesse verwendet, wenden Sie die AppUserModelID auf jeden Prozess an. Ob Sie die gleiche AppUserModelID für jeden Prozess verwenden, hängt davon ab, ob jeder Prozess als Teil der Hauptanwendung oder als einzelne Entitäten angezeigt werden soll.
-   Um bestimmte Fenster von einer Gruppe im gleichen Prozess zu trennen, verwenden Sie den Eigenschaftenspeicher des Fensters, um eine einzelne AppUserModelID auf die Fenster anzuwenden, die Sie trennen möchten, und wenden Sie dann eine andere AppUserModelID auf den Prozess an. Jedes Fenster in diesem Prozess, das nicht explizit mit der AppUserModelID auf Fensterebene bezeichnet wurde, erbt die AppUserModelID des Prozesses.
-   Wenn einer Anwendung ein Dateityp zugeordnet ist, weisen Sie die AppUserModelID in der [ProgID-Registrierung](fa-progids.md) des Dateityps zu. Wenn eine einzelne ausführbare Datei in verschiedenen Modi gestartet wird, die dem Benutzer als unterschiedliche Anwendungen angezeigt werden, ist für jeden Modus eine separate AppUserModelID erforderlich. In diesem Fall müssen mehrere ProgID-Registrierungen für den Dateityp vorhanden sein, die jeweils eine andere AppUserModelID aufweisen.
-   Wenn es mehrere Verknüpfungsspeicherorte gibt, von denen ein Benutzer eine Anwendung starten kann (im **Startmenü,** auf dem Desktop oder an anderer Stelle), rufen Sie den Eigenschaftenspeicher der Verknüpfung ab, um eine einzelne AppUserModelID auf alle Verknüpfungen als Verknüpfungseigenschaften anzuwenden.
-   Wenn [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) von einer Anwendung explizit aufgerufen wird, verwenden Sie die AppUserModelID im Aufruf. Wenn das allgemeine Dateidialogfeld zum Öffnen oder Speichern von Dateien verwendet wird, wird **SHAddToRecentDocs** vom Dialogfeld im Namen der Anwendung aufgerufen. Dieser Aufruf kann die explizite AppUserModelID aus dem Prozess ableiten. Wenn jedoch eine explizite AppUserModelID als Fenstereigenschaft angewendet wird, kann das allgemeine Dateidialogfeld nicht die richtige AppUserModelID bestimmen. In diesem Fall muss die Anwendung selbst **SHAddToRecentDocs** explizit aufrufen und ihr die richtige AppUserModelID bereitstellen. Darüber hinaus muss die Anwendung verhindern, dass der allgemeine Dateidialog **SHAddToRecentDocs** in ihrem Namen aufruft, indem das \_ FOS-Flag DONTADDTORECENT in der **GetOptions-Methode** von [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) oder [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog)festgelegt wird.

## <a name="registering-an-application-as-a-host-process"></a>Registrieren einer Anwendung als Hostprozess

Eine Anwendung kann den IsHostApp-Registrierungseintrag so festlegen, dass der Prozess dieser ausführbaren Datei von der Taskleiste als Hostprozess betrachtet wird. Dies wirkt sich auf die Gruppierung und die Standardeinträge Sprungliste aus.

Das folgende Beispiel zeigt den erforderlichen Registrierungseintrag. Beachten Sie, dass dem Eintrag kein Wert zugewiesen ist. dies ist alles, was erforderlich ist. Es handelt sich um einen REG \_ NULL-Wert.

```
HKEY_CLASSES_ROOT
   Applications
      example.exe
         IsHostApp
```

Wenn entweder der Prozess selbst oder die Zum Starten des Prozesses verwendete Verknüpfungsdatei über eine explizite AppUserModelID verfügt, wird die Hostprozessliste ignoriert, und die Anwendung wird von der Taskleiste als normale Anwendung behandelt. Die ausgeführten Fenster der Anwendung werden unter einer einzigen Taskleistenschaltfläche gruppiert, und die Anwendung kann an die Taskleiste angeheftet werden.

Wenn nur der Name der ausführbaren Datei des ausgeführten Prozesses ohne explizite AppUserModelID bekannt ist und diese ausführbare Datei in der Liste des Hostprozesses enthalten ist, wird jede Instanz des Prozesses als separate Entität für die Taskleistengruppierung behandelt. Die Taskleistenschaltfläche, die einer bestimmten Instanz des Prozesses zugeordnet ist, zeigt keine Option zum Anheften/Lösen oder ein Startsymbol für eine neue Instanz des Prozesses an. Der Prozess kann auch nicht in die Liste der am häufigsten verwendeten (MFU) des **Startmenüs** aufgenommen werden. Wenn der Prozess jedoch über eine Verknüpfung gestartet wurde, die Startargumente enthält (in der Regel der Zielinhalt, der als "Anwendung" hostet), kann das System die Identität bestimmen, und die Anwendung kann angeheftet und neu gestartet werden.

## <a name="exclusion-lists-for-taskbar-pinning-and-recentfrequent-lists"></a>Ausschlusslisten für Taskleisten-Anheften und Zuletzt durchgeführte/häufige Listen

Anwendungen, Prozesse und Fenster können festlegen, dass sie für das Anheften an die Taskleiste oder für die Aufnahme in die MFU-Liste des **Startmenüs** nicht verfügbar sind. Hierfür gibt es drei Mechanismen:

1.  Fügen Sie der Registrierung der Anwendung den Eintrag NoStartPage hinzu, wie hier gezeigt:

    ```
    HKEY_CLASSES_ROOT
       Applications
          Example.exe
             NoStartPage
    ```

    Die dem NoStartPage-Eintrag zugeordneten Daten werden ignoriert. Nur das Vorhandensein des Eintrags ist erforderlich. Daher ist der ideale Typ für NoStartPage REG \_ NONE.

    Beachten Sie, dass jede Verwendung einer expliziten AppUserModelID den NoStartPage-Eintrag überschreibt. Wenn eine explizite AppUserModelID auf eine Verknüpfung, einen Prozess oder ein Fenster angewendet wird, kann sie angeheftet werden und ist für die MFU-Liste des **Startmenüs** geeignet.

2.  Legen Sie die [System.AppUserModel.PreventPinning-Eigenschaft](../properties/props-system-appusermodel-preventpinning.md) für Fenster und Verknüpfungen fest. Diese Eigenschaft muss in einem Fenster vor der [PKEY \_ AppUserModel \_ ID-Eigenschaft](../properties/props-system-appusermodel-id.md) festgelegt werden.
3.  Fügen Sie eine explizite AppUserModelID als Wert unter dem folgenden Registrierungsunterschlüssel hinzu, wie hier gezeigt:

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      FileAssociation
                         NoStartPageAppUserModelIDs
                            AppUserModelID1
                            AppUserModelID2
                            AppUserModelID3
    ```

    Jeder Eintrag ist ein REG \_ NULL-Wert mit dem Namen der AppUserModelID. AppUserModelID in dieser Liste kann nicht angeheftet werden und kann nicht in die MFU-Liste des **Startmenüs** aufgenommen werden.

Beachten Sie, dass bestimmte ausführbare Dateien sowie Verknüpfungen, die bestimmte Zeichenfolgen im Namen enthalten, automatisch vom Anheften und Einschließen in die MFU-Liste ausgeschlossen werden.

> [!Note]  
> Dieser automatische Ausschluss kann durch Anwenden einer expliziten AppUserModelID überschrieben werden.

 

Wenn eine der folgenden Zeichenfolgen unabhängig von der Schreibung im Kontextnamen enthalten ist, kann das Programm nicht angeheftet werden und wird nicht in der Liste der am häufigsten verwendeten Zeichenfolgen angezeigt (gilt nicht für Windows 10):

-   Dokumentation
-   Hilfe
-   Installieren
-   Weitere Informationen
-   Lesen Sie mich.
-   Lesen sie zuerst.
-   Infodatei
-   Entfernen
-   Einrichten
-   Support
-   Neuerungen

Die folgende Liste von Programmen kann nicht angeheftet werden und ist von der Liste der am häufigsten verwendeten Programme ausgeschlossen.

-   Applaunch.exe
-   Control.exe
-   Dfsvc.exe
-   Dllhost.exe
-   Guestmodemsg.exe
-   Hh.exe
-   Install.exe
-   Isuninst.exe
-   Lnkstub.exe
-   Mmc.exe
-   Mshta.exe
-   Msiexec.exe
-   Msoobe.exe
-   Rundll32.exe
-   Setup.exe
-   St5unst.exe
-   Unwise.exe
-   Unwise32.exe
-   Werfault.exe
-   Winhlp32.exe
-   Wlrmdr.exe
-   Wuapp.exe

Die obigen Listen werden in den folgenden Registrierungswerten gespeichert.

> [!Note]  
> Diese Listen sollten nicht von Anwendungen geändert werden. Verwenden Sie eine der zuvor aufgeführten Ausschlusslistenmethoden für dieselbe Benutzeroberfläche.

 

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FileAssociation
                     AddRemoveApps
                     HostApps
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**SetCurrentProcessExplicitAppUserModelID**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-setcurrentprocessexplicitappusermodelid)
</dt> <dt>

[**GetCurrentProcessExplicitAppUserModelID**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-getcurrentprocessexplicitappusermodelid)
</dt> <dt>

[Taskleistenerweiterungen](taskbar-extensions.md)
</dt> <dt>

[**ICustomDestinationList::SetAppID**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-setappid)
</dt> <dt>

[**IApplicationDocumentLists::SetAppID**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-setappid)
</dt> <dt>

[**IApplicationDestinations::SetAppID**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdestinations-setappid)
</dt> <dt>

[**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow)
</dt> </dl>

 

 
