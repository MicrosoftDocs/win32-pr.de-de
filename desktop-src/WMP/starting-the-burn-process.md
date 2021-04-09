---
title: Der Verbrennungsprozess wird gestartet.
description: Der Verbrennungsprozess wird gestartet.
ms.assetid: 91442bd2-1a68-465c-b865-63d309f33d55
keywords:
- Windows Media Player, CD-brennen
- Windows Media Player-Objektmodell, CD-brennen
- Objektmodell, CD-brennen
- Windows Media Player ActiveX-Steuerelement, CD-brennen
- ActiveX-Steuerelement, CD-brennen
- Windows Media Player Mobile ActiveX-Steuerelement, CD-brennen
- Windows Media Player Mobile, CD-brennen
- CD-brennen, Startvorgang zum Brennen
- Brennen von CDs, Starten des Brennvorgangs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4a35f473eebe35bffd48ac802dcfe79082689de
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103948446"
---
# <a name="starting-the-burn-process"></a>Der Verbrennungsprozess wird gestartet.

Bevor Sie beginnen können, müssen Sie eine Wiedergabeliste zum Brennen zuweisen. Verwenden Sie [iwmpcdromburn::p UT \_ burnwiedergabe](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnplaylist) , um eine Wiedergabeliste zum Brennen anzugeben.


```C++
HRESULT CMainDlg::PutPlaylist (void)
{
    // Specify the burn playlist.   
    HRESULT hr = m_spCdromBurn->put_burnPlaylist(m_spPlaylist);

    // Update the status information.
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromBurn->refreshStatus();
    }

    return hr;
}

```



Weitere Informationen zum Verwenden von Wiedergabelisten finden Sie unter [iwmpwiedergabe](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist).

Um den Brennvorgang zu starten, nennen Sie [iwmpcdromburn:: startburn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-startburn).


```C++
// Start burning.
hr = m_spCdromBurn->startBurn();

```



Sie können den Brennvorgang beenden, indem Sie [iwmpcdromburn:: stopburn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-stopburn)aufrufen.


```C++
// Stop burning.
hr = m_spCdromBurn->stopBurn();

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Brennen einer CD**](burning-a-cd.md)
</dt> <dt>

[**Abrufen der Schnittstelle zum Brennen von CDs**](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[**Löschen einer erneut beschreibbaren CD**](erasing-a-rewritable-cd.md)
</dt> <dt>

[**Abrufen des Laufwerks und des Festplatten Status**](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[**Abrufen des Verbrauchs Status**](retrieving-the-burn-status.md)
</dt> </dl>

 

 




