---
title: Container Browser
description: Eine Anwendung kann die DsBrowseForContainer-Funktion verwenden, um ein Dialogfeld anzuzeigen, das verwendet werden kann, um die Container in einem Active Directory-Domäne-Dienst zu durchsuchen.
ms.assetid: aa88d565-ff25-4082-964a-9a230d2607f2
ms.tgt_platform: multiple
keywords:
- Container Browser-AD
- Container AD, Browser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 964c67873cc7936a75e2b9c1cdf331d0fa1fdae1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038790"
---
# <a name="container-browser"></a>Container Browser

Eine Anwendung kann die [**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) -Funktion verwenden, um ein Dialogfeld anzuzeigen, das verwendet werden kann, um die Container in einem Active Directory-Domäne-Dienst zu durchsuchen. Das Dialogfeld zeigt die Container in einem Struktur Format an und ermöglicht es dem Benutzer, mithilfe der Tastatur und der Maus durch die Struktur zu navigieren. Wenn der Benutzer ein Element im Dialogfeld auswählt, wird der ADsPath des Containers bereitgestellt, der vom Benutzer ausgewählt wurde.

[**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) nimmt einen Zeiger auf eine [**dsbrowseinfo**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa) -Struktur, die Daten über das Dialogfeld enthält, und gibt den ADsPath des ausgewählten Elements zurück.

Der **pszroot** -Member ist ein Zeiger auf eine Unicode-Zeichenfolge, die den Stamm Container der Struktur enthält. Wenn **pszroot** **null** ist, enthält die Struktur die gesamte Struktur.

Der **pszpath** -Member empfängt den ADsPath des ausgewählten Objekts. Es ist möglich, einen bestimmten Container anzugeben, der beim ersten Anzeigen des Dialog Felds sichtbar und ausgewählt werden soll. Dies wird erreicht, indem **pszpath** auf den ADsPath des Elements festgelegt wird, das ausgewählt werden soll, und das Flag von **dsbi \_ expandonopen** in **dwFlags** festgelegt wird.

Der Inhalt und das Verhalten des Dialog Felds können auch zur Laufzeit gesteuert werden, indem eine [**bffcallback**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) -Funktion implementiert wird. Die **bffcallback** -Funktion wird von der Anwendung implementiert und wird aufgerufen, wenn bestimmte Ereignisse auftreten. Eine Anwendung kann diese Ereignisse verwenden, um zu steuern, wie die Elemente im Dialogfeld angezeigt werden, sowie den eigentlichen Inhalt des Dialog Felds. Beispielsweise kann eine Anwendung die im Dialogfeld angezeigten Elemente filtern, indem Sie eine **bffcallback** -Funktion implementiert, die die **DSBM \_ queryinsert** -Benachrichtigung verarbeiten kann. Wenn eine **DSBM- \_ queryinsert** -Benachrichtigung empfangen wird, verwenden Sie das **pszadspath** -Member der [**dsbitem**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) -Struktur, um zu bestimmen, welches Element eingefügt werden soll. Wenn die Anwendung feststellt, dass das Element nicht angezeigt werden soll, kann Sie das Element ausblenden, indem Sie die folgenden Schritte ausführen.

1.  Fügen Sie dem **dwMask** -Member der [**dsbitem**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) -Struktur das **dsbf \_ State** -Flag hinzu.
2.  Fügen Sie dem **dwstatemask** -Member der [**dsbitem**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) -Struktur das ausgeblendete **dssb \_** -Flag hinzu.
3.  Fügen Sie dem **dwstate** -Member der [**dsbitem**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) -Struktur das ausgeblendete **dssb \_** -Flag hinzu.
4.  Gibt einen Wert ungleich 0 (null) aus der [**bffcallback**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) -Funktion zurück.

Zusätzlich zum Ausblenden bestimmter Elemente kann eine Anwendung den Text und das Symbol ändern, die für das Element angezeigt werden, indem die **DSBM \_ queryinsert** -Benachrichtigung verarbeitet wird. Weitere Informationen finden Sie unter [**dsbitem**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema).

Die [**bffcallback**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) -Funktion kann die **\_ initialisierte bffm** -Benachrichtigung verwenden, um das Handle des Dialog Felds abzurufen. Die Anwendung kann dieses Handle verwenden, um Nachrichten, wie z. **b. bffm \_ enableok**, an das Dialogfeld zu senden. Weitere Informationen zu den Nachrichten, die an das Dialogfeld gesendet werden können, finden Sie unter [**bffcallback**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback).

Das Dialogfeld Handle kann auch verwendet werden, um direkten Zugriff auf die Steuerelemente im Dialogfeld zu erhalten. **Dsbid \_ Banner** ist der Bezeichner für das statische Text Steuerelement, in dem der **psztitle** -Member der [**dsbrowseinfo**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa) -Struktur angezeigt wird. **Dsbid \_ Containerlist** ist der Bezeichner des Strukturansicht-Steuer Elements, mit dem der Inhalt der Struktur angezeigt wird. Die Verwendung dieser Elemente sollte nach Möglichkeit vermieden werden, um zukünftige Probleme mit der Anwendungs Kompatibilität zu vermeiden.

