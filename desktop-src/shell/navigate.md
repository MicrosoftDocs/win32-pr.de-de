---
description: Sie verfügen nun über alle wesentlichen Elemente, die zum Navigieren an einer beliebigen Stelle im Namespace erforderlich sind.
ms.assetid: bd9f903d-bea6-494f-af81-d90457dc2647
title: Navigieren im Namespace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2778fc21df12e9228f9335a52c04556e97563cba5f8a4cb6b82eb779944c451
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111480"
---
# <a name="navigating-the-namespace"></a>Navigieren im Namespace

Sie verfügen nun über alle wesentlichen Elemente, die zum Navigieren an einer beliebigen Stelle im Namespace erforderlich sind. Die einfachste Möglichkeit zum Starten besteht darin, dass Ihre Anwendung [**SHGetDesktopFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder) aufruft, um die [**IShellFolder-Schnittstelle**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) des Desktops abzurufen. Um dann nach unten durch den Namespace zu navigieren, kann Ihre Anwendung die folgenden Schritte ausführen:

1.  Aufzählen des Ordnerinhalts.
2.  Bestimmen Sie, welche Objekte Unterordner sind, und wählen Sie eines aus.
3.  Binden Sie an den Unterordner, um seine [**IShellFolder-Schnittstelle**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) abzurufen.

Wiederholen Sie diese Schritte so oft wie nötig, um das Ziel zu erreichen.

## <a name="a-simple-example-of-namespace-navigation"></a>Ein einfaches Beispiel für die Namespacenavigation

Der folgende Codeausschnitt ist eine einfache Konsolenanwendung, die eine Reihe der verfahren veranschaulicht, die in den vorherigen Abschnitten erläutert wurden. Die Fehlerüberprüfung wurde aus Gründen der Übersichtlichkeit ausgelassen. Die Anwendung führt die folgenden Aufgaben durch:

1.  Ruft die [**IShellFolder-Schnittstelle**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) des Ordners Programme ab ([mithilfe der IShellFolder-Schnittstelle](folder-info.md)).
2.  Listet den Inhalt des Ordners auf ([Aufzählen des Inhalts eines Ordners](folder-info.md)).
3.  Bestimmt alle Anzeigenamen und gibt sie aus ([Bestimmen von Anzeigenamen und anderen Eigenschaften](folder-info.md)).
4.  Sucht nach einem Unterordner ([Abrufen eines Zeigers auf die IShellFolder-Schnittstelle eines Unterordners](folder-info.md)).
5.  Bindet an den ersten gefundenen Unterordner ( Abrufen eines Zeigers auf die[IShellFolder-Schnittstelle eines Unterordners](folder-info.md)).
6.  Gibt die Anzeigenamen der Objekte im Unterordner aus.


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



 

 
