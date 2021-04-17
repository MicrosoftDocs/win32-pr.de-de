---
description: Verwenden des Windows Media Audio Voice-Codecs
ms.assetid: 771acb04-33a4-4ea3-8f50-e5e3dbdf9495
title: Verwenden des Windows Media Audio Voice-Codecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d636bd97b76e23acc6b68da87c8a206b17dea60a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530467"
---
# <a name="using-the-windows-media-audio-voice-codec"></a><span data-ttu-id="690f5-103">Verwenden des Windows Media Audio Voice-Codecs</span><span class="sxs-lookup"><span data-stu-id="690f5-103">Using the Windows Media Audio Voice Codec</span></span>

<span data-ttu-id="690f5-104">Der Windows Media Audio Voice-Codec bietet eine niedrige Bitrate-Komprimierung, die für Audioinhalte optimiert ist.</span><span class="sxs-lookup"><span data-stu-id="690f5-104">The Windows Media Audio Voice codec provides low bit-rate compression optimized for audio containing speech.</span></span> <span data-ttu-id="690f5-105">Die Fähigkeit des Codecs, solche kleinen Stichproben zu liefern, ist auf den begrenzten Frequenzbereich der Klänge der menschlichen Stimme zurückzuführen.</span><span class="sxs-lookup"><span data-stu-id="690f5-105">The ability of the codec to produce such small samples is due to the limited frequency range of the sounds of the human voice.</span></span> <span data-ttu-id="690f5-106">Diese Optimierung bedeutet, dass ein dedizierter sprach Encoder eine Ausgabe mit schlechter Qualität für Inhalte erstellt, die kompliziertere Sounds wie Musik enthalten.</span><span class="sxs-lookup"><span data-stu-id="690f5-106">This optimization means that a dedicated voice encoder creates poor-quality output for content that contains more complicated sounds, like music.</span></span> <span data-ttu-id="690f5-107">Der Windows Media Audio Voice-Codec kompensiert jedoch dieses potenzielle Qualitätsproblem, indem es separate Modi für sprach-, Musik-und gemischte Inhalte bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="690f5-107">However, the Windows Media Audio Voice codec compensates for this potential quality issue by providing separate modes for voice, music, and mixed content.</span></span> <span data-ttu-id="690f5-108">Der Codec analysiert gemischte Inhalte, um zu bestimmen, welcher Modus für die einzelnen Teile der Datei verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="690f5-108">The codec analyzes mixed content to determine which mode to use for each portion of the file.</span></span>

<span data-ttu-id="690f5-109">Der Windows Media Audio Voice-Codec wird in das durch den Klassen Bezeichner CLSID CWMSPEncMediaObject2 identifizierte Codierungs Objekt implementiert \_ , und im Decoderobjekt, das durch den Klassen Bezeichner CLSID \_ cwmspdecmediaobject identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="690f5-109">The Windows Media Audio Voice codec is implemented in the encoder object identified by the class identifier CLSID\_CWMSPEncMediaObject2, and in the decoder object identified by the class identifier CLSID\_CWMSPDecMediaObject.</span></span> <span data-ttu-id="690f5-110">Das Formattag von Medientypen, die diesen Codec verwenden, ist 0x00a.</span><span class="sxs-lookup"><span data-stu-id="690f5-110">The format tag of media types using this codec is 0x00A.</span></span>

## <a name="configuring-the-encoder"></a><span data-ttu-id="690f5-111">Konfigurieren des Encoders</span><span class="sxs-lookup"><span data-stu-id="690f5-111">Configuring the Encoder</span></span>

<span data-ttu-id="690f5-112">Der sprach Encoder unterstützt drei Modi: Sprache, Musik und gemischt.</span><span class="sxs-lookup"><span data-stu-id="690f5-112">The voice encoder supports three modes: speech, music, and mixed.</span></span> <span data-ttu-id="690f5-113">Jeder Modus ist so optimiert, dass die besten Ergebnisse für diesen Inhaltstyp erzielt werden.</span><span class="sxs-lookup"><span data-stu-id="690f5-113">Each mode is optimized to get the best results for that type of content.</span></span> <span data-ttu-id="690f5-114">Sie können den Modus des Voice-Encoders konfigurieren, indem Sie die Methoden von **IPropertyStore** verwenden, um die Eigenschaft " [mfpkey \_ wmavoice \_ ENC \_ musicvoiceclassmode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) " festzulegen.</span><span class="sxs-lookup"><span data-stu-id="690f5-114">You can configure the mode of the voice encoder by using the methods of **IPropertyStore** to set the [MFPKEY\_WMAVOICE\_ENC\_MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) property.</span></span>

