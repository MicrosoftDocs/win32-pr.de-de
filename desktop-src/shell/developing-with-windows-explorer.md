---
description: Windows-Explorer ist eine leistungsstarke Anwendung zum Durchsuchen und Verwalten von Ressourcen.
ms.assetid: 879CE652-EDC0-4a14-925E-C83763133BE5
title: Entwickeln mit Windows-Explorer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b7b68d48f2d1becea23311847a5ce41b3776321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484387"
---
# <a name="developing-with-windows-explorer"></a><span data-ttu-id="6d208-103">Entwickeln mit Windows-Explorer</span><span class="sxs-lookup"><span data-stu-id="6d208-103">Developing with Windows Explorer</span></span>

<span data-ttu-id="6d208-104">Windows-Explorer ist eine leistungsstarke Anwendung zum Durchsuchen und Verwalten von Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="6d208-104">Windows Explorer is a powerful resource-browsing and management application.</span></span> <span data-ttu-id="6d208-105">Der Zugriff auf den Windows-Explorer ist als integriertes Ganzes über Explorer.exe oder die [**IExplorerBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) -Schnittstelle möglich.</span><span class="sxs-lookup"><span data-stu-id="6d208-105">Windows Explorer can be accessed as an integrated whole through Explorer.exe or the [**IExplorerBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) interface.</span></span> <span data-ttu-id="6d208-106">Windows Explorer (Explorer.exe) kann mit [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) oder einer ähnlichen Funktion als separater Prozess erzeugt werden.</span><span class="sxs-lookup"><span data-stu-id="6d208-106">Windows Explorer (Explorer.exe) can be spawned as a separate process using [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) or a similar function.</span></span>

