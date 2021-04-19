---
description: Dienst Schnittstellen
ms.assetid: 264a0e86-49e9-4777-956b-a83e9db52a25
title: Dienst Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31687cc1c1283eb59c7731743eaf4ece0127b392
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349082"
---
# <a name="service-interfaces"></a>Dienst Schnittstellen

Einige Schnittstellen in Media Foundation müssen durch Aufrufen von [**imfgetservice:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) abgerufen werden, anstatt durch Aufrufen von **QueryInterface**. Die [**GetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) -Methode funktioniert wie QueryInterface, aber mit den folgenden unterschieden:

-   Zusätzlich zum Schnittstellen Bezeichner wird eine dienstbezeichnerguid benötigt.
-   Es kann einen Zeiger auf ein anderes Objekt zurückgeben, das die-Schnittstelle implementiert, anstatt einen Zeiger auf das ursprüngliche Objekt zurückzugeben, das abgefragt wird.

> [!Note]  
> Die [**imfgetservice**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) -Schnittstelle ähnelt der **IServiceProvider** -Schnittstelle, die in einigen anderen APIs verwendet wird.

 

Bei einem *Dienst* handelt es sich um eine bestimmte Schnittstelle, die von einer bestimmten Objektklasse über die [**IMF GetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) -Schnittstelle abgerufen wird Die folgenden Dienste sind definiert.