<span data-ttu-id="690f5-115">Wenn der Windows Media Audio Voice-Codec für gemischte Inhalte konfiguriert ist, erkennt er automatisch die im Inhalt vorhandenen Musikpassagen.</span><span class="sxs-lookup"><span data-stu-id="690f5-115">When configured for mixed content, the Windows Media Audio Voice codec will automatically detect passages of music in the content.</span></span> <span data-ttu-id="690f5-116">Wenn Sie mit den Ergebnissen nicht zufrieden sind, können Sie den Speicherort der Musik im Inhalt mithilfe einer Bearbeitungs Entscheidungs Liste ("EDL") angeben.</span><span class="sxs-lookup"><span data-stu-id="690f5-116">If you are not satisfied with the results, you can specify the location of music in the content using an editing decision list (EDL).</span></span> <span data-ttu-id="690f5-117">Weitere Informationen finden Sie unter [using an Bearbeitung Decision List for Encoding Voice](usingavoiceeditingdecisionlist.md).</span><span class="sxs-lookup"><span data-stu-id="690f5-117">For more information, see [Using an Editing Decision List for Encoding Voice](usingavoiceeditingdecisionlist.md).</span></span>

<span data-ttu-id="690f5-118">Im Gegensatz zu den anderen audioencodern können Sie den Wert für das Puffer Fenster für sprach Inhalt mithilfe der Eigenschaft [mfpkey \_ wmavoice \_ ENC \_ bufferwindow](mfpkey-wmavoice-enc-bufferwindowproperty.md) festlegen.</span><span class="sxs-lookup"><span data-stu-id="690f5-118">Unlike the other audio encoders, you can set the buffer window value for voice content by using the [MFPKEY\_WMAVOICE\_ENC\_BufferWindow](mfpkey-wmavoice-enc-bufferwindowproperty.md) property.</span></span> <span data-ttu-id="690f5-119">Die Standardwerte sollten jedoch in den meisten Fällen einwandfrei funktionieren.</span><span class="sxs-lookup"><span data-stu-id="690f5-119">However, the default values should work fine in most cases.</span></span>

> [!Note]  
>    <span data-ttu-id="690f5-120">Beim Konfigurieren des sprach Encoders ist es sehr wichtig, dass Sie den Ausgabetyp festlegen, bevor Sie den Eingabetyp festlegen.</span><span class="sxs-lookup"><span data-stu-id="690f5-120">When configuring the voice encoder, it is very important that you set the output type before you set the input type.</span></span> <span data-ttu-id="690f5-121">Dies ist die empfohlene Reihenfolge von Vorgängen für alle Audiocodecs, aber der sprach Encoder kann fehlerhafte Ausgabetypen melden, wenn eine Eingabe festgelegt wird, wenn Sie **imediaobject:: getoutputtype** oder **imftransform:: getoutputtype** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="690f5-121">This is the recommended order of operations for all of the audio codecs, but the voice encoder can report erroneous output types if an input is set when you call **IMediaObject::GetOutputType** or **IMFTransform::GetOutputType**.</span></span>

 

## <a name="decoding"></a><span data-ttu-id="690f5-122">Decodierung</span><span class="sxs-lookup"><span data-stu-id="690f5-122">Decoding</span></span>

<span data-ttu-id="690f5-123">Es gibt keine besonderen Anforderungen für das Decodieren von sprach Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="690f5-123">There are no special requirements for decoding voice audio.</span></span> <span data-ttu-id="690f5-124">Weitere Informationen finden Sie unter [Konfigurieren der Audiodecodierung](configuringaudiodecoding.md).</span><span class="sxs-lookup"><span data-stu-id="690f5-124">Form more information, see [Configuring Audio Decoding](configuringaudiodecoding.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="690f5-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="690f5-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="690f5-126">Arbeiten mit Audiodaten</span><span class="sxs-lookup"><span data-stu-id="690f5-126">Working with Audio</span></span>](workingwithaudio.md)
</dt> </dl>

 

 



