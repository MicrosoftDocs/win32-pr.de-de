---
title: Die OnSearch-Methode
description: Die OnSearch-Methode
ms.assetid: 709bb428-1a5e-4b8d-8622-5fcc816f0a1a
keywords:
- Windows Media Player-Plug-Ins, OnSearch-Methode
- Plug-Ins, OnSearch-Methode
- Benutzeroberflächen-Plug-Ins, OnSearch-Methode
- Benutzeroberflächen-Plug-Ins, OnSearch-Methode
- OnSearch-Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49ab5cb4b26d291a940ed329e2422240e6fc36e5ba980431af169d58f1398fdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118118000"
---
# <a name="the-onsearch-method"></a>Die OnSearch-Methode

Die OnSearch-Methode wird von Windows Media Player, wenn auf die **Schaltfläche** Suchen geklickt wird. Diese Methode ruft das aktuelle **Media-Objekt** ab und übergibt es an die LaunchPage-Methode.

Der folgende Code wird verwendet, um diese Methode zu implementieren:


```C++
LRESULT OnSearch(WORD wNotifyCode, WORD wID, HWND hwndCtl, BOOL& fHandled)
{
    HRESULT hr;
    CComPtr<IWMPMedia> spMedia;

    if( m_pPlugin && m_pPlugin->m_spCore )
    {
        // Get a pointer to the current media item.
        hr = m_pPlugin->m_spCore->get_currentMedia(&spMedia);
        if (SUCCEEDED(hr) && spMedia)
        {
            LaunchPage(spMedia);
        }
    else
        {
            MessageBox(_T("There is no media loaded."), _T("Warn"), MB_OK | MB_ICONWARNING);
        }
    }
    return 0;
}

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren von CPluginWindow**](implementing-cpluginwindow.md)
</dt> </dl>

 

 




