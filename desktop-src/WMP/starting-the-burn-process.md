---
title: Starten des Burn-Prozesses
description: Starten des Burn-Prozesses
ms.assetid: 91442bd2-1a68-465c-b865-63d309f33d55
keywords:
- Windows Media Player,CD-1600
- Windows Media Player Objektmodell, CD-Platte
- Objektmodell, CD-Umrechnung
- Windows Media Player ActiveX,CD-Gesteuerte
- ActiveX-Steuerelement, CD-Gesteuerte
- Windows Media Player Mobile ActiveX-Steuerelement, CD-Gesteuerte
- Windows Media Player Mobil, CD-Platte
- CD-Platte,Starten des Burn-Prozesses
- CDs für Das Starten des Burn-Prozesses
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50f5620ba8fa6ab911cf0fd594fd27f139b5061d1383575f861dadfec45dabbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995080"
---
# <a name="starting-the-burn-process"></a>Starten des Burn-Prozesses

Bevor sie beginnen kann, müssen Sie eine Wiedergabeliste zuweisen, die verbraucht werden soll. Geben Sie mit [IWMPC csvLive::p ut \_ burnPlaylist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnplaylist) eine Wiedergabeliste für die Wiedergabeliste an.


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



Informationen zur Verwendung von Wiedergabelisten finden Sie unter [IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist).

Um den Vorgang zu starten, rufen [Sie IWMPC csv Überschreiben::start Überschreiben](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-startburn)auf.


```C++
// Start burning.
hr = m_spCdromBurn->startBurn();

```



Sie können den Vorgang zum Beenden des Vorgangs beenden, indem [Sie IWMPCaku Überschn.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-stopburn)


```C++
// Stop burning.
hr = m_spCdromBurn->stopBurn();

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Ausknänden einer CD**](burning-a-cd.md)
</dt> <dt>

[**Abrufen der Schnittstelle zum Brennen von CDs**](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[**Löschen einer erneut beschreibbaren CD**](erasing-a-rewritable-cd.md)
</dt> <dt>

[**Abrufen des Laufwerk- und Datenträgerstatus**](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[**Abrufen des Burn-Status**](retrieving-the-burn-status.md)
</dt> </dl>

 

 




