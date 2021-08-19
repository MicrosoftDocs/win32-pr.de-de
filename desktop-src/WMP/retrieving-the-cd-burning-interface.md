---
title: Abrufen der Schnittstelle zum Brennen von CDs
description: Abrufen der Schnittstelle zum Brennen von CDs
ms.assetid: d52f7b27-a327-4656-8dc2-0b075264d295
keywords:
- Windows Media Player,CD-1
- Windows Media Player-Objektmodell,CD-Endung
- Objektmodell, CD-1
- Windows Media Player ActiveX,CD-Sicherung
- ActiveX-Steuerelement,CD-Endung
- Windows Media Player Mobile ActiveX-Steuerelement, CD-Steuerung
- Windows Media Player Mobil, CD-1
- CD-Auflistung,Abrufen der IWMPCcollection-Schnittstelle
- '- CDs,Abrufen der IWMPCcollection-Schnittstelle'
- IWMPCcollection-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84013d5df4244fc30c9cb52e3447d15f60e559befe1223f0964934dd8ca1e1cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123200"
---
# <a name="retrieving-the-cd-burning-interface"></a>Abrufen der Schnittstelle zum Brennen von CDs

Um die CD-Laufwerke auf dem Computer des Benutzers aufzählen zu können, verwenden Sie **die IWMPCcollection-Schnittstelle.** Sie rufen einen Zeiger auf diese Schnittstelle ab, indem Sie [IWMPCore::get \_ ccollection aufrufen.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection)

Mithilfe der **Methoden "get \_ count"** und **"item"** können Sie die Sammlung iterieren, um einen [IWMPC interface-Zeiger](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) für jedes CD-Laufwerk auf dem Computer des Benutzers abzurufen.

Die **IWMPC cri-Schnittstelle** stellt ein einzelnes CD-Laufwerk dar. Bevor Sie mit dem Erstellen einer CD beginnen, müssen Sie **zunächst QueryInterface** über einen **IWMPCführungszeiger** aufrufen, um einen Zeiger auf die [IWMPCleitschnittstelle](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) abzurufen.

Im folgenden Codebeispiel wird veranschaulicht, wie eine Schnittstelle abgerufen wird, um eine CD auf einem bestimmten Laufwerk zu installieren:


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

[**Erstellen einer CD**](burning-a-cd.md)
</dt> <dt>

[**Starten des Burn-Prozesses**](starting-the-burn-process.md)
</dt> <dt>

[**Löschen einer erneut beschreibbaren CD**](erasing-a-rewritable-cd.md)
</dt> <dt>

[**Abrufen des Laufwerk- und Datenträgerstatus**](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[**Abrufen des Burn-Status**](retrieving-the-burn-status.md)
</dt> <dt>

[**IWMPCcollection-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> </dl>

 

 




