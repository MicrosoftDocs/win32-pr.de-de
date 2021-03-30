---
description: Bevor Sie ein Namespace Objekt verwenden können, benötigen Sie eine Möglichkeit, es zu identifizieren.
ms.assetid: 54225481-a147-4d29-a642-24c9b59fc3ac
title: Die ID eines Ordners wird erhalten.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb2e62454bf27f2c203f59aecb325cefe6537d2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994734"
---
# <a name="getting-a-folders-id"></a><span data-ttu-id="42e00-103">Die ID eines Ordners wird erhalten.</span><span class="sxs-lookup"><span data-stu-id="42e00-103">Getting a Folder's ID</span></span>

<span data-ttu-id="42e00-104">Bevor Sie ein Namespace Objekt verwenden können, benötigen Sie eine Möglichkeit, es zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="42e00-104">Before you can make use of a namespace object, you need a way to identify it.</span></span> <span data-ttu-id="42e00-105">Dies bedeutet, dass entweder der Zeiger auf eine Element Bezeichner Liste (PIDL) oder im Fall von Dateisystemobjekten der Pfad erhalten wird.</span><span class="sxs-lookup"><span data-stu-id="42e00-105">This means obtaining either its pointer to an item identifier list (PIDL) or, in the case of file system objects, its path.</span></span> <span data-ttu-id="42e00-106">In diesem Abschnitt werden zwei der einfacheren Methoden zum Abrufen von Objekt-IDs erläutert.</span><span class="sxs-lookup"><span data-stu-id="42e00-106">This section discusses two of the simpler ways to obtain object IDs.</span></span>

