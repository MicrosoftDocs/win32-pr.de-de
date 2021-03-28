---
description: Sie verfügen jetzt über alle wesentlichen Elemente, die erforderlich sind, um im-Namespace zu navigieren.
ms.assetid: bd9f903d-bea6-494f-af81-d90457dc2647
title: Navigieren im Namespace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d24993369222fb32f9de6c79a0c998b1d7be9f2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041846"
---
# <a name="navigating-the-namespace"></a><span data-ttu-id="f7ff8-103">Navigieren im Namespace</span><span class="sxs-lookup"><span data-stu-id="f7ff8-103">Navigating the Namespace</span></span>

<span data-ttu-id="f7ff8-104">Sie verfügen jetzt über alle wesentlichen Elemente, die erforderlich sind, um im-Namespace zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="f7ff8-104">You now have all the essential elements needed to navigate anywhere in the namespace.</span></span> <span data-ttu-id="f7ff8-105">Die einfachste Möglichkeit zum Einstieg besteht darin, dass Ihre Anwendung [**shgetdesktopfolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder) aufruft, um die [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) -Schnittstelle des Desktops abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f7ff8-105">The simplest way to start is to have your application call [**SHGetDesktopFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder) to retrieve the desktop's [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface.</span></span> <span data-ttu-id="f7ff8-106">Wenn Sie dann nach unten durch den-Namespace navigieren möchten, kann die Anwendung die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="f7ff8-106">Then, to navigate downward through the namespace, your application can follow these steps:</span></span>

1.  <span data-ttu-id="f7ff8-107">Listet den Inhalt des Ordners auf.</span><span class="sxs-lookup"><span data-stu-id="f7ff8-107">Enumerate the folder's contents.</span></span>
2.  <span data-ttu-id="f7ff8-108">Legen Sie fest, welche Objekte Unterordner sind, und wählen Sie einen aus.</span><span class="sxs-lookup"><span data-stu-id="f7ff8-108">Determine which objects are subfolders, and select one.</span></span>
3.  <span data-ttu-id="f7ff8-109">Binden Sie an den Unterordner, um die [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) -Schnittstelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f7ff8-109">Bind to the subfolder to retrieve its [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface.</span></span>

<span data-ttu-id="f7ff8-110">Wiederholen Sie diese Schritte so oft wie erforderlich, um das Ziel zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="f7ff8-110">Repeat these steps as often as necessary to reach the target.</span></span>

## <a name="a-simple-example-of-namespace-navigation"></a><span data-ttu-id="f7ff8-111">Ein einfaches Beispiel für die Namespace Navigation</span><span class="sxs-lookup"><span data-stu-id="f7ff8-111">A Simple Example of Namespace Navigation</span></span>

<span data-ttu-id="f7ff8-112">Der folgende Teil des Beispielcodes ist eine einfache Konsolenanwendung, die eine Reihe von Verfahren veranschaulicht, die in den vorherigen Abschnitten erläutert werden.</span><span class="sxs-lookup"><span data-stu-id="f7ff8-112">The following piece of sample code is a simple console application that illustrates a number of the procedures discussed in the preceding sections.</span></span> <span data-ttu-id="f7ff8-113">Die Fehlerüberprüfung wurde aus Gründen der Übersichtlichkeit ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="f7ff8-113">Error checking has been omitted for clarity.</span></span> <span data-ttu-id="f7ff8-114">Die Anwendung führt die folgenden Aufgaben durch:</span><span class="sxs-lookup"><span data-stu-id="f7ff8-114">The application performs the following tasks:</span></span>

