---
description: Auflisten von Audiotypen für bestimmte Codierungs Modi
ms.assetid: d44960eb-da5e-4379-ba9d-cb804559dc53
title: Auflisten von Audiotypen für bestimmte Codierungs Modi (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16a8b97afdd48cb1d7828f80778aa9fcf8dc1ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393269"
---
# <a name="enumerating-audio-types-for-specific-encoding-modes-microsoft-media-foundation"></a><span data-ttu-id="8ce58-103">Auflisten von Audiotypen für bestimmte Codierungs Modi (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="8ce58-103">Enumerating Audio Types for Specific Encoding Modes (Microsoft Media Foundation)</span></span>

<span data-ttu-id="8ce58-104">Die vom Audioencoder akzeptierten Eingabe-und Ausgabemedien Typen sind sehr strukturiert.</span><span class="sxs-lookup"><span data-stu-id="8ce58-104">The input and output media types accepted by the audio encoder are very structured.</span></span> <span data-ttu-id="8ce58-105">Sie müssen unterstützte Ausgabetypen abrufen, indem Sie die **imediaobject:: getoutputtype** -Methode oder **imftransform:: getoutputtype** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8ce58-105">You must obtain supported output types by calling **IMediaObject::GetOutputType** method or **IMFTransform::GetOutputType**.</span></span> <span data-ttu-id="8ce58-106">Nachdem Sie einen Ausgabetyp erhalten haben, dürfen Sie ihn nicht mehr ändern.</span><span class="sxs-lookup"><span data-stu-id="8ce58-106">After you get an output type, you must not alter it.</span></span>

<span data-ttu-id="8ce58-107">Wenn Sie einen anderen Codierungs Modus als einen einzigen Pass-CBR verwenden möchten, müssen Sie den-Modus festlegen und dann die Ausgabetypen für diesen Modus auflisten. der Encoder ändert die unterstützten Ausgabetypen, je nachdem, welcher Modus festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="8ce58-107">If you want to use an encoding mode other than one-pass CBR, you must set the mode and then enumerate the output types for that mode; the encoder changes the supported output types depending upon the mode set.</span></span> <span data-ttu-id="8ce58-108">Die Eigenschaften, die den Codierungs Modus steuern, sind [**mfpkey \_ vbrenabled**](mfpkey-vbrenabledproperty.md) und [**mfpkey \_ passesused**](mfpkey-passesusedproperty.md).</span><span class="sxs-lookup"><span data-stu-id="8ce58-108">The properties that control the encoding mode are [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) and [**MFPKEY\_PASSESUSED**](mfpkey-passesusedproperty.md).</span></span> <span data-ttu-id="8ce58-109">Wenn der Modus im Encoder festgelegt ist, müssen Sie einen Ausgabetyp ohne Änderung auflisten und auswählen, ebenso wie bei CBR.</span><span class="sxs-lookup"><span data-stu-id="8ce58-109">When the mode is set in the encoder, you must enumerate and select an output type, using it without alteration, just as with CBR.</span></span>

## <a name="identifying-quality-based-vbr-types"></a><span data-ttu-id="8ce58-110">Identifizieren von Qualitäts basierten VBR-Typen</span><span class="sxs-lookup"><span data-stu-id="8ce58-110">Identifying Quality Based VBR Types</span></span>

<span data-ttu-id="8ce58-111">Die Vorgehensweise zum Identifizieren von Qualitäts basierten VBR-Typen hängt davon ab, ob der Encoder als DirectX Media Object (DMO) fungiert oder als Media Foundation Transform (MFT) fungiert.</span><span class="sxs-lookup"><span data-stu-id="8ce58-111">The procedure for identifying quality based VBR types depends on whether the encoder is acting as a DirectX Media Object (DMO) or acting as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="8ce58-112">Informationen dazu, wann ein Encoder als DMO oder MFT fungiert, finden Sie auf den einzelnen Codec-Referenzseiten unter [Codec-Objekte](codecobjects.md).</span><span class="sxs-lookup"><span data-stu-id="8ce58-112">For information on when an encoder acts as a DMO or an MFT, see the individual codec reference pages under [Codec Objects](codecobjects.md).</span></span>

<span data-ttu-id="8ce58-113">Wenn ein Audioencoder als DMO fungiert und Sie den Encoder für die Verwendung von One-Pass-VBR konfigurieren, listet er alle unterstützten Ausgabetypen auf.</span><span class="sxs-lookup"><span data-stu-id="8ce58-113">When an audio encoder is acting as a DMO and you configure the encoder to use one-pass VBR, it enumerates all of the supported output types.</span></span> <span data-ttu-id="8ce58-114">Allerdings möchten Sie in der Regel einen 1-Pass-VBR-Typ auf Grundlage des Quality-Parameters auswählen.</span><span class="sxs-lookup"><span data-stu-id="8ce58-114">However, you will typically want to select a one-pass VBR type based on the quality parameter.</span></span> <span data-ttu-id="8ce58-115">Der Encoder legt den Qualitäts Wert für einstufige VBR-Ausgabetypen im **navgbytespersec** -Member der **WaveFormatEx** -Struktur ab, auf die durch **DMO \_ Media \_ Type. pbformat** verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="8ce58-115">The encoder puts the quality value for one-pass VBR output types in the **nAvgBytesPerSec** member of the **WAVEFORMATEX** structure pointed to by **DMO\_MEDIA\_TYPE.pbFormat**.</span></span>

<span data-ttu-id="8ce58-116">Dieser Wert wird in folgendem Format gespeichert: 0x7fffffxx, wobei XX der Qualitäts Wert ist (von 0 bis 100).</span><span class="sxs-lookup"><span data-stu-id="8ce58-116">This value is stored in the following format: 0x7FFFFFXX, where XX is the quality value (from 0 to 100).</span></span> <span data-ttu-id="8ce58-117">Beispielsweise wird mit dem **navgbytespersec** -Wert 0x7fffff62 der Qualitätsgrad 98 (0x62 = 98) angegeben.</span><span class="sxs-lookup"><span data-stu-id="8ce58-117">For example, the **nAvgBytesPerSec** value of 0x7FFFFF62 specifies quality level 98 (0x62 = 98).</span></span>

<span data-ttu-id="8ce58-118">Im folgenden Beispiel wird gezeigt, wie die Qualitätsstufe eines Formats überprüft wird, wenn der Encoder als DMO fungiert.</span><span class="sxs-lookup"><span data-stu-id="8ce58-118">The following example shows how to check the quality level of a format when the encoder is acting as a DMO.</span></span>


```
void ShowQuality(WAVEFORMATEX* pWave)
{
    // Store the average bytes per second in a local variable
    // with a more manageable name.
    DWORD dwBps = pWave->nAvgBytesPerSec;

    // Verify that the value is a VBR quality level by using 
    // a bitmask to check for the bit pattern 0x7FFFFFXX. 
    if(dwBps & 0x7FFFFF00 == 0x7FFFFF00)
        printf("VBR Quality: %d%%\n",(dwBps & 0x000000FF));
    else // Not a valid VBR quality value.
        printf("Not a valid one-pass VBR audio format.\n");
}
```



<span data-ttu-id="8ce58-119">Wenn der Encoder als MFT fungiert und einen Ausgabetyp bei einem Aufrufen von **getavailableoutputtype** auflistet, können Sie die MFT für die zuletzt **\_ \_ \_ aufgelistete \_ vbrquality-Eigenschaft von mfpkey** Abfragen.</span><span class="sxs-lookup"><span data-stu-id="8ce58-119">When the encoder is acting as an MFT and it enumerates an output type on a call to **GetAvailableOutputType**, you can query the MFT for the **MFPKEY\_MOST\_RECENTLY\_ENUMERATED\_VBRQUALITY** property.</span></span> <span data-ttu-id="8ce58-120">Der zurückgegebene Wert gibt die VBR-Qualität des zuletzt zurückgegebenen Ausgabemedien Typs an.</span><span class="sxs-lookup"><span data-stu-id="8ce58-120">The value returned indicates the VBR quality of the most recently returned output media type.</span></span> <span data-ttu-id="8ce58-121">Anschließend können Sie diesen Wert verwenden, um die [**\_ gewünschte \_ Eigenschaft "mfpkey**](mfpkey-desired-vbrqualityproperty.md) " des Encoders festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8ce58-121">Then you can use that value to set the [**MFPKEY\_DESIRED\_VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) property of the encoder.</span></span>

## <a name="setting-peak-constraints"></a><span data-ttu-id="8ce58-122">Festlegen von Spitzen Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="8ce58-122">Setting Peak Constraints</span></span>

<span data-ttu-id="8ce58-123">Bei Qualitäts basierter VBR (One-Pass) und uneingeschränkter 2-Pass-VBR sind nach dem Abrufen des Ausgabe Typs keine weiteren Einstellungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8ce58-123">For quality based VBR (one-pass) and unconstrained two-pass VBR, no additional settings are required after retrieving the output type.</span></span> <span data-ttu-id="8ce58-124">Wenn Sie VBR mit hoher Last verwenden möchten, rufen Sie einen Ausgabetyp mit aktiviertem VBR und zwei Durchläufen ab.</span><span class="sxs-lookup"><span data-stu-id="8ce58-124">To use peak-constrained VBR, retrieve an output type with VBR enabled and two passes set.</span></span> <span data-ttu-id="8ce58-125">Dieser Typ beschreibt ohne Änderung die nicht eingeschränkten VBR-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="8ce58-125">This type, without alteration, describes unconstrained VBR settings.</span></span> <span data-ttu-id="8ce58-126">Legen Sie zum Festlegen von Spitzen Einschränkungen die Eigenschaften [mfpkey \_ Rmax](mfpkey-rmaxproperty.md) und [mfpkey \_ bmax](mfpkey-bmaxproperty.md) fest.</span><span class="sxs-lookup"><span data-stu-id="8ce58-126">To set peak constraints, set the [MFPKEY\_RMAX](mfpkey-rmaxproperty.md) and [MFPKEY\_BMAX](mfpkey-bmaxproperty.md) properties.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8ce58-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8ce58-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ce58-128">Konfigurieren der Audiocodierung</span><span class="sxs-lookup"><span data-stu-id="8ce58-128">Configuring Audio Encoding</span></span>](configuringaudioencoding.md)
</dt> <dt>

[<span data-ttu-id="8ce58-129">Suchen von Audioencoder-Ausgabetypen</span><span class="sxs-lookup"><span data-stu-id="8ce58-129">Finding Audio Encoder Output Types</span></span>](findingaudioencoderoutputtypes.md)
</dt> <dt>

[<span data-ttu-id="8ce58-130">Verwenden von Two-Pass Codierung</span><span class="sxs-lookup"><span data-stu-id="8ce58-130">Using Two-Pass Encoding</span></span>](usingtwoencodingpasses.md)
</dt> <dt>

[<span data-ttu-id="8ce58-131">Verwenden der VBR-Codierung</span><span class="sxs-lookup"><span data-stu-id="8ce58-131">Using VBR Encoding</span></span>](usingvbrencoding.md)
</dt> </dl>

 

 



