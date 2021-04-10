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
# <a name="container-browser"></a><span data-ttu-id="1ee22-105">Container Browser</span><span class="sxs-lookup"><span data-stu-id="1ee22-105">Container Browser</span></span>

<span data-ttu-id="1ee22-106">Eine Anwendung kann die [**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) -Funktion verwenden, um ein Dialogfeld anzuzeigen, das verwendet werden kann, um die Container in einem Active Directory-Domäne-Dienst zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="1ee22-106">An application can use the [**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) function to display a dialog box that can be used to browse through the containers in an Active Directory Domain Service.</span></span> <span data-ttu-id="1ee22-107">Das Dialogfeld zeigt die Container in einem Struktur Format an und ermöglicht es dem Benutzer, mithilfe der Tastatur und der Maus durch die Struktur zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="1ee22-107">The dialog box displays the containers in a tree format and enables the user to navigate through the tree using the keyboard and mouse.</span></span> <span data-ttu-id="1ee22-108">Wenn der Benutzer ein Element im Dialogfeld auswählt, wird der ADsPath des Containers bereitgestellt, der vom Benutzer ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="1ee22-108">When the user selects an item in the dialog box, the ADsPath of the container selected by the user is provided.</span></span>

<span data-ttu-id="1ee22-109">[**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) nimmt einen Zeiger auf eine [**dsbrowseinfo**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa) -Struktur, die Daten über das Dialogfeld enthält, und gibt den ADsPath des ausgewählten Elements zurück.</span><span class="sxs-lookup"><span data-stu-id="1ee22-109">[**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) takes a pointer to a [**DSBROWSEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa) structure that contains data about the dialog box and returns the ADsPath of the selected item.</span></span>

<span data-ttu-id="1ee22-110">Der **pszroot** -Member ist ein Zeiger auf eine Unicode-Zeichenfolge, die den Stamm Container der Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="1ee22-110">The **pszRoot** member is a pointer to a Unicode string that contains the root container of the tree.</span></span> <span data-ttu-id="1ee22-111">Wenn **pszroot** **null** ist, enthält die Struktur die gesamte Struktur.</span><span class="sxs-lookup"><span data-stu-id="1ee22-111">If **pszRoot** is **NULL**, the tree will contain the entire tree.</span></span>

<span data-ttu-id="1ee22-112">Der **pszpath** -Member empfängt den ADsPath des ausgewählten Objekts.</span><span class="sxs-lookup"><span data-stu-id="1ee22-112">The **pszPath** member receives the ADsPath of the selected object.</span></span> <span data-ttu-id="1ee22-113">Es ist möglich, einen bestimmten Container anzugeben, der beim ersten Anzeigen des Dialog Felds sichtbar und ausgewählt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1ee22-113">It is possible to specify a particular container to be visible and selected when the dialog box is first displayed.</span></span> <span data-ttu-id="1ee22-114">Dies wird erreicht, indem **pszpath** auf den ADsPath des Elements festgelegt wird, das ausgewählt werden soll, und das Flag von **dsbi \_ expandonopen** in **dwFlags** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="1ee22-114">This is accomplished by setting **pszPath** to the ADsPath of the item to be selected and setting the **DSBI\_EXPANDONOPEN** flag in **dwFlags**.</span></span>

<span data-ttu-id="1ee22-115">Der Inhalt und das Verhalten des Dialog Felds können auch zur Laufzeit gesteuert werden, indem eine [**bffcallback**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) -Funktion implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="1ee22-115">The contents and behavior of the dialog box can also be controlled at runtime by implementing a [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) function.</span></span> <span data-ttu-id="1ee22-116">Die **bffcallback** -Funktion wird von der Anwendung implementiert und wird aufgerufen, wenn bestimmte Ereignisse auftreten.</span><span class="sxs-lookup"><span data-stu-id="1ee22-116">The **BFFCallBack** function is implemented by the application and is called when certain events occur.</span></span> <span data-ttu-id="1ee22-117">Eine Anwendung kann diese Ereignisse verwenden, um zu steuern, wie die Elemente im Dialogfeld angezeigt werden, sowie den eigentlichen Inhalt des Dialog Felds.</span><span class="sxs-lookup"><span data-stu-id="1ee22-117">An application can use these events to control how the items in the dialog box are displayed as well as the actual contents of the dialog box.</span></span> <span data-ttu-id="1ee22-118">Beispielsweise kann eine Anwendung die im Dialogfeld angezeigten Elemente filtern, indem Sie eine **bffcallback** -Funktion implementiert, die die **DSBM \_ queryinsert** -Benachrichtigung verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="1ee22-118">For example, an application can filter the items displayed in the dialog box by implementing a **BFFCallBack** function that can handle the **DSBM\_QUERYINSERT** notification.</span></span> <span data-ttu-id="1ee22-119">Wenn eine **DSBM- \_ queryinsert** -Benachrichtigung empfangen wird, verwenden Sie das **pszadspath** -Member der [**dsbitem**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) -Struktur, um zu bestimmen, welches Element eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1ee22-119">When a **DSBM\_QUERYINSERT** notification is received, use the **pszADsPath** member of the [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) structure to determine which item is about to be inserted.</span></span> <span data-ttu-id="1ee22-120">Wenn die Anwendung feststellt, dass das Element nicht angezeigt werden soll, kann Sie das Element ausblenden, indem Sie die folgenden Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="1ee22-120">If the application determines that the item should not be displayed, it can hide the item by performing the following steps.</span></span>