> [!Note]  
> <span data-ttu-id="6d208-107">Die Befehlszeilenoptionen für Explorer.exe werden auf der Microsoft Windows-Support-Website im Artikel [Windows-Explorer-Command-Line Optionen](https://support.microsoft.com/kb/152457)dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="6d208-107">Command-line options for Explorer.exe are documented on the Microsoft Windows Support site in the article [Windows Explorer Command-Line Options](https://support.microsoft.com/kb/152457).</span></span>

 

<span data-ttu-id="6d208-108">Geöffnete Explorer-Fenster können mithilfe von [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) (CLSID shellwindows) ermittelt und programmiert werden \_ , und neue Instanzen von Windows-Explorer können mithilfe von [**IWebBrowser2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752127(v=vs.85)) (CLSID \_ shellbrowserwindow) erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6d208-108">Open explorer windows can be discovered and programmed by using [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) (CLSID\_ShellWindows), and new instances of Windows Explorer can be created by using [**IWebBrowser2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752127(v=vs.85)) (CLSID\_ShellBrowserWindow).</span></span>

<span data-ttu-id="6d208-109">Im folgenden Codebeispiel wird veranschaulicht, wie das Windows-Explorer-Automatisierungs Modell zum Erstellen und ermitteln von Explorer-Fenstern verwendet werden kann, die ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6d208-109">The following code sample demonstrates how the Windows Explorer automation model can be used to create and discover explorer windows that are running.</span></span>


```
#define _WIN32_WINNT 0x0600
#define _WIN32_IE 0x0700
#define _UNICODE

#include <windows.h>
#include <shobjidl.h>
#include <shlobj.h>
#include <shlwapi.h>
#include <strsafe.h>
#include <propvarutil.h>
 
#pragma comment(lib, "shlwapi.lib")
#pragma comment(lib, "ole32.lib")
#pragma comment(lib, "shell32.lib")
#pragma comment(lib, "propsys.lib")
 
// Use the Shell Windows object to find all of the explorer and IExplorer 
// windows and close them.
 
void CloseExplorerWindows()
{
    IShellWindows* psw;
    
    if (SUCCEEDED(CoCreateInstance(CLSID_ShellWindows, 
                                   NULL,  
                                   CLSCTX_LOCAL_SERVER, 
                                   IID_PPV_ARGS(&psw))))
    {
        VARIANT v = { VT_I4 };
        if (SUCCEEDED(psw->get_Count(&v.lVal)))
        {
            // Walk backward to make sure that the windows that close
            // do not cause the array to be reordered.
            while (--v.lVal >= 0)
            {
                IDispatch *pdisp;
                
                if (S_OK == psw->Item(v, &pdisp))
                {
                    IWebBrowser2 *pwb;
                    if (SUCCEEDED(pdisp->QueryInterface(IID_PPV_ARGS(&pwb))))
                    {
                        pwb->Quit();
                        pwb->Release();
                    }
                    pdisp->Release();
                }
            }
        }
        psw->Release();
    }
}
 
// Convert an IShellItem or IDataObject into a VARIANT that holds an IDList
// suitable for use with IWebBrowser2::Navigate2.
 
HRESULT InitVariantFromObject(IUnknown *punk, VARIANT *pvar)
{
    VariantInit(pvar);
 
    PIDLIST_ABSOLUTE pidl;
    HRESULT hr = SHGetIDListFromObject(punk, &pidl);
    if (SUCCEEDED(hr))
    {
        hr = InitVariantFromBuffer(pidl, ILGetSize(pidl), pvar);
        CoTaskMemFree(pidl);
    }
    return hr;
}
 
HRESULT ParseItemAsVariant(PCWSTR pszItem, IBindCtx *pbc, VARIANT *pvar)
{
    VariantInit(pvar);
 
    IShellItem *psi;
    HRESULT hr = SHCreateItemFromParsingName(pszItem, NULL, IID_PPV_ARGS(&psi));
    if (SUCCEEDED(hr))
    {
        hr = InitVariantFromObject(psi, pvar);
        psi->Release();
    }
    return hr;
}

HRESULT GetKnownFolderAsVariant(REFKNOWNFOLDERID kfid, VARIANT *pvar)
{
    VariantInit(pvar);
 
    PIDLIST_ABSOLUTE pidl;
    HRESULT hr = SHGetKnownFolderIDList(kfid, 0, NULL, &pidl);
    if (SUCCEEDED(hr))
    {
        hr = InitVariantFromBuffer(pidl, ILGetSize(pidl), pvar);
        CoTaskMemFree(pidl);
    }
    return hr;
}

HRESULT GetShellItemFromCommandLine(REFIID riid, void **ppv)
{
    *ppv = NULL;
    HRESULT hr = E_FAIL;

    int cArgs;
    PWSTR *ppszCmd = CommandLineToArgvW(GetCommandLineW(), &cArgs);
    if (ppszCmd && cArgs > 1)
    {
        WCHAR szSpec[MAX_PATH];
        StringCchCopyW(szSpec, ARRAYSIZE(szSpec), ppszCmd[1]);
        PathUnquoteSpacesW(szSpec);

        hr = szSpec[0] ? S_OK : E_FAIL;   // Protect against empty data
        if (SUCCEEDED(hr))
        {
            hr = SHCreateItemFromParsingName(szSpec, NULL, riid, ppv);
            if (FAILED(hr))
            {
                WCHAR szFolder[MAX_PATH];
                GetCurrentDirectoryW(ARRAYSIZE(szFolder), szFolder);

                hr = PathAppendW(szFolder, szSpec) ? S_OK : E_FAIL;
                if (SUCCEEDED(hr))
                {
                    hr = SHCreateItemFromParsingName(szFolder, NULL, riid, ppv);
                }
            }
        }
    }
    return hr;
}

HRESULT GetShellItemFromCommandLineAsVariant(VARIANT *pvar)
{
    VariantInit(pvar);

    IShellItem *psi;
    HRESULT hr = GetShellItemFromCommandLine(IID_PPV_ARGS(&psi));
    if (SUCCEEDED(hr))
    {
        hr = InitVariantFromObject(psi, pvar);
        psi->Release();
    }
    return hr;
}

void OpenWindow()
{
    IWebBrowser2 *pwb;
    HRESULT hr = CoCreateInstance(CLSID_ShellBrowserWindow, 
                                  NULL,
                                  CLSCTX_LOCAL_SERVER, 
                                  IID_PPV_ARGS(&pwb));
    if (SUCCEEDED(hr))
    {
        CoAllowSetForegroundWindow(pwb, 0);

        pwb->put_Left(100);
        pwb->put_Top(100);
        pwb->put_Height(600);
        pwb->put_Width(800);
 
        VARIANT varTarget = {0};
        hr = GetShellItemFromCommandLineAsVariant(&varTarget);
        if (FAILED(hr))
        {
            hr = GetKnownFolderAsVariant(FOLDERID_UsersFiles, &varTarget);
        }

        if (SUCCEEDED(hr))
        {
            VARIANT vEmpty = {0};
            hr = pwb->Navigate2(&varTarget, &vEmpty, &vEmpty, &vEmpty, &vEmpty);
            if (SUCCEEDED(hr))
            {
                pwb->put_Visible(VARIANT_TRUE);
            }
            VariantClear(&varTarget);
        }
        pwb->Release();
    }
}

int WINAPI WinMain(HINSTANCE, HINSTANCE, LPSTR, int)
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED |  COINIT_DISABLE_OLE1DDE);
    if (SUCCEEDED(hr))
    {
        CloseExplorerWindows();

        OpenWindow();

        CoUninitialize();
    }
    return 0;
}
```



<span data-ttu-id="6d208-110">Der Windows-Explorer-Client Bereich kann mithilfe der [IExplorerBrowser](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) -Schnittstelle gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="6d208-110">The Windows Explorer client area can be hosted by using the [IExplorerBrowser](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) interface.</span></span> <span data-ttu-id="6d208-111">Die Steuerelemente Windows Explorer-Client und Namespace Tree sind Standardkomponenten von Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="6d208-111">The Windows Explorer client and the namespace tree controls are standard components of Windows Vista and later.</span></span> <span data-ttu-id="6d208-112">Entwickler können die Schnittstellen als Bausteine wieder verwenden.</span><span class="sxs-lookup"><span data-stu-id="6d208-112">Developers can reuse the interfaces as building components.</span></span> <span data-ttu-id="6d208-113">Diese Steuerelemente werden häufig verwendet, um angepasste explorergeeignete explorerelemente für die Problemdomäne zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6d208-113">One common use of these controls is to create customized explorers appropriate to the problem domain.</span></span>

<span data-ttu-id="6d208-114">Die Steuerelemente in Windows-Explorer werden in die folgenden Funktions Kategorien eingeteilt:</span><span class="sxs-lookup"><span data-stu-id="6d208-114">The controls in Windows Explorer are classified into the following functional categories:</span></span>

-   [<span data-ttu-id="6d208-115">Navigations Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="6d208-115">Navigation Controls</span></span>](#navigation-controls)
-   [<span data-ttu-id="6d208-116">Command-Steuerelemente für Befehle</span><span class="sxs-lookup"><span data-stu-id="6d208-116">Command Controls</span></span>](#command-controls)
-   [<span data-ttu-id="6d208-117">Eigenschaften-und Vorschau Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="6d208-117">Property and Preview Controls</span></span>](#property-and-preview-controls)
-   [<span data-ttu-id="6d208-118">Filtern und Anzeigen von Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="6d208-118">Filtering and View Controls</span></span>](#filtering-and-view-controls)
-   [<span data-ttu-id="6d208-119">ListView-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="6d208-119">Listview Control</span></span>](#listview-control)

## <a name="navigation-controls"></a><span data-ttu-id="6d208-120">Navigations Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="6d208-120">Navigation Controls</span></span>

<span data-ttu-id="6d208-121">Navigations Steuerelemente unterstützen Benutzer beim Bestimmen des Kontexts und Navigieren im zugeordneten logischen Domänen Bereich, dem sogenannten Pagespace.</span><span class="sxs-lookup"><span data-stu-id="6d208-121">Navigation controls assist users in determining context and navigating the associated logical domain space, called the pagespace.</span></span> <span data-ttu-id="6d208-122">Der Pagespace für Windows-Explorer ist beispielsweise der Shellnamespace.</span><span class="sxs-lookup"><span data-stu-id="6d208-122">For example, the pagespace for Windows Explorer is the Shell namespace.</span></span> <span data-ttu-id="6d208-123">Pagespaces bestehen aus null oder mehr Seiten.</span><span class="sxs-lookup"><span data-stu-id="6d208-123">Pagespaces are composed of zero or more pages.</span></span>

<span data-ttu-id="6d208-124">In der folgenden Tabelle sind die Navigations Steuerelemente aufgeführt und beschrieben, die in Windows-Explorer in den Betriebssystemen Windows Vista und höher verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="6d208-124">The following table lists and describes the navigation controls available in Windows Explorer in the Windows Vista and later operating systems.</span></span>



| <span data-ttu-id="6d208-125">Navigations Steuerelement</span><span class="sxs-lookup"><span data-stu-id="6d208-125">Navigation control</span></span>               | <span data-ttu-id="6d208-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6d208-126">Description</span></span>                                                                                                                                                                                |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d208-127">Adressleiste (Breadcrumb-Steuerelement)</span><span class="sxs-lookup"><span data-stu-id="6d208-127">Address Bar (Breadcrumb control)</span></span> | <span data-ttu-id="6d208-128">Zeigt die Adresse der aktuellen Seite im Pagespace an.</span><span class="sxs-lookup"><span data-stu-id="6d208-128">Displays the address of the current page in the pagespace.</span></span> <span data-ttu-id="6d208-129">Sie können auf Breadcrumb-Schaltflächen klicken, um zu einem beliebigen Vorgänger im Pagespace zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="6d208-129">Breadcrumb buttons can be clicked to navigate to any ancestor in the pagespace.</span></span> <span data-ttu-id="6d208-130">Benutzer können auch URLs und Pfade eingeben, um zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="6d208-130">Users can also type URLs and paths to navigate.</span></span> |
| <span data-ttu-id="6d208-131">Ordnerstruktur</span><span class="sxs-lookup"><span data-stu-id="6d208-131">Folder Tree</span></span>                      | <span data-ttu-id="6d208-132">Stellt eine neue Version eines Tree-Steuer Elements bereit, das für große Seitenbereiche optimiert ist.</span><span class="sxs-lookup"><span data-stu-id="6d208-132">Provides a new version of a tree control, optimized for large pagespaces.</span></span>                                                                                                                  |
| <span data-ttu-id="6d208-133">Reise</span><span class="sxs-lookup"><span data-stu-id="6d208-133">Travel</span></span>                           | <span data-ttu-id="6d208-134">Ermöglicht die relative Navigation durch Webstil-Schaltflächen wie " **zurück** " und " **Vorwärts**".</span><span class="sxs-lookup"><span data-stu-id="6d208-134">Enables relative navigation through web-style buttons such as **Back** and **Forward**.</span></span>                                                                                                    |
| <span data-ttu-id="6d208-135">Titel</span><span class="sxs-lookup"><span data-stu-id="6d208-135">Title</span></span>                            | <span data-ttu-id="6d208-136">Zeigt den Namen und den Kontext des aktuellen Explorers an.</span><span class="sxs-lookup"><span data-stu-id="6d208-136">Displays the current explorer name and context.</span></span>                                                                                                                                            |
| <span data-ttu-id="6d208-137">Pagespace</span><span class="sxs-lookup"><span data-stu-id="6d208-137">Pagespace</span></span>                        | <span data-ttu-id="6d208-138">Zeigt die aktuelle Verzweigung des Pagespace an.</span><span class="sxs-lookup"><span data-stu-id="6d208-138">Displays the current branch of the pagespace.</span></span> <span data-ttu-id="6d208-139">Seiten können nach verschiedenen Kriterien angeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="6d208-139">Pages can be ordered by different criteria.</span></span> <span data-ttu-id="6d208-140">Benutzer können auf eine Seite klicken, um zu dieser zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="6d208-140">Users can click a page to navigate to it.</span></span>                                                        |



 

## <a name="command-controls"></a><span data-ttu-id="6d208-141">Command-Steuerelemente für Befehle</span><span class="sxs-lookup"><span data-stu-id="6d208-141">Command Controls</span></span>

<span data-ttu-id="6d208-142">Befehls Steuerelemente kündigen den Benutzern die Features und Funktionen von Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="6d208-142">Command controls advertise the features and functionality of the Windows Explorer to users.</span></span> <span data-ttu-id="6d208-143">Diese Steuerelemente führen entweder allgemeine Aktionen oder Aktionen aus, die für ein ausgewähltes Element oder bestimmte Elemente spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="6d208-143">These controls perform either general actions or actions specific to one selected item or items.</span></span>



| <span data-ttu-id="6d208-144">Befehls Steuerelement</span><span class="sxs-lookup"><span data-stu-id="6d208-144">Command control</span></span> | <span data-ttu-id="6d208-145">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6d208-145">Description</span></span>                                                                                                                                                                                        |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d208-146">Symbolleiste</span><span class="sxs-lookup"><span data-stu-id="6d208-146">Toolbar</span></span>         | <span data-ttu-id="6d208-147">Zeigt Schaltflächen für häufig verwendete Befehle an (eine neue Version einer Befehls Symbolleiste).</span><span class="sxs-lookup"><span data-stu-id="6d208-147">Displays buttons for commonly used commands (a new version of a command toolbar).</span></span> <span data-ttu-id="6d208-148">Zu den Anpassungsoptionen zählen Dropdown-Schaltflächen, unterteilte Schaltflächen, optionaler beschreibender Text und ein Überlauf Bereich.</span><span class="sxs-lookup"><span data-stu-id="6d208-148">Customization options include drop-down buttons, split buttons, optional descriptive text, and an overflow area.</span></span> |
| <span data-ttu-id="6d208-149">Hero</span><span class="sxs-lookup"><span data-stu-id="6d208-149">Hero</span></span>            | <span data-ttu-id="6d208-150">Wird als einzelnes, optionales benutzerdefiniertes Steuerelement in der Mitte der Symbolleiste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6d208-150">Appears as a single, optional, custom control in the center of the toolbar.</span></span> <span data-ttu-id="6d208-151">Er stellt den primären Befehl für den aktuellen Kontext dar.</span><span class="sxs-lookup"><span data-stu-id="6d208-151">It represents the primary command for the current context.</span></span>                                                             |
| <span data-ttu-id="6d208-152">Menüleiste</span><span class="sxs-lookup"><span data-stu-id="6d208-152">Menu Bar</span></span>        | <span data-ttu-id="6d208-153">Zeigt Befehle über Menüs an.</span><span class="sxs-lookup"><span data-stu-id="6d208-153">Presents commands through menus.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="6d208-154">Kontextmenü</span><span class="sxs-lookup"><span data-stu-id="6d208-154">Context Menu</span></span>    | <span data-ttu-id="6d208-155">Listet eine Kontext relevante Teilmenge verfügbarer Befehle auf, die als Ergebnis des Rechtsklick auf ein Element angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6d208-155">Lists a contextually relevant subset of available commands that are displayed as a result of right-clicking an item.</span></span>                                                                               |



 

## <a name="property-and-preview-controls"></a><span data-ttu-id="6d208-156">Eigenschaften-und Vorschau Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="6d208-156">Property and Preview Controls</span></span>

<span data-ttu-id="6d208-157">Eigenschaften-und Vorschau Steuerelemente werden verwendet, um Vorschau Elemente anzuzeigen und Element Eigenschaften anzuzeigen und zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="6d208-157">Property and preview controls are used to preview items, and to view and edit item properties.</span></span>



| <span data-ttu-id="6d208-158">Control</span><span class="sxs-lookup"><span data-stu-id="6d208-158">Control</span></span>    | <span data-ttu-id="6d208-159">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6d208-159">Description</span></span>                                                                                                                                                                                                                                        |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d208-160">Vorschau</span><span class="sxs-lookup"><span data-stu-id="6d208-160">Preview</span></span>    | <span data-ttu-id="6d208-161">Zeigt eine Vorschau des ausgewählten Elements an, z. b. eine Miniaturansicht oder ein Live Symbol.</span><span class="sxs-lookup"><span data-stu-id="6d208-161">Displays a preview of the selected item, such as a thumbnail or a Live Icon.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="6d208-162">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6d208-162">Properties</span></span> | <span data-ttu-id="6d208-163">Zeigt die Eigenschaften des ausgewählten Elements an.</span><span class="sxs-lookup"><span data-stu-id="6d208-163">Displays properties of the selected item.</span></span> <span data-ttu-id="6d208-164">Bei Mehrfachauswahl wird eine Zusammenfassung der Eigenschaften für die ausgewählte Gruppe von Elementen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6d208-164">For multiple selections, it displays a summary of properties for the selected group of items.</span></span> <span data-ttu-id="6d208-165">Bei einer null-Auswahl wird eine Zusammenfassung der Eigenschaften für die aktuelle Seite (Inhalt von ListView) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6d208-165">For a null selection, it displays a summary of properties for the current page (contents of the listview).</span></span> |



 

## <a name="filtering-and-view-controls"></a><span data-ttu-id="6d208-166">Filtern und Anzeigen von Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="6d208-166">Filtering and View Controls</span></span>

<span data-ttu-id="6d208-167">Filter-und Sicht Steuerelemente werden verwendet, um den Satz von Elementen in der ListView zu manipulieren und die Darstellung von Elementen in der ListView zu ändern.</span><span class="sxs-lookup"><span data-stu-id="6d208-167">Filtering and view controls are used to manipulate the set of items in the listview and to change the presentation of items in the listview.</span></span>



| <span data-ttu-id="6d208-168">Control</span><span class="sxs-lookup"><span data-stu-id="6d208-168">Control</span></span>   | <span data-ttu-id="6d208-169">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6d208-169">Description</span></span>                                                                                                                 |
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d208-170">Filtern</span><span class="sxs-lookup"><span data-stu-id="6d208-170">Filter</span></span>    | <span data-ttu-id="6d208-171">Filtert oder ordnet Elemente in einer ListView auf der Grundlage von Eigenschaften an, die als Spalten aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="6d208-171">Filters or arranges items in a listview based on properties listed as columns.</span></span> <span data-ttu-id="6d208-172">Wenn Sie auf eine Spalte klicken, wird diese Eigenschaft sortiert.</span><span class="sxs-lookup"><span data-stu-id="6d208-172">Clicking on a column sorts by that property.</span></span> |
| <span data-ttu-id="6d208-173">Wordwheel</span><span class="sxs-lookup"><span data-stu-id="6d208-173">Wordwheel</span></span> | <span data-ttu-id="6d208-174">Filtert dynamisch und inkrementell die angezeigten Elemente in einer ListView basierend auf einer Eingabetext Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="6d208-174">Dynamically and incrementally filters the displayed items in a listview based on an input text string.</span></span>                      |
| <span data-ttu-id="6d208-175">Sicht</span><span class="sxs-lookup"><span data-stu-id="6d208-175">View</span></span>      | <span data-ttu-id="6d208-176">Ermöglicht dem Benutzer das Ändern des Ansichtsmodus eines ListView-Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="6d208-176">Enables the user to change the view mode of a listview control.</span></span> <span data-ttu-id="6d208-177">Ein Schieberegler kann verwendet werden, um die Symbolgröße zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="6d208-177">A slider can be used to determine icon size.</span></span>                |



 

## <a name="listview-control"></a><span data-ttu-id="6d208-178">ListView-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="6d208-178">Listview Control</span></span>

<span data-ttu-id="6d208-179">Das ListView-Steuerelement wird zum Anzeigen eines Satzes von Elementen in einem der vier Ansichtsmodi verwendet: Details, Kacheln, Symbole oder Panorama.</span><span class="sxs-lookup"><span data-stu-id="6d208-179">The listview control is used to view a set of items in one of four view modes: details, tiles, icons, or panorama.</span></span> <span data-ttu-id="6d208-180">Das ListView-Steuerelement ermöglicht es dem Benutzer auch, ein oder mehrere Elemente auszuwählen und zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="6d208-180">The listview control also enables the user to select and activate one or more items.</span></span>

> [!Caution]  
> <span data-ttu-id="6d208-181">Obwohl einige dieser Steuerelemente Namen und/oder Funktionen aufweisen, die den im System. Windows. Controls-Namespace gefundenen Standard-Windows Presentation Foundation (WPF)-Steuerelementen ähneln, sind Sie unterschiedliche Klassen.</span><span class="sxs-lookup"><span data-stu-id="6d208-181">Although some of these controls have names and/or functionality that is similar to standard Windows Presentation Foundation (WPF) controls found in the System.Windows.Controls namespace, they are distinct classes.</span></span>

 

<span data-ttu-id="6d208-182">Diese separaten Steuerelemente arbeiten größtenteils über Ereignisse, die entweder durch eine Benutzerinteraktion oder durch die Steuerelemente selbst generiert werden.</span><span class="sxs-lookup"><span data-stu-id="6d208-182">These separate controls work together largely through events generated either by user interaction or by the controls themselves.</span></span> <span data-ttu-id="6d208-183">In der folgenden Tabelle werden die drei primären Ereignis Kategorien aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="6d208-183">The following table shows the three primary event categories.</span></span>



| <span data-ttu-id="6d208-184">Ereigniskategorie</span><span class="sxs-lookup"><span data-stu-id="6d208-184">Event category</span></span> | <span data-ttu-id="6d208-185">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6d208-185">Example</span></span>                                                       |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="6d208-186">Navigation</span><span class="sxs-lookup"><span data-stu-id="6d208-186">Navigation</span></span>     | <span data-ttu-id="6d208-187">Von einer Seite zu einer anderen wechseln.</span><span class="sxs-lookup"><span data-stu-id="6d208-187">Going from one page to another.</span></span>                               |
| <span data-ttu-id="6d208-188">Auswahl</span><span class="sxs-lookup"><span data-stu-id="6d208-188">Selection</span></span>      | <span data-ttu-id="6d208-189">Ändern der aktuellen Auswahl in der ListView.</span><span class="sxs-lookup"><span data-stu-id="6d208-189">Changing the current selection in the listview.</span></span>               |
| <span data-ttu-id="6d208-190">Änderung anzeigen</span><span class="sxs-lookup"><span data-stu-id="6d208-190">View Change</span></span>    | <span data-ttu-id="6d208-191">Ändern der Präsentations Reihenfolge oder des Ansichtsmodus in ListView.</span><span class="sxs-lookup"><span data-stu-id="6d208-191">Changing the presentation order or view mode in the listview.</span></span> |



 

 

 