Im folgenden C++-Codebeispiel wird gezeigt, wie die [**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) -Funktion verwendet wird, um das Dialogfeld "Container Browser" zu erstellen und eine [**bffcallback**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) -Funktion zu implementieren. [**Bffcallback**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) verwendet die **DSBM- \_ queryinsert** -Benachrichtigung, um den anzeigen Amen für jedes Element in den Distinguished Name des Elements zu ändern.


```C++
#include <shlobj.h>
#include <dsclient.h>
#include <atlbase.h>

/**********

    WideCharToLocal()
   
***********/

int WideCharToLocal(LPTSTR pLocal, LPWSTR pWide, DWORD dwChars)
{
    *pLocal = NULL;
    size_t nWideLength = 0;
    wchar_t *pwszSubstring;

    nWideLength = wcslen(pWide);

#ifdef UNICODE
    if(nWideLength < dwChars)
    {
        wcsncpy_s(pLocal, pWide, dwChars);
    }
    else
    {
        wcsncpy_s(pLocal, pWide, dwChars-1);
        pLocal[dwChars-1] = NULL;
    }
#else
    if(nWideLength < dwChars)
    {
        WideCharToMultiByte(    CP_ACP, 
                                0, 
                                pWide, 
                                -1, 
                                pLocal, 
                                dwChars, 
                                NULL, 
                                NULL);
    }
    else
    {
        pwszSubstring = new WCHAR[dwChars];
        wcsncpy_s(pwszSubstring,pWide,dwChars-1);
        pwszSubstring[dwChars-1] = NULL;

        WideCharToMultiByte(    CP_ACP, 
                                0, 
                                pwszSubstring, 
                                -1, 
                                pLocal, 
                                dwChars, 
                                NULL, 
                                NULL);

    delete [] pwszSubstring;
    }
#endif

    return lstrlen(pLocal);
}

/**********

    BrowseCallback()

***********/

int CALLBACK BrowseCallback(HWND hWnd, 
                            UINT uMsg, 
                            LPARAM lParam, 
                            LPARAM lpData)
{
    switch(uMsg)
    {
    case DSBM_QUERYINSERT:
        {
            BOOL fReturn = FALSE;
            DSBITEM *pItem = (DSBITEM*)lParam;

            /*
            If this is to the root item, get the distinguished name 
            for the object and set the display name to the 
            distinguished name.
            */
            if(!(pItem->dwState & DSBS_ROOT))
            {
                HRESULT hr;
                IADs    *pads;

                hr = ADsGetObject(pItem->pszADsPath , 
                    IID_IADs, (LPVOID*)&pads);
                if(SUCCEEDED(hr))
                {
                    VARIANT var;

                    VariantInit(&var);
                    hr = pads->Get(CComBSTR("distinguishedName"), 
                        &var);
                    if(SUCCEEDED(hr))
                    {
                        if(VT_BSTR == var.vt)
                        {
                            WideCharToLocal(pItem->szDisplayName, 
                                var.bstrVal, 
                                DSB_MAX_DISPLAYNAME_CHARS);
                            pItem->dwMask |= DSBF_DISPLAYNAME;
                            fReturn = TRUE;
                        }
                        
                        VariantClear(&var);
                    }
                    
                    pads->Release();
                }
            }

            return fReturn;
        }

        break;
    }
    
    return FALSE;
}

/***********

    BrowseForContainer()

************/

HRESULT BrowseForContainer(HWND hwndParent, 
    LPOLESTR *ppContainerADsPath)
{
    HRESULT hr = E_FAIL;
    DSBROWSEINFO dsbi;
    OLECHAR wszPath[MAX_PATH * 2];
    DWORD result;
 
    if(!ppContainerADsPath)
    {
        return E_INVALIDARG;
    }
 
    ZeroMemory(&dsbi, sizeof(dsbi));
    dsbi.hwndOwner = hwndParent;
    dsbi.cbStruct = sizeof (DSBROWSEINFO);
    dsbi.pszCaption = TEXT("Browse for a Container");
    dsbi.pszTitle = TEXT("Select an Active Directory container.");
    dsbi.pszRoot = NULL;
    dsbi.pszPath = wszPath;
    dsbi.cchPath = sizeof(wszPath)/sizeof(OLECHAR);
    dsbi.dwFlags = DSBI_INCLUDEHIDDEN |
                    DSBI_IGNORETREATASLEAF|
                    DSBI_RETURN_FORMAT;
    dsbi.pfnCallback = BrowseCallback;
    dsbi.lParam = 0;
    dsbi.dwReturnFormat = ADS_FORMAT_X500;
 
    // Display the browse dialog box.
    // Returns -1, 0, IDOK, or IDCANCEL.
    result = DsBrowseForContainer(&dsbi); 
    if(IDOK == result)
    {
        // Allocate memory for the string.
        *ppContainerADsPath = (OLECHAR*)CoTaskMemAlloc(
            sizeof(OLECHAR)*(wcslen(wszPath) + 1));
        if(*ppContainerADsPath)
        {
            wcscpy_s(*ppContainerADsPath, wszPath);
            // Caller must free using CoTaskMemFree. 
            hr = S_OK;
        }
        else
        {
            hr = E_FAIL;
        }
    }
    else
    {
        hr = E_FAIL;
    }
 
    return hr;
}
```



 

 