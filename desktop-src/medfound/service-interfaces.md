---
description: Dienstschnittstellen
ms.assetid: 264a0e86-49e9-4777-956b-a83e9db52a25
title: Dienstschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d99155eb5cfb8c435281a5f23567759931cc53fae3743d9c76ce7be75f68c380
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060411"
---
# <a name="service-interfaces"></a>Dienstschnittstellen

Einige Schnittstellen in Media Foundation müssen abgerufen werden, indem [**SIE VOMGETService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) aufrufen, anstatt **queryInterface** aufzurufen. Die [**GetService-Methode**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) funktioniert wie QueryInterface, jedoch mit den folgenden Unterschieden:

-   Zusätzlich zum Schnittstellenbezeichner wird eine Dienstbezeichner-GUID verwendet.
-   Sie kann einen Zeiger auf ein anderes Objekt zurückgeben, das die -Schnittstelle implementiert, anstatt einen Zeiger auf das ursprüngliche Objekt zurückzugeben, das abgefragt wird.

> [!Note]  
> Die [**INTERFACESGetService-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) ähnelt der **IServiceProvider-Schnittstelle,** die in einigen anderen APIs verwendet wird.

 

Ein *Dienst* ist eine bestimmte Schnittstelle, die von einer bestimmten Klasse von -Objekten über die [**INTERFACESGetService-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) abgerufen wird. Die folgenden Dienste sind definiert.



