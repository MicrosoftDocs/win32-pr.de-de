---
title: Abrufen der Schnittstelle zum Brennen von CDs
description: Abrufen der Schnittstelle zum Brennen von CDs
ms.assetid: d52f7b27-a327-4656-8dc2-0b075264d295
keywords:
- Windows Media Player, CD-brennen
- Windows Media Player-Objektmodell, CD-brennen
- Objektmodell, CD-brennen
- Windows Media Player ActiveX-Steuerelement, CD-brennen
- ActiveX-Steuerelement, CD-brennen
- Windows Media Player Mobile ActiveX-Steuerelement, CD-brennen
- Windows Media Player Mobile, CD-brennen
- CD-brennen, Abrufen der iwmpcdromcollection-Schnittstelle
- Brennen von CDs, Abrufen der iwmpcdromcollection-Schnittstelle
- Iwmpcdromcollection-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b63763f9dd99bbaf88ae099edb53ba072cd1a25e
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104038671"
---
# <a name="retrieving-the-cd-burning-interface"></a>Abrufen der Schnittstelle zum Brennen von CDs

Um die CD-Laufwerke auf dem Computer des Benutzers aufzulisten, verwenden Sie die **iwmpcdromcollection** -Schnittstelle. Sie rufen einen Zeiger auf diese Schnittstelle ab, indem Sie [iwmpcore:: get \_ cdromcollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection)aufrufen.

Mithilfe der **get \_ count** -und **Item** -Methoden können Sie die Auflistung durchlaufen, um einen [iwmpcdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) -Schnittstellen Zeiger für jedes CD-Laufwerk auf dem Computer des Benutzers abzurufen.

Die **iwmpcdrom** -Schnittstelle stellt ein einzelnes CD-Laufwerk dar. Bevor Sie mit dem Brennen einer CD beginnen, müssen Sie zuerst **QueryInterface** über einen **iwmpcdrom** -Zeiger aufrufen, um einen Zeiger auf die [iwmpcdromburn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) -Schnittstelle abzurufen.

Im folgenden Codebeispiel wird veranschaulicht, wie Sie eine Schnittstelle zum Brennen einer CD auf einem bestimmten Laufwerk abrufen:


```C++
HRESULT CMainDlg::GetCdromDriveCount (long &lDriveCount)
{
    hr = m_spPlayer->get_cdromCollection(&m_spCdromCollection);

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
HRESULT CMainDlg::GetCdromBurnInterface (long lIndex)
{
    // Get the IWMPCdrom interface.
    m_spCdrom.Release();
    HRESULT hr = m_spCdromCollection->item(lIndex, &m_spCdrom);
    if (SUCCEEDED(hr))
    {
        // Get the IWMPCdromBurn interface.
        m_spCdromBurn.Release();
        hr = m_spCdrom->QueryInterface(&m_spCdromBurn);
    }

    return hr;
}

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Brennen einer CD**](burning-a-cd.md)
</dt> <dt>

[**Der Verbrennungsprozess wird gestartet.**](starting-the-burn-process.md)
</dt> <dt>

[**Löschen einer erneut beschreibbaren CD**](erasing-a-rewritable-cd.md)
</dt> <dt>

[**Abrufen des Laufwerks und des Festplatten Status**](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[**Abrufen des Verbrauchs Status**](retrieving-the-burn-status.md)
</dt> <dt>

[**Iwmpcdromcollection-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> </dl>

 

 




