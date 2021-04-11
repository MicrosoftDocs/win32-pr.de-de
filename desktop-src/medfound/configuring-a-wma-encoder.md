---
description: Festlegen eines Ausgabe Typs für einen WMA-Encoder
ms.assetid: 0a1a22bb-460f-4ac2-be76-4249997441de
title: Festlegen eines Ausgabe Typs für einen WMA-Encoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c6b078dc2426b062a90f706c5d113960f54ce32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127961"
---
# <a name="setting-an-output-type-for-a-wma-encoder"></a><span data-ttu-id="d7f04-103">Festlegen eines Ausgabe Typs für einen WMA-Encoder</span><span class="sxs-lookup"><span data-stu-id="d7f04-103">Setting an Output Type for a WMA Encoder</span></span>

<span data-ttu-id="d7f04-104">Um einen gültigen Ausgabetyp für einen Windows Media Audio-Encoder (WMA) zu erstellen, müssen Sie über die folgenden Informationen verfügen:</span><span class="sxs-lookup"><span data-stu-id="d7f04-104">To create a valid output type for a Windows Media Audio (WMA) encoder, you must have the following information:</span></span>

-   <span data-ttu-id="d7f04-105">Der audiountertyp, der das codierte WMA-Format repmmert.</span><span class="sxs-lookup"><span data-stu-id="d7f04-105">The audio subtype that repesents the encoded WMA format.</span></span> <span data-ttu-id="d7f04-106">Siehe [audiountertyp-GUIDs](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="d7f04-106">See [Audio Subtype GUIDs](audio-subtype-guids.md).</span></span>
-   <span data-ttu-id="d7f04-107">Die Konfigurations Eigenschaften, die für den Encoder festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d7f04-107">The configuration properties to set on the encoder.</span></span>

    <span data-ttu-id="d7f04-108">Die Konfigurations Eigenschaften sind in der Dokumentation zu Windows Media Audio und Video Codec und DSP-APIs dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="d7f04-108">The configuration properties are documented in the Windows Media Audio and Video Codec and DSP APIs documentation.</span></span> <span data-ttu-id="d7f04-109">Weitere Informationen finden Sie unter "audiostreameigenschaften" in den [Codierungs Eigenschaften](configuring-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="d7f04-109">For more information, see "Audio Stream Properties" in [Encoding Properties](configuring-the-encoder.md).</span></span>

### <a name="windows-vista-or-later"></a><span data-ttu-id="d7f04-110">Windows Vista oder höher</span><span class="sxs-lookup"><span data-stu-id="d7f04-110">Windows Vista or Later</span></span>

<span data-ttu-id="d7f04-111">Um einen gültigen Ausgabetyp für den Encoder zu erhalten, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="d7f04-111">To get a valid output type for the encoder, perform the following steps.</span></span>

1.  <span data-ttu-id="d7f04-112">Verwenden Sie die Funktion [**mftenum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) oder [**mftenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) zum Erstellen einer Instanz des Encoders.</span><span class="sxs-lookup"><span data-stu-id="d7f04-112">Use the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) or [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function to create an instance of the encoder.</span></span>
2.  <span data-ttu-id="d7f04-113">Fragen Sie den Encoder nach der **IPropertyStore** -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="d7f04-113">Query the encoder for the **IPropertyStore** interface.</span></span>
3.  <span data-ttu-id="d7f04-114">Verwenden Sie die **IPropertyStore** -Schnittstelle, um den Encoder zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="d7f04-114">Use the **IPropertyStore** interface to configure the encoder.</span></span>
4.  <span data-ttu-id="d7f04-115">Rufen Sie die unterstützten Ausgabetypen ab, indem Sie [**imftransform:: getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) in einer Schleife aufrufen, bis der Encoder die Datei " **MF \_ E \_ No \_ more \_** " zurückgibt und Sie den Ziel Medientyp auswählen.</span><span class="sxs-lookup"><span data-stu-id="d7f04-115">Retrieve the supported output types by calling [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) in a loop until the encoder returns **MF\_E\_NO\_MORE\_TYPES** and you choose the target media type.</span></span> <span data-ttu-id="d7f04-116">I</span><span class="sxs-lookup"><span data-stu-id="d7f04-116">I</span></span>
5.  <span data-ttu-id="d7f04-117">Aufrufen von [**imftransform:: setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) , um den Medientyp für die Komprimierung für den Encoder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d7f04-117">Call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) to set the compression media type on the encoder.</span></span>

### <a name="windows-7"></a><span data-ttu-id="d7f04-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d7f04-118">Windows 7</span></span>

<span data-ttu-id="d7f04-119">Um einen gültigen Ausgabetyp für den Encoder in Windows 7 zu erhalten, stellt Media Foundation die [**mftranscodegetaudiooutputavailabletypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) -Funktion bereit.</span><span class="sxs-lookup"><span data-stu-id="d7f04-119">To get a valid output type for the encoder in Windows 7, Media Foundation provides the [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) function.</span></span> <span data-ttu-id="d7f04-120">Für eine Anwendung muss der audiountertyp erforderlich sein, der die codierte WMA-und Codierungs Eigenschaften ableitet.</span><span class="sxs-lookup"><span data-stu-id="d7f04-120">An application must pass required the audio subtype that repesents the encoded WMA and the encoding properties.</span></span> <span data-ttu-id="d7f04-121">Die Eigenschaften sind erforderlich, da der Encoder die unterstützten Ausgabetypen abhängig vom festgelegten Modus ändert.</span><span class="sxs-lookup"><span data-stu-id="d7f04-121">The properties are required because the encoder changes the supported output types depending upon the mode set.</span></span>

> [!Note]  
> <span data-ttu-id="d7f04-122">[**Mftranscodegetaudiooutputavailabletypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes)wird nur für die [Konstante Bitrate-Codierung](constant-bit-rate-encoding.md)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d7f04-122">[**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes)is only supported for [Constant Bit Rate Encoding](constant-bit-rate-encoding.md).</span></span>

 

<span data-ttu-id="d7f04-123">Wenn der-Vorgang erfolgreich ist, empfängt die Anwendung eine Liste der IUnknown-Zeiger der unterstützten Ausgabemedien Typen in einem [**imfcollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="d7f04-123">If the call succeeds, the application receives a list of IUnknown pointers of the supported output media types in an [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) object.</span></span> <span data-ttu-id="d7f04-124">Um den Typ des Ausgabe Mediums festzulegen, suchen Sie nach dem Typ, der mit dem Zieltyp übereinstimmt, und geben Sie [**imftransform:: setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) ein, um den Typ der Komprimierungs Medien für den Encoder</span><span class="sxs-lookup"><span data-stu-id="d7f04-124">To set the output media type, find the one that matches your target type and call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) to set the compression media type on the encoder.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7f04-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d7f04-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7f04-126">Instanziieren eines MFT-Encoders</span><span class="sxs-lookup"><span data-stu-id="d7f04-126">Instantiating an Encoder MFT</span></span>](instantiating-the-encoder-mft.md)
</dt> <dt>

[<span data-ttu-id="d7f04-127">Windows Media Encoder</span><span class="sxs-lookup"><span data-stu-id="d7f04-127">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> </dl>

 

 