| Dienst Bezeichner                          | Schnittstelle                                                                                                                                | Objekte, die diesen Dienst möglicherweise verfügbar machen                                                                                                            |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| MF \_ - \_ Metadatenanbieter- \_ Dienst             | [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)                                                                                       | Medienquellen                                                                                                                                     |
| MF- \_ MediaSource- \_ Dienst                    | [**Imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                                                                                                 | Wird in Windows 8.1 und höher unterstützt.<br/>                                                                                                    |
| MF- \_ PMP- \_ Server \_ Kontext                    | [**Imfpmpserver**](/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver)                                                                                                     | PMP-Medien Sitzung (Protected Media Path).                                                                                                         |
| MF \_ Quality \_ Services                       | [**IMF-Empfehlung**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)                                                                                             | Medienquellen:                                                                                                                                    |
| MF- \_ Raten \_ Steuerungs \_ Dienst                  | [**Imfratecontrol**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)                                                                                                 | Medienquellen, Medien Sitzung                                                                                                                      |
| MF- \_ Raten \_ Steuerungs \_ Dienst                  | [**Imfratesupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)                                                                                                 | Medienquellen, Medien senken, Medien Sitzung                                                                                                         |
| MF- \_ Remote \_ Proxy                           | [**Imfremoteproxy**](/windows/desktop/api/mfidl/nn-mfidl-imfremoteproxy)                                                                                                 | Proxys für Remote Objekte.                                                                                                                       |
| MF- \_ Sami- \_ Dienst                           | [**Imsasamistyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle)                                                                                                     | Synchronisierte samische Medienaustausch-Medienquelle (Sami).                                                                                    |
| Anbieter Dienst für die MF- \_ Quell \_ Präsentation \_ \_ | [**Imfmediasourcepresentationprovider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcepresentationprovider)                                                         | Sequencer-Quelle                                                                                                                                  |
| MF- \_ Zeit Code \_ Dienst                       | [**IMF timecodetranslation**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate)                                                                                     | ASF-Medienquelle.                                                                                                                                 |
| MF- \_ toponode- \_ Attribut-Editor- \_ \_ Dienst    | [**Imftopologynoentattributeeditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor)                                                                 | Mediensitzung                                                                                                                                     |
| im MF- \_ \_ Objekt                         | [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)                                                                                                   | Umschließende Objekte                                                                                                                                   |
| mit MF \_ umschließtem \_ Puffer \_ Dienst                |                                                                                                                                          | Wird in Windows 8.1 und höher unterstützt.<br/>                                                                                                    |
| umschließtes MF- \_ \_ Beispiel \_ Servic                 |                                                                                                                                          | Wird in Windows 8.1 und höher unterstützt.<br/>                                                                                                    |
| MF- \_ workqueue- \_ Dienste                     | [**IMF workqueueservices**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)                                                                                     | Mediensitzung                                                                                                                                     |
| MF- \_ Dienst "savejob" \_                     | [**Imsasavejob**](/windows/desktop/api/mfidl/nn-mfidl-imfsavejob)                                                                                                         | Bytestreams                                                                                                                                      |
| MF-Quell \_ Statistik \_ Dienst            | **IPropertyStore**                                                                                                                       | Netzwerkquelle. Verwenden Sie diesen Dienst zum Abrufen von Netzwerk Statistiken. Weitere Informationen finden Sie unter [**MF-Quell \_ Statistik Eigenschaft**](mfnetsource-statistics-property.md). |
| Mr \_ - \_ \_ audiorichtliniendienst                  | [**IMF audiopolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)                                                                                                 | Audiorenderer                                                                                                                                    |
| Mr- \_ Puffer \_ Dienst                         | **IDirect3DSurface9**                                                                                                                    | DirectX-Oberflächen Puffer                                                                                                                           |
| \_Erfassungs \_ Richtlinien \_ - \_ volumedienst        | [**Imbersimpleaudiovolume**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume)                                                                                     | Quelle für Audioerfassung                                                                                                                              |
| \_ \_ \_ richtlinienvolumedienst                 | [**Imbersimpleaudiovolume**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume)                                                                                     | Audiorenderer                                                                                                                                    |
| Mr- \_ Stream- \_ \_ volumedienst                 | [**IMF audiostreamvolume**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume)                                                                                     | Audiorenderer                                                                                                                                    |
| Mr- \_ Video \_ Beschleunigungs \_ Dienst            | [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9), [ **idirectxvideoaccelerationservice**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice) | Erweiterter Videorenderer (EVR)                                                                                                                     |
| Mr- \_ Video \_ Beschleunigungs \_ Dienst            | [**Idirectxvideomemoryconfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)                                                             | Eingabe Pins im DirectShow-EVR-Filter                                                                                                           |
| Mr- \_ Video \_ Beschleunigungs \_ Dienst            | [**IMF videosamplezuordcator-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator)                                                                     | EVR-senken von Datenströmen.                                                                                                                                 |
| Mr- \_ Video- \_ Mixer- \_ Dienst                   | Verschiedene Schnittstellen, die vom EVR-Mixer verfügbar gemacht werden Siehe [Verwenden der Video-Mixer](using-the-video-mixer-controls.md)-Steuerelemente.                   | EVR                                                                                                                                               |
| Mr- \_ Video- \_ Rendering- \_ Dienst                  | Verschiedene Schnittstellen, die vom EVR Presenter verfügbar gemacht werden. Weitere Informationen finden [Sie unter Verwenden der Video Anzeige Steuerelemente](using-the-video-display-controls.md).           | EVR                                                                                                                                               |



 

Sie müssen [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) verwenden, um die in dieser Tabelle aufgelisteten Schnittstellen aus den in dieser Tabelle aufgeführten Objekten zu erhalten.

In einigen Fällen wird eine Schnittstelle als Dienst durch eine Klasse von Objekten zurückgegeben und von einer anderen Klasse von Objekten über **QueryInterface** zurückgegeben. Die Referenzseiten für jede Schnittstelle geben an, wann [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) verwendet werden soll und wann **QueryInterface** verwendet werden soll.

> [!Caution]  
> Ein Objekt kann so implementiert werden, dass es eine Dienst Schnittstelle über **QueryInterface** und [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice)zurückgibt. Die Verwendung von **QueryInterface** , wenn **GetService** erforderlich ist, kann jedoch später zu Kompatibilitätsproblemen führen.

 

Die [**mfgetservice**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) -Funktion ist eine Hilfsfunktion, die ein Objekt für [**imfgetservice**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) abfragt und dann die [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) -Methode des Objekts aufruft.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Medien Sitzung für [**IMF GetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) abgefragt, und die [**imfratecontrol**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) -Schnittstelle wird abgerufen.


```C++
IMFGetService *pGetService = NULL;
IMFRateControl *pRateControl = NULL;
HRESULT hr = S_OK;

hr = pMediaSession->QueryInterface(
    IID_IMFGetService, 
    (void**)&pGetService);

if (SUCCEEDED(hr))
{
    hr = pGetService->GetService(
        MF_RATE_CONTROL_SERVICE, 
        IID_IMFRateControl,
        (void**)&pRateControl);
}
if (SUCCEEDED(hr))
{
    // Use IMFRateControl. (Not shown.)
}

// Clean up.
SAFE_REELEASE(pGetService);
SAFE_RELEASE(pRateControl);
```



Das folgende Beispiel entspricht dem vorherigen Beispiel, verwendet jedoch die [**mfgetservice**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) -Funktion.


```C++
IMFRateControl *pRateControl = NULL;
HRESULT hr = S_OK;

hr = MFGetService(
    pMediaSession, 
    MF_RATE_CONTROL_SERVICE, 
    IID_IMFRateControl, 
    (void**) &pRateCtl 
); 
if (SUCCEEDED(hr))
{
    // Use IMFRateControl. (Not shown.)
}

// Clean up.
SAFE_RELEASE(pRateControl);
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IMF GetService-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
</dt> <dt>

[Media Foundation Plattform-APIs](media-foundation-platform-apis.md)
</dt> </dl>

 

 




