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
# <a name="common-item-dialog"></a><span data-ttu-id="0537d-103">Dialog Feld für allgemeine Elemente</span><span class="sxs-lookup"><span data-stu-id="0537d-103">Common Item Dialog</span></span>

<span data-ttu-id="0537d-104">Ab Windows Vista ersetzt das allgemeine Element Dialogfeld das ältere allgemeine Datei Dialogfeld, wenn es verwendet wird, um eine Datei zu öffnen oder zu speichern.</span><span class="sxs-lookup"><span data-stu-id="0537d-104">Starting with Windows Vista, the Common Item Dialog supersedes the older Common File Dialog when used to open or save a file.</span></span> <span data-ttu-id="0537d-105">Das Dialogfeld für allgemeine Elemente wird in zwei Variationen verwendet: dem Dialogfeld **Öffnen** und dem Dialogfeld **Speichern** .</span><span class="sxs-lookup"><span data-stu-id="0537d-105">The Common Item Dialog is used in two variations: the **Open** dialog and the **Save** dialog.</span></span> <span data-ttu-id="0537d-106">In diesen beiden Dialogfeldern wird der größte Teil ihrer Funktionalität genutzt, aber jede verfügt über eigene eindeutige Methoden.</span><span class="sxs-lookup"><span data-stu-id="0537d-106">These two dialogs share most of their functionality, but each has its own unique methods.</span></span>

<span data-ttu-id="0537d-107">Diese neuere Version heißt das allgemeine Element Dialogfeld, wird jedoch in der meisten Dokumentation weiterhin als gemeinsames Datei Dialogfeld bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="0537d-107">While this newer version is named the Common Item Dialog, it continues to be called the Common File Dialog in most documentation.</span></span> <span data-ttu-id="0537d-108">Wenn Sie nicht speziell mit einer älteren Version von Windows arbeiten, sollten Sie davon ausgehen, dass sich jede beliebige Angabe des allgemeinen Datei Dialogfelds auf dieses allgemeine Element Dialogfeld bezieht.</span><span class="sxs-lookup"><span data-stu-id="0537d-108">Unless you are dealing specifically with an older version of Windows, you should assume that any mention of the Common File Dialog refers to this Common Item Dialog.</span></span>

<span data-ttu-id="0537d-109">Die folgenden Themen werden hier behandelt:</span><span class="sxs-lookup"><span data-stu-id="0537d-109">The following topics are discussed here:</span></span>

