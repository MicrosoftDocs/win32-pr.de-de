---
title: Abrufen der Rippingschnittstelle
description: Abrufen der Rippingschnittstelle
ms.assetid: 760610eb-e356-4b50-b865-53557ba9b815
keywords:
- Windows Media Player,CD-Lässing
- Windows Media Player-Objektmodell,CD-Bebauung
- Objektmodell,CD-Bebauung
- Windows Media Player ActiveX,CD-Kontrolle
- ActiveX,CD-Steuerung
- Windows Media Player Mobile ActiveX,CD-Steuerung
- Windows Media Player Mobil, CD-10
- CD-Benutzeroberfläche, IWMPCiererRip-Schnittstelle
- -CDs, IWMPCiererRip-Schnittstelle
- IWMPCiererRip-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2179e4f38eee121d7b8fefc028adf232eb724264362396c8cacedfcc55b162d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002550"
---
# <a name="retrieving-the-ripping-interface"></a>Abrufen der Rippingschnittstelle

Um die CD-Laufwerke auf dem Computer des Benutzers aufzählen zu können, verwenden Sie **die IWMPCcollection-Schnittstelle.** Rufen Sie einen Zeiger auf diese Schnittstelle ab, indem [Sie IWMPCore::get \_ ccollection aufrufen.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection)

Mithilfe der [Methoden get \_ count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-get_count) und [item](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-item) können Sie die Sammlung iterieren, um eine [IWMPCome-Schnittstelle](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) für jedes CD-Laufwerk auf dem Computer des Benutzers abzurufen.

Die **IWMPC cri-Schnittstelle** stellt ein einzelnes CD-Laufwerk dar. Bevor Sie mit dem Erstellen einer CD beginnen, müssen Sie **zunächst QueryInterface** über einen **IWMPCome-Zeiger** aufrufen, um die [IWMPCiusRip-Schnittstelle abzurufen.](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)

Im folgenden Codebeispiel wird veranschaulicht, wie sie eine Schnittstelle zum Beschriften einer CD von einem bestimmten Laufwerk abrufen:


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

[**Erstellen einer CD**](ripping-a-cd.md)
</dt> <dt>

[**Starten des Reißprozesses**](starting-the-rip-process.md)
</dt> <dt>

[**Abrufen des Reißstatus**](retrieving-the-rip-status.md)
</dt> <dt>

[**Auswählen von Elementen für "Besendung"**](selecting-items-for-ripping.md)
</dt> <dt>

[**IWMPCcollection-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> </dl>

 

 




