---
title: Abrufen des Laufwerks und des Festplatten Status
description: Abrufen des Laufwerks und des Festplatten Status
ms.assetid: 5e3e6107-d2bc-450c-a86e-5d3ef7b3092a
keywords:
- Windows Media Player, CD-brennen
- Windows Media Player-Objektmodell, CD-brennen
- Objektmodell, CD-brennen
- Windows Media Player ActiveX-Steuerelement, CD-brennen
- ActiveX-Steuerelement, CD-brennen
- Windows Media Player Mobile ActiveX-Steuerelement, CD-brennen
- Windows Media Player Mobile, CD-brennen
- CD-brennen, Abrufen von Laufwerk-und Festplatten Status
- Brennen von CDs, Abrufen von Laufwerks-und Festplatten Status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eab66581c336f642fd53b22f81949847d0a1c89
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103858024"
---
# <a name="retrieving-the-drive-and-disc-status"></a>Abrufen des Laufwerks und des Festplatten Status

Vor dem Starten eines CD-Brennvorgangs müssen Sie sicherstellen, dass das ausgewählte CD-ROM-Laufwerk den Vorgang unterstützt, den Sie ausführen möchten. Beispielsweise müssen Sie überprüfen, ob eine CD gelöscht werden kann, bevor Sie [iwmpcdromburn:: Erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase)aufrufen. Der folgende Code zeigt ein Beispiel für die Verwendung von [iwmpcdromburn:: IsAvailable](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-isavailable) , um zu bestimmen, ob ein Vorgang unterstützt wird:


```C++
VARIANT_BOOL vbResult;
    
// Check whether this drive can burn CDs.
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("Burn");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->isAvailable(bstrItem, &vbResult);
}
if (SUCCEEDED(hr))
{
    if (VARIANT_TRUE == vbResult)
    {
        // The current drive can burn CDs.
    }
}

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Brennen einer CD**](burning-a-cd.md)
</dt> <dt>

[**Abrufen der Schnittstelle zum Brennen von CDs**](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[**Der Verbrennungsprozess wird gestartet.**](starting-the-burn-process.md)
</dt> <dt>

[**Löschen einer erneut beschreibbaren CD**](erasing-a-rewritable-cd.md)
</dt> <dt>

[**Abrufen des Verbrauchs Status**](retrieving-the-burn-status.md)
</dt> </dl>

 

 




