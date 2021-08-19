---
title: Die OnCreate-Methode
description: Die OnCreate-Methode
ms.assetid: b23546b3-968f-41d8-ba07-3d694152c3ed
keywords:
- Windows Media Player Plug-Ins, OnCreate-Methode
- Plug-Ins, OnCreate-Methode
- Benutzeroberflächen-Plug-Ins, OnCreate-Methode
- UI-Plug-Ins, OnCreate-Methode
- OnCreate-Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac52b1c58c6799f89d29fb1ee24c09767fee26729e760b2b454f1a359bd57596
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118118108"
---
# <a name="the-oncreate-method"></a>Die OnCreate-Methode

Die OnCreate-Methode wird aufgerufen, wenn das Plug-In-Fenster zum ersten Mal erstellt wird.

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



Diese Methode erstellt die Schaltfläche **Suchen** und ordnet sie der IDC \_ SEARCH-Befehls-ID zu, die am Anfang der Datei definiert ist:


```C++
#define IDC_SEARCH 2000

```



Diese Befehls-ID wird der OnSearch-Methode im zuvor beschriebenen Meldungszuordnungsabschnitt zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren von CPluginWindow**](implementing-cpluginwindow.md)
</dt> </dl>

 

 