1.  <span data-ttu-id="1ee22-121">Fügen Sie dem **dwMask** -Member der [**dsbitem**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) -Struktur das **dsbf \_ State** -Flag hinzu.</span><span class="sxs-lookup"><span data-stu-id="1ee22-121">Add the **DSBF\_STATE** flag to the **dwMask** member of the [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) structure.</span></span>
2.  <span data-ttu-id="1ee22-122">Fügen Sie dem **dwstatemask** -Member der [**dsbitem**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) -Struktur das ausgeblendete **dssb \_** -Flag hinzu.</span><span class="sxs-lookup"><span data-stu-id="1ee22-122">Add the **DSBS\_HIDDEN** flag to the **dwStateMask** member of the [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) structure.</span></span>
3.  <span data-ttu-id="1ee22-123">Fügen Sie dem **dwstate** -Member der [**dsbitem**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) -Struktur das ausgeblendete **dssb \_** -Flag hinzu.</span><span class="sxs-lookup"><span data-stu-id="1ee22-123">Add the **DSBS\_HIDDEN** flag to the **dwState** member of the [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) structure.</span></span>
4.  <span data-ttu-id="1ee22-124">Gibt einen Wert ungleich 0 (null) aus der [**bffcallback**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) -Funktion zurück.</span><span class="sxs-lookup"><span data-stu-id="1ee22-124">Return a nonzero value from the [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) function.</span></span>

<span data-ttu-id="1ee22-125">Zusätzlich zum Ausblenden bestimmter Elemente kann eine Anwendung den Text und das Symbol ändern, die für das Element angezeigt werden, indem die **DSBM \_ queryinsert** -Benachrichtigung verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="1ee22-125">In addition to hiding certain items, an application can modify the text and icon displayed for the item by handling the **DSBM\_QUERYINSERT** notification.</span></span> <span data-ttu-id="1ee22-126">Weitere Informationen finden Sie unter [**dsbitem**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema).</span><span class="sxs-lookup"><span data-stu-id="1ee22-126">For more information, see [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema).</span></span>

<span data-ttu-id="1ee22-127">Die [**bffcallback**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) -Funktion kann die **\_ initialisierte bffm** -Benachrichtigung verwenden, um das Handle des Dialog Felds abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1ee22-127">The [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) function can use the **BFFM\_INITIALIZED** notification to obtain the handle of the dialog box.</span></span> <span data-ttu-id="1ee22-128">Die Anwendung kann dieses Handle verwenden, um Nachrichten, wie z. **b. bffm \_ enableok**, an das Dialogfeld zu senden.</span><span class="sxs-lookup"><span data-stu-id="1ee22-128">The application can use this handle to send messages, such as **BFFM\_ENABLEOK**, to the dialog box.</span></span> <span data-ttu-id="1ee22-129">Weitere Informationen zu den Nachrichten, die an das Dialogfeld gesendet werden können, finden Sie unter [**bffcallback**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback).</span><span class="sxs-lookup"><span data-stu-id="1ee22-129">For more information about the messages that can be sent to the dialog box, see [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback).</span></span>

<span data-ttu-id="1ee22-130">Das Dialogfeld Handle kann auch verwendet werden, um direkten Zugriff auf die Steuerelemente im Dialogfeld zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1ee22-130">The dialog box handle can also be used to gain direct access to the controls in the dialog box.</span></span> <span data-ttu-id="1ee22-131">**Dsbid \_ Banner** ist der Bezeichner für das statische Text Steuerelement, in dem der **psztitle** -Member der [**dsbrowseinfo**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa) -Struktur angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1ee22-131">**DSBID\_BANNER** is the identifier for the static text control that the **pszTitle** member of the [**DSBROWSEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa) structure is displayed in.</span></span> <span data-ttu-id="1ee22-132">**Dsbid \_ Containerlist** ist der Bezeichner des Strukturansicht-Steuer Elements, mit dem der Inhalt der Struktur angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1ee22-132">**DSBID\_CONTAINERLIST** is the identifier of the tree view control used to display the tree contents.</span></span> <span data-ttu-id="1ee22-133">Die Verwendung dieser Elemente sollte nach Möglichkeit vermieden werden, um zukünftige Probleme mit der Anwendungs Kompatibilität zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="1ee22-133">Use of these items should be avoided, if possible, to prevent future application compatibility problems.</span></span>

<span data-ttu-id="1ee22-134">Im folgenden C++-Codebeispiel wird gezeigt, wie die [**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) -Funktion verwendet wird, um das Dialogfeld "Container Browser" zu erstellen und eine [**bffcallback**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) -Funktion zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="1ee22-134">The following C++ code example shows how to use the [**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) function to create the container browser dialog box and implement a [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) function.</span></span> <span data-ttu-id="1ee22-135">[**Bffcallback**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) verwendet die **DSBM- \_ queryinsert** -Benachrichtigung, um den anzeigen Amen für jedes Element in den Distinguished Name des Elements zu ändern.</span><span class="sxs-lookup"><span data-stu-id="1ee22-135">The [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) uses the **DSBM\_QUERYINSERT** notification to change the display name for each item to the distinguished name of the item.</span></span>


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



 

 