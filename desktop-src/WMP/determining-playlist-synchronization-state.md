---
title: Status der Wiedergabelisten Synchronisierung
description: Status der Wiedergabelisten Synchronisierung
ms.assetid: 634b659b-c3ae-4957-b17e-18fd92e915be
keywords:
- Windows Media Player, Synchronisierungs Wiedergabelisten
- Windows Media Player-Objektmodell, Synchronisierungs Wiedergabelisten
- Objektmodell, Synchronisierungs Wiedergabelisten
- Windows Media Player Mobile, Synchronisierungs Wiedergabelisten
- Windows Media Player ActiveX-Steuerelement, Synchronisierungs Wiedergabelisten
- Windows Media Player Mobile ActiveX-Steuerelement, Synchronisierungs Wiedergabelisten
- ActiveX-Steuerung, Synchronisierungs Wiedergabelisten
- Wiedergabelisten, Synchronisierung
- Metadatei-Wiedergabelisten, Synchronisierung
- Windows Media Metadatei-Wiedergabelisten, Synchronisierung
- Portable Geräte, bestimmen des Status der Synchronisierungs Wiedergabe
- Synchronisierungs Wiedergabelisten, Synchronisierungs Status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9758cfbb73c698a40d6d4f48e645e57750d8a332
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106337207"
---
# <a name="determining-playlist-synchronization-state"></a>Status der Wiedergabelisten Synchronisierung

Windows Media Player 10 oder höher verwendet das **SyncState** -Attribut, um Informationen darüber zu erhalten, ob eine bestimmte digitale Mediendatei auf ein tragbares Gerät kopiert wurde, und im Falle eines Fehlers, ob das Kopieren fehlgeschlagen ist, da das Gerät nicht über genügend Arbeitsspeicher verfügt.

Im folgenden Beispielcode wird eine Funktion erstellt, die diese Informationen aus einer digitalen Mediendatei abruft. Die Funktion übernimmt die folgenden Parameter:

-   *pmedia*. Zeiger auf eine **iwmpmedia** -Schnittstelle, die die zu überprüfende digitale Mediendatei darstellt.
-   *lpsindex*: Der Partnerschafts Index des aktuellen Geräts.
-   *pulondevice*. Zeiger auf eine **Long** -Variable, die den Wert empfängt, der angibt, ob die digitale Mediendatei auf das Gerät kopiert wurde.
-   *puldidnotfit*. Zeiger auf eine **Long** -Variable, die den Wert empfängt, der angibt, ob der Kopiervorgang fehlgeschlagen ist, da das Gerät nicht über genügend Arbeitsspeicher verfügt.

Die im **SyncState** -Attribut enthaltenen Informationen werden bitweise codiert. Sie können sehen, wie diese Funktion im Beispielcode zum Auflisten [der Medienelemente](enumerating-the-media-items.md)verwendet wird.


```C++
STDMETHODIMP CSyncSettings::GetPartnershipSyncState(IWMPMedia* pMedia, long lPsIndex, ULONG *pulOnDevice, ULONG *pulDidNotFit)
{
    ATLASSERT(pMedia); 
    ATLASSERT(lPsIndex > 0 && 
              lPsIndex < 17);
    ATLASSERT(pulOnDevice);
    ATLASSERT(pulDidNotFit);
  
    CComVariant varSyncStateVal;   
    CComPtr<IWMPMedia> spMedia(pMedia); 
    CComPtr<IWMPMedia3> spMedia3;     
    HRESULT hr = spMedia.QueryInterface(&spMedia3); 
    ULONG ulSyncState = 0; // Stores the ulVal member of varSyncStateVal. 
    ULONG lLSB = 0; // Represents least significant bit: Did the media fail to copy because it would not fit?
    ULONG lMSB = 0; // Represents most significant bit: Is the media on the device?

    // Calculate the bit shift required to isolate the partnership bit 
    // pair from the SyncState attribute.
    const int iRshift = (lPsIndex - 1) * 2;

    if(SUCCEEDED(hr) && spMedia3)
    {       
        hr = spMedia3->getItemInfoByType(CComBSTR("SyncState"), CComBSTR(""), 0, &varSyncStateVal);
    }

    if(SUCCEEDED(hr) && varSyncStateVal.vt == VT_UI4)
    {   
        // Get the value.
        ulSyncState = varSyncStateVal.ulVal;

        // Shift the bit pair to the rightmost position.
        ulSyncState >>= iRshift; 

        // Mask the rightmost bit pair.
        ulSyncState &= 3;

        // Get the LSB         
        lLSB = ulSyncState & ~2; // Sets the 2E1 bit to zero. 

        // Get the MSB
        ulSyncState >>= 1;
        lMSB = ulSyncState;       
    }

    // Return the bits.
    *pulOnDevice = lMSB;
    *pulDidNotFit = lLSB;

    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmpmedia-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[**IWMPMedia3:: getItemInfoByType**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia3-getiteminfobytype)
</dt> <dt>

[**Synchronisierungs Wiedergabelisten**](managing-synchronization-playlists.md)
</dt> <dt>

[**SyncState-Attribut**](syncstate-attribute.md)
</dt> </dl>

 

 




