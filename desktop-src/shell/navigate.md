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
# <a name="navigating-the-namespace"></a>Navigieren im Namespace

Sie verfügen jetzt über alle wesentlichen Elemente, die erforderlich sind, um im-Namespace zu navigieren. Die einfachste Möglichkeit zum Einstieg besteht darin, dass Ihre Anwendung [**shgetdesktopfolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder) aufruft, um die [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) -Schnittstelle des Desktops abzurufen. Wenn Sie dann nach unten durch den-Namespace navigieren möchten, kann die Anwendung die folgenden Schritte ausführen:

1.  Listet den Inhalt des Ordners auf.
2.  Legen Sie fest, welche Objekte Unterordner sind, und wählen Sie einen aus.
3.  Binden Sie an den Unterordner, um die [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) -Schnittstelle abzurufen.

Wiederholen Sie diese Schritte so oft wie erforderlich, um das Ziel zu erreichen.

## <a name="a-simple-example-of-namespace-navigation"></a>Ein einfaches Beispiel für die Namespace Navigation

Der folgende Teil des Beispielcodes ist eine einfache Konsolenanwendung, die eine Reihe von Verfahren veranschaulicht, die in den vorherigen Abschnitten erläutert werden. Die Fehlerüberprüfung wurde aus Gründen der Übersichtlichkeit ausgelassen. Die Anwendung führt die folgenden Aufgaben durch:

1.  Ruft die [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) -Schnittstelle des Programmdatei Ordners ab ([mithilfe der IShellFolder-Schnittstelle](folder-info.md)).
2.  Listet den Inhalt des Ordners auf ([Listet den Inhalt eines Ordners auf](folder-info.md)).
3.  Bestimmt alle anzeigen Amen und druckt sie ([bestimmen von anzeigen Amen und anderen Eigenschaften](folder-info.md)).
4.  Sucht nach einem Unterordner ([mit einem Zeiger auf die IShellFolder-Schnittstelle eines unter Ordners](folder-info.md)).
5.  Bindet an den ersten untergeordneten Ordner, der gefunden wird (das[erhalten eines Zeigers auf die IShellFolder-Schnittstelle eines unter Ordners](folder-info.md)).
6.  Gibt die anzeigen amen der Objekte im Unterordner aus.


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



 

 
