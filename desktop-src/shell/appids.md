---
description: App-Benutzer Modell-IDs (appusermudelids) werden von der Taskleiste in Windows 7-Systemen und späteren Systemen ausgiebig verwendet, um Prozesse, Dateien und Fenster einer bestimmten Anwendung zuzuordnen.
ms.assetid: ebce2d99-6f20-4545-9f12-d79cd8d0828f
title: Anwendungs Benutzer Modell-IDs (appusermudelids)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46b79f0bdd7fb5e6c4d5c41caa3cd6be3f4fb57e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525415"
---
# <a name="application-user-model-ids-appusermodelids"></a>Anwendungs Benutzer Modell-IDs (appusermudelids)

App-Benutzer Modell-IDs (appusermudelids) werden von der Taskleiste in Windows 7-Systemen und späteren Systemen ausgiebig verwendet, um Prozesse, Dateien und Fenster einer bestimmten Anwendung zuzuordnen. In einigen Fällen ist es ausreichend, die interne appusermodelid zu verlassen, die einem Prozess vom System zugewiesen wird. Allerdings muss eine Anwendung, die über mehrere Prozesse oder eine Anwendung verfügt, die in einem Host Prozess ausgeführt wird, möglicherweise explizit identifiziert werden, damit Sie die ansonsten ungleichen Fenster unter einer einzigen Task leisten Schaltfläche gruppieren und den Inhalt der Sprung Liste der Anwendung steuern kann.