| Dienstbezeichner                          | Schnittstelle                                                                                                                                | Objekte, die diesen Dienst verfügbar machen könnten                                                                                                            |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| MF \_ METADATA \_ PROVIDER \_ SERVICE             | [**PILLARMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)                                                                                       | Medienquellen                                                                                                                                     |
| MF \_ MEDIASOURCE \_ SERVICE                    | [**WFMEDIASOURCE**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                                                                                                 | Wird in Windows 8.1 und höher unterstützt.<br/>                                                                                                    |
| MF \_ \_ PMP-SERVERKONTEXT \_                    | [**IMFPMPServer**](/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver)                                                                                                     | PMP-Mediensitzung (Protected Media Path).                                                                                                         |
| MF \_ QUALITY \_ SERVICES                       | [**HAPQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)                                                                                             | Medienquellen.                                                                                                                                    |
| MF \_ RATE \_ CONTROL \_ SERVICE                  | [**THICKNESSRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)                                                                                                 | Medienquellen, Mediensitzung                                                                                                                      |
| MF \_ RATE \_ CONTROL \_ SERVICE                  | [**1000000000**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)                                                                                                 | Medienquellen, Mediensenken, Mediensitzung                                                                                                         |
| MF \_ REMOTE \_ PROXY                           | [**TRIESRemoteProxy**](/windows/desktop/api/mfidl/nn-mfidl-imfremoteproxy)                                                                                                 | Proxys für Remoteobjekte.                                                                                                                       |
| MF \_ SAMI \_ SERVICE                           | [**ERMITSCHNITTSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle)                                                                                                     | SAMI-Medienquelle (Synchronized Accessible Media Interchange).                                                                                    |
| MF \_ SOURCE \_ PRESENTATION \_ PROVIDER \_ SERVICE | [**IMFMediaSourcePresentationProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcepresentationprovider)                                                         | Sequencerquelle                                                                                                                                  |
| MF \_ TIMECODE \_ SERVICE                       | [**CODTIMECODETranslate**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate)                                                                                     | ASF-Medienquelle.                                                                                                                                 |
| MF \_ \_ TOPONODE-ATTRIBUT-EDITOR-DIENST \_ \_    | [**TOPTOPOLOGYNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor)                                                                 | Mediensitzung                                                                                                                                     |
| MF \_ WRAPPED \_ OBJECT                         | [**GIGABYTEByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)                                                                                                   | Umschlossene Objekte                                                                                                                                   |
| MF \_ WRAPPED \_ BUFFER \_ SERVICE                |                                                                                                                                          | Wird in Windows 8.1 und höher unterstützt.<br/>                                                                                                    |
| MF \_ WRAPPED \_ SAMPLE \_ SERVICEC                 |                                                                                                                                          | Wird in Windows 8.1 und höher unterstützt.<br/>                                                                                                    |
| MF \_ WORKQUEUE \_ SERVICES                     | [**MENUWorkQueueServices**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)                                                                                     | Mediensitzung                                                                                                                                     |
| MFNET \_ \_ SAVEJOB-DIENST                     | [**1000000000000**](/windows/desktop/api/mfidl/nn-mfidl-imfsavejob)                                                                                                         | Bytestreams                                                                                                                                      |
| MFNETSOURCE \_ STATISTICS \_ SERVICE            | **Ipropertystore**                                                                                                                       | Netzwerkquelle. Verwenden Sie diesen Dienst, um Netzwerkstatistiken abzurufen. Siehe [**MFNETSOURCE \_ STATISTICS-Eigenschaft.**](mfnetsource-statistics-property.md) |
| \_ \_ MR-AUDIORICHTLINIENDIENST \_                  | [**VERALTENAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)                                                                                                 | Audiorenderer                                                                                                                                    |
| MR \_ BUFFER \_ SERVICE                         | **IDirect3DSurface9**                                                                                                                    | DirectX-Oberflächenpuffer                                                                                                                           |
| MR \_ CAPTURE \_ POLICY \_ VOLUME \_ SERVICE        | [**VERALTENSimpleAudioVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume)                                                                                     | Audioaufnahmequelle                                                                                                                              |
| MR \_ POLICY \_ VOLUME \_ SERVICE                 | [**VERALTENSimpleAudioVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume)                                                                                     | Audiorenderer                                                                                                                                    |
| MR \_ STREAM \_ VOLUME \_ SERVICE                 | [**VERALTENAudioStreamVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume)                                                                                     | Audiorenderer                                                                                                                                    |
| \_ \_ MR-VIDEOBESCHLEUNIGUNGSDIENST \_            | [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9), [ **IDirectXVideoAccelerationService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice) | Erweiterter Videorenderer (EVR)                                                                                                                     |
| \_ \_ MR-VIDEOBESCHLEUNIGUNGSDIENST \_            | [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)                                                             | Eingabepins für den DirectShow EVR-Filter                                                                                                           |
| \_ \_ MR-VIDEOBESCHLEUNIGUNGSDIENST \_            | [**DINNERVideoSampleAllocator-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator)                                                                     | EVR-Streamsenken.                                                                                                                                 |
| MR \_ VIDEO \_ MIXER \_ SERVICE                   | Verschiedene Schnittstellen, die vom EVR-Mixer verfügbar gemacht werden. Weitere Informationen finden Sie [unter Verwenden der Video Mixer-Steuerelemente.](using-the-video-mixer-controls.md)                   | Evr                                                                                                                                               |
| MR \_ VIDEO \_ RENDER \_ SERVICE                  | Verschiedene Schnittstellen, die vom EVR-Presenter verfügbar gemacht werden. Weitere Informationen finden Sie [unter Verwenden der Videoanzeigesteuerelemente.](using-the-video-display-controls.md)           | Evr                                                                                                                                               |



 

Sie müssen [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) verwenden, um die in dieser Tabelle aufgeführten Schnittstellen aus den in dieser Tabelle aufgeführten Objekten abzurufen.

In einigen Fällen wird eine Schnittstelle als Dienst von einer Klasse von -Objekten und über **QueryInterface** von einer anderen Klasse von -Objekten zurückgegeben. Die Referenzseiten für jede Schnittstelle geben an, wann [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) und wann **QueryInterface** verwendet werden soll.

> [!Caution]  
> Ein Objekt kann so implementiert werden, dass es eine Dienstschnittstelle über **QueryInterface** und [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice)zurückgibt. Die Verwendung **von QueryInterface,** **wenn GetService** erforderlich ist, kann jedoch später zu Kompatibilitätsproblemen führen.

 

Die [**MFGetService-Funktion**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) ist eine Hilfsfunktion, die ein Objekt für [**DENTGETService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) abfragt und dann die [**GetService-Methode**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) des Objekts aufruft.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Media Session für [**DEN BERGETService abgefragt**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) und die [**BERRATEControl-Schnittstelle abgefragt.**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)


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



Das folgende Beispiel entspricht dem vorherigen Beispiel, verwendet jedoch die [**MFGetService-Funktion.**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice)


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

[**BENUTZEROBERFLÄCHEGetService-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
</dt> <dt>

[Media Foundation Plattform-APIs](media-foundation-platform-apis.md)
</dt> </dl>

 

 




