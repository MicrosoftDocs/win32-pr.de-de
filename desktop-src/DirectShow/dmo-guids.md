---
description: In der folgenden Tabelle sind die für Microsoft DirectX Media Object (DMO)-Kategorien definierten global eindeutigen Bezeichner (GUIDs) aufgelistet. Diese GUIDs werden in der Header Datei "dmoreg. h" definiert und von der Bibliothek "dmuguids. lib" exportiert.
ms.assetid: d67debd0-8ecb-41ab-bc6c-b27cba97c65a
title: DMO-GUIDs (dmoreg. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c10d5bd917d6368d398362e76ffa9ea8255933ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368414"
---
# <a name="dmo-guids"></a><span data-ttu-id="26526-104">DMO-GUIDs</span><span class="sxs-lookup"><span data-stu-id="26526-104">DMO GUIDs</span></span>

<span data-ttu-id="26526-105">In der folgenden Tabelle sind die für Microsoft DirectX Media Object (DMO)-Kategorien definierten global eindeutigen Bezeichner (GUIDs) aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="26526-105">The following table lists the globally unique identifiers (GUIDs) defined for Microsoft DirectX Media Object (DMO) categories.</span></span> <span data-ttu-id="26526-106">Diese GUIDs werden in der Header Datei "dmoreg. h" definiert und von der Bibliothek "dmuguids. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="26526-106">These GUIDs are defined in the header file Dmoreg.h and exported by the Dmoguids.lib library.</span></span>

<span data-ttu-id="26526-107">Übergeben Sie zum Auflisten der in einer Kategorie registrierten DMOS die entsprechende GUID an die [**dmuenum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="26526-107">To enumerate the DMOs registered in a category, pass the corresponding GUID to the [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) function.</span></span>



| <span data-ttu-id="26526-108">GUID</span><span class="sxs-lookup"><span data-stu-id="26526-108">GUID</span></span>                                                                                                                                                                                                                     | <span data-ttu-id="26526-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="26526-109">Description</span></span>                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------|
| <span id="DMOCATEGORY_AUDIO_DECODER"></span><span id="dmocategory_audio_decoder"></span><dl> <span data-ttu-id="26526-110"><dt>**dmucategory \_ - \_ Audiodecoder**</dt></span><span class="sxs-lookup"><span data-stu-id="26526-110"><dt>**DMOCATEGORY\_AUDIO\_DECODER**</dt></span></span> </dl>                       | <span data-ttu-id="26526-111">Audiodecoder</span><span class="sxs-lookup"><span data-stu-id="26526-111">Audio decoder</span></span><br/>        |
| <span id="DMOCATEGORY_AUDIO_EFFECT"></span><span id="dmocategory_audio_effect"></span><dl> <span data-ttu-id="26526-112"><dt>**dmucategory \_ - \_ Audioeffekt**</dt></span><span class="sxs-lookup"><span data-stu-id="26526-112"><dt>**DMOCATEGORY\_AUDIO\_EFFECT**</dt></span></span> </dl>                          | <span data-ttu-id="26526-113">Audioeffekt</span><span class="sxs-lookup"><span data-stu-id="26526-113">Audio effect</span></span><br/>         |
| <span id="DMOCATEGORY_AUDIO_ENCODER"></span><span id="dmocategory_audio_encoder"></span><dl> <span data-ttu-id="26526-114"><dt>**dmucategory \_ - \_ Audioencoder**</dt></span><span class="sxs-lookup"><span data-stu-id="26526-114"><dt>**DMOCATEGORY\_AUDIO\_ENCODER**</dt></span></span> </dl>                       | <span data-ttu-id="26526-115">Audioencoder</span><span class="sxs-lookup"><span data-stu-id="26526-115">Audio encoder</span></span><br/>        |
| <span id="DMOCATEGORY_VIDEO_DECODER"></span><span id="dmocategory_video_decoder"></span><dl> <span data-ttu-id="26526-116"><dt>**dmucategory- \_ Video \_ Decoder**</dt></span><span class="sxs-lookup"><span data-stu-id="26526-116"><dt>**DMOCATEGORY\_VIDEO\_DECODER**</dt></span></span> </dl>                       | <span data-ttu-id="26526-117">Video Decoder</span><span class="sxs-lookup"><span data-stu-id="26526-117">Video decoder</span></span><br/>        |
| <span id="DMOCATEGORY_VIDEO_EFFECT"></span><span id="dmocategory_video_effect"></span><dl> <span data-ttu-id="26526-118"><dt>**dmucategory- \_ Video \_ Effekt**</dt></span><span class="sxs-lookup"><span data-stu-id="26526-118"><dt>**DMOCATEGORY\_VIDEO\_EFFECT**</dt></span></span> </dl>                          | <span data-ttu-id="26526-119">Video Effekt</span><span class="sxs-lookup"><span data-stu-id="26526-119">Video effect</span></span><br/>         |
| <span id="DMOCATEGORY_VIDEO_ENCODER"></span><span id="dmocategory_video_encoder"></span><dl> <span data-ttu-id="26526-120"><dt>**dmucategory- \_ Video \_ Encoder**</dt></span><span class="sxs-lookup"><span data-stu-id="26526-120"><dt>**DMOCATEGORY\_VIDEO\_ENCODER**</dt></span></span> </dl>                       | <span data-ttu-id="26526-121">Video Encoder</span><span class="sxs-lookup"><span data-stu-id="26526-121">Video encoder</span></span><br/>        |
| <span id="DMOCATEGORY_AUDIO_CAPTURE_EFFECT"></span><span id="dmocategory_audio_capture_effect"></span><dl> <span data-ttu-id="26526-122"><dt>**dmucategory \_ - \_ audioerfassungs \_ Effekt**</dt></span><span class="sxs-lookup"><span data-stu-id="26526-122"><dt>**DMOCATEGORY\_AUDIO\_CAPTURE\_EFFECT**</dt></span></span> </dl> | <span data-ttu-id="26526-123">Audioerfassungs Effekt</span><span class="sxs-lookup"><span data-stu-id="26526-123">Audio capture effect</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="26526-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26526-124">Requirements</span></span>



| <span data-ttu-id="26526-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26526-125">Requirement</span></span> | <span data-ttu-id="26526-126">Wert</span><span class="sxs-lookup"><span data-stu-id="26526-126">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="26526-127">Header</span><span class="sxs-lookup"><span data-stu-id="26526-127">Header</span></span><br/> | <dl> <span data-ttu-id="26526-128"><dt>Dmoreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="26526-128"><dt>Dmoreg.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26526-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26526-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26526-130">DMO-Konstanten</span><span class="sxs-lookup"><span data-stu-id="26526-130">DMO Constants</span></span>](dmo-constants.md)
</dt> </dl>

 

 




