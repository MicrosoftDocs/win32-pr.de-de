---
description: Gibt an, ob der Audiodecoder eine hochauflösende Ausgabe bereitstellt.
ms.assetid: a96bd78f-982c-43fa-b2d3-8caba4aa84b6
title: MFPKEY_WMADEC_HIRESOUTPUT-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd59bc6b8b0e74be1daaea4a61ca82c810a0ca79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345268"
---
# <a name="mfpkey_wmadec_hiresoutput-property"></a><span data-ttu-id="2fdfc-103">Mfpkey \_ wmadec \_ hiresoutput (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2fdfc-103">MFPKEY\_WMADEC\_HIRESOUTPUT Property</span></span>

<span data-ttu-id="2fdfc-104">Gibt an, ob der Audiodecoder eine hochauflösende Ausgabe bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="2fdfc-104">Specifies whether the audio decoder should deliver high-resolution output.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="2fdfc-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="2fdfc-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="2fdfc-106">g \_ wszwmachiresoutput</span><span class="sxs-lookup"><span data-stu-id="2fdfc-106">g\_wszWMACHiResOutput</span></span>

## <a name="data-type"></a><span data-ttu-id="2fdfc-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="2fdfc-107">Data Type</span></span>

<span data-ttu-id="2fdfc-108">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="2fdfc-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="2fdfc-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="2fdfc-109">Default Value</span></span>

<span data-ttu-id="2fdfc-110">**Variant \_ false**</span><span class="sxs-lookup"><span data-stu-id="2fdfc-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="2fdfc-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2fdfc-111">Remarks</span></span>

<span data-ttu-id="2fdfc-112">Legen Sie diese Eigenschaft auf Variant true fest, \_ um Multichannel-oder 24-Bit-Audioinhalte zu decodieren, oder Audiodaten mit einer Stichprobenrate größer als 48.000 Hz.</span><span class="sxs-lookup"><span data-stu-id="2fdfc-112">Set this property to VARIANT\_TRUE to decode multichannel or 24-bit audio content, or audio with a sample rate greater than 48,000 Hz.</span></span> <span data-ttu-id="2fdfc-113">Wenn der Inhalt in hoher Auflösung codiert ist, diese Eigenschaft aber Variant \_ false ist, gelten die folgenden Verhaltensweisen:</span><span class="sxs-lookup"><span data-stu-id="2fdfc-113">If the content is encoded in high resolution, but this property is VARIANT\_FALSE, the following behaviors apply:</span></span>

-   <span data-ttu-id="2fdfc-114">Die DMO-Ausgabe wird auf einen 16-Bit-, 48-kHz-Stereo Wert beschränkt.</span><span class="sxs-lookup"><span data-stu-id="2fdfc-114">The DMO output will be limited to 16-bit, 48-KHz stereo.</span></span>
-   <span data-ttu-id="2fdfc-115">Der MFT listet Ausgabe Modi auf, die auf 16 Bits beschränkt sind und keine Änderungen in der Kanalanzahl oder der Samplingrate beinhalten.</span><span class="sxs-lookup"><span data-stu-id="2fdfc-115">The MFT will enumerate output modes that are limited to 16 bits and do not involve changes in channel count or sampling rate.</span></span>

<span data-ttu-id="2fdfc-116">Die Eigenschaften von hochauflösende Audiodaten werden in einer [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) -Struktur, nicht in [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)), weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="2fdfc-116">The properties of high-resolution audio are passed in a [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure, not [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)).</span></span>

<span data-ttu-id="2fdfc-117">Die Ausgabe mit hoher Auflösung ist nur verfügbar, wenn der Decoder unter Windows XP oder höher ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2fdfc-117">High-resolution output is available only if the decoder is running on Windows XP or later.</span></span> <span data-ttu-id="2fdfc-118">Sie können diese Eigenschaft unabhängig von dem Betriebssystem festlegen, auf dem Ihre Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2fdfc-118">You can set this property regardless of the operating system on which your application is running.</span></span> <span data-ttu-id="2fdfc-119">Unter Windows-Versionen vor Windows XP ignoriert der Decoder diese Einstellung und stellt eine Standardausgabe bereit.</span><span class="sxs-lookup"><span data-stu-id="2fdfc-119">On versions of Windows earlier than Windows XP, the decoder will ignore this setting and deliver standard output.</span></span>

<span data-ttu-id="2fdfc-120">Viele Spieler (einschließlich Windows Media Player 9-Serie und höher) legen diesen Wert für den gesamten Inhalt fest.</span><span class="sxs-lookup"><span data-stu-id="2fdfc-120">Many players (including Windows Media Player 9 Series and later) set this value for all content.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fdfc-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2fdfc-121">Requirements</span></span>



| <span data-ttu-id="2fdfc-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2fdfc-122">Requirement</span></span> | <span data-ttu-id="2fdfc-123">Wert</span><span class="sxs-lookup"><span data-stu-id="2fdfc-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2fdfc-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2fdfc-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2fdfc-125">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2fdfc-125">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2fdfc-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2fdfc-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2fdfc-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2fdfc-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2fdfc-128">Header</span><span class="sxs-lookup"><span data-stu-id="2fdfc-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fdfc-129"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fdfc-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fdfc-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2fdfc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fdfc-131">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2fdfc-131">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