-   [<span data-ttu-id="0537d-110">Ifiledialog, IFileOpenDialog und IFileSaveDialog</span><span class="sxs-lookup"><span data-stu-id="0537d-110">IFileDialog, IFileOpenDialog, and IFileSaveDialog</span></span>](#ifiledialog-ifileopendialog-and-ifilesavedialog)
    -   [<span data-ttu-id="0537d-111">Beispiel Verwendung</span><span class="sxs-lookup"><span data-stu-id="0537d-111">Sample Usage</span></span>](#sample-usage)
-   [<span data-ttu-id="0537d-112">Lauschen auf Ereignisse aus dem Dialog Feld</span><span class="sxs-lookup"><span data-stu-id="0537d-112">Listening to Events from the Dialog</span></span>](#listening-to-events-from-the-dialog)
    -   [<span data-ttu-id="0537d-113">OnFileOk</span><span class="sxs-lookup"><span data-stu-id="0537d-113">OnFileOk</span></span>](#onfileok)
    -   [<span data-ttu-id="0537d-114">Onshareverletzungs und onüberschreibung</span><span class="sxs-lookup"><span data-stu-id="0537d-114">OnShareViolation and OnOverwrite</span></span>](#onshareviolation-and-onoverwrite)
-   [<span data-ttu-id="0537d-115">Anpassen des Dialog Felds</span><span class="sxs-lookup"><span data-stu-id="0537d-115">Customizing the Dialog</span></span>](#customizing-the-dialog)
    -   [<span data-ttu-id="0537d-116">Hinzufügen von Optionen zur Schaltfläche "OK"</span><span class="sxs-lookup"><span data-stu-id="0537d-116">Adding Options to the OK Button</span></span>](#adding-options-to-the-ok-button)
    -   [<span data-ttu-id="0537d-117">Reagieren auf Ereignisse in hinzugefügten Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="0537d-117">Responding to Events in Added Controls</span></span>](#responding-to-events-in-added-controls)
-   [<span data-ttu-id="0537d-118">Vollständige Beispiele</span><span class="sxs-lookup"><span data-stu-id="0537d-118">Full Samples</span></span>](#full-samples)
-   [<span data-ttu-id="0537d-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0537d-119">Related topics</span></span>](#related-topics)

## <a name="ifiledialog-ifileopendialog-and-ifilesavedialog"></a><span data-ttu-id="0537d-120">Ifiledialog, IFileOpenDialog und IFileSaveDialog</span><span class="sxs-lookup"><span data-stu-id="0537d-120">IFileDialog, IFileOpenDialog, and IFileSaveDialog</span></span>

<span data-ttu-id="0537d-121">Windows Vista stellt Implementierungen der Dialogfelder zum **Öffnen** und **Speichern** bereit: CLSID \_ fileopendialog und CLSID \_ filesavedialog.</span><span class="sxs-lookup"><span data-stu-id="0537d-121">Windows Vista provides implementations of the **Open** and **Save** dialogs: CLSID\_FileOpenDialog and CLSID\_FileSaveDialog.</span></span> <span data-ttu-id="0537d-122">Diese Dialogfelder werden hier angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0537d-122">Those dialog boxes are shown here.</span></span>

![Screenshot des Dialog Felds "Öffnen"](images/cid/openfiledialog.png)

![Screenshot des Dialog Felds "Speichern unter"](images/cid/savefiledialog.png)

<span data-ttu-id="0537d-125">[**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) und [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog) erben von [**ifiledialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) und teilen viele ihrer Funktionen.</span><span class="sxs-lookup"><span data-stu-id="0537d-125">[**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) and [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog) inherit from [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) and share much of their functionality.</span></span> <span data-ttu-id="0537d-126">Außerdem unterstützt das  Dialogfeld Öffnen **IFileOpenDialog**, und das Dialogfeld **Speichern** unterstützt **IFileSaveDialog**.</span><span class="sxs-lookup"><span data-stu-id="0537d-126">In addition, the **Open** dialog supports **IFileOpenDialog**, and the **Save** dialog supports **IFileSaveDialog**.</span></span>

<span data-ttu-id="0537d-127">Die Implementierung der allgemeinen Element Dialogfelder in Windows Vista bietet gegenüber der in früheren Versionen bereitgestellten Implementierung verschiedene Vorteile:</span><span class="sxs-lookup"><span data-stu-id="0537d-127">The Common Item Dialog implementation found in Windows Vista provides several advantages over the implementation provided in earlier versions:</span></span>

-   <span data-ttu-id="0537d-128">Unterstützt die direkte Verwendung des Shell-Namespace über [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) anstelle der Verwendung von Dateisystem Pfaden.</span><span class="sxs-lookup"><span data-stu-id="0537d-128">Supports direct use of the Shell namespace through [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) instead of using file system paths.</span></span>
-   <span data-ttu-id="0537d-129">Ermöglicht die einfache Anpassung des Dialog Felds, z. b. das Festlegen der Bezeichnung auf der Schaltfläche **OK** , ohne dass eine Hook-Prozedur erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="0537d-129">Enables simple customization of the dialog, such as setting the label on the **OK** button, without requiring a hook procedure.</span></span>
-   <span data-ttu-id="0537d-130">Unterstützt eine umfangreichere Anpassung des Dialog Felds durch das Hinzufügen eines Satzes von datengesteuerten Steuerelementen, die ohne eine Win32-Dialogfeld Vorlage ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0537d-130">Supports more extensive customization of the dialog by the addition of a set of data-driven controls that operate without a Win32 dialog template.</span></span> <span data-ttu-id="0537d-131">Dieses Anpassungs Schema gibt den aufrufenden Prozess aus dem Benutzeroberflächen Layout frei.</span><span class="sxs-lookup"><span data-stu-id="0537d-131">This customization scheme frees the calling process from UI layout.</span></span> <span data-ttu-id="0537d-132">Da Änderungen am Dialogfeld Entwurf weiterhin dieses Datenmodell verwenden, ist die Dialog-Implementierung nicht an die jeweilige aktuelle Version des Dialog Felds gebunden.</span><span class="sxs-lookup"><span data-stu-id="0537d-132">Since any changes to the dialog design continue to use this data model, the dialog implementation is not tied to the specific current version of the dialog.</span></span>
-   <span data-ttu-id="0537d-133">Unterstützt die aufruferbenachrichtigung über Ereignisse im Dialogfeld, z. b. Auswahl Änderungen oder Dateityp Änderungen.</span><span class="sxs-lookup"><span data-stu-id="0537d-133">Supports caller notification of events within the dialog, such as selection change or file type change.</span></span> <span data-ttu-id="0537d-134">Ermöglicht es dem aufrufenden Prozess außerdem, bestimmte Ereignisse im Dialogfeld zu verbinden, z. b. die-Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="0537d-134">Also enables the calling process to hook certain events in the dialog, such as the parsing.</span></span>
-   <span data-ttu-id="0537d-135">Führt neue Dialogfeld Funktionen ein, z. b. das Hinzufügen von vom Aufrufer **angegebenen Stellen zur** Leiste</span><span class="sxs-lookup"><span data-stu-id="0537d-135">Introduces new dialog features such as adding caller-specified places to the **Places** bar.</span></span>
-   <span data-ttu-id="0537d-136">Im Dialogfeld **Speichern** können Entwickler die neuen Metadatenfeatures der Windows Vista-Shell nutzen.</span><span class="sxs-lookup"><span data-stu-id="0537d-136">In the **Save** dialog, developers can take advantage of new metadata features of the Windows Vista Shell.</span></span>

<span data-ttu-id="0537d-137">Außerdem können Entwickler die folgenden Schnittstellen implementieren:</span><span class="sxs-lookup"><span data-stu-id="0537d-137">Additionally, developers can choose to implement the following interfaces:</span></span>

-   <span data-ttu-id="0537d-138">[**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) zum Empfangen von Benachrichtigungen über Ereignisse innerhalb des Dialog Felds.</span><span class="sxs-lookup"><span data-stu-id="0537d-138">[**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) to receive notifications of events within the dialog.</span></span>
-   <span data-ttu-id="0537d-139">[**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) zum Hinzufügen von Steuerelementen zum Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="0537d-139">[**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) to add controls to the dialog.</span></span>
-   <span data-ttu-id="0537d-140">[**Ifiledialogcontrolevents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) , um über Ereignisse in diesen hinzugefügten Steuerelementen benachrichtigt zu werden.</span><span class="sxs-lookup"><span data-stu-id="0537d-140">[**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) to be notified of events in those added controls.</span></span>

<span data-ttu-id="0537d-141">Im Dialogfeld zum **Öffnen** oder **Speichern** wird ein [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) -oder [**ishellitemarray**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray) -Objekt an den aufrufenden Prozess zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0537d-141">The **Open** or **Save** dialog returns an [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) or [**IShellItemArray**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray) object to the calling process.</span></span> <span data-ttu-id="0537d-142">Der Aufrufer kann dann ein einzelnes **IShellItem** -Objekt verwenden, um einen Dateisystempfad abzurufen oder einen Stream für das Element zu öffnen, um Informationen zu lesen oder zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="0537d-142">The caller can then use an individual **IShellItem** object to get a file system path or to open a stream on the item to read or write information.</span></span>

<span data-ttu-id="0537d-143">Flags und Optionen, die für die neuen Dialogmethoden verfügbar sind, ähneln den älteren **ofn** -Flags, die in der [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) -Struktur gefunden werden und in [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) und [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0537d-143">Flags and options available to the new dialog methods are very similar to the older **OFN** flags found in the [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure and used in [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) and [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea).</span></span> <span data-ttu-id="0537d-144">Viele von Ihnen sind identisch, mit der Ausnahme, dass Sie mit einem Fos-Präfix beginnen.</span><span class="sxs-lookup"><span data-stu-id="0537d-144">Many of them are exactly the same, except that they begin with an FOS prefix.</span></span> <span data-ttu-id="0537d-145">Die komplette Liste finden Sie in den Themen [**ifiledialog:: GetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions) und [**ifiledialog:: slitoptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) .</span><span class="sxs-lookup"><span data-stu-id="0537d-145">The complete list can be found in the [**IFileDialog::GetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions) and [**IFileDialog::SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) topics.</span></span> <span data-ttu-id="0537d-146">Dialogfelder zum **Öffnen** und **Speichern** werden standardmäßig mit den gängigsten Flags erstellt.</span><span class="sxs-lookup"><span data-stu-id="0537d-146">**Open** and **Save** dialogs are created by default with the most common flags.</span></span> <span data-ttu-id="0537d-147">Für das Dialogfeld " **Öffnen** " ist dies (z. b. "Fos \_ pathmustexist; \| \_ filemustexist \| Fos \_ nochangedir"), und für das Dialogfeld " **Speichern** " ist dies ("Fos \_ overwrite-prompt \| Fos \_ noreadonlyreturn \| Fos \_ pathmustexist Fos \| \_ nochangedir)"</span><span class="sxs-lookup"><span data-stu-id="0537d-147">For the **Open** dialog, this is (FOS\_PATHMUSTEXIST \| FOS\_FILEMUSTEXIST \| FOS\_NOCHANGEDIR) and for the **Save** dialog this is (FOS\_OVERWRITEPROMPT \| FOS\_NOREADONLYRETURN \| FOS\_PATHMUSTEXIST \| FOS\_NOCHANGEDIR).</span></span>

<span data-ttu-id="0537d-148">[**Ifiledialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) und die untergeordneten Schnittstellen erben von und erweitern [**imodalwindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow).</span><span class="sxs-lookup"><span data-stu-id="0537d-148">[**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) and its descendant interfaces inherit from and extend [**IModalWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow).</span></span> <span data-ttu-id="0537d-149">[**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) nimmt als einzigen Parameter das Handle des übergeordneten Fensters an.</span><span class="sxs-lookup"><span data-stu-id="0537d-149">[**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) takes as its only parameter the handle of the parent window.</span></span> <span data-ttu-id="0537d-150">Wenn **anzeigen** erfolgreich zurückgegeben wurde, ist ein gültiges Ergebnis vorhanden.</span><span class="sxs-lookup"><span data-stu-id="0537d-150">If **Show** returns successfully, there is a valid result.</span></span> <span data-ttu-id="0537d-151">Wenn Sie zurückgibt `HRESULT_FROM_WIN32(ERROR_CANCELLED)` , bedeutet dies, dass der Benutzer das Dialogfeld abgebrochen hat.</span><span class="sxs-lookup"><span data-stu-id="0537d-151">If it returns `HRESULT_FROM_WIN32(ERROR_CANCELLED)`, it means the user canceled the dialog.</span></span> <span data-ttu-id="0537d-152">Möglicherweise wird auch ein anderer Fehlercode wie z. b. " **E \_ outo-Memory**" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0537d-152">It might also legitimately return another error code such as **E\_OUTOFMEMORY**.</span></span>

### <a name="sample-usage"></a><span data-ttu-id="0537d-153">Beispielverwendung</span><span class="sxs-lookup"><span data-stu-id="0537d-153">Sample Usage</span></span>

<span data-ttu-id="0537d-154">In den folgenden Abschnitten wird Beispielcode für eine Vielzahl von Dialog Aufgaben veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="0537d-154">The following sections show example code for a variety of dialog tasks.</span></span>

-   [<span data-ttu-id="0537d-155">Grundlegende Verwendung</span><span class="sxs-lookup"><span data-stu-id="0537d-155">Basic Usage</span></span>](#basic-usage)
-   [<span data-ttu-id="0537d-156">Einschränken der Ergebnisse auf Datei System Elemente</span><span class="sxs-lookup"><span data-stu-id="0537d-156">Limiting Results to File System Items</span></span>](#limiting-results-to-file-system-items)
-   [<span data-ttu-id="0537d-157">Angeben von Dateitypen für ein Dialog Feld</span><span class="sxs-lookup"><span data-stu-id="0537d-157">Specifying File Types for a Dialog</span></span>](#specifying-file-types-for-a-dialog)
-   [<span data-ttu-id="0537d-158">Steuern des Standard Ordners</span><span class="sxs-lookup"><span data-stu-id="0537d-158">Controlling the Default Folder</span></span>](#controlling-the-default-folder)
-   [<span data-ttu-id="0537d-159">Hinzufügen von Elementen zur Leiste "Plätze"</span><span class="sxs-lookup"><span data-stu-id="0537d-159">Adding Items to the Places Bar</span></span>](#adding-items-to-the-places-bar)
-   [<span data-ttu-id="0537d-160">Zustands Persistenz</span><span class="sxs-lookup"><span data-stu-id="0537d-160">State Persistence</span></span>](#state-persistence)
-   [<span data-ttu-id="0537d-161">MultiSelect-Funktionen</span><span class="sxs-lookup"><span data-stu-id="0537d-161">Multiselect Capabilities</span></span>](#multiselect-capabilities)

<span data-ttu-id="0537d-162">Den größten Teil des Beispielcodes finden Sie im Beispiel zum Windows SDK [allgemeinen Datei Dialogfeld](samples-commonfiledialog.md).</span><span class="sxs-lookup"><span data-stu-id="0537d-162">Most of the sample code can be found in the Windows SDK [Common File Dialog Sample](samples-commonfiledialog.md).</span></span>

### <a name="basic-usage"></a><span data-ttu-id="0537d-163">Grundlegende Verwendung</span><span class="sxs-lookup"><span data-stu-id="0537d-163">Basic Usage</span></span>

<span data-ttu-id="0537d-164">Im folgenden Beispiel wird veranschaulicht, wie ein Dialogfeld **Öffnen** gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="0537d-164">The following example illustrates how to launch an **Open** dialog.</span></span> <span data-ttu-id="0537d-165">In diesem Beispiel ist es auf Microsoft Word-Dokumente beschränkt.</span><span class="sxs-lookup"><span data-stu-id="0537d-165">In this example, it is restricted to Microsoft Word documents.</span></span>

> [!Note]  
> <span data-ttu-id="0537d-166">In mehreren Beispielen in diesem Thema wird die- `CDialogEventHandler_CreateInstance` Hilfsfunktion zum Erstellen einer Instanz der [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) -Implementierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="0537d-166">Several examples in this topic use the `CDialogEventHandler_CreateInstance` helper function to create an instance of the [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) implementation.</span></span> <span data-ttu-id="0537d-167">Wenn Sie diese Funktion in Ihrem eigenen Code verwenden möchten, kopieren Sie den Quellcode für die `CDialogEventHandler_CreateInstance` Funktion aus dem [Beispiel "Common File Dialog](samples-commonfiledialog.md)", aus dem alle Beispiele in diesem Thema entnommen werden.</span><span class="sxs-lookup"><span data-stu-id="0537d-167">To use this function in your own code, copy the source code for the `CDialogEventHandler_CreateInstance` function from the [Common File Dialog Sample](samples-commonfiledialog.md), from which all of the examples in this topic are taken.</span></span>

 


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



### <a name="limiting-results-to-file-system-items"></a><span data-ttu-id="0537d-168">Einschränken der Ergebnisse auf Datei System Elemente</span><span class="sxs-lookup"><span data-stu-id="0537d-168">Limiting Results to File System Items</span></span>

<span data-ttu-id="0537d-169">Im folgenden Beispiel wird veranschaulicht, wie die Ergebnisse auf Dateisystem Elemente beschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="0537d-169">The following example, taken from above, demonstrates how to restrict results to file system items.</span></span> <span data-ttu-id="0537d-170">Beachten Sie, dass [**ifiledialog:: SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) das neue Flag einem Wert hinzufügt, der über [**ifiledialog:: GetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions)abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="0537d-170">Note that [**IFileDialog::SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) adds the new flag to a value obtained through [**IFileDialog::GetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions).</span></span> <span data-ttu-id="0537d-171">Dies ist die empfohlene Methode.</span><span class="sxs-lookup"><span data-stu-id="0537d-171">This is the recommended method.</span></span>


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



### <a name="specifying-file-types-for-a-dialog"></a><span data-ttu-id="0537d-172">Angeben von Dateitypen für ein Dialog Feld</span><span class="sxs-lookup"><span data-stu-id="0537d-172">Specifying File Types for a Dialog</span></span>

<span data-ttu-id="0537d-173">Um bestimmte Dateitypen festzulegen, die vom Dialog behandelt werden können, verwenden Sie die [**ifiledialog:: SetFileTypes**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfiletypes) -Methode.</span><span class="sxs-lookup"><span data-stu-id="0537d-173">To set specific file types that the dialog can handle, use the [**IFileDialog::SetFileTypes**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfiletypes) method.</span></span> <span data-ttu-id="0537d-174">Diese Methode akzeptiert ein Array von [**comdlg \_ FILTERSPEC**](/windows/desktop/api/Shtypes/ns-shtypes-comdlg_filterspec) -Strukturen, von denen jedes einen Dateityp darstellt.</span><span class="sxs-lookup"><span data-stu-id="0537d-174">That method accepts an array of [**COMDLG\_FILTERSPEC**](/windows/desktop/api/Shtypes/ns-shtypes-comdlg_filterspec) structures, each of which represents a file type.</span></span>

<span data-ttu-id="0537d-175">Der Standard Erweiterungsmechanismus in einem Dialogfeld ändert sich nicht von [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) und [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea).</span><span class="sxs-lookup"><span data-stu-id="0537d-175">The default extension mechanism in a dialog is unchanged from [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) and [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea).</span></span> <span data-ttu-id="0537d-176">Die Dateinamenerweiterung, die an den Text angehängt wird, den der Benutzer in das Bearbeitungsfeld Dateiname eingibt, wird beim Öffnen des Dialog Felds initialisiert.</span><span class="sxs-lookup"><span data-stu-id="0537d-176">The file name extension that is appended to the text the user types in the file name edit box is initialized when the dialog opens.</span></span> <span data-ttu-id="0537d-177">Er sollte dem Standard Dateityp entsprechen (der beim Öffnen des Dialog Felds ausgewählt wird).</span><span class="sxs-lookup"><span data-stu-id="0537d-177">It should match the default file type (that selected as the dialog opens).</span></span> <span data-ttu-id="0537d-178">Wenn der Standard Dateityp " \* . \* " lautet. (alle Dateien), kann die Datei eine Erweiterung Ihrer Wahl sein.</span><span class="sxs-lookup"><span data-stu-id="0537d-178">If the default file type is "\*.\*" (all files), the file can be an extension of your choice.</span></span> <span data-ttu-id="0537d-179">Wenn der Benutzer einen anderen Dateityp auswählt, wird die Erweiterung automatisch auf die erste Dateinamenerweiterung aktualisiert, die diesem Dateityp zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0537d-179">If the user chooses a different file type, the extension automatically updates to the first file name extension associated with that file type.</span></span> <span data-ttu-id="0537d-180">Wenn der Benutzer "." auswählt \* . \* (alle Dateien), dann wird die Erweiterung auf den ursprünglichen Wert zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="0537d-180">If the user chooses "\*.\*" (all files), then the extension reverts to its original value.</span></span>

<span data-ttu-id="0537d-181">Im folgenden Beispiel wird veranschaulicht, wie dies oben geschehen ist.</span><span class="sxs-lookup"><span data-stu-id="0537d-181">The following example illustrates how this was done above.</span></span>


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



### <a name="controlling-the-default-folder"></a><span data-ttu-id="0537d-182">Steuern des Standard Ordners</span><span class="sxs-lookup"><span data-stu-id="0537d-182">Controlling the Default Folder</span></span>

<span data-ttu-id="0537d-183">Fast jeder Ordner im Shell-Namespace kann als Standardordner für den Dialog verwendet werden (der Ordner, der angezeigt wird, wenn der Benutzer eine Datei öffnen oder speichern möchte).</span><span class="sxs-lookup"><span data-stu-id="0537d-183">Almost any folder in the Shell namespace can be used as the default folder for the dialog (the folder presented when the user chooses to open or save a file).</span></span> <span data-ttu-id="0537d-184">Rufen Sie [**ifiledialog:: SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) auf, bevor Sie " [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) " aufrufen, um dies zu tun.</span><span class="sxs-lookup"><span data-stu-id="0537d-184">Call [**IFileDialog::SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) prior to calling [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) to do so.</span></span>

<span data-ttu-id="0537d-185">Der Standardordner ist der Ordner, in dem das Dialogfeld gestartet wird, wenn ein Benutzer es zum ersten Mal in der Anwendung öffnet.</span><span class="sxs-lookup"><span data-stu-id="0537d-185">The default folder is the folder in which the dialog starts the first time a user opens it from your application.</span></span> <span data-ttu-id="0537d-186">Anschließend wird das Dialogfeld im letzten Ordner geöffnet, den ein Benutzer geöffnet hat, oder in dem letzten Ordner, der zum Speichern eines Elements verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="0537d-186">After that, the dialog will open in the last folder a user opened or the last folder they used to save an item.</span></span> <span data-ttu-id="0537d-187">Weitere Informationen finden Sie unter [Zustands Persistenz](#state-persistence) .</span><span class="sxs-lookup"><span data-stu-id="0537d-187">See [State Persistence](#state-persistence) for more details.</span></span>

<span data-ttu-id="0537d-188">Durch Aufrufen von [**ifiledialog:: SetFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfolder)können Sie erzwingen, dass das Dialogfeld immer den gleichen Ordner anzeigt, wenn es geöffnet wird, unabhängig von der vorherigen Benutzeraktion.</span><span class="sxs-lookup"><span data-stu-id="0537d-188">You can force the dialog to always show the same folder when it opens, regardless of previous user action, by calling [**IFileDialog::SetFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfolder).</span></span> <span data-ttu-id="0537d-189">Dies wird jedoch nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="0537d-189">However, we do not recommended doing this.</span></span> <span data-ttu-id="0537d-190">Wenn Sie **SetFolder** aufrufen, bevor Sie das Dialogfeld anzeigen, wird der letzte Speicherort, in dem der Benutzer gespeichert oder geöffnet hat, nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0537d-190">If you call **SetFolder** before you display the dialog box, the most recent location that the user saved to or opened from is not shown.</span></span> <span data-ttu-id="0537d-191">Wenn es keinen besonderen Grund für dieses Verhalten gibt, ist es keine gute oder erwartete Benutzer Darstellung und sollte vermieden werden.</span><span class="sxs-lookup"><span data-stu-id="0537d-191">Unless there is a very specific reason for this behavior, it is not a good or expected user experience and should be avoided.</span></span> <span data-ttu-id="0537d-192">In fast allen Instanzen ist [**ifiledialog:: SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) die bessere Methode.</span><span class="sxs-lookup"><span data-stu-id="0537d-192">In almost all instances, [**IFileDialog::SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) is the better method.</span></span>

<span data-ttu-id="0537d-193">Wenn Sie ein Dokument zum ersten Mal im Dialogfeld **Speichern** speichern, sollten Sie dieselben Richtlinien befolgen, um den ursprünglichen Ordner zu bestimmen, wie im Dialogfeld **Öffnen** .</span><span class="sxs-lookup"><span data-stu-id="0537d-193">When saving a document for the first time in the **Save** dialog, you should follow the same guidelines in determining the initial folder as you did in the **Open** dialog.</span></span> <span data-ttu-id="0537d-194">Wenn der Benutzer ein bereits vorhandenes Dokument bearbeitet, öffnen Sie das Dialogfeld in dem Ordner, in dem das Dokument gespeichert ist, und füllen Sie das Bearbeitungsfeld mit dem Namen des Dokuments auf.</span><span class="sxs-lookup"><span data-stu-id="0537d-194">If the user is editing a previously existing document, open the dialog in the folder where that document is stored, and populate the edit box with that document's name.</span></span> <span data-ttu-id="0537d-195">Rufen Sie [**IFileSaveDialog:: setsaveasitem**](/windows/desktop/api/Shobjidl_core/nf-shobjidl_core-ifilesavedialog-setsaveasitem) mit dem aktuellen Element vor dem Aufrufen von [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show)auf.</span><span class="sxs-lookup"><span data-stu-id="0537d-195">Call [**IFileSaveDialog::SetSaveAsItem**](/windows/desktop/api/Shobjidl_core/nf-shobjidl_core-ifilesavedialog-setsaveasitem) with the current item prior to calling [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show).</span></span>

### <a name="adding-items-to-the-places-bar"></a><span data-ttu-id="0537d-196">Hinzufügen von Elementen zur Leiste "Plätze"</span><span class="sxs-lookup"><span data-stu-id="0537d-196">Adding Items to the Places Bar</span></span>

<span data-ttu-id="0537d-197">Das folgende Beispiel veranschaulicht das Hinzufügen von Elementen zur Leiste " **Plätze** ":</span><span class="sxs-lookup"><span data-stu-id="0537d-197">The following example demonstrates the addition of items to the **Places** bar:</span></span>


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



### <a name="state-persistence"></a><span data-ttu-id="0537d-198">Zustands Persistenz</span><span class="sxs-lookup"><span data-stu-id="0537d-198">State Persistence</span></span>

<span data-ttu-id="0537d-199">Vor Windows Vista wurde ein Zustand, wie z. b. der zuletzt besuchte Ordner, pro Prozess gespeichert.</span><span class="sxs-lookup"><span data-stu-id="0537d-199">Prior to Windows Vista, a state, such as the last visited folder, was saved on a per-process basis.</span></span> <span data-ttu-id="0537d-200">Diese Informationen wurden jedoch unabhängig von der jeweiligen Aktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="0537d-200">However, that information was used regardless of the particular action.</span></span> <span data-ttu-id="0537d-201">Beispielsweise würde eine Anwendung zur Videobearbeitung denselben Ordner im Dialogfeld " **Rendering als** " enthalten, wie dies im Dialogfeld " **Medien importieren** " der Fall wäre.</span><span class="sxs-lookup"><span data-stu-id="0537d-201">For example, a video editing application would present the same folder in the **Render As** dialog as is would in the **Import Media** dialog.</span></span> <span data-ttu-id="0537d-202">In Windows Vista können Sie durch die Verwendung von GUIDs spezifischer werden.</span><span class="sxs-lookup"><span data-stu-id="0537d-202">In Windows Vista you can be more specific through the use of GUIDs.</span></span> <span data-ttu-id="0537d-203">Um dem Dialogfeld eine **GUID** zuzuweisen, nennen Sie [**ifiledialog:: setclientguid**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setclientguid).</span><span class="sxs-lookup"><span data-stu-id="0537d-203">To assign a **GUID** to the dialog, call [**iFileDialog::SetClientGuid**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setclientguid).</span></span>

### <a name="multiselect-capabilities"></a><span data-ttu-id="0537d-204">MultiSelect-Funktionen</span><span class="sxs-lookup"><span data-stu-id="0537d-204">Multiselect Capabilities</span></span>

<span data-ttu-id="0537d-205">Die MultiSelect-Funktionalität ist im Dialogfeld **Öffnen** mit der [**GetResults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) -Methode verfügbar, wie hier gezeigt.</span><span class="sxs-lookup"><span data-stu-id="0537d-205">Multiselect functionality is available in the **Open** dialog using the [**GetResults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) method as shown here.</span></span>


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



## <a name="listening-to-events-from-the-dialog"></a><span data-ttu-id="0537d-206">Lauschen auf Ereignisse aus dem Dialog Feld</span><span class="sxs-lookup"><span data-stu-id="0537d-206">Listening to Events from the Dialog</span></span>

<span data-ttu-id="0537d-207">Ein Aufruf ender Prozess kann eine [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) -Schnittstelle mit dem Dialogfeld mithilfe der Methoden [**ifiledialog:: Rat**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-advise) und [**ifiledialog:: unempfehlung**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-unadvise) registrieren, wie hier gezeigt.</span><span class="sxs-lookup"><span data-stu-id="0537d-207">A calling process can register an [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) interface with the dialog by using the [**IFileDialog::Advise**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-advise) and [**IFileDialog::Unadvise**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-unadvise) methods as shown here.</span></span>

<span data-ttu-id="0537d-208">Dies wird aus dem Beispiel " [grundlegende Verwendung](#basic-usage) " entnommen.</span><span class="sxs-lookup"><span data-stu-id="0537d-208">This is taken from the [Basic Usage](#basic-usage) sample.</span></span>


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



<span data-ttu-id="0537d-209">Der Großteil der Dialogfeld Verarbeitung würde hier eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="0537d-209">The bulk of the dialog processing would be placed here.</span></span>


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



<span data-ttu-id="0537d-210">Der Aufrufprozess kann Ereignisse für Benachrichtigungen verwenden, wenn der Benutzer den Ordner, den Dateityp oder die Auswahl ändert.</span><span class="sxs-lookup"><span data-stu-id="0537d-210">The calling process can use events for notification when the user changes the folder, file type, or selection.</span></span> <span data-ttu-id="0537d-211">Diese Ereignisse sind besonders nützlich, wenn der aufrufende Prozess dem Dialog Steuerelemente hinzugefügt hat (siehe [Anpassen des Dialog](#customizing-the-dialog)Felds) und den Zustand dieser Steuerelemente als Reaktion auf diese Ereignisse ändern müssen.</span><span class="sxs-lookup"><span data-stu-id="0537d-211">These events are particularly useful when the calling process has added controls to the dialog (see [Customizing the Dialog](#customizing-the-dialog)) and must change the state of those controls in reaction to these events.</span></span> <span data-ttu-id="0537d-212">In allen Fällen ist die Fähigkeit des aufrufenden Prozesses, benutzerdefinierten Code bereitzustellen, wie z. b. das Freigeben von Verstößen, das Überschreiben von Dateien oder das ermitteln, ob eine Datei gültig ist, bevor das Dialogfeld geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="0537d-212">Useful in all cases is the ability of the calling process to provide custom code to deal with situations such as sharing violations, overwriting files, or determining if a file is valid before the dialog closes.</span></span> <span data-ttu-id="0537d-213">Einige dieser Fälle werden in diesem Abschnitt beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0537d-213">Some of those cases are described in this section.</span></span>

### <a name="onfileok"></a><span data-ttu-id="0537d-214">OnFileOk</span><span class="sxs-lookup"><span data-stu-id="0537d-214">OnFileOk</span></span>

<span data-ttu-id="0537d-215">Diese Methode wird aufgerufen, nachdem der Benutzer ein Element auswählt hat, kurz bevor das Dialogfeld geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="0537d-215">This method is called after the user chooses an item, just before the dialog closes.</span></span> <span data-ttu-id="0537d-216">Die Anwendung kann dann [**ifiledialog:: GetResult**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) oder [**IFileOpenDialog:: GetResults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) wie folgt aufgerufen werden, nachdem das Dialogfeld geschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="0537d-216">The application can then call [**IFileDialog::GetResult**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) or [**IFileOpenDialog::GetResults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) as would be done once the dialog had closed.</span></span> <span data-ttu-id="0537d-217">Wenn das ausgewählte Element akzeptabel ist, können Sie S OK zurückgeben \_ .</span><span class="sxs-lookup"><span data-stu-id="0537d-217">If the item chosen is acceptable, they can return S\_OK.</span></span> <span data-ttu-id="0537d-218">Andernfalls geben Sie "false" zurück \_ und zeigen die Benutzeroberfläche an, die dem Benutzer mitteilt, warum das ausgewählte Element ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="0537d-218">Otherwise, they return S\_FALSE and display UI that tells the user why the chosen item is not valid.</span></span> <span data-ttu-id="0537d-219">Wenn S \_ false zurückgegeben wird, wird das Dialogfeld nicht geschlossen.</span><span class="sxs-lookup"><span data-stu-id="0537d-219">If S\_FALSE is returned, the dialog does not close.</span></span>

<span data-ttu-id="0537d-220">Der aufrufende Prozess kann das Fenster Handle des Dialog Felds selbst als übergeordnetes Element der Benutzeroberfläche verwenden.</span><span class="sxs-lookup"><span data-stu-id="0537d-220">The calling process can use the window handle of the dialog itself as the parent of the UI.</span></span> <span data-ttu-id="0537d-221">Dieses Handle kann abgerufen werden, indem Sie zuerst [**IOleWindow:: QueryInterface**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) aufrufen und dann [**IOleWindow:: GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) mit dem Handle aufrufen, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="0537d-221">That handle can be obtained by first calling [**IOleWindow::QueryInterface**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) and then calling [**IOleWindow::GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) with the handle as shown in this example.</span></span>


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



### <a name="onshareviolation-and-onoverwrite"></a><span data-ttu-id="0537d-222">Onshareverletzungs und onüberschreibung</span><span class="sxs-lookup"><span data-stu-id="0537d-222">OnShareViolation and OnOverwrite</span></span>

<span data-ttu-id="0537d-223">Wenn sich der Benutzer für das Überschreiben einer Datei im Dialogfeld " **Speichern** " entscheidet, oder wenn eine Datei verwendet wird, die gespeichert oder ersetzt wird und nicht geschrieben werden kann (eine Freigabe Verletzung), kann die Anwendung benutzerdefinierte Funktionen bereitstellen, um das Standardverhalten des Dialog Felds zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="0537d-223">If the user chooses to overwrite a file in the **Save** dialog, or if a file being saved or replaced is in use and cannot be written to (a sharing violation), the application can provide custom functionality to override the default behavior of the dialog.</span></span> <span data-ttu-id="0537d-224">Wenn eine Datei überschrieben wird, wird im Dialogfeld standardmäßig eine Eingabeaufforderung angezeigt, die dem Benutzer ermöglicht, diese Aktion zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="0537d-224">By default, when overwriting a file, the dialog displays a prompt allowing the user to verify this action.</span></span> <span data-ttu-id="0537d-225">Bei Freigabe Verstößen wird im Dialogfeld standardmäßig eine Fehlermeldung angezeigt, es wird nicht geschlossen, und der Benutzer muss eine andere Auswahl treffen.</span><span class="sxs-lookup"><span data-stu-id="0537d-225">For sharing violations, by default the dialog displays an error message, it does not close, and the user is required to make another choice.</span></span> <span data-ttu-id="0537d-226">Der aufrufenden Prozess kann diese Standardwerte überschreiben und die eigene Benutzeroberfläche anzeigen, wenn gewünscht.</span><span class="sxs-lookup"><span data-stu-id="0537d-226">The calling process can override these defaults and display its own UI if desired.</span></span> <span data-ttu-id="0537d-227">Das Dialogfeld kann angewiesen werden, die Datei abzulehnen und offen zu bleiben oder die Datei zu akzeptieren und erfolgreich zu schließen.</span><span class="sxs-lookup"><span data-stu-id="0537d-227">The dialog can be instructed to refuse the file and remain open or accept the file and close successfully.</span></span>

## <a name="customizing-the-dialog"></a><span data-ttu-id="0537d-228">Anpassen des Dialog Felds</span><span class="sxs-lookup"><span data-stu-id="0537d-228">Customizing the Dialog</span></span>

<span data-ttu-id="0537d-229">Eine Vielzahl von Steuerelementen können dem Dialogfeld hinzugefügt werden, ohne eine Win32-Dialogfeld Vorlage bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="0537d-229">A variety of controls can be added to the dialog without supplying a Win32 dialog template.</span></span> <span data-ttu-id="0537d-230">Diese Steuerelemente umfassen PUSHBUTTON, ComboBox, EditBox, checkbutton, RadioButton-Listen, Gruppen, Trennzeichen und statische Text Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="0537d-230">These controls include PushButton, ComboBox, EditBox, CheckButton, RadioButton lists, Groups, Separators, and Static Text controls.</span></span> <span data-ttu-id="0537d-231">Rufen Sie **QueryInterface** im Dialog Objekt ([**ifiledialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog), [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog)oder [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog)) auf, um einen [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) -Zeiger zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0537d-231">Call **QueryInterface** on the dialog object ([**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog), [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog), or [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog)) to obtain an [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) pointer.</span></span> <span data-ttu-id="0537d-232">Verwenden Sie diese Schnittstelle, um Steuerelemente hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="0537d-232">Use that interface to add controls.</span></span> <span data-ttu-id="0537d-233">Jedes Steuerelement verfügt über eine zugeordnete, vom Aufrufer bereitgestellte ID sowie einen *sichtbaren* und *aktivierten* Zustand, der vom aufrufenden Prozess festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="0537d-233">Each control has an associated caller-supplied ID as well as a *visible* and *enabled* state that can be set by the calling process.</span></span> <span data-ttu-id="0537d-234">Einigen Steuerelementen, z. b. PUSHBUTTON, sind auch Text zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="0537d-234">Some controls, such as PushButton, also have text associated with them.</span></span>

<span data-ttu-id="0537d-235">Einer "visuellen Gruppe" können mehrere Steuerelemente hinzugefügt werden, die als eine Einheit im Layout des Dialog Felds verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="0537d-235">Multiple controls can be added into a "visual group" that moves as a single unit in the layout of the dialog.</span></span> <span data-ttu-id="0537d-236">Gruppen kann eine Bezeichnung zugeordnet sein.</span><span class="sxs-lookup"><span data-stu-id="0537d-236">Groups can have a label associated with them.</span></span>

<span data-ttu-id="0537d-237">Steuerelemente können nur hinzugefügt werden, bevor das Dialogfeld angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="0537d-237">Controls can be added only before the dialog is shown.</span></span> <span data-ttu-id="0537d-238">Wenn das Dialogfeld angezeigt wird, können Steuerelemente jedoch wie gewünscht ausgeblendet oder angezeigt werden, möglicherweise als Reaktion auf eine Benutzeraktion.</span><span class="sxs-lookup"><span data-stu-id="0537d-238">However, once the dialog is displayed, controls can be hidden or shown as desired, perhaps in response to user action.</span></span> <span data-ttu-id="0537d-239">In den folgenden Beispielen wird gezeigt, wie eine Optionsfeld Liste zum Dialogfeld hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="0537d-239">The following examples show how to add a radio button list to the dialog.</span></span>


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





### <a name="adding-options-to-the-ok-button"></a><span data-ttu-id="0537d-240">Hinzufügen von Optionen zur Schaltfläche "OK"</span><span class="sxs-lookup"><span data-stu-id="0537d-240">Adding Options to the OK Button</span></span>

<span data-ttu-id="0537d-241">Entsprechend können Sie die Schaltflächen " **Öffnen** " oder " **Speichern** " auswählen, bei denen es sich um die Schaltfläche " **OK** " für die entsprechenden Dialog Typen handelt.</span><span class="sxs-lookup"><span data-stu-id="0537d-241">Similarly, choices can be added to the **Open** or **Save** buttons, which are the **OK** button for their respective dialog types.</span></span> <span data-ttu-id="0537d-242">Die Optionen sind über ein Dropdown-Listenfeld zugänglich, das an die Schaltfläche angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="0537d-242">The options are accessible through a drop-down list box attached to the button.</span></span> <span data-ttu-id="0537d-243">Das erste Element in der Liste wird der Text für die Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="0537d-243">The first item in the list becomes the text for the button.</span></span> <span data-ttu-id="0537d-244">Das folgende Beispiel zeigt, wie Sie eine Schaltfläche **Öffnen** mit zwei Möglichkeiten bereitstellen: "Öffnen" und "als schreibgeschützt öffnen".</span><span class="sxs-lookup"><span data-stu-id="0537d-244">The following example shows how to provide an **Open** button with two possibilities: "Open" and "Open as read-only".</span></span>


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





<span data-ttu-id="0537d-245">Die Auswahl des Benutzers kann überprüft werden, nachdem der Dialog von der [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) -Methode wie bei einem Kombinations Feld zurückgegeben wurde, oder er kann im Rahmen der Verarbeitung durch [**IFileDialogEvents:: OnFileOk**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onfileok)überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="0537d-245">The user's choice can be verified after the dialog returns from the [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) method as you would for a ComboBox, or it can verified as part of the handling by [**IFileDialogEvents::OnFileOk**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onfileok).</span></span>

### <a name="responding-to-events-in-added-controls"></a><span data-ttu-id="0537d-246">Reagieren auf Ereignisse in hinzugefügten Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="0537d-246">Responding to Events in Added Controls</span></span>

<span data-ttu-id="0537d-247">Der Ereignishandler, der vom aufrufenden Prozess bereitgestellt wird, kann [**ifiledialogcontrolevents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) zusätzlich zu [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents)implementieren.</span><span class="sxs-lookup"><span data-stu-id="0537d-247">The events handler provided by the calling process can implement [**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) in addition to [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents).</span></span> <span data-ttu-id="0537d-248">**Ifiledialogcontrolevents** ermöglicht dem aufrufenden Prozess, auf diese Ereignisse zu reagieren:</span><span class="sxs-lookup"><span data-stu-id="0537d-248">**IFileDialogControlEvents** enables the calling process to react to these events:</span></span>

-   <span data-ttu-id="0537d-249">PUSHBUTTON geklickt</span><span class="sxs-lookup"><span data-stu-id="0537d-249">PushButton clicked</span></span>
-   <span data-ttu-id="0537d-250">Kontrollkästchen Zustand geändert</span><span class="sxs-lookup"><span data-stu-id="0537d-250">CheckButton state changed</span></span>
-   <span data-ttu-id="0537d-251">Ausgewähltes Element in einem Menü, ComboBox oder RadioButton-Liste</span><span class="sxs-lookup"><span data-stu-id="0537d-251">Item selected from a menu, ComboBox, or RadioButton list</span></span>
-   <span data-ttu-id="0537d-252">Aktivieren des Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="0537d-252">Control activating.</span></span> <span data-ttu-id="0537d-253">Dies wird gesendet, wenn ein Menü im Begriff ist, eine Dropdown Liste anzuzeigen, falls der aufrufenden Prozess die Elemente in der Liste ändern möchte.</span><span class="sxs-lookup"><span data-stu-id="0537d-253">This is sent when a menu is about to display a drop-down list, in case the calling process wants to change the items in the list.</span></span>

## <a name="full-samples"></a><span data-ttu-id="0537d-254">Vollständige Beispiele</span><span class="sxs-lookup"><span data-stu-id="0537d-254">Full Samples</span></span>

<span data-ttu-id="0537d-255">Im folgenden finden Sie umfassende, herunterladbare C++-Beispiele aus dem Windows Software Development Kit (SDK), die die Verwendung von und die Interaktion mit dem Dialog Feld "allgemeine Elemente" veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="0537d-255">The following are complete, downloadable C++ samples from the Windows Software Development Kit (SDK) which demonstrate the use of and interaction with the Common Item Dialog.</span></span>

-   [<span data-ttu-id="0537d-256">Dialogfeld „Gemeinsame Dateien“ (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="0537d-256">Common File Dialog Sample</span></span>](samples-commonfiledialog.md)
-   [<span data-ttu-id="0537d-257">Modi des Dialogfelds „Gemeinsame Dateien“ (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="0537d-257">Common File Dialog Modes Sample</span></span>](samples-commonfiledialogmodes.md)

## <a name="related-topics"></a><span data-ttu-id="0537d-258">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0537d-258">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0537d-259">**IID \_ PPV-Argumente \_**</span><span class="sxs-lookup"><span data-stu-id="0537d-259">**IID\_PPV\_ARGS**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 
