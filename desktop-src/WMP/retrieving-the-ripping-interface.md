---
title: Abrufen der Rippingschnittstelle
description: Abrufen der Rippingschnittstelle
ms.assetid: 760610eb-e356-4b50-b865-53557ba9b815
keywords:
- Windows Media Player, CD-einreißen
- Windows Media Player-Objektmodell, CD-einreißen
- Objektmodell, CD-einreißen
- Windows Media Player ActiveX-Steuerelement, CD-einreißen
- ActiveX-Steuerelement, CD-einreißen
- Windows Media Player Mobile ActiveX-Steuerelement, CD-einreißen
- Windows Media Player Mobile, CD-einreißen
- CD-Ripping, iwmpcdromrip-Schnittstelle
- einreißen CDs, iwmpcdromrip-Schnittstelle
- Iwmpcdromrip-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 903fa285404700e35363a94239c79706e7af0e34
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "103858076"
---
# <a name="retrieving-the-ripping-interface"></a>Abrufen der Rippingschnittstelle

Um die CD-Laufwerke auf dem Computer des Benutzers aufzulisten, verwenden Sie die **iwmpcdromcollection** -Schnittstelle. Rufen Sie einen Zeiger auf diese Schnittstelle ab, indem [Sie iwmpcore:: get \_ cdromcollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection)aufrufen.

Mithilfe der [get \_ count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-get_count) -und [Item](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-item) -Methoden können Sie die Auflistung durchlaufen, um eine [iwmpcdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) -Schnittstelle für jedes CD-Laufwerk auf dem Computer des Benutzers abzurufen.

Die **iwmpcdrom** -Schnittstelle stellt ein einzelnes CD-Laufwerk dar. Bevor Sie mit dem Einreißen einer CD beginnen, müssen Sie zuerst **QueryInterface** über einen **iwmpcdrom** -Zeiger aufrufen, um die [iwmpcdromrip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) -Schnittstelle abzurufen.

Im folgenden Codebeispiel wird veranschaulicht, wie Sie eine Schnittstelle zum einreißen einer CD von einem bestimmten Laufwerk abrufen:


```C++
HRESULT CMainDlg::GetCdromDriveCount (long &lDriveCount)
{
    HRESULT hr = m_spPlayer->get_cdromCollection(&m_spCdromCollection);

    // Get the number of CDROM drives.
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromCollection->get_count(&lDriveCount);
    }

    return hr;
}

// lIndex refers to the index of the current drive,
// which must be less than the value retrieved by
// GetCdromDriveCount above.
HRESULT CMainDlg::GetCdromRipInterface (long lIndex)
{
    // Get the IWMPCdrom interface.
    m_spCdrom.Release();
    HRESULT hr = m_spCdromCollection->item(lIndex, &m_spCdrom);
    if (SUCCEEDED(hr))
    {
        // Get the IWMPCdromRip interface.
        m_spCdromRip.Release();
        hr = m_spCdrom->QueryInterface(&m_spCdromRip);
    }

    return hr;
}

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Ripping einer CD**](ripping-a-cd.md)
</dt> <dt>

[**Der RIP-Prozess wird gestartet.**](starting-the-rip-process.md)
</dt> <dt>

[**Abrufen des Status "RIP"**](retrieving-the-rip-status.md)
</dt> <dt>

[**Auswählen von Elementen für das Ripping**](selecting-items-for-ripping.md)
</dt> <dt>

[**Iwmpcdromcollection-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> </dl>

 

 




