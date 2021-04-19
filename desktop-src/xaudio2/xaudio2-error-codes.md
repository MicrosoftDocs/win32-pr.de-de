---
description: XAudio2 spezifische Fehlercodes, die von XAudio2-Methoden zurückgegeben werden.
ms.assetid: 42a1c21c-4b14-114a-d79e-15a61eb2139b
title: XAudio2-Fehler Codes (XAudio2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7011786c3db7f660dee7a3323861abd88c57835
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373957"
---
# <a name="xaudio2-error-codes"></a><span data-ttu-id="401e2-103">XAudio2-Fehler Codes</span><span class="sxs-lookup"><span data-stu-id="401e2-103">XAudio2 Error Codes</span></span>

<span data-ttu-id="401e2-104">XAudio2 spezifische Fehlercodes, die von XAudio2-Methoden zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="401e2-104">XAudio2 specific error codes returned by XAudio2 methods.</span></span>



| <span data-ttu-id="401e2-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="401e2-105">Constant/value</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="401e2-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="401e2-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_E_INVALID_CALL"></span><span id="xaudio2_e_invalid_call"></span><dl> <span data-ttu-id="401e2-107"><dt>**XAUDIO2 \_ E \_ ungültiger- \_ Rückruf**</dt> <dt>0x88960001</dt></span><span class="sxs-lookup"><span data-stu-id="401e2-107"><dt>**XAUDIO2\_E\_INVALID\_CALL**</dt> <dt>0x88960001</dt></span></span> </dl>                          | <span data-ttu-id="401e2-108">Wird von XAudio2 für bestimmte API-Verwendungs Fehler (ungültige Aufrufe usw.) zurückgegeben, die nur schwer zu vermeiden sind und von einem Titel zur Laufzeit behandelt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="401e2-108">Returned by XAudio2 for certain API usage errors (invalid calls and so on) that are hard to avoid completely and should be handled by a title at runtime.</span></span> <span data-ttu-id="401e2-109">(API-Verwendungs Fehler, die vollständig vermeidbar sind, wie z. b. ungültige Parameter, verursachen eine Assert in Debugbuilds und undefiniertes Verhalten in Einzelhandels Builds, sodass kein Fehlercode für Sie definiert ist.)</span><span class="sxs-lookup"><span data-stu-id="401e2-109">(API usage errors that are completely avoidable, such as invalid parameters, cause an ASSERT in debug builds and undefined behavior in retail builds, so no error code is defined for them.)</span></span><br/> |
| <span id="XAUDIO2_E_XMA_DECODER_ERROR"></span><span id="xaudio2_e_xma_decoder_error"></span><dl> <span data-ttu-id="401e2-110"><dt>**XAUDIO2 \_ E \_ XMA \_ - \_ Decoderfehler**</dt> <dt>0x88960002</dt></span><span class="sxs-lookup"><span data-stu-id="401e2-110"><dt>**XAUDIO2\_E\_XMA\_DECODER\_ERROR**</dt> <dt>0x88960002</dt></span></span> </dl>          | <span data-ttu-id="401e2-111">Nicht BEHEB barer Fehler bei der Xbox 360-XMA-Hardware.</span><span class="sxs-lookup"><span data-stu-id="401e2-111">The Xbox 360 XMA hardware suffered an unrecoverable error.</span></span><br/>                                                                                                                                                                                                                                                                                             |
| <span id="XAUDIO2_E_XAPO_CREATION_FAILED"></span><span id="xaudio2_e_xapo_creation_failed"></span><dl> <span data-ttu-id="401e2-112"><dt>**XAUDIO2 \_ Fehler beim \_ \_ Erstellen von \_ E xapo**</dt> <dt>0x88960003</dt> .</span><span class="sxs-lookup"><span data-stu-id="401e2-112"><dt>**XAUDIO2\_E\_XAPO\_CREATION\_FAILED**</dt> <dt>0x88960003</dt></span></span> </dl> | <span data-ttu-id="401e2-113">Ein Effekt konnte nicht instanziiert werden.</span><span class="sxs-lookup"><span data-stu-id="401e2-113">An effect failed to instantiate.</span></span><br/>                                                                                                                                                                                                                                                                                                                       |
| <span id="XAUDIO2_E_DEVICE_INVALIDATED"></span><span id="xaudio2_e_device_invalidated"></span><dl> <span data-ttu-id="401e2-114"><dt>**XAUDIO2 \_ E \_ - \_ Gerät**</dt> hat <dt>0x88960004</dt> ungültig</span><span class="sxs-lookup"><span data-stu-id="401e2-114"><dt>**XAUDIO2\_E\_DEVICE\_INVALIDATED**</dt> <dt>0x88960004</dt></span></span> </dl>        | <span data-ttu-id="401e2-115">Ein Audiogerät kann nicht mehr verwendet werden, da es nicht mehr funktioniert oder ein anderes Ereignis ist</span><span class="sxs-lookup"><span data-stu-id="401e2-115">An audio device became unusable through being unplugged or some other event.</span></span><br/>                                                                                                                                                                                                                                                                           |



## <a name="remarks"></a><span data-ttu-id="401e2-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="401e2-116">Remarks</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="401e2-117">Plattformanforderungen</span><span class="sxs-lookup"><span data-stu-id="401e2-117">Platform Requirements</span></span>

<span data-ttu-id="401e2-118">Windows 10 (xaudio2.9); Windows 8, Windows Phone 8 (xaudio2,8); DirectX SDK (xaudio2,7)</span><span class="sxs-lookup"><span data-stu-id="401e2-118">Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)</span></span>

## <a name="requirements"></a><span data-ttu-id="401e2-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="401e2-119">Requirements</span></span>



| <span data-ttu-id="401e2-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="401e2-120">Requirement</span></span> | <span data-ttu-id="401e2-121">Wert</span><span class="sxs-lookup"><span data-stu-id="401e2-121">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="401e2-122">Header</span><span class="sxs-lookup"><span data-stu-id="401e2-122">Header</span></span><br/> | <dl> <span data-ttu-id="401e2-123"><dt>Xaudio2. h</dt></span><span class="sxs-lookup"><span data-stu-id="401e2-123"><dt>Xaudio2.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="401e2-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="401e2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="401e2-125">XAudio2:: Konstanten</span><span class="sxs-lookup"><span data-stu-id="401e2-125">XAudio2::Constants</span></span>](constants.md)
</dt> </dl>

 

 




