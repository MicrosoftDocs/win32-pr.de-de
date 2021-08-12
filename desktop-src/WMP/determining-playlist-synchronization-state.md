---
title: Bestimmen des Wiedergabelistensynchronisierungsstatus
description: Bestimmen des Wiedergabelistensynchronisierungsstatus
ms.assetid: 634b659b-c3ae-4957-b17e-18fd92e915be
keywords:
- Windows Media Player, Synchronisierungswiedergabelisten
- Windows Media Player Objektmodell, Synchronisierungswiedergabelisten
- Objektmodell, Synchronisierungswiedergabelisten
- Windows Media Player Mobile Wiedergabelisten, Synchronisierungswiedergabelisten
- Windows Media Player ActiveX-Steuerelement, Synchronisierungswiedergabelisten
- Windows Media Player Mobile ActiveX-Steuerelement, Wiedergabelisten für die Synchronisierung
- ActiveX-Steuerelement, Synchronisierungswiedergabelisten
- Wiedergabelisten, Synchronisierung
- Metafile-Wiedergabelisten, Synchronisierung
- Windows Medienmetadatei-Wiedergabelisten, Synchronisierung
- Portable Geräte, Bestimmen des Wiedergabelistenzustands der Synchronisierung
- Synchronisierungswiedergabelisten, Synchronisierungsstatus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14af59f66d1b21eac00208ecc805f756761256e47a35042694bcd65e6f96558
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118579459"
---
# <a name="determining-playlist-synchronization-state"></a>Bestimmen des Wiedergabelistensynchronisierungsstatus

Windows Media Player 10 oder höher verwendet das **SyncState-Attribut,** um Informationen darüber zu enthalten, ob eine bestimmte digitale Mediendatei auf ein portables Gerät kopiert wurde, und im Fall eines Fehlers, ob beim Kopieren ein Fehler aufgetreten ist, weil das Gerät nicht über genügend Arbeitsspeicher verfügte.

Der folgende Beispielcode erstellt eine Funktion, die diese Informationen aus einer digitalen Mediendatei abruft. Die Funktion verwendet die folgenden Parameter:

-   *pMedia*. Zeiger auf eine **IWMPMedia-Schnittstelle,** die die zu überprüfende digitale Mediendatei darstellt.
-   *lPsIndex*. Partnerschaftsindex des aktuellen Geräts.
-   *pulOnDevice*. Zeiger auf  eine long-Variable, die den Wert empfängt, der angibt, ob die digitale Mediendatei auf das Gerät kopiert wurde.
-   *pulDidNotFit*. Zeiger auf  eine long-Variable, die den Wert empfängt, der angibt, ob beim Kopiervorgang ein Fehler aufgetreten ist, weil das Gerät nicht über genügend Arbeitsspeicher verfügte.

Die im **SyncState-Attribut** enthaltenen Informationen werden bitweise codiert. Wie diese Funktion verwendet wird, erfahren Sie im Beispielcode unter [Aufzählen der Medienelemente.](enumerating-the-media-items.md)


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

[**IWMPMedia-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[**IWMPMedia3::getItemInfoByType**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia3-getiteminfobytype)
</dt> <dt>

[**Verwalten von Synchronisierungswiedergabelisten**](managing-synchronization-playlists.md)
</dt> <dt>

[**SyncState-Attribut**](syncstate-attribute.md)
</dt> </dl>

 

 




