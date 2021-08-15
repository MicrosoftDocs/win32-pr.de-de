---
title: Abrufen des Laufwerk- und Datenträgerstatus
description: Abrufen des Laufwerk- und Datenträgerstatus
ms.assetid: 5e3e6107-d2bc-450c-a86e-5d3ef7b3092a
keywords:
- Windows Media Player,CD-1
- Windows Media Player-Objektmodell,CD-1
- Objektmodell, CD-1
- Windows Media Player ActiveX,CD-1
- ActiveX,CD-1
- Windows Media Player Mobile ActiveX-Steuerelement, CD-Steuerung
- Windows Media Player Mobil, CD-1
- CD-10,Abrufen des Laufwerks- und Datenträgerstatus
- '- CDs, Abrufen des Laufwerks- und Datenträgerstatus'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 664315972158b4cf68e7f766f98be095a27d7fa8496f983305cc6baaafe784d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746272"
---
# <a name="retrieving-the-drive-and-disc-status"></a>Abrufen des Laufwerk- und Datenträgerstatus

Bevor Sie einen CD-Vorgang starten, müssen Sie sicherstellen, dass das ausgewählte CD-ROM-Laufwerk den Vorgang unterstützt, den Sie ausführen möchten. Sie müssen z. B. überprüfen, ob eine CD gelöscht werden kann, bevor [Sie IWMPC datei::erase aufrufen.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase) Der folgende Code zeigt ein Beispiel für die Verwendung [von IWMPC wie folgt: :isAvailable,](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-isavailable) um zu bestimmen, ob ein Vorgang unterstützt wird:


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

[**Erstellen einer CD**](burning-a-cd.md)
</dt> <dt>

[**Abrufen der Schnittstelle zum Brennen von CDs**](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[**Starten des Burn-Prozesses**](starting-the-burn-process.md)
</dt> <dt>

[**Löschen einer erneut beschreibbaren CD**](erasing-a-rewritable-cd.md)
</dt> <dt>

[**Abrufen des Burn-Status**](retrieving-the-burn-status.md)
</dt> </dl>

 

 