1.  <span data-ttu-id="f7ff8-115">Ruft die [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) -Schnittstelle des Programmdatei Ordners ab ([mithilfe der IShellFolder-Schnittstelle](folder-info.md)).</span><span class="sxs-lookup"><span data-stu-id="f7ff8-115">Retrieves the Program Files folder's [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface ([Using the IShellFolder Interface](folder-info.md)).</span></span>
2.  <span data-ttu-id="f7ff8-116">Listet den Inhalt des Ordners auf ([Listet den Inhalt eines Ordners auf](folder-info.md)).</span><span class="sxs-lookup"><span data-stu-id="f7ff8-116">Enumerates the contents of the folder ([Enumerating the Contents of a Folder](folder-info.md)).</span></span>
3.  <span data-ttu-id="f7ff8-117">Bestimmt alle anzeigen Amen und druckt sie ([bestimmen von anzeigen Amen und anderen Eigenschaften](folder-info.md)).</span><span class="sxs-lookup"><span data-stu-id="f7ff8-117">Determines all the display names and prints them ([Determining Display Names and Other Properties](folder-info.md)).</span></span>
4.  <span data-ttu-id="f7ff8-118">Sucht nach einem Unterordner ([mit einem Zeiger auf die IShellFolder-Schnittstelle eines unter Ordners](folder-info.md)).</span><span class="sxs-lookup"><span data-stu-id="f7ff8-118">Looks for a subfolder ([Getting a Pointer to a Subfolder's IShellFolder Interface](folder-info.md)).</span></span>
5.  <span data-ttu-id="f7ff8-119">Bindet an den ersten untergeordneten Ordner, der gefunden wird (das[erhalten eines Zeigers auf die IShellFolder-Schnittstelle eines unter Ordners](folder-info.md)).</span><span class="sxs-lookup"><span data-stu-id="f7ff8-119">Binds to the first subfolder it finds ([Getting a Pointer to a Subfolder's IShellFolder Interface](folder-info.md)).</span></span>
6.  <span data-ttu-id="f7ff8-120">Gibt die anzeigen amen der Objekte im Unterordner aus.</span><span class="sxs-lookup"><span data-stu-id="f7ff8-120">Prints the display names of the objects in the subfolder.</span></span>


```
#include <shlobj.h>
#include <shlwapi.h>
#include <iostream.h>

main()
{
    LPITEMIDLIST pidlProgFiles = NULL;
    LPITEMIDLIST pidlItems = NULL;
    IShellFolder *psfFirstFolder = NULL;
    IShellFolder *psfDeskTop = NULL;
    IShellFolder *psfProgFiles = NULL;
    LPENUMIDLIST ppenum = NULL;
    ULONG celtFetched;
    HRESULT hr;
    STRRET strDispName;
    TCHAR pszDisplayName[MAX_PATH];
    ULONG uAttr;
   
    CoInitialize( NULL );
    
    hr = SHGetFolderLocation(NULL, CSIDL_PROGRAM_FILES, NULL, 0, &pidlProgFiles);

    hr = SHGetDesktopFolder(&psfDeskTop);

    hr = psfDeskTop->BindToObject(pidlProgFiles, NULL, IID_IShellFolder, (LPVOID *) &psfProgFiles);
    psfDeskTop->Release();

    hr = psfProgFiles->EnumObjects(NULL,SHCONTF_FOLDERS | SHCONTF_NONFOLDERS, &ppenum);

    while( hr = ppenum->Next(1,&pidlItems, &celtFetched) == S_OK && (celtFetched) == 1)
    {
        psfProgFiles->GetDisplayNameOf(pidlItems, SHGDN_INFOLDER, &strDispName);
        StrRetToBuf(&strDispName, pidlItems, pszDisplayName, MAX_PATH);
        cout << pszDisplayName << '\n';
        if(!psfFirstFolder)
        {
            uAttr = SFGAO_FOLDER;
            psfProgFiles->GetAttributesOf(1, (LPCITEMIDLIST *) &pidlItems, &uAttr);
            if(uAttr & SFGAO_FOLDER)
            {
                hr = psfProgFiles->BindToObject(pidlItems, NULL, IID_IShellFolder, (LPVOID *) &psfFirstFolder);
            }
        }
        CoTaskMemFree(pidlItems);
    }

    cout << "\n\n";

    ppenum->Release();

    if(psfFirstFolder)
    {
        hr = psfFirstFolder->EnumObjects(NULL,SHCONTF_FOLDERS | SHCONTF_NONFOLDERS, &ppenum);

        while( hr = ppenum->Next(1,&pidlItems, &celtFetched) == S_OK && (celtFetched) == 1)
        {
            psfFirstFolder->GetDisplayNameOf(pidlItems, SHGDN_INFOLDER, &strDispName);
            StrRetToBuf(&strDispName, pidlItems, pszDisplayName, MAX_PATH);
            cout << pszDisplayName << '\n';
            CoTaskMemFree(pidlItems);
        }
    }

    ppenum->Release();
    CoTaskMemFree(pidlProgFiles);
    psfProgFiles->Release();
    psfFirstFolder->Release();

    CoUninitialize();
    return 0;
}
```



 

 
