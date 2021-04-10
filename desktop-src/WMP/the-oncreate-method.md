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
# <a name="the-oncreate-method"></a>Die OnCreate-Methode

Die OnCreate-Methode wird aufgerufen, wenn das Plug-in-Fenster zum ersten Mal erstellt wird.

Der folgende Code wird verwendet, um diese Methode zu implementieren:


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



Diese Methode erstellt die **Such** Schaltfläche und ordnet Sie der IDC- \_ Such Befehls-ID zu, die am Anfang der Datei definiert wird:


```C++
#define IDC_SEARCH 2000

```



Diese Befehls-ID wird der onSearch-Methode im zuvor beschriebenen Abschnitt Message Map zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren von cpluginwindow**](implementing-cpluginwindow.md)
</dt> </dl>

 

 