<span data-ttu-id="42e00-107">Verwenden Sie die [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) -Schnittstelle für einen leistungsstärkeren Ansatz, der mit einem beliebigen Ordner funktioniert.</span><span class="sxs-lookup"><span data-stu-id="42e00-107">For a more powerful approach that will work with any folder, use the [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface.</span></span> <span data-ttu-id="42e00-108">Weitere [Informationen finden Sie unter Informationen zum Inhalt eines Ordners](folder-info.md) .</span><span class="sxs-lookup"><span data-stu-id="42e00-108">See [Getting Information About the Contents of a Folder](folder-info.md) for more details.</span></span>

-   [<span data-ttu-id="42e00-109">Das Dialog Feld "openfiles"</span><span class="sxs-lookup"><span data-stu-id="42e00-109">The OpenFiles Dialog Box</span></span>](#the-openfiles-dialog-box)
-   [<span data-ttu-id="42e00-110">Das Dialog Feld "shbrowsforfolder"</span><span class="sxs-lookup"><span data-stu-id="42e00-110">The SHBrowseForFolder Dialog Box</span></span>](#the-shbrowseforfolder-dialog-box)
-   [<span data-ttu-id="42e00-111">Besondere Ordner und CSIDLs</span><span class="sxs-lookup"><span data-stu-id="42e00-111">Special Folders and CSIDLs</span></span>](#special-folders-and-csidls)
-   [<span data-ttu-id="42e00-112">Ein einfaches Beispiel für die Verwendung von CSIDLs und shbrowcforfolder</span><span class="sxs-lookup"><span data-stu-id="42e00-112">A Simple Example of How to Use CSIDLs and SHBrowseForFolder</span></span>](#a-simple-example-of-how-to-use-csidls-and-shbrowseforfolder)

## <a name="the-openfiles-dialog-box"></a><span data-ttu-id="42e00-113">Das Dialog Feld "openfiles"</span><span class="sxs-lookup"><span data-stu-id="42e00-113">The OpenFiles Dialog Box</span></span>

<span data-ttu-id="42e00-114">Um dem Benutzer zu ermöglichen, im-Namespace zu navigieren und einen Ordner auszuwählen, kann die Anwendung die [**ifiledialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) -Schnittstelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="42e00-114">To enable the user to navigate the namespace and select a folder, your application can use the [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) interface.</span></span> <span data-ttu-id="42e00-115">Wenn Sie diese Schnittstelle mit dem Flag " **Fos \_ pickfolders** " aufrufen, wird das Dialogfeld " [Dateien öffnen](../dlgbox/open-and-save-as-dialog-boxes.md) " im Modus "Pick Folders" geöffnet.</span><span class="sxs-lookup"><span data-stu-id="42e00-115">Calling this interface with the **FOS\_PICKFOLDERS** flag launches the [Open Files](../dlgbox/open-and-save-as-dialog-boxes.md) common dialog box in "pick folders" mode.</span></span>

<span data-ttu-id="42e00-116">Für Windows Vista und höher ist dies die empfohlene Methode zum Auswählen von Ordnern.</span><span class="sxs-lookup"><span data-stu-id="42e00-116">For Windows Vista and later, this is the recommended way to pick folders.</span></span>

## <a name="the-shbrowseforfolder-dialog-box"></a><span data-ttu-id="42e00-117">Das Dialog Feld "shbrowsforfolder"</span><span class="sxs-lookup"><span data-stu-id="42e00-117">The SHBrowseForFolder Dialog Box</span></span>

<span data-ttu-id="42e00-118">Um dem Benutzer zu ermöglichen, im-Namespace zu navigieren und einen Ordner auszuwählen, kann die Anwendung einfach [**shbrowseforfolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="42e00-118">To enable the user to navigate the namespace and select a folder, your application can simply invoke [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).</span></span> <span data-ttu-id="42e00-119">Durch Aufrufen dieser Funktion wird ein Dialogfeld mit einer Benutzeroberfläche gestartet, das ähnlich wie die allgemeinen Dialogfelder [Öffnen oder SaveAs](../dlgbox/open-and-save-as-dialog-boxes.md) funktioniert.</span><span class="sxs-lookup"><span data-stu-id="42e00-119">Calling this function launches a dialog box with a UI that works somewhat like the [Open or SaveAs](../dlgbox/open-and-save-as-dialog-boxes.md) common dialog boxes.</span></span>

<span data-ttu-id="42e00-120">Wenn der Benutzer einen Ordner auswählt, gibt [**shbrowsforfolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) die voll qualifizierte PIDL und den anzeigen amen des Ordners zurück.</span><span class="sxs-lookup"><span data-stu-id="42e00-120">When the user selects a folder, [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) returns the folder's fully qualified PIDL and its display name.</span></span> <span data-ttu-id="42e00-121">Wenn sich der Ordner im Dateisystem befindet, kann die Anwendung die PIDL in einen Pfad konvertieren, indem Sie [**shgetpathfromittlerlist**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="42e00-121">If the folder is in the file system, the application can convert the PIDL to a path by calling [**SHGetPathFromIDList**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista).</span></span> <span data-ttu-id="42e00-122">Die Anwendung kann auch den Bereich der Ordner einschränken, aus denen der Benutzer auswählen kann, indem er einen Stamm Ordner angibt.</span><span class="sxs-lookup"><span data-stu-id="42e00-122">The application can also restrict the range of folders that the user can select from by specifying a root folder.</span></span> <span data-ttu-id="42e00-123">Nur Ordner, die sich unterhalb des Stamms im-Namespace befinden, werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="42e00-123">Only folders that are below that root in the namespace will appear.</span></span> <span data-ttu-id="42e00-124">Die folgende Abbildung zeigt das Dialogfeld **shbrowseforfolder** , wobei der Stamm Ordner auf Programme festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="42e00-124">The following illustration shows the **SHBrowseForFolder** dialog box, with the root folder set to Program Files.</span></span>

![Screenshot des Dialog Felds "Ordner suchen"](images/shell1.png)

<span data-ttu-id="42e00-126">Ein einfaches Beispiel für die Verwendung von " [**shbrowsforfolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) " wird später bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="42e00-126">A simple example of how to use [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) is provided later.</span></span>

## <a name="special-folders-and-csidls"></a><span data-ttu-id="42e00-127">Besondere Ordner und CSIDLs</span><span class="sxs-lookup"><span data-stu-id="42e00-127">Special Folders and CSIDLs</span></span>

<span data-ttu-id="42e00-128">Eine Reihe häufig verwendeter Ordner werden vom System als *spezielle* Ordner bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="42e00-128">A number of commonly used folders are designated as *special* by the system.</span></span> <span data-ttu-id="42e00-129">Diese Ordner haben einen klar definierten Zweck, und die meisten sind auf allen Systemen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="42e00-129">These folders have a well-defined purpose, and most of them are present on all systems.</span></span> <span data-ttu-id="42e00-130">Auch wenn Sie nicht anfänglich vorhanden sind, werden Ihre Namen und Speicherorte weiterhin definiert, sodass Sie später hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="42e00-130">Even if they are not present initially, their names and locations are still defined, so they can be added later.</span></span> <span data-ttu-id="42e00-131">Die Sammlung spezieller Ordner umfasst alle standardmäßigen virtuellen Ordner des Systems, z. b. Drucker, eigene Dokumente und Netzwerkumgebung.</span><span class="sxs-lookup"><span data-stu-id="42e00-131">The collection of special folders includes all of the system's standard virtual folders, such as Printers, My Documents, and Network Neighborhood.</span></span> <span data-ttu-id="42e00-132">Es enthält auch eine Reihe von standardmäßigen Dateisystem Ordnern, wie z. b. Programme und System.</span><span class="sxs-lookup"><span data-stu-id="42e00-132">It also includes a number of standard file system folders, such as Program Files and System.</span></span>

<span data-ttu-id="42e00-133">Obwohl die Ordner eine Standardkomponente aller Systeme sind, können Ihre Namen und Speicherorte im-Namespace variieren.</span><span class="sxs-lookup"><span data-stu-id="42e00-133">Even though the folders are a standard component of all systems, their names and locations in the namespace can vary.</span></span> <span data-ttu-id="42e00-134">Beispielsweise ist das System Verzeichnis c: \\ Winnt \\ system32 auf einigen Systemen und C: \\ Windows \\ system32 auf anderen Systemen.</span><span class="sxs-lookup"><span data-stu-id="42e00-134">For example, the System directory is C:\\Winnt\\System32 on some systems and C:\\Windows\\System32 on others.</span></span> <span data-ttu-id="42e00-135">In der Vergangenheit stellten Umgebungsvariablen den Namen und den Speicherort eines speziellen Ordners auf einem bestimmten System fest.</span><span class="sxs-lookup"><span data-stu-id="42e00-135">In the past, environment variables provided a way to determine the name and location of a special folder on any particular system.</span></span> <span data-ttu-id="42e00-136">Die Shell bietet nun eine robustere und flexiblere Möglichkeit, spezielle Ordner, [**CSIDLs**](csidl.md), zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="42e00-136">The Shell now provides a more robust and flexible way to identify special folders, [**CSIDLs**](csidl.md).</span></span> <span data-ttu-id="42e00-137">Sie sollten Sie in der Regel anstelle von Umgebungsvariablen verwenden.</span><span class="sxs-lookup"><span data-stu-id="42e00-137">You should generally use them instead of environment variables.</span></span>

<span data-ttu-id="42e00-138">CSIDLs stellen eine einheitliche Möglichkeit dar, um spezielle Ordner unabhängig von Ihrem Namen oder Speicherort auf einem bestimmten System zu identifizieren und zu lokalisieren.</span><span class="sxs-lookup"><span data-stu-id="42e00-138">CSIDLs provide a uniform way of identifying and locating special folders, regardless of their name or location on a particular system.</span></span> <span data-ttu-id="42e00-139">Im Gegensatz zu Umgebungsvariablen können CSIDLs sowohl mit virtuellen Ordnern als auch mit Dateisystem Ordnern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="42e00-139">Unlike environment variables, CSIDLs can be used with virtual folders as well as file system folders.</span></span> <span data-ttu-id="42e00-140">Jedem speziellen Ordner ist eine eindeutige CSIDL zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="42e00-140">Each special folder has a unique CSIDL assigned to it.</span></span> <span data-ttu-id="42e00-141">Beispielsweise verfügt der Ordner "Programme Dateisystem" über eine CSIDL von **CSIDL- \_ Programm \_ Dateien**, und der virtuelle Ordner der Netzwerkumgebung verfügt über eine CSIDL des **CSIDL- \_ Netzwerks**.</span><span class="sxs-lookup"><span data-stu-id="42e00-141">For example, the Program Files file system folder has a CSIDL of **CSIDL\_PROGRAM\_FILES**, and the Network Neighborhood virtual folder has a CSIDL of **CSIDL\_NETWORK**.</span></span>

<span data-ttu-id="42e00-142">Eine CSIDL wird in Verbindung mit einer von mehreren Shellfunktionen verwendet, um die PIDL eines speziellen Ordners oder den Pfad eines speziellen Dateisystem Ordners abzurufen.</span><span class="sxs-lookup"><span data-stu-id="42e00-142">A CSIDL is used in conjunction with one of several Shell functions to retrieve a special folder's PIDL, or a special file system folder's path.</span></span> <span data-ttu-id="42e00-143">Wenn der Ordner auf einem System nicht vorhanden ist, kann die Anwendung erzwingen, dass er erstellt wird, indem er die CSIDL mit dem **CSIDL- \_ Flag \_ Create** kombiniert.</span><span class="sxs-lookup"><span data-stu-id="42e00-143">If the folder does not exist on a system, your application can force it to be created by combining its CSIDL with **CSIDL\_FLAG\_CREATE**.</span></span> <span data-ttu-id="42e00-144">Die CSIDL kann an die folgenden Funktionen übergeben werden:</span><span class="sxs-lookup"><span data-stu-id="42e00-144">The CSIDL can be passed to the following functions:</span></span>

-   <span data-ttu-id="42e00-145">[**Shgetfolderlocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation): Ruft die PIDL eines speziellen Ordners ab.</span><span class="sxs-lookup"><span data-stu-id="42e00-145">[**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation), which retrieves the PIDL of a special folder.</span></span>
-   <span data-ttu-id="42e00-146">[**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha): Ruft den Pfad eines speziellen Dateisystem Ordners ab.</span><span class="sxs-lookup"><span data-stu-id="42e00-146">[**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha), which retrieves the path of a file system special folder.</span></span>

<span data-ttu-id="42e00-147">Beachten Sie, dass diese beiden Funktionen mit Version 5,0 der Shell eingeführt wurden und die Funktionen " [**SHGetSpecialFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation) " und " [**SHGetSpecialFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderpatha) " ersetzen.</span><span class="sxs-lookup"><span data-stu-id="42e00-147">Note that these two functions were introduced with version 5.0 of the Shell and supersede the [**SHGetSpecialFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation) and [**SHGetSpecialFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderpatha) functions.</span></span>

## <a name="a-simple-example-of-how-to-use-csidls-and-shbrowseforfolder"></a><span data-ttu-id="42e00-148">Ein einfaches Beispiel für die Verwendung von CSIDLs und shbrowcforfolder</span><span class="sxs-lookup"><span data-stu-id="42e00-148">A Simple Example of How to Use CSIDLs and SHBrowseForFolder</span></span>

<span data-ttu-id="42e00-149">Die folgende Beispiel Funktion, pidlbrowse, veranschaulicht die Verwendung von CSIDLs zum Abrufen der PIDL eines Ordners und das Verwenden von [**shbrowsforfolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) , um den Benutzer zum Auswählen eines Ordners zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="42e00-149">The following sample function, PidlBrowse, illustrates how to use CSIDLs to retrieve a folder's PIDL, and use [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) to have the user select a folder.</span></span> <span data-ttu-id="42e00-150">Er gibt die PIDL und den anzeigen amen des ausgewählten Ordners zurück.</span><span class="sxs-lookup"><span data-stu-id="42e00-150">It returns the PIDL and display name of the selected folder.</span></span>


```
LPITEMIDLIST PidlBrowse(HWND hwnd, int nCSIDL, LPSTR pszDisplayName)
{
    LPITEMIDLIST pidlRoot = NULL;
    LPITEMIDLIST pidlSelected = NULL;
    BROWSEINFO bi = {0};

    if(nCSIDL)
    {
        SHGetFolderLocation(hwnd, nCSIDL, NULL, NULL, &pidlRoot);
    }

    else
    {
        pidlRoot = NULL;
    }

    bi.hwndOwner = hwnd;
    bi.pidlRoot = pidlRoot;
    bi.pszDisplayName = pszDisplayName;
    bi.lpszTitle = "Choose a folder";
    bi.ulFlags = 0;
    bi.lpfn = NULL;
    bi.lParam = 0;

    pidlSelected = SHBrowseForFolder(&bi);

    if(pidlRoot)
    {
        CoTaskMemFree(pidlRoot);
    }

    return pidlSelected;
}
```



<span data-ttu-id="42e00-151">Die aufrufenden Anwendung übergibt ein Fenster Handle, das von [**shbrowseforfolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera)benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="42e00-151">The calling application passes in a window handle, which is needed by [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).</span></span> <span data-ttu-id="42e00-152">Der *ncsidl* -Parameter ist eine optionale CSIDL, die verwendet wird, um einen Stamm Ordner anzugeben.</span><span class="sxs-lookup"><span data-stu-id="42e00-152">The *nCSIDL* parameter is an optional CSIDL that is used to specify a root folder.</span></span> <span data-ttu-id="42e00-153">Es werden nur Ordner unter dem Stamm Ordner in der Hierarchie angezeigt.</span><span class="sxs-lookup"><span data-stu-id="42e00-153">Only folders below the root folder in the hierarchy will be displayed.</span></span> <span data-ttu-id="42e00-154">Die zuvor gezeigte Abbildung wurde durch Aufrufen dieser Funktion generiert, wobei *ncsidl* auf **CSIDL- \_ Programm \_ Dateien** festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="42e00-154">The illustration shown earlier was generated by calling this function with *nCSIDL* set to **CSIDL\_PROGRAM\_FILES**.</span></span> <span data-ttu-id="42e00-155">Die aufrufenden Anwendung übergibt auch den Zeichen folgen Puffer *pszDisplayName*, um den anzeigen amen des ausgewählten Ordners zu speichern, wenn pidlbrowse zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="42e00-155">The calling application also passes in a string buffer, *pszDisplayName*, to hold the display name of the selected folder when PidlBrowse returns.</span></span> <span data-ttu-id="42e00-156">Es liegt in der Verantwortung der aufrufenden Anwendung, die von **shbrowseforfolder** zurückgegebene idlist mithilfe von " [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)" freizugeben.</span><span class="sxs-lookup"><span data-stu-id="42e00-156">It is the responsibility of the calling application to free the IDList returned by **SHBrowseForFolder** using [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

 

 