-   [Anwendungs definierte und System-Defined appusermudelids](#application-defined-and-system-defined-appusermodelids)
-   [So erstellen Sie eine Application-Defined "appusermodelid"](#how-to-form-an-application-defined-appusermodelid)
-   [Wo eine appusermodelid zugewiesen werden soll](#where-to-assign-an-appusermodelid)
-   [Registrieren einer Anwendung als Host Prozess](#registering-an-application-as-a-host-process)
-   [Ausschluss Listen für das Anheften und aktuelle/häufige Listen der Taskleiste](#exclusion-lists-for-taskbar-pinning-and-recentfrequent-lists)
-   [Zugehörige Themen](#related-topics)

## <a name="application-defined-and-system-defined-appusermodelids"></a>Application-Defined und System-Defined appusermudelids

Einige Anwendungen deklarieren keine explizite appusermodelid. Sie sind optional. In diesem Fall verwendet das System eine Reihe von Heuristik, um eine interne appusermodelid zuzuweisen. Es gibt jedoch einen Leistungsvorteil, wenn diese Berechnungen vermieden werden und eine explizite appusermodelid die einzige Möglichkeit ist, eine exakte Benutzererfahrung zu gewährleisten. Daher wird dringend empfohlen, eine explizite ID festzulegen. Anwendungen können keine vom System zugewiesene appusermodelid abrufen.

Wenn eine Anwendung eine explizite appusermodelid verwendet, muss Sie auch allen laufenden Fenstern oder Prozessen, Verknüpfungen und Dateizuordnungen dieselbe appusermodelid zuweisen. Außerdem muss diese appusermodelid verwendet werden, wenn die Sprung Liste über [**ICustomDestinationList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist)und in allen Aufrufen von " [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs)" angepasst wird.

> [!Note]  
> Wenn Anwendungen nicht über eine explizite appusermodelid verfügen, müssen Sie die Methoden " [**iapplicationdestination**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdestinations)", " [**iapplicationdocumentlists**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdocumentlists)" und " [**ICustomDestinationList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist) " sowie " [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) " innerhalb der Anwendung abrufen. Wenn diese Methoden von einem anderen Prozess aufgerufen werden, z. b. einem Installationsprogramm oder einem Deinstallationsprogramm, kann das System nicht die richtige appusermodelid generieren, und diese Aufrufe haben keine Auswirkung.

 

Die folgenden Elemente beschreiben allgemeine Szenarien, die eine explizite appusermodelid erfordern. Außerdem zeigen Sie auf Fälle, in denen mehrere explizite appusermudelids verwendet werden sollen.

-   Bei einer einzelnen ausführbaren Datei mit einer Benutzeroberfläche mit mehreren Modi, die dem Benutzer als separate Anwendungen angezeigt wird, sollten jedem Modus unterschiedliche appusermudelids zugewiesen werden. Beispielsweise sollte ein Teil einer Anwendung, der Benutzern als unabhängige Umgebung angezeigt wird, die Sie an die Taskleiste anheften und von der restlichen Anwendung aus starten können, über eine eigene appusermodelid verfügen, die von der Haupterfahrung getrennt ist.
-   Mehrere Verknüpfungen mit unterschiedlichen Argumenten, die dazu führen, dass der Benutzer als dieselbe Anwendung angezeigt wird, sollten eine appusermodelid für alle Tastenkombinationen verwenden. Windows Internet Explorer verfügt beispielsweise über unterschiedliche Verknüpfungen für verschiedene Modi (z. b. das Starten ohne Add-ons), aber Sie sollten für den Benutzer als eine einzelne Internet Explorer-Instanz angezeigt werden.
-   Eine ausführbare Datei, die als Host Prozess fungiert und Ziel Inhalt ausführt, da sich eine Anwendung als [Host Anwendung registrieren](#registering-an-application-as-a-host-process)muss. Anschließend kann Sie jeder erkannten Erfahrung, die Sie hostet, unterschiedliche appusermudelids zuweisen. Alternativ kann der Host Prozess dem gehosteten Programm ermöglichen, seine appusermudelids festzulegen. In jedem Fall muss der Host Prozess einen Datensatz der Quelle der appusermudelids (entweder selbst oder die gehostete Anwendung) beibehalten. In diesem Fall gibt es keine primäre Benutzer Darstellung des Host Prozesses ohne den Ziel Inhalt. Beispiele hierfür sind lokale Windows-Remote Anwendungen (Rail), die Java-Laufzeit, RunDLL32.exe oder DLLHost.exe.

    Im Fall vorhandener gehosteter Anwendungen versucht das System, individuelle Erfahrungen zu identifizieren, aber neue Anwendungen sollten explizite appusermudelids verwenden, um die gewünschte Benutzererfahrung zu gewährleisten.

-   Kooperative oder verkettete Prozesse, die an den Benutzer Teil derselben Anwendung sind, sollten die gleiche appusermodelid für jeden Prozess anwenden. Beispiele hierfür sind Spiele mit einem Start Programmprozess (verkettete) und Microsoft Windows-Media Player, die in einem einzigen Prozess ausgeführt werden können, und die Hauptanwendung, die in einem anderen Prozess ausgeführt wird (kooperativ).
-   Eine Erweiterung des Shell-Namespace, die als separate Anwendung für mehr als das Durchsuchen und Verwalten von Inhalten in Windows-Explorer fungiert, sollte in den Ordnereigenschaften eine appusermodelid zuweisen. Ein Beispiel hierfür ist die Systemsteuerung.
-   In einer Virtualisierungsumgebung, wie z. b. einem Bereitstellungs Framework, sollte die Virtualisierungsumgebung jeder verwalteten Anwendung verschiedene appusermudelids zuweisen. In diesen Fällen verwendet ein Anwendungs Starter einen Vermittler Prozess zum Einrichten der Umgebung und übergibt dann den Vorgang an einen anderen Prozess zum Ausführen der Anwendung. Beachten Sie, dass das System dazu führt, dass der laufende Ziel Prozess nicht wieder mit der Verknüpfung verknüpft wird, da die Verknüpfung auf den Vermittler Prozess verweist.

    Wenn eine Anwendung über mehrere Fenster, Verknüpfungen oder Prozesse verfügt, sollte die zugewiesene appusermodelid der Anwendung auch auf jedes dieser Teile von der Virtualisierungsumgebung angewendet werden.

    Ein Beispiel für diese Situation ist das ClickOnce-Framework, das appusermudelids ordnungsgemäß für die von ihm verwalteten Anwendungen zuweist. Wie in allen solchen Umgebungen sollten Anwendungen, die von ClickOnce bereitgestellt und verwaltet werden, keine expliziten appusermudelids selbst zuweisen, da dies mit den von ClickOnce zugewiesenen appusermudelids in Konflikt steht und zu unerwarteten Ergebnissen führt.

## <a name="how-to-form-an-application-defined-appusermodelid"></a>So erstellen Sie eine Application-Defined "appusermodelid"

Eine Anwendung muss Ihre appusermodelid in der folgenden Form bereitstellen. Er darf nicht mehr als 128 Zeichen enthalten und darf keine Leerzeichen enthalten. Jeder Abschnitt sollte mit Pascal-Schreib-und Schreib vor.

`CompanyName.ProductName.SubProduct.VersionInformation`

`CompanyName` und `ProductName` sollten immer verwendet werden, während die `SubProduct` `VersionInformation` Teile und optional sind und abhängig von den Anforderungen der Anwendung sind. `SubProduct` ermöglicht einer Hauptanwendung, die aus mehreren untergeordneten Anwendungen besteht, eine separate Task leisten Schaltfläche für jede unter Anwendung und die zugehörigen Fenster bereitzustellen. `VersionInformation` ermöglicht die Koexistenz zweier Versionen einer Anwendung, während Sie als diskrete Entitäten betrachtet werden. Wenn eine Anwendung nicht auf diese Weise verwendet werden soll, `VersionInformation` sollte ausgelassen werden, damit eine aktualisierte Version die gleiche appusermodelid wie die von ihr ersetzte Version verwenden kann.

## <a name="where-to-assign-an-appusermodelid"></a>Wo eine appusermodelid zugewiesen werden soll

Wenn eine Anwendung eine oder mehrere explizite appusermudelids verwendet, sollte diese appusermudelids an den folgenden Orten und Situationen angewendet werden:

-   In der [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) -Eigenschaft der Verknüpfungs Datei der Anwendung. Eine Verknüpfung (als [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka), CLSID \_ shelllink oder eine LNK-Datei) unterstützt Eigenschaften über [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) und andere in der Shell verwendete Mechanismen für die Eigenschafts Einstellung. Dadurch kann die Taskleiste die richtige Verknüpfung zum Anheften identifizieren und sicherstellen, dass Windows, das zum Prozess gehört, ordnungsgemäß mit der Schaltfläche der Taskleiste verknüpft ist.
    > [!Note]  
    > Die [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) -Eigenschaft sollte auf eine Verknüpfung angewendet werden, wenn diese Verknüpfung erstellt wird. Bei Verwendung der Microsoft Windows Installer (MSI) zum Installieren der Anwendung ermöglicht die [msishortcutproperty](../msi/msishortcutproperty-table.md) -Tabelle, dass appusermodelid auf die Verknüpfung angewendet wird, wenn Sie während der Installation erstellt wird.

     

-   Als Eigenschaft eines beliebigen Windows-Betriebs in der Anwendung. Dies kann auf zwei Arten festgelegt werden:

    1.  Wenn verschiedene Fenster, die im Besitz eines Prozesses sind, unterschiedliche appusermudelids zum Steuern der Task leisten Gruppierung benötigen, verwenden Sie [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow)), um den Eigenschaften Speicher des Fensters abzurufen und appusermodelid als Fenster Eigenschaft festzulegen.
    2.  Wenn alle Fenster im Prozess die gleiche appusermodelid verwenden, legen Sie die appusermodelid für den Prozess fest, aber [**SetCurrentProcessExplicitAppUserModelID**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-setcurrentprocessexplicitappusermodelid). Eine Anwendung muss **SetCurrentProcessExplicitAppUserModelID** aufrufen, um Ihre appusermodelid während der anfänglichen Start Routine einer Anwendung festzulegen, bevor die Anwendung eine Benutzeroberfläche anzeigt, eine Bearbeitung der Sprung Listen durchführt oder das System veranlasst, jeden beliebigen Aufrufe von " [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs)" auszuführen.

    Eine appusermodelid auf Fenster Ebene überschreibt eine appusermodelid auf Prozessebene.

    Wenn eine Anwendung eine explizite appusermodelid auf der Fenster Ebene festlegt, kann die Anwendung die Besonderheiten des Befehls zum Neustarten für die zugehörige Task leisten Schaltfläche bereitstellen. Um diese Informationen bereitzustellen, werden die folgenden Eigenschaften verwendet:

    -   [System. appusermodel. relaunchcommand](../properties/props-system-appusermodel-relaunchcommand.md)
    -   [System. appusermodel. relaunchdisplaynameresource](../properties/props-system-appusermodel-relaunchdisplaynameresource.md)
    -   [System. appusermodel. relaunchienresource](../properties/props-system-appusermodel-relaunchiconresource.md)

    > [!Note]  
    > Wenn eine Verknüpfung vorhanden ist, um die Anwendung zu starten, sollte eine Anwendung appusermodelid als Eigenschaft der Verknüpfung anwenden, anstatt die Neustart Eigenschaften zu verwenden. In diesem Fall werden die Befehlszeile, das Symbol und der Text der Verknüpfung verwendet, um dieselben Informationen wie die Neustart Eigenschaften bereitzustellen.

     

    Eine explizite appusermodelid auf Fenster Ebene kann auch die [System. appusermodel. preventpinning](../properties/props-system-appusermodel-preventpinning.md) -Eigenschaft verwenden, um anzugeben, dass Sie nicht zum Fixieren oder Neusenden verfügbar sein soll.

-   Rufen Sie in einem Aufruf von anpassen oder aktualisieren ([**ICustomDestinationList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist)) die Sprung Liste der Anwendung ab ([**iapplicationdocumentlists**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdocumentlists)), oder löschen Sie Sie ([**iapplicationdestination**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdestinations)).
-   In der Datei Zuordnungs Registrierung (über die [ProgID](fa-progids.md)), wenn die Anwendung die automatisch generierten **aktuellen** oder **häufigen** Ziellisten des Systems verwendet. Auf diese Zuordnungs Informationen wird von " [**shaddtor ecentdocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs)" verwiesen. Diese Informationen werden auch verwendet, wenn [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) -Ziele mithilfe von [**ICustomDestinationList:: AppendCategory**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-appendcategory)zu benutzerdefinierten Sprung Listen hinzugefügt werden.
-   In jedem beliebigen-Befehl stellt die Anwendung " [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs)" direkt zur Anwendung. Wenn die Anwendung vom allgemeinen Datei Dialogfeld abhängig ist, um in Ihrem Auftrag Aufrufe an " **SHAddToRecentDocs** " auszuführen, können diese Aufrufe nur dann die explizite appusermodelid ableiten, wenn die appusermodelid für den gesamten Prozess festgelegt ist. Wenn die Anwendung appuserwdelids in Ihrem Fenster anstelle von für den Prozess festlegt, muss die Anwendung alle Aufrufe von " **SHAddToRecentDocs** " selbst mit ihrer expliziten appusermodelid ausführen, und es wird verhindert, dass das allgemeine Datei Dialogfeld eigene Aufrufe durchführen kann. Dies muss jedes Mal erfolgen, wenn ein Element geöffnet wird, um sicherzustellen, dass die **aktuellen** oder **häufigen** Abschnitte der Sprung Liste der Anwendung korrekt sind.

In den folgenden Abschnitten werden häufige Szenarien beschrieben, und es wird erläutert, wo explizite appusermudelids in diesen Szenarien angewendet werden.

-   Wenn ein einzelner Prozess mehrere Anwendungen enthält, rufen Sie mit [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow) den Eigenschaften Speicher des Fensters ab, und legen Sie appusermodelid als Fenster Eigenschaft fest.
-   Wenn eine Anwendung mehrere Prozesse verwendet, wenden Sie die appusermodelid auf jeden Prozess an. Ob Sie für jeden Prozess dieselbe appusermodelid verwenden, hängt davon ab, ob jeder Prozess als Teil der Hauptanwendung oder als einzelne Entitäten angezeigt werden soll.
-   Wenn Sie bestimmte Fenster von einem Satz im gleichen Prozess trennen möchten, verwenden Sie den Eigenschaften Speicher des Fensters, um eine einzelne appusermodelid auf die Fenster anzuwenden, die Sie trennen möchten, und wenden Sie dann eine andere appusermodelid auf den Prozess an. Jedes Fenster in diesem Prozess, das nicht explizit mit der appusermodelid auf Fenster Ebene gekennzeichnet war, erbt die appusermodelid des Prozesses.
-   Wenn ein Dateityp einer Anwendung zugeordnet ist, weisen Sie die appusermodelid in der [ProgID](fa-progids.md) -Registrierung des Dateityps zu. Wenn eine einzelne ausführbare Datei in verschiedenen Modi gestartet wird, die dem Benutzer als unterschiedliche Anwendungen angezeigt werden, ist für jeden Modus eine separate appusermodelid erforderlich. In diesem Fall müssen mehrere ProgID-Registrierungen für den Dateityp vorhanden sein, die jeweils über eine andere appusermodelid verfügen.
-   Wenn mehrere Verknüpfungs Orte vorhanden sind, von denen ein Benutzer eine Anwendung starten kann (im **Startmenü** auf dem Desktop oder an einem anderen Ort), rufen Sie den Eigenschafts Speicher der Verknüpfung ab, um eine einzelne appusermodelid auf alle Verknüpfungen als Verknüpfungs Eigenschaften anzuwenden.
-   Wenn von einer Anwendung ein expliziter Rückruf an " [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) " erfolgt, verwenden Sie die appusermodelid im-Befehl. Wenn das Dialogfeld "common file" verwendet wird, um Dateien zu öffnen oder zu speichern, wird " **shaddtor ecentdocs** " im Auftrag der Anwendung vom Dialog aufgerufen. Dieser Befehl kann die explizite appusermodelid aus dem Prozess ableiten. Wenn jedoch eine explizite appusermodelid als Fenster Eigenschaft angewendet wird, kann das allgemeine Datei Dialogfeld die richtige appusermodelid nicht ermitteln. In diesem Fall muss die Anwendung selbst den Namen " **SHAddToRecentDocs** " explizit abrufen und die richtige "appusermodelid" bereitstellen. Darüber hinaus muss die Anwendung verhindern, dass das Dialogfeld für die gemeinsame Datei in Ihrem Auftrag " **SHAddToRecentDocs** " aufrufen kann, indem das Flag "Fos \_ dontaddtorecent" in der **GetOptions** -Methode von [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) oder [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog)angegeben wird.

## <a name="registering-an-application-as-a-host-process"></a>Registrieren einer Anwendung als Host Prozess

Eine Anwendung kann den ishostapp-Registrierungs Eintrag so festlegen, dass der Prozess dieser ausführbaren Datei von der Taskleiste als Host Prozess angesehen wird. Dies wirkt sich auf die Gruppierungs-und Standard Sprung Listeneinträge aus.

Das folgende Beispiel zeigt den erforderlichen Registrierungs Eintrag. Beachten Sie, dass dem Eintrag kein Wert zugewiesen ist. Das vorhanden sein ist alles, was erforderlich ist. Dabei handelt es sich um einen reg- \_ NULL-Wert.

```
HKEY_CLASSES_ROOT
   Applications
      example.exe
         IsHostApp
```

Wenn entweder der Prozess selbst oder die zum Starten des Prozesses verwendete Verknüpfungs Datei über eine explizite appusermodelid verfügt, wird die Host Prozessliste ignoriert, und die Anwendung wird von der Taskleiste als normale Anwendung behandelt. Die Betriebs Fenster der Anwendung werden in einer einzigen Task leisten Schaltfläche zusammengefasst, und die Anwendung kann an die Taskleiste angeheftet werden.

Wenn nur der ausführbare Name des ausführenden Prozesses ohne explizite appusermodelid bekannt ist und diese ausführbare Datei in der Liste der Host Prozesse enthalten ist, wird jede Instanz des Prozesses als separate Entität für die Task leisten Gruppierung behandelt. In der Task leisten Schaltfläche, die einer bestimmten Instanz des Prozesses zugeordnet ist, wird keine PIN/unpin-Option oder ein Start Symbol für eine neue Instanz des Prozesses angezeigt. Der Prozess kann auch nicht in die Liste der am häufigsten verwendeten (MFU) **Startmenüs** eingefügt werden. Wenn der Prozess jedoch über eine Verknüpfung gestartet wurde, die Start Argumente enthält (in der Regel der Ziel Inhalt, der als "Anwendung" gehostet wird), kann das System die Identität ermitteln, und die Anwendung kann fixiert und neu gestartet werden.

## <a name="exclusion-lists-for-taskbar-pinning-and-recentfrequent-lists"></a>Ausschluss Listen für das Anheften und aktuelle/häufige Listen der Taskleiste

Anwendungen, Prozesse und Windows können auswählen, dass Sie sich selbst nicht für das **anheften** an die Taskleiste oder die Einbindung in die MFU-Liste des Start Menüs entscheiden. Hierfür gibt es drei Mechanismen:

1.  Fügen Sie den NoStartPage-Eintrag zur Registrierung der Anwendung hinzu, wie hier gezeigt:

    ```
    HKEY_CLASSES_ROOT
       Applications
          Example.exe
             NoStartPage
    ```

    Die dem NoStartPage-Eintrag zugeordneten Daten werden ignoriert. Nur das vorhanden sein des Eintrags ist erforderlich. Daher ist der ideale Typ für NoStartPage "reg \_ None".

    Beachten Sie, dass jede Verwendung einer expliziten appusermodelid den NoStartPage-Eintrag überschreibt. Wenn eine explizite appusermodelid auf eine Verknüpfung, einen Prozess oder ein Fenster angewendet wird, wird Sie gepinckbar und ist für die MFU-Liste des **Start** Menüs geeignet.

2.  Legen Sie die [System. appusermodel. preventpinning](../properties/props-system-appusermodel-preventpinning.md) -Eigenschaft unter Windows und Verknüpfungen fest. Diese Eigenschaft muss in einem Fenster vor der Eigenschaft [pkey \_ appusermodel \_ ID](../properties/props-system-appusermodel-id.md) festgelegt werden.
3.  Fügen Sie eine explizite appusermodelid als Wert unter dem folgenden Registrierungs Unterschlüssel hinzu, wie hier gezeigt:

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

    Jeder Eintrag ist ein reg- \_ NULL-Wert mit dem Namen der appusermodelid. Alle in dieser Liste gefundenen appusermodelid-Werte können nicht in die MFU-Liste des **Start** Menüs aufgenommen werden.

Beachten Sie, dass bestimmte ausführbare Dateien und Verknüpfungen, die bestimmte Zeichen folgen in Ihrem Namen enthalten, automatisch vom anhechern und einschließen in die MFU-Liste ausgeschlossen werden.

> [!Note]  
> Dieser automatische Ausschluss kann überschrieben werden, indem eine explizite appusermodelid angewendet wird.

 

Wenn eine der folgenden Zeichen folgen, unabhängig von der Groß-/Kleinschreibung, im Verknüpfungs Namen enthalten ist, kann das Programm nicht festgelegt werden und wird nicht in der am häufigsten verwendeten Liste angezeigt (gilt nicht für Windows 10):

-   Dokumentation
-   Hilfe
-   Installieren
-   Weitere Informationen
-   Lesezugriff
-   Zuerst lesen
-   Infodatei
-   Remove (Entfernen)
-   Einrichten
-   Support
-   Neuerungen

Die folgende Liste der Programme ist nicht pinckbar und wird aus der Liste der am häufigsten verwendeten Programme ausgeschlossen.

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

Die vorangehenden Listen werden in den folgenden Registrierungs Werten gespeichert.

> [!Note]  
> Diese Listen sollten nicht von Anwendungen geändert werden. Verwenden Sie eine der zuvor aufgeführten Methoden der Ausschlussliste für die gleiche Funktion.

 

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

[**Getcurrentprocessexplicitappusermodelid**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-getcurrentprocessexplicitappusermodelid)
</dt> <dt>

[Task leisten Erweiterungen](taskbar-extensions.md)
</dt> <dt>

[**ICustomDestinationList:: "abtappid"**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-setappid)
</dt> <dt>

[**Iapplicationdocumentlists:: abtappid**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-setappid)
</dt> <dt>

[**Iapplicationdestination:: abtappid**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdestinations-setappid)
</dt> <dt>

[**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow)
</dt> </dl>

 

 
