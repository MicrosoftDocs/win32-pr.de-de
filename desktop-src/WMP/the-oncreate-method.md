---
title: Die OnCreate-Methode
description: Die OnCreate-Methode
ms.assetid: b23546b3-968f-41d8-ba07-3d694152c3ed
keywords:
- Windows Media Player-Plug-ins, OnCreate-Methode
- Plug-ins, OnCreate-Methode
- Benutzeroberflächen-Plug-ins, OnCreate-Methode
- UI-Plug-ins, OnCreate-Methode
- OnCreate-Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d896ed9ebc6e9dc2bff9ff24ad23d50f7905c24
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855511"
---
# <a name="the-oncreate-method"></a><span data-ttu-id="b9f04-108">Die OnCreate-Methode</span><span class="sxs-lookup"><span data-stu-id="b9f04-108">The OnCreate Method</span></span>

<span data-ttu-id="b9f04-109">Die OnCreate-Methode wird aufgerufen, wenn das Plug-in-Fenster zum ersten Mal erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b9f04-109">The OnCreate method is called when the plug-in window is first created.</span></span>

<span data-ttu-id="b9f04-110">Der folgende Code wird verwendet, um diese Methode zu implementieren:</span><span class="sxs-lookup"><span data-stu-id="b9f04-110">The following code is used to implement this method:</span></span>


```C++
LRESULT OnCreate(UINT uMsg, WPARAM wParam, LPARAM lParam, BOOL& bHandled)
{
    HWND hCtrl = ::CreateWindowEx(0L, _T("BUTTON"), _T("Search"),
        WS_CHILD | BS_PUSHBUTTON, 10, 10, 100, 30, m_hWnd, 
        (HMENU)IDC_SEARCH, _Module.GetResourceInstance(), NULL);
    ::ShowWindow(hCtrl, SW_SHOW );
    return 0;
}

```



<span data-ttu-id="b9f04-111">Diese Methode erstellt die **Such** Schaltfläche und ordnet Sie der IDC- \_ Such Befehls-ID zu, die am Anfang der Datei definiert wird:</span><span class="sxs-lookup"><span data-stu-id="b9f04-111">This method creates the **Search** button and associates it with the IDC\_SEARCH command ID, which is defined at the beginning of the file:</span></span>


```C++
#define IDC_SEARCH 2000

```



<span data-ttu-id="b9f04-112">Diese Befehls-ID wird der onSearch-Methode im zuvor beschriebenen Abschnitt Message Map zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="b9f04-112">This command ID is mapped to the OnSearch method in the message map section described previously.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9f04-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b9f04-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9f04-114">**Implementieren von cpluginwindow**</span><span class="sxs-lookup"><span data-stu-id="b9f04-114">**Implementing CPluginWindow**</span></span>](implementing-cpluginwindow.md)
</dt> </dl>

 

 




