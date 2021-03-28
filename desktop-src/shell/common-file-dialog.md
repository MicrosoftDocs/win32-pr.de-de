---
description: Ab Windows Vista ersetzt das allgemeine Element Dialogfeld das ältere allgemeine Datei Dialogfeld, wenn es verwendet wird, um eine Datei zu öffnen oder zu speichern.
title: Dialog Feld für allgemeine Elemente
ms.topic: article
ms.date: 05/31/2018
ms.assetid: f8846148-89a5-4b9b-ad68-56137a5c2f65
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 896514779b2ba3d11d3db0551f82e21f1d4120b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342848"
---
# <a name="common-item-dialog"></a>Dialog Feld für allgemeine Elemente

Ab Windows Vista ersetzt das allgemeine Element Dialogfeld das ältere allgemeine Datei Dialogfeld, wenn es verwendet wird, um eine Datei zu öffnen oder zu speichern. Das Dialogfeld für allgemeine Elemente wird in zwei Variationen verwendet: dem Dialogfeld **Öffnen** und dem Dialogfeld **Speichern** . In diesen beiden Dialogfeldern wird der größte Teil ihrer Funktionalität genutzt, aber jede verfügt über eigene eindeutige Methoden.

Diese neuere Version heißt das allgemeine Element Dialogfeld, wird jedoch in der meisten Dokumentation weiterhin als gemeinsames Datei Dialogfeld bezeichnet. Wenn Sie nicht speziell mit einer älteren Version von Windows arbeiten, sollten Sie davon ausgehen, dass sich jede beliebige Angabe des allgemeinen Datei Dialogfelds auf dieses allgemeine Element Dialogfeld bezieht.

Die folgenden Themen werden hier behandelt:

-   [Ifiledialog, IFileOpenDialog und IFileSaveDialog](#ifiledialog-ifileopendialog-and-ifilesavedialog)
    -   [Beispiel Verwendung](#sample-usage)
-   [Lauschen auf Ereignisse aus dem Dialog Feld](#listening-to-events-from-the-dialog)
    -   [OnFileOk](#onfileok)
    -   [Onshareverletzungs und onüberschreibung](#onshareviolation-and-onoverwrite)
-   [Anpassen des Dialog Felds](#customizing-the-dialog)
    -   [Hinzufügen von Optionen zur Schaltfläche "OK"](#adding-options-to-the-ok-button)
    -   [Reagieren auf Ereignisse in hinzugefügten Steuerelementen](#responding-to-events-in-added-controls)
-   [Vollständige Beispiele](#full-samples)
-   [Zugehörige Themen](#related-topics)

## <a name="ifiledialog-ifileopendialog-and-ifilesavedialog"></a>Ifiledialog, IFileOpenDialog und IFileSaveDialog

Windows Vista stellt Implementierungen der Dialogfelder zum **Öffnen** und **Speichern** bereit: CLSID \_ fileopendialog und CLSID \_ filesavedialog. Diese Dialogfelder werden hier angezeigt.

![Screenshot des Dialog Felds "Öffnen"](images/cid/openfiledialog.png)

![Screenshot des Dialog Felds "Speichern unter"](images/cid/savefiledialog.png)

[**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) und [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog) erben von [**ifiledialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) und teilen viele ihrer Funktionen. Außerdem unterstützt das  Dialogfeld Öffnen **IFileOpenDialog**, und das Dialogfeld **Speichern** unterstützt **IFileSaveDialog**.

Die Implementierung der allgemeinen Element Dialogfelder in Windows Vista bietet gegenüber der in früheren Versionen bereitgestellten Implementierung verschiedene Vorteile:

-   Unterstützt die direkte Verwendung des Shell-Namespace über [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) anstelle der Verwendung von Dateisystem Pfaden.
-   Ermöglicht die einfache Anpassung des Dialog Felds, z. b. das Festlegen der Bezeichnung auf der Schaltfläche **OK** , ohne dass eine Hook-Prozedur erforderlich ist.
-   Unterstützt eine umfangreichere Anpassung des Dialog Felds durch das Hinzufügen eines Satzes von datengesteuerten Steuerelementen, die ohne eine Win32-Dialogfeld Vorlage ausgeführt werden. Dieses Anpassungs Schema gibt den aufrufenden Prozess aus dem Benutzeroberflächen Layout frei. Da Änderungen am Dialogfeld Entwurf weiterhin dieses Datenmodell verwenden, ist die Dialog-Implementierung nicht an die jeweilige aktuelle Version des Dialog Felds gebunden.
-   Unterstützt die aufruferbenachrichtigung über Ereignisse im Dialogfeld, z. b. Auswahl Änderungen oder Dateityp Änderungen. Ermöglicht es dem aufrufenden Prozess außerdem, bestimmte Ereignisse im Dialogfeld zu verbinden, z. b. die-Verarbeitung.
-   Führt neue Dialogfeld Funktionen ein, z. b. das Hinzufügen von vom Aufrufer **angegebenen Stellen zur** Leiste
-   Im Dialogfeld **Speichern** können Entwickler die neuen Metadatenfeatures der Windows Vista-Shell nutzen.

Außerdem können Entwickler die folgenden Schnittstellen implementieren:

-   [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) zum Empfangen von Benachrichtigungen über Ereignisse innerhalb des Dialog Felds.
-   [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) zum Hinzufügen von Steuerelementen zum Dialogfeld.
-   [**Ifiledialogcontrolevents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) , um über Ereignisse in diesen hinzugefügten Steuerelementen benachrichtigt zu werden.

Im Dialogfeld zum **Öffnen** oder **Speichern** wird ein [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) -oder [**ishellitemarray**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray) -Objekt an den aufrufenden Prozess zurückgegeben. Der Aufrufer kann dann ein einzelnes **IShellItem** -Objekt verwenden, um einen Dateisystempfad abzurufen oder einen Stream für das Element zu öffnen, um Informationen zu lesen oder zu schreiben.

Flags und Optionen, die für die neuen Dialogmethoden verfügbar sind, ähneln den älteren **ofn** -Flags, die in der [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) -Struktur gefunden werden und in [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) und [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea)verwendet werden. Viele von Ihnen sind identisch, mit der Ausnahme, dass Sie mit einem Fos-Präfix beginnen. Die komplette Liste finden Sie in den Themen [**ifiledialog:: GetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions) und [**ifiledialog:: slitoptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) . Dialogfelder zum **Öffnen** und **Speichern** werden standardmäßig mit den gängigsten Flags erstellt. Für das Dialogfeld " **Öffnen** " ist dies (z. b. "Fos \_ pathmustexist; \| \_ filemustexist \| Fos \_ nochangedir"), und für das Dialogfeld " **Speichern** " ist dies ("Fos \_ overwrite-prompt \| Fos \_ noreadonlyreturn \| Fos \_ pathmustexist Fos \| \_ nochangedir)"

[**Ifiledialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) und die untergeordneten Schnittstellen erben von und erweitern [**imodalwindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow). [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) nimmt als einzigen Parameter das Handle des übergeordneten Fensters an. Wenn **anzeigen** erfolgreich zurückgegeben wurde, ist ein gültiges Ergebnis vorhanden. Wenn Sie zurückgibt `HRESULT_FROM_WIN32(ERROR_CANCELLED)` , bedeutet dies, dass der Benutzer das Dialogfeld abgebrochen hat. Möglicherweise wird auch ein anderer Fehlercode wie z. b. " **E \_ outo-Memory**" zurückgegeben.

### <a name="sample-usage"></a>Beispielverwendung

In den folgenden Abschnitten wird Beispielcode für eine Vielzahl von Dialog Aufgaben veranschaulicht.

-   [Grundlegende Verwendung](#basic-usage)
-   [Einschränken der Ergebnisse auf Datei System Elemente](#limiting-results-to-file-system-items)
-   [Angeben von Dateitypen für ein Dialog Feld](#specifying-file-types-for-a-dialog)
-   [Steuern des Standard Ordners](#controlling-the-default-folder)
-   [Hinzufügen von Elementen zur Leiste "Plätze"](#adding-items-to-the-places-bar)
-   [Zustands Persistenz](#state-persistence)
-   [MultiSelect-Funktionen](#multiselect-capabilities)

Den größten Teil des Beispielcodes finden Sie im Beispiel zum Windows SDK [allgemeinen Datei Dialogfeld](samples-commonfiledialog.md).

### <a name="basic-usage"></a>Grundlegende Verwendung

Im folgenden Beispiel wird veranschaulicht, wie ein Dialogfeld **Öffnen** gestartet wird. In diesem Beispiel ist es auf Microsoft Word-Dokumente beschränkt.

> [!Note]  
> In mehreren Beispielen in diesem Thema wird die- `CDialogEventHandler_CreateInstance` Hilfsfunktion zum Erstellen einer Instanz der [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) -Implementierung verwendet. Wenn Sie diese Funktion in Ihrem eigenen Code verwenden möchten, kopieren Sie den Quellcode für die `CDialogEventHandler_CreateInstance` Funktion aus dem [Beispiel "Common File Dialog](samples-commonfiledialog.md)", aus dem alle Beispiele in diesem Thema entnommen werden.

 


```C++
HRESULT BasicFileOpen()
{
    // CoCreate the File Open Dialog object.
    IFileDialog *pfd = NULL;
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&pfd));
    if (SUCCEEDED(hr))
    {
        // Create an event handling object, and hook it up to the dialog.
        IFileDialogEvents *pfde = NULL;
        hr = CDialogEventHandler_CreateInstance(IID_PPV_ARGS(&pfde));
        if (SUCCEEDED(hr))
        {
            // Hook up the event handler.
            DWORD dwCookie;
            hr = pfd->Advise(pfde, &dwCookie);
            if (SUCCEEDED(hr))
            {
                // Set the options on the dialog.
                DWORD dwFlags;

                // Before setting, always get the options first in order 
                // not to override existing options.
                hr = pfd->GetOptions(&dwFlags);
                if (SUCCEEDED(hr))
                {
                    // In this case, get shell items only for file system items.
                    hr = pfd->SetOptions(dwFlags | FOS_FORCEFILESYSTEM);
                    if (SUCCEEDED(hr))
                    {
                        // Set the file types to display only. 
                        // Notice that this is a 1-based array.
                        hr = pfd->SetFileTypes(ARRAYSIZE(c_rgSaveTypes), c_rgSaveTypes);
                        if (SUCCEEDED(hr))
                        {
                            // Set the selected file type index to Word Docs for this example.
                            hr = pfd->SetFileTypeIndex(INDEX_WORDDOC);
                            if (SUCCEEDED(hr))
                            {
                                // Set the default extension to be ".doc" file.
                                hr = pfd->SetDefaultExtension(L"doc;docx");
                                if (SUCCEEDED(hr))
                                {
                                    // Show the dialog
                                    hr = pfd->Show(NULL);
                                    if (SUCCEEDED(hr))
                                    {
                                        // Obtain the result once the user clicks 
                                        // the 'Open' button.
                                        // The result is an IShellItem object.
                                        IShellItem *psiResult;
                                        hr = pfd->GetResult(&psiResult);
                                        if (SUCCEEDED(hr))
                                        {
                                            // We are just going to print out the 
                                            // name of the file for sample sake.
                                            PWSTR pszFilePath = NULL;
                                            hr = psiResult->GetDisplayName(SIGDN_FILESYSPATH, 
                                                               &pszFilePath);
                                            if (SUCCEEDED(hr))
                                            {
                                                TaskDialog(NULL,
                                                           NULL,
                                                           L"CommonFileDialogApp",
                                                           pszFilePath,
                                                           NULL,
                                                           TDCBF_OK_BUTTON,
                                                           TD_INFORMATION_ICON,
                                                           NULL);
                                                CoTaskMemFree(pszFilePath);
                                            }
                                            psiResult->Release();
                                        }
                                    }
                                }
                            }
                        }
                    }
                }
                // Unhook the event handler.
                pfd->Unadvise(dwCookie);
            }
            pfde->Release();
        }
        pfd->Release();
    }
    return hr;
}
```



### <a name="limiting-results-to-file-system-items"></a>Einschränken der Ergebnisse auf Datei System Elemente

Im folgenden Beispiel wird veranschaulicht, wie die Ergebnisse auf Dateisystem Elemente beschränkt werden. Beachten Sie, dass [**ifiledialog:: SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) das neue Flag einem Wert hinzufügt, der über [**ifiledialog:: GetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions)abgerufen wurde. Dies ist die empfohlene Methode.


```C++
                // Set the options on the dialog.
                DWORD dwFlags;

                // Before setting, always get the options first in order 
                // not to override existing options.
                hr = pfd->GetOptions(&dwFlags);
                if (SUCCEEDED(hr))
                {
                    // In this case, get shell items only for file system items.
                    hr = pfd->SetOptions(dwFlags | FOS_FORCEFILESYSTEM);
```



### <a name="specifying-file-types-for-a-dialog"></a>Angeben von Dateitypen für ein Dialog Feld

Um bestimmte Dateitypen festzulegen, die vom Dialog behandelt werden können, verwenden Sie die [**ifiledialog:: SetFileTypes**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfiletypes) -Methode. Diese Methode akzeptiert ein Array von [**comdlg \_ FILTERSPEC**](/windows/desktop/api/Shtypes/ns-shtypes-comdlg_filterspec) -Strukturen, von denen jedes einen Dateityp darstellt.

Der Standard Erweiterungsmechanismus in einem Dialogfeld ändert sich nicht von [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) und [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea). Die Dateinamenerweiterung, die an den Text angehängt wird, den der Benutzer in das Bearbeitungsfeld Dateiname eingibt, wird beim Öffnen des Dialog Felds initialisiert. Er sollte dem Standard Dateityp entsprechen (der beim Öffnen des Dialog Felds ausgewählt wird). Wenn der Standard Dateityp " \* . \* " lautet. (alle Dateien), kann die Datei eine Erweiterung Ihrer Wahl sein. Wenn der Benutzer einen anderen Dateityp auswählt, wird die Erweiterung automatisch auf die erste Dateinamenerweiterung aktualisiert, die diesem Dateityp zugeordnet ist. Wenn der Benutzer "." auswählt \* . \* (alle Dateien), dann wird die Erweiterung auf den ursprünglichen Wert zurückgesetzt.

Im folgenden Beispiel wird veranschaulicht, wie dies oben geschehen ist.


```C++
                        // Set the file types to display only. 
                        // Notice that this is a 1-based array.
                        hr = pfd->SetFileTypes(ARRAYSIZE(c_rgSaveTypes), c_rgSaveTypes);
                        if (SUCCEEDED(hr))
                        {
                            // Set the selected file type index to Word Docs for this example.
                            hr = pfd->SetFileTypeIndex(INDEX_WORDDOC);
                            if (SUCCEEDED(hr))
                            {
                                // Set the default extension to be ".doc" file.
                                hr = pfd->SetDefaultExtension(L"doc;docx");
```



### <a name="controlling-the-default-folder"></a>Steuern des Standard Ordners

Fast jeder Ordner im Shell-Namespace kann als Standardordner für den Dialog verwendet werden (der Ordner, der angezeigt wird, wenn der Benutzer eine Datei öffnen oder speichern möchte). Rufen Sie [**ifiledialog:: SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) auf, bevor Sie " [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) " aufrufen, um dies zu tun.

Der Standardordner ist der Ordner, in dem das Dialogfeld gestartet wird, wenn ein Benutzer es zum ersten Mal in der Anwendung öffnet. Anschließend wird das Dialogfeld im letzten Ordner geöffnet, den ein Benutzer geöffnet hat, oder in dem letzten Ordner, der zum Speichern eines Elements verwendet wurde. Weitere Informationen finden Sie unter [Zustands Persistenz](#state-persistence) .

Durch Aufrufen von [**ifiledialog:: SetFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfolder)können Sie erzwingen, dass das Dialogfeld immer den gleichen Ordner anzeigt, wenn es geöffnet wird, unabhängig von der vorherigen Benutzeraktion. Dies wird jedoch nicht empfohlen. Wenn Sie **SetFolder** aufrufen, bevor Sie das Dialogfeld anzeigen, wird der letzte Speicherort, in dem der Benutzer gespeichert oder geöffnet hat, nicht angezeigt. Wenn es keinen besonderen Grund für dieses Verhalten gibt, ist es keine gute oder erwartete Benutzer Darstellung und sollte vermieden werden. In fast allen Instanzen ist [**ifiledialog:: SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) die bessere Methode.

Wenn Sie ein Dokument zum ersten Mal im Dialogfeld **Speichern** speichern, sollten Sie dieselben Richtlinien befolgen, um den ursprünglichen Ordner zu bestimmen, wie im Dialogfeld **Öffnen** . Wenn der Benutzer ein bereits vorhandenes Dokument bearbeitet, öffnen Sie das Dialogfeld in dem Ordner, in dem das Dokument gespeichert ist, und füllen Sie das Bearbeitungsfeld mit dem Namen des Dokuments auf. Rufen Sie [**IFileSaveDialog:: setsaveasitem**](/windows/desktop/api/Shobjidl_core/nf-shobjidl_core-ifilesavedialog-setsaveasitem) mit dem aktuellen Element vor dem Aufrufen von [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show)auf.

### <a name="adding-items-to-the-places-bar"></a>Hinzufügen von Elementen zur Leiste "Plätze"

Das folgende Beispiel veranschaulicht das Hinzufügen von Elementen zur Leiste " **Plätze** ":


```C++
HRESULT AddItemsToCommonPlaces()
{
    // CoCreate the File Open Dialog object.
    IFileDialog *pfd = NULL;
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&pfd));
    if (SUCCEEDED(hr))
    {
        // Always use known folders instead of hard-coding physical file paths.
        // In this case we are using Public Music KnownFolder.
        IKnownFolderManager *pkfm = NULL;
        hr = CoCreateInstance(CLSID_KnownFolderManager, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&pkfm));
        if (SUCCEEDED(hr))
        {
            // Get the known folder.
            IKnownFolder *pKnownFolder = NULL;
            hr = pkfm->GetFolder(FOLDERID_PublicMusic, &pKnownFolder);
            if (SUCCEEDED(hr))
            {
                // File Dialog APIs need an IShellItem that represents the location.
                IShellItem *psi = NULL;
                hr = pKnownFolder->GetShellItem(0, IID_PPV_ARGS(&psi));
                if (SUCCEEDED(hr))
                {
                    // Add the place to the bottom of default list in Common File Dialog.
                    hr = pfd->AddPlace(psi, FDAP_BOTTOM);
                    if (SUCCEEDED(hr))
                    {
                        // Show the File Dialog.
                        hr = pfd->Show(NULL);
                        if (SUCCEEDED(hr))
                        {
                            //
                            // You can add your own code here to handle the results.
                            //
                        }
                    }
                    psi->Release();
                }
                pKnownFolder->Release();
            }
            pkfm->Release();
        }
        pfd->Release();
    }
    return hr;
}
```



### <a name="state-persistence"></a>Zustands Persistenz

Vor Windows Vista wurde ein Zustand, wie z. b. der zuletzt besuchte Ordner, pro Prozess gespeichert. Diese Informationen wurden jedoch unabhängig von der jeweiligen Aktion verwendet. Beispielsweise würde eine Anwendung zur Videobearbeitung denselben Ordner im Dialogfeld " **Rendering als** " enthalten, wie dies im Dialogfeld " **Medien importieren** " der Fall wäre. In Windows Vista können Sie durch die Verwendung von GUIDs spezifischer werden. Um dem Dialogfeld eine **GUID** zuzuweisen, nennen Sie [**ifiledialog:: setclientguid**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setclientguid).

### <a name="multiselect-capabilities"></a>MultiSelect-Funktionen

Die MultiSelect-Funktionalität ist im Dialogfeld **Öffnen** mit der [**GetResults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) -Methode verfügbar, wie hier gezeigt.


```C++
HRESULT MultiselectInvoke()
{
    IFileOpenDialog *pfd;
    
    // CoCreate the dialog object.
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                                  NULL, 
                                  CLSCTX_INPROC_SERVER, 
                                  IID_PPV_ARGS(&pfd));

    if (SUCCEEDED(hr))
    {
        DWORD dwOptions;
        // Specify multiselect.
        hr = pfd->GetOptions(&dwOptions);
        
        if (SUCCEEDED(hr))
        {
            hr = pfd->SetOptions(dwOptions | FOS_ALLOWMULTISELECT);
        }

        if (SUCCEEDED(hr))
        {
            // Show the Open dialog.
            hr = pfd->Show(NULL);

            if (SUCCEEDED(hr))
            {
                // Obtain the result of the user interaction.
                IShellItemArray *psiaResults;
                hr = pfd->GetResults(&psiaResults);
                
                if (SUCCEEDED(hr))
                {
                    //
                    // You can add your own code here to handle the results.
                    //
                    psiaResults->Release();
                }
            }
        }
        pfd->Release();
    }
    return hr;
}
```



## <a name="listening-to-events-from-the-dialog"></a>Lauschen auf Ereignisse aus dem Dialog Feld

Ein Aufruf ender Prozess kann eine [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) -Schnittstelle mit dem Dialogfeld mithilfe der Methoden [**ifiledialog:: Rat**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-advise) und [**ifiledialog:: unempfehlung**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-unadvise) registrieren, wie hier gezeigt.

Dies wird aus dem Beispiel " [grundlegende Verwendung](#basic-usage) " entnommen.


```C++
        // Create an event handling object, and hook it up to the dialog.
        IFileDialogEvents *pfde = NULL;
        hr = CDialogEventHandler_CreateInstance(IID_PPV_ARGS(&pfde));
        if (SUCCEEDED(hr))
        {
            // Hook up the event handler.
            DWORD dwCookie;
            hr = pfd->Advise(pfde, &dwCookie);
```



Der Großteil der Dialogfeld Verarbeitung würde hier eingefügt werden.


```C++
                // Unhook the event handler.
                pfd->Unadvise(dwCookie);
            }
            pfde->Release();
        }
        pfd->Release();
    }
    return hr;
}
```



Der Aufrufprozess kann Ereignisse für Benachrichtigungen verwenden, wenn der Benutzer den Ordner, den Dateityp oder die Auswahl ändert. Diese Ereignisse sind besonders nützlich, wenn der aufrufende Prozess dem Dialog Steuerelemente hinzugefügt hat (siehe [Anpassen des Dialog](#customizing-the-dialog)Felds) und den Zustand dieser Steuerelemente als Reaktion auf diese Ereignisse ändern müssen. In allen Fällen ist die Fähigkeit des aufrufenden Prozesses, benutzerdefinierten Code bereitzustellen, wie z. b. das Freigeben von Verstößen, das Überschreiben von Dateien oder das ermitteln, ob eine Datei gültig ist, bevor das Dialogfeld geschlossen wird. Einige dieser Fälle werden in diesem Abschnitt beschrieben.

### <a name="onfileok"></a>OnFileOk

Diese Methode wird aufgerufen, nachdem der Benutzer ein Element auswählt hat, kurz bevor das Dialogfeld geschlossen wird. Die Anwendung kann dann [**ifiledialog:: GetResult**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) oder [**IFileOpenDialog:: GetResults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) wie folgt aufgerufen werden, nachdem das Dialogfeld geschlossen wurde. Wenn das ausgewählte Element akzeptabel ist, können Sie S OK zurückgeben \_ . Andernfalls geben Sie "false" zurück \_ und zeigen die Benutzeroberfläche an, die dem Benutzer mitteilt, warum das ausgewählte Element ungültig ist. Wenn S \_ false zurückgegeben wird, wird das Dialogfeld nicht geschlossen.

Der aufrufende Prozess kann das Fenster Handle des Dialog Felds selbst als übergeordnetes Element der Benutzeroberfläche verwenden. Dieses Handle kann abgerufen werden, indem Sie zuerst [**IOleWindow:: QueryInterface**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) aufrufen und dann [**IOleWindow:: GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) mit dem Handle aufrufen, wie im folgenden Beispiel gezeigt.


```C++
HRESULT CDialogEventHandler::OnFileOk(IFileDialog *pfd) 
{ 
    IShellItem *psiResult;
    HRESULT hr = pfd->GetResult(&psiResult);
    
    if (SUCCEEDED(hr))
    {
        SFGAOF attributes;
        hr = psiResult->GetAttributes(SFGAO_COMPRESSED, &attributes);
    
        if (SUCCEEDED(hr))
        {
            if (attributes & SFGAO_COMPRESSED)
            {
                // Accept the file.
                hr = S_OK;
            }
            else
            {
                // Refuse the file.
                hr = S_FALSE;
                
                _DisplayMessage(pfd, L"Not a compressed file.");
            }
        }
        psiResult->Release();
    }
    return hr;
};

HRESULT CDialogEventHandler::_DisplayMessage(IFileDialog *pfd, PCWSTR pszMessage)
{
    IOleWindow *pWindow;
    HRESULT hr = pfd->QueryInterface(IID_PPV_ARGS(&pWindow));
    
    if (SUCCEEDED(hr))
    {
        HWND hwndDialog;
        hr = pWindow->GetWindow(&hwndDialog);
    
        if (SUCCEEDED(hr))
        {
            MessageBox(hwndDialog, pszMessage, L"An error has occurred", MB_OK);
        }
        pWindow->Release();
    }
    return hr;
}
```



### <a name="onshareviolation-and-onoverwrite"></a>Onshareverletzungs und onüberschreibung

Wenn sich der Benutzer für das Überschreiben einer Datei im Dialogfeld " **Speichern** " entscheidet, oder wenn eine Datei verwendet wird, die gespeichert oder ersetzt wird und nicht geschrieben werden kann (eine Freigabe Verletzung), kann die Anwendung benutzerdefinierte Funktionen bereitstellen, um das Standardverhalten des Dialog Felds zu überschreiben. Wenn eine Datei überschrieben wird, wird im Dialogfeld standardmäßig eine Eingabeaufforderung angezeigt, die dem Benutzer ermöglicht, diese Aktion zu überprüfen. Bei Freigabe Verstößen wird im Dialogfeld standardmäßig eine Fehlermeldung angezeigt, es wird nicht geschlossen, und der Benutzer muss eine andere Auswahl treffen. Der aufrufenden Prozess kann diese Standardwerte überschreiben und die eigene Benutzeroberfläche anzeigen, wenn gewünscht. Das Dialogfeld kann angewiesen werden, die Datei abzulehnen und offen zu bleiben oder die Datei zu akzeptieren und erfolgreich zu schließen.

## <a name="customizing-the-dialog"></a>Anpassen des Dialog Felds

Eine Vielzahl von Steuerelementen können dem Dialogfeld hinzugefügt werden, ohne eine Win32-Dialogfeld Vorlage bereitzustellen. Diese Steuerelemente umfassen PUSHBUTTON, ComboBox, EditBox, checkbutton, RadioButton-Listen, Gruppen, Trennzeichen und statische Text Steuerelemente. Rufen Sie **QueryInterface** im Dialog Objekt ([**ifiledialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog), [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog)oder [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog)) auf, um einen [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) -Zeiger zu erhalten. Verwenden Sie diese Schnittstelle, um Steuerelemente hinzuzufügen. Jedes Steuerelement verfügt über eine zugeordnete, vom Aufrufer bereitgestellte ID sowie einen *sichtbaren* und *aktivierten* Zustand, der vom aufrufenden Prozess festgelegt werden kann. Einigen Steuerelementen, z. b. PUSHBUTTON, sind auch Text zugeordnet.

Einer "visuellen Gruppe" können mehrere Steuerelemente hinzugefügt werden, die als eine Einheit im Layout des Dialog Felds verschoben werden. Gruppen kann eine Bezeichnung zugeordnet sein.

Steuerelemente können nur hinzugefügt werden, bevor das Dialogfeld angezeigt wird. Wenn das Dialogfeld angezeigt wird, können Steuerelemente jedoch wie gewünscht ausgeblendet oder angezeigt werden, möglicherweise als Reaktion auf eine Benutzeraktion. In den folgenden Beispielen wird gezeigt, wie eine Optionsfeld Liste zum Dialogfeld hinzugefügt wird.


```C++
// Controls
#define CONTROL_GROUP           2000
#define CONTROL_RADIOBUTTONLIST 2
#define CONTROL_RADIOBUTTON1    1
#define CONTROL_RADIOBUTTON2    2       // It is OK for this to have the same ID
                    // as CONTROL_RADIOBUTTONLIST, because it 
                    // is a child control under CONTROL_RADIOBUTTONLIST


// This code snippet demonstrates how to add custom controls in the Common File Dialog.
HRESULT AddCustomControls()
{
    // CoCreate the File Open Dialog object.
    IFileDialog *pfd = NULL;
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                                  NULL, 
                                  CLSCTX_INPROC_SERVER, 
                                  IID_PPV_ARGS(&pfd));
    if (SUCCEEDED(hr))
    {
        // Create an event handling object, and hook it up to the dialog.
        IFileDialogEvents   *pfde       = NULL;
        DWORD               dwCookie    = 0;
        hr = CDialogEventHandler_CreateInstance(IID_PPV_ARGS(&pfde));
        if (SUCCEEDED(hr))
        {
            // Hook up the event handler.
            hr = pfd->Advise(pfde, &dwCookie);
            if (SUCCEEDED(hr))
            {
                // Set up a Customization.
                IFileDialogCustomize *pfdc = NULL;
                hr = pfd->QueryInterface(IID_PPV_ARGS(&pfdc));
                if (SUCCEEDED(hr))
                {
                    // Create a Visual Group.
                    hr = pfdc->StartVisualGroup(CONTROL_GROUP, L&quot;Sample Group&quot;);
                    if (SUCCEEDED(hr))
                    {
                        // Add a radio-button list.
                        hr = pfdc->AddRadioButtonList(CONTROL_RADIOBUTTONLIST);
                        if (SUCCEEDED(hr))
                        {
                            // Set the state of the added radio-button list.
                            hr = pfdc->SetControlState(CONTROL_RADIOBUTTONLIST, 
                                               CDCS_VISIBLE | CDCS_ENABLED);
                            if (SUCCEEDED(hr))
                            {
                                // Add individual buttons to the radio-button list.
                                hr = pfdc->AddControlItem(CONTROL_RADIOBUTTONLIST,
                                                          CONTROL_RADIOBUTTON1,
                                                          L&quot;Change Title to ABC&quot;);
                                if (SUCCEEDED(hr))
                                {
                                    hr = pfdc->AddControlItem(CONTROL_RADIOBUTTONLIST,
                                                              CONTROL_RADIOBUTTON2,
                                                              L&quot;Change Title to XYZ&quot;);
                                    if (SUCCEEDED(hr))
                                    {
                                        // Set the default selection to option 1.
                                        hr = pfdc->SetSelectedControlItem(CONTROL_RADIOBUTTONLIST,
                                                                          CONTROL_RADIOBUTTON1);
                                    }
                                }
                            }
                        }
                        // End the visual group.
                        pfdc->EndVisualGroup();
                    }
                    pfdc->Release();
                }

                if (FAILED(hr))
                {
                    // Unadvise here in case we encounter failures 
                    // before we get a chance to show the dialog.
                    pfd->Unadvise(dwCookie);
                }
            }
            pfde->Release();
        }

        if (SUCCEEDED(hr))
        {
            // Now show the dialog.
            hr = pfd->Show(NULL);
            if (SUCCEEDED(hr))
            {
                //
                // You can add your own code here to handle the results.
                //
            }
            // Unhook the event handler.
            pfd->Unadvise(dwCookie);
        }
        pfd->Release();
    }
    return hr;
}
```





### <a name="adding-options-to-the-ok-button"></a>Hinzufügen von Optionen zur Schaltfläche "OK"

Entsprechend können Sie die Schaltflächen " **Öffnen** " oder " **Speichern** " auswählen, bei denen es sich um die Schaltfläche " **OK** " für die entsprechenden Dialog Typen handelt. Die Optionen sind über ein Dropdown-Listenfeld zugänglich, das an die Schaltfläche angefügt ist. Das erste Element in der Liste wird der Text für die Schaltfläche. Das folgende Beispiel zeigt, wie Sie eine Schaltfläche **Öffnen** mit zwei Möglichkeiten bereitstellen: "Öffnen" und "als schreibgeschützt öffnen".


```C++
// OpenChoices options
#define OPENCHOICES 0
#define OPEN 0
#define OPEN_AS_READONLY 1


HRESULT AddOpenChoices()
{
    // CoCreate the File Open Dialog object.
    IFileDialog *pfd = NULL;
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&pfd));
    if (SUCCEEDED(hr))
    {
        // Create an event handling object, and hook it up to the dialog.
        IFileDialogEvents   *pfde       = NULL;
        DWORD               dwCookie    = 0;
        hr = CDialogEventHandler_CreateInstance(IID_PPV_ARGS(&pfde));
        if (SUCCEEDED(hr))
        {
            // Hook up the event handler.
            hr = pfd->Advise(pfde, &dwCookie);
            if (SUCCEEDED(hr))
            {
                // Set up a Customization.
                IFileDialogCustomize *pfdc = NULL;
                hr = pfd->QueryInterface(IID_PPV_ARGS(&pfdc));
                if (SUCCEEDED(hr))
                {
                    hr = pfdc->EnableOpenDropDown(OPENCHOICES);
                    if (SUCCEEDED(hr))
                    {
                        hr = pfdc->AddControlItem(OPENCHOICES, OPEN, L&quot;&Open&quot;);
                    }                    
                    if (SUCCEEDED(hr))
                    {
                        hr = pfdc->AddControlItem(OPENCHOICES, 
                                                OPEN_AS_READONLY, 
                                                L&quot;Open as &read-only&quot;);
                    }
                    if (SUCCEEDED(hr))
                    {
                        pfd->Show(NULL);
                    }
                }
                pfdc->Release();
            }
            pfd->Unadvise(dwCookie);
        }
        pfde->Release();
    }
    pfd->Release();
    return hr;
}
```





Die Auswahl des Benutzers kann überprüft werden, nachdem der Dialog von der [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) -Methode wie bei einem Kombinations Feld zurückgegeben wurde, oder er kann im Rahmen der Verarbeitung durch [**IFileDialogEvents:: OnFileOk**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onfileok)überprüft werden.

### <a name="responding-to-events-in-added-controls"></a>Reagieren auf Ereignisse in hinzugefügten Steuerelementen

Der Ereignishandler, der vom aufrufenden Prozess bereitgestellt wird, kann [**ifiledialogcontrolevents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) zusätzlich zu [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents)implementieren. **Ifiledialogcontrolevents** ermöglicht dem aufrufenden Prozess, auf diese Ereignisse zu reagieren:

-   PUSHBUTTON geklickt
-   Kontrollkästchen Zustand geändert
-   Ausgewähltes Element in einem Menü, ComboBox oder RadioButton-Liste
-   Aktivieren des Steuer Elements. Dies wird gesendet, wenn ein Menü im Begriff ist, eine Dropdown Liste anzuzeigen, falls der aufrufenden Prozess die Elemente in der Liste ändern möchte.

## <a name="full-samples"></a>Vollständige Beispiele

Im folgenden finden Sie umfassende, herunterladbare C++-Beispiele aus dem Windows Software Development Kit (SDK), die die Verwendung von und die Interaktion mit dem Dialog Feld "allgemeine Elemente" veranschaulichen.

-   [Dialogfeld „Gemeinsame Dateien“ (Beispiel)](samples-commonfiledialog.md)
-   [Modi des Dialogfelds „Gemeinsame Dateien“ (Beispiel)](samples-commonfiledialogmodes.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IID \_ PPV-Argumente \_**](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 
