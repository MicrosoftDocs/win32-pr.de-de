---
description: Ab Windows Vista ersetzt das Dialogfeld "Allgemeines Element" das ältere Dialogfeld "Allgemeine Datei", wenn es zum Öffnen oder Speichern einer Datei verwendet wird.
title: Dialogfeld "Allgemeines Element"
ms.topic: article
ms.date: 05/31/2018
ms.assetid: f8846148-89a5-4b9b-ad68-56137a5c2f65
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 2956bf7329ff9c92b777199d040d1275aa827cfa9ea9c8bfbec175d234b204f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943520"
---
# <a name="common-item-dialog"></a>Dialogfeld "Allgemeines Element"

Ab Windows Vista ersetzt das Dialogfeld "Allgemeines Element" das ältere Dialogfeld "Allgemeine Datei", wenn es zum Öffnen oder Speichern einer Datei verwendet wird. Das Dialogfeld "Allgemeines Element" wird in zwei Varianten verwendet: im **Dialogfeld** Öffnen und **im Dialogfeld Speichern.** Diese beiden Dialoge teilen sich den Größten ihrer Funktionalität, aber jedes dialogfeld verfügt über eigene eindeutige Methoden.

Diese neuere Version heißt zwar "Dialogfeld für allgemeine Elemente", wird aber in den meisten Dokumentationen weiterhin als Dialogfeld "Gemeinsame Datei" bezeichnet. Sofern Sie nicht speziell mit einer älteren Version von Windows arbeiten, sollten Sie davon ausgehen, dass jede Erwähnung des Dialogfelds "Gemeinsame Datei" auf dieses Dialogfeld für allgemeine Elemente verweist.

Die folgenden Themen werden hier erläutert:

-   [IFileDialog, IFileOpenDialog und IFileSaveDialog](#ifiledialog-ifileopendialog-and-ifilesavedialog)
    -   [Beispielverwendung](#sample-usage)
-   [Lauschen auf Ereignisse über den Dialog](#listening-to-events-from-the-dialog)
    -   [Onfileok](#onfileok)
    -   [OnShareViolation und OnOverwrite](#onshareviolation-and-onoverwrite)
-   [Anpassen des Dialogs](#customizing-the-dialog)
    -   [Hinzufügen von Optionen zur Schaltfläche "OK"](#adding-options-to-the-ok-button)
    -   [Reagieren auf Ereignisse in hinzugefügten Steuerelementen](#responding-to-events-in-added-controls)
-   [Vollständige Beispiele](#full-samples)
-   [Zugehörige Themen](#related-topics)

## <a name="ifiledialog-ifileopendialog-and-ifilesavedialog"></a>IFileDialog, IFileOpenDialog und IFileSaveDialog

Windows Vista stellt Implementierungen der Dialogfelder **Öffnen** und **Speichern** bereit: CLSID \_ FileOpenDialog und CLSID \_ FileSaveDialog. Diese Dialogfelder werden hier angezeigt.

![Screenshot des geöffneten Dialogfelds](images/cid/openfiledialog.png)

![Screenshot des Dialogfelds "Speichern unter"](images/cid/savefiledialog.png)

[**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) und [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog) erben von [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) und teilen einen großen Teil ihrer Funktionalität. Darüber hinaus unterstützt das **Dialogfeld Öffnen** **IFileOpenDialog** und das **Dialogfeld** Speichern **IFileSaveDialog**.

Die Common Item Dialog-Implementierung in Windows Vista bietet mehrere Vorteile gegenüber der Implementierung, die in früheren Versionen bereitgestellt wurde:

-   Unterstützt die direkte Verwendung des Shell-Namespace über [**IShellItem anstelle**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) von Dateisystempfaden.
-   Ermöglicht eine einfache Anpassung des Dialogfelds, z. B. das Festlegen der Bezeichnung auf die **Schaltfläche OK,** ohne dass eine Hookprozedur erforderlich ist.
-   Unterstützt eine umfangreichere Anpassung des Dialogs durch hinzufügen einer Reihe von datengesteuerten Steuerelementen, die ohne Win32-Dialogvorlage funktionieren. Dieses Anpassungsschema gibt den aufrufenden Prozess aus dem Benutzeroberflächenlayout frei. Da alle Änderungen am Dialogentwurf dieses Datenmodell weiterhin verwenden, ist die Dialogimplementierung nicht an die spezifische aktuelle Version des Dialogs gebunden.
-   Unterstützt aufruferbenachrichtigungen über Ereignisse im Dialogfeld, z. B. Auswahländerung oder Dateitypänderung. Ermöglicht es dem aufrufenden Prozess auch, bestimmte Ereignisse im Dialog zu hooken, z. B. die Analyse.
-   Führt neue Dialogfeatures ein, z. B. das Hinzufügen von vom Aufrufer angegebenen Stellen zur **Ortsleiste.**
-   Im Dialogfeld **Speichern** können Entwickler neue Metadatenfeatures der Vista-Shell Windows nutzen.

Darüber hinaus können Entwickler die folgenden Schnittstellen implementieren:

-   [**IFileDialogEvents zum**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) Empfangen von Benachrichtigungen über Ereignisse im Dialogfeld.
-   [**IFileDialogCustomize,**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) um dem Dialogfeld Steuerelemente hinzuzufügen.
-   [**IFileDialogControlEvents,**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) um über Ereignisse in diesen hinzugefügten Steuerelementen benachrichtigt zu werden.

Das **Dialogfeld Öffnen** oder **Speichern** gibt ein [**IShellItem-**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) oder [**IShellItemArray-Objekt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray) an den aufrufenden Prozess zurück. Der Aufrufer kann dann ein einzelnes **IShellItem-Objekt** verwenden, um einen Dateisystempfad zu erhalten oder einen Stream für das Element zu öffnen, um Informationen zu lesen oder zu schreiben.

Flags und Optionen, die für die neuen Dialogmethoden verfügbar sind, ähneln den älteren **OFN-Flags** in der [**OPENFILENAME-Struktur,**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) die in [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) und [**GetSaveFileName verwendet werden.**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea) Viele davon sind identisch, mit der Ausnahme, dass sie mit einem FOS-Präfix beginnen. Die vollständige Liste finden Sie in den Themen [**IFileDialog::GetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions) und [**IFileDialog::SetOptions.**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) **Dialogfelder** **zum Öffnen** und Speichern werden standardmäßig mit den gängigsten Flags erstellt. Für  das Dialogfeld Öffnen ist dies (FOS PATHMUSTEXIST FOS FILEMUSTEXIST FOS NOCHANGEDIR), und für das Dialogfeld Speichern ist dies \_ \| \_ \| \_ (FOS  \_ OVERWRITEPROMPT \| FOS \_ NOREADONLYRETURN \| FOS \_ PATHMUSTEXIST \| FOS \_ NOCHANGEDIR).

[**IFileDialog und**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) seine Nachfolgerschnittstellen erben von und erweitern [**IModalWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow). [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) verwendet als einzigen Parameter das Handle des übergeordneten Fensters. Wenn **Show** erfolgreich zurückgegeben wird, gibt es ein gültiges Ergebnis. Wenn zurückgegeben `HRESULT_FROM_WIN32(ERROR_CANCELLED)` wird, bedeutet dies, dass der Benutzer den Dialog abgebrochen hat. Möglicherweise wird auch ein anderer Fehlercode wie **E \_ OUTOFMEMORY zurückgegeben.**

### <a name="sample-usage"></a>Beispielverwendung

Die folgenden Abschnitte zeigen Beispielcode für eine Vielzahl von Dialogaufgaben.

-   [Grundlegende Verwendung](#basic-usage)
-   [Beschränken von Ergebnissen auf Dateisystemelemente](#limiting-results-to-file-system-items)
-   [Angeben von Dateitypen für ein Dialogfeld](#specifying-file-types-for-a-dialog)
-   [Steuern des Standardordners](#controlling-the-default-folder)
-   [Hinzufügen von Elementen zur Leiste "Orte"](#adding-items-to-the-places-bar)
-   [Zustandspersistenz](#state-persistence)
-   [Multiselect-Funktionen](#multiselect-capabilities)

Den größten Teil des Beispielcodes finden Sie im Windows SDK [Common File Dialog Sample](samples-commonfiledialog.md).

### <a name="basic-usage"></a>Grundlegende Verwendung

Im folgenden Beispiel wird das Starten eines Dialogfelds **Öffnen** veranschaulicht. In diesem Beispiel ist sie auf Microsoft Word beschränkt.

> [!Note]  
> In mehreren Beispielen in diesem Thema wird die `CDialogEventHandler_CreateInstance` Hilfsfunktion verwendet, um eine Instanz der [**IFileDialogEvents-Implementierung zu**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) erstellen. Um diese Funktion in Ihrem eigenen Code zu verwenden, kopieren Sie den Quellcode für die Funktion aus dem Beispiel des Dialogfelds "Allgemeine Datei", aus dem alle Beispiele `CDialogEventHandler_CreateInstance` in diesem Thema stammen. [](samples-commonfiledialog.md)

 


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



### <a name="limiting-results-to-file-system-items"></a>Beschränken von Ergebnissen auf Dateisystemelemente

Das folgende Beispiel aus dem obigen Beispiel veranschaulicht, wie Ergebnisse auf Dateisystemelemente beschränkt werden. Beachten [**Sie, dass IFileDialog::SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) das neue Flag zu einem Wert hinzufügt, der über [**IFileDialog::GetOptions ermittelt wurde.**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions) Dies ist die empfohlene Methode.


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



### <a name="specifying-file-types-for-a-dialog"></a>Angeben von Dateitypen für ein Dialogfeld

Verwenden Sie die [**IFileDialog::SetFileTypes-Methode,**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfiletypes) um bestimmte Dateitypen zu festlegen, die vom Dialogfeld verarbeitet werden können. Diese Methode akzeptiert ein Array von [**COMDLG \_ FILTERSPEC-Strukturen,**](/windows/desktop/api/Shtypes/ns-shtypes-comdlg_filterspec) von denen jede einen Dateityp darstellt.

Der Standarderweiterungsmechanismus in einem Dialogfeld wird nicht von [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) und [**GetSaveFileName geändert.**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea) Die Dateierweiterung, die an den Text angefügt wird, den der Benutzer im Bearbeitungsfeld für Dateinamen ein gibt, wird initialisiert, wenn das Dialogfeld geöffnet wird. Er sollte mit dem Standarddateityp übereinstimmen (der ausgewählt wird, wenn das Dialogfeld geöffnet wird). Wenn der Standarddateityp "" \* \* ist. (alle Dateien), kann die Datei eine Erweiterung Ihrer Wahl sein. Wenn der Benutzer einen anderen Dateityp auswählt, wird die Erweiterung automatisch auf die erste Dateierweiterung aktualisiert, die diesem Dateityp zugeordnet ist. Wenn der Benutzer "" \* \* auswählt. (alle Dateien), dann wird die Erweiterung auf ihren ursprünglichen Wert zurückverwendet.

Im folgenden Beispiel wird veranschaulicht, wie dies oben erfolgt ist.


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



### <a name="controlling-the-default-folder"></a>Steuern des Standardordners

Fast jeder Ordner im Shellnamespace kann als Standardordner für das Dialogfeld verwendet werden (der Ordner, der angezeigt wird, wenn der Benutzer eine Datei öffnet oder speichern soll). Rufen [**Sie IFileDialog::SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) auf, bevor [**Sie Show aufrufen.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show)

Der Standardordner ist der Ordner, in dem das Dialogfeld gestartet wird, wenn ein Benutzer ihn zum ersten Mal in Ihrer Anwendung öffnet. Danach wird das Dialogfeld im letzten Ordner geöffnet, den ein Benutzer geöffnet hat, oder im letzten Ordner, den er zum Speichern eines Elements verwendet hat. Weitere [Informationen finden Sie unter Zustandspersistenz.](#state-persistence)

Sie können erzwingen, dass das Dialogfeld beim Öffnen immer denselben Ordner zeigt, unabhängig von der vorherigen Benutzeraktion, indem Sie [**IFileDialog::SetFolder aufrufen.**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfolder) Es wird jedoch davon abraten, dies zu tun. Wenn Sie **SetFolder aufrufen,** bevor Sie das Dialogfeld anzeigen, wird der letzte Speicherort, an dem der Benutzer gespeichert oder geöffnet hat, nicht angezeigt. Sofern es keinen sehr spezifischen Grund für dieses Verhalten gibt, ist es keine gute oder erwartete Benutzererfahrung und sollte vermieden werden. In fast allen Instanzen ist [**IFileDialog::SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) die bessere Methode.

Wenn Sie ein Dokument zum  ersten Mal im Dialogfeld Speichern speichern, sollten Sie die gleichen Richtlinien befolgen, um den anfänglichen Ordner wie im **Dialogfeld Öffnen zu** bestimmen. Wenn der Benutzer ein zuvor vorhandenes Dokument bearbeitet, öffnen Sie das Dialogfeld in dem Ordner, in dem das Dokument gespeichert ist, und füllen Sie das Bearbeitungsfeld mit dem Namen dieses Dokuments auf. Rufen [**Sie IFileSaveDialog::SetSaveAsItem**](/windows/desktop/api/Shobjidl_core/nf-shobjidl_core-ifilesavedialog-setsaveasitem) mit dem aktuellen Element auf, bevor Sie [**Show aufrufen.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show)

### <a name="adding-items-to-the-places-bar"></a>Hinzufügen von Elementen zur Leiste "Orte"

Im folgenden Beispiel wird das Addition von Elementen zur Leiste **Orte** veranschaulicht:


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



### <a name="state-persistence"></a>Zustandspersistenz

Vor Windows Vista wurde ein Zustand, z. B. der zuletzt besuchten Ordner, pro Prozess gespeichert. Diese Informationen wurden jedoch unabhängig von der jeweiligen Aktion verwendet. Beispielsweise würde eine Videobearbeitungsanwendung im Dialogfeld **Rendern unter** den gleichen Ordner wie im Dialogfeld **Medien importieren** anzeigen. In Windows Vista können Sie durch die Verwendung von GUIDs spezifischer sein. Um dem Dialogfeld eine **GUID** zuzuweisen, rufen [**Sie iFileDialog::SetClientGuid auf.**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setclientguid)

### <a name="multiselect-capabilities"></a>Multiselect-Funktionen

Die Multiselect-Funktionalität ist im Dialogfeld **Öffnen** mithilfe der [**GetResults-Methode**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) verfügbar, wie hier gezeigt.


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



## <a name="listening-to-events-from-the-dialog"></a>Lauschen auf Ereignisse über das Dialogfeld

Ein aufrufende Prozess kann eine [**IFileDialogEvents-Schnittstelle**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) mithilfe der Methoden [**IFileDialog::Advise**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-advise) und [**IFileDialog::Unadvise**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-unadvise) wie hier gezeigt beim Dialog registrieren.

Dies stammt aus dem Beispiel ["Grundlegende Verwendung".](#basic-usage)


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



Der Großteil der Dialogverarbeitung würde hier platziert werden.


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



Der aufrufende Prozess kann Ereignisse für Benachrichtigungen verwenden, wenn der Benutzer den Ordner, den Dateityp oder die Auswahl ändert. Diese Ereignisse sind besonders nützlich, wenn der aufrufende Prozess dem Dialog Steuerelemente hinzugefügt hat (siehe [Anpassen des Dialogs)](#customizing-the-dialog)und den Zustand dieser Steuerelemente als Reaktion auf diese Ereignisse ändern muss. In allen Fällen ist die Fähigkeit des aufrufenden Prozesses nützlich, benutzerdefinierten Code bereitzustellen, um mit Situationen wie der Freigabe von Verstößen, dem Überschreiben von Dateien oder dem Bestimmen der Gültigkeit einer Datei vor dem Schließen des Dialogs umzugehen. Einige dieser Fälle werden in diesem Abschnitt beschrieben.

### <a name="onfileok"></a>Onfileok

Diese Methode wird aufgerufen, nachdem der Benutzer ein Element ausgewählt hat, kurz bevor das Dialogfeld geschlossen wird. Die Anwendung kann dann [**IFileDialog::GetResult**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) oder [**IFileOpenDialog::GetResults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) aufrufen, wie dies nach dem Schließen des Dialogs der Fall wäre. Wenn das ausgewählte Element akzeptabel ist, kann es S \_ OK zurückgeben. Andernfalls geben sie S \_ FALSE zurück und zeigen eine Benutzeroberfläche an, die dem Benutzer mitgibt, warum das ausgewählte Element ungültig ist. Wenn S \_ FALSE zurückgegeben wird, wird das Dialogfeld nicht geschlossen.

Der aufrufende Prozess kann das Fensterhandle des Dialogs selbst als übergeordnetes Element der Benutzeroberfläche verwenden. Dieses Handle kann abgerufen werden, indem zuerst [**IOleWindow::QueryInterface**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) und dann [**IOleWindow::GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) mit dem Handle aufgerufen wird, wie in diesem Beispiel gezeigt.


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



### <a name="onshareviolation-and-onoverwrite"></a>OnShareViolation und OnOverwrite

Wenn der Benutzer sich entscheidet, eine Datei im Dialogfeld **Speichern** zu überschreiben, oder wenn eine gespeicherte oder ersetzte Datei verwendet wird und nicht in geschrieben werden kann (eine Freigabeverletzung), kann die Anwendung benutzerdefinierte Funktionen bereitstellen, um das Standardverhalten des Dialogs zu überschreiben. Standardmäßig zeigt das Dialogfeld beim Überschreiben einer Datei eine Eingabeaufforderung an, mit der der Benutzer diese Aktion überprüfen kann. Bei Freigabeverletzungen zeigt das Dialogfeld standardmäßig eine Fehlermeldung an, die nicht geschlossen wird, und der Benutzer muss eine andere Auswahl treffen. Der aufrufende Prozess kann diese Standardwerte überschreiben und bei Bedarf eine eigene Benutzeroberfläche anzeigen. Das Dialogfeld kann angewiesen werden, die Datei abzulehnen und geöffnet zu bleiben oder die Datei zu akzeptieren und erfolgreich zu schließen.

## <a name="customizing-the-dialog"></a>Anpassen des Dialogfelds

Dem Dialogfeld kann eine Vielzahl von Steuerelementen hinzugefügt werden, ohne eine Win32-Dialogfeldvorlage bereitstellen zu müssen. Zu diesen Steuerelementen gehören PushButton-, ComboBox-, EditBox-, CheckButton-, RadioButton-Listen, Gruppen, Trennzeichen und statische Textsteuerelemente. Rufen Sie **QueryInterface** für das Dialogobjekt ([**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog), [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog)oder [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog)) auf, um einen [**IFileDialogCustomize-Zeiger**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) abzurufen. Verwenden Sie diese Schnittstelle, um Steuerelemente hinzuzufügen. Jedes Steuerelement verfügt über eine vom Aufrufer bereitgestellte ID sowie einen *sichtbaren* und *aktivierten* Zustand, der vom aufrufenden Prozess festgelegt werden kann. Einigen Steuerelementen, z. B. PushButton, ist auch Text zugeordnet.

Mehrere Steuerelemente können einer "visuellen Gruppe" hinzugefügt werden, die als einzelne Einheit im Layout des Dialogfelds verschoben wird. Gruppen kann eine Bezeichnung zugeordnet sein.

Steuerelemente können nur hinzugefügt werden, bevor das Dialogfeld angezeigt wird. Sobald das Dialogfeld angezeigt wird, können Steuerelemente jedoch ausgeblendet oder wie gewünscht angezeigt werden, möglicherweise als Reaktion auf eine Benutzeraktion. In den folgenden Beispielen wird veranschaulicht, wie dem Dialogfeld eine Optionsfeldliste hinzugefügt wird.


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

Auf ähnliche Weise können optionen zu den Schaltflächen **Öffnen** oder **Speichern** hinzugefügt werden. Dies ist die Schaltfläche **OK** für die jeweiligen Dialogtypen. Auf die Optionen kann über ein Dropdownlistenfeld zugegriffen werden, das an die Schaltfläche angefügt ist. Das erste Element in der Liste wird zum Text für die Schaltfläche. Das folgende Beispiel zeigt, wie Sie eine Schaltfläche **Öffnen** mit zwei Möglichkeiten bereitstellen: "Öffnen" und "Als schreibgeschützt öffnen".


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





Die Auswahl des Benutzers kann überprüft werden, nachdem der Dialog von der [**Show-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) wie bei einem ComboBox-Objekt zurückgegeben wurde, oder sie kann im Rahmen der Verarbeitung durch [**IFileDialogEvents::OnFileOk**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onfileok)überprüft werden.

### <a name="responding-to-events-in-added-controls"></a>Reagieren auf Ereignisse in hinzugefügten Steuerelementen

Der vom aufrufenden Prozess bereitgestellte Ereignishandler kann zusätzlich zu [**IFileDialogEvents IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) implementieren. [](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) **IFileDialogControlEvents** ermöglicht dem aufrufenden Prozess, auf diese Ereignisse zu reagieren:

-   Klick auf PushButton
-   CheckButton-Status geändert
-   Ausgewähltes Element in einer Menü-, ComboBox- oder RadioButton-Liste
-   Steuerungsaktivierung. Dies wird gesendet, wenn in einem Menü eine Dropdownliste angezeigt wird, falls der aufrufende Prozess die Elemente in der Liste ändern möchte.

## <a name="full-samples"></a>Vollständige Beispiele

Im Folgenden finden Sie vollständige, herunterladbare C++-Beispiele aus dem Windows Software Development Kit (SDK), die die Verwendung von und die Interaktion mit dem Dialogfeld "Allgemeine Elemente" veranschaulichen.

-   [Dialogfeld „Gemeinsame Dateien“ (Beispiel)](samples-commonfiledialog.md)
-   [Modi des Dialogfelds „Gemeinsame Dateien“ (Beispiel)](samples-commonfiledialogmodes.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IID \_ PPV \_ ARGS**](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 
