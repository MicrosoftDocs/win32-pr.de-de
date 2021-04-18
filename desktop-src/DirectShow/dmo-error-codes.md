---
description: In der folgenden Tabelle sind die für Microsoft DirectX Media Objects (DMOs) spezifischen Fehlercodes enthalten. Diese Fehlercodes sind in der Header Datei mediaerr. h definiert.
ms.assetid: 1ded5656-084d-4315-a414-aebf4a1820dc
title: DMO-Fehler Codes (mediaerr. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d76c8cd5e7001751cd2cf9eb7da4d88b2dc100bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365797"
---
# <a name="dmo-error-codes"></a><span data-ttu-id="da4f1-104">DMO-Fehler Codes</span><span class="sxs-lookup"><span data-stu-id="da4f1-104">DMO Error Codes</span></span>

<span data-ttu-id="da4f1-105">In der folgenden Tabelle sind die für Microsoft DirectX Media Objects (DMOs) spezifischen Fehlercodes enthalten.</span><span class="sxs-lookup"><span data-stu-id="da4f1-105">The following table contains error codes that are specific to Microsoft DirectX Media Objects (DMOs).</span></span> <span data-ttu-id="da4f1-106">Diese Fehlercodes sind in der Header Datei mediaerr. h definiert.</span><span class="sxs-lookup"><span data-stu-id="da4f1-106">These error codes are defined in the header file Mediaerr.h.</span></span>



| <span data-ttu-id="da4f1-107">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="da4f1-107">Constant/value</span></span>                                                                                                                                                                                                                                                  | <span data-ttu-id="da4f1-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="da4f1-108">Description</span></span>                                                                                                                                                         |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DMO_E_INVALIDSTREAMINDEX"></span><span id="dmo_e_invalidstreamindex"></span><dl> <span data-ttu-id="da4f1-109"><dt>**DMO \_ E \_ invalidstreamindex**</dt> <dt>0x80040201</dt></span><span class="sxs-lookup"><span data-stu-id="da4f1-109"><dt>**DMO\_E\_INVALIDSTREAMINDEX**</dt> <dt>0x80040201</dt></span></span> </dl> | <span data-ttu-id="da4f1-110">Ungültiger streamindex.</span><span class="sxs-lookup"><span data-stu-id="da4f1-110">Invalid stream index.</span></span><br/>                                                                                                                                    |
| <span id="DMO_E_INVALIDTYPE"></span><span id="dmo_e_invalidtype"></span><dl> <span data-ttu-id="da4f1-111"><dt>**DMO \_ E \_ invalidtype**</dt> <dt>0x80040202</dt></span><span class="sxs-lookup"><span data-stu-id="da4f1-111"><dt>**DMO\_E\_INVALIDTYPE**</dt> <dt>0x80040202</dt></span></span> </dl>                      | <span data-ttu-id="da4f1-112">Ungültiger Medientyp.</span><span class="sxs-lookup"><span data-stu-id="da4f1-112">Invalid media type.</span></span><br/>                                                                                                                                      |
| <span id="DMO_E_TYPE_NOT_SET"></span><span id="dmo_e_type_not_set"></span><dl> <span data-ttu-id="da4f1-113"><dt>**DMO \_ E- \_ Typ \_ nicht \_ festgelegt**</dt> <dt>0x80040203</dt></span><span class="sxs-lookup"><span data-stu-id="da4f1-113"><dt>**DMO\_E\_TYPE\_NOT\_SET**</dt> <dt>0x80040203</dt></span></span> </dl>                 | <span data-ttu-id="da4f1-114">Der Medientyp wurde nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="da4f1-114">Media type was not set.</span></span> <span data-ttu-id="da4f1-115">Mindestens ein Stream erfordert einen Medientyp, bevor dieser Vorgang ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="da4f1-115">One or more streams require a media type before this operation can be performed.</span></span><br/>                                                 |
| <span id="DMO_E_NOTACCEPTING"></span><span id="dmo_e_notaccepting"></span><dl> <span data-ttu-id="da4f1-116"><dt>**DMO \_ E nicht \_ akzeptieren**</dt> <dt>0x80040204</dt></span><span class="sxs-lookup"><span data-stu-id="da4f1-116"><dt>**DMO\_E\_NOTACCEPTING**</dt> <dt>0x80040204</dt></span></span> </dl>                   | <span data-ttu-id="da4f1-117">Daten können für diesen Datenstrom nicht akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="da4f1-117">Data cannot be accepted on this stream.</span></span> <span data-ttu-id="da4f1-118">Möglicherweise müssen Sie mehr Ausgabedaten verarbeiten. Weitere Informationen finden Sie unter [**imediaobject::P rocessinput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processinput).</span><span class="sxs-lookup"><span data-stu-id="da4f1-118">You might need to process more output data; see [**IMediaObject::ProcessInput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processinput).</span></span><br/> |
| <span id="DMO_E_TYPE_NOT_ACCEPTED"></span><span id="dmo_e_type_not_accepted"></span><dl> <span data-ttu-id="da4f1-119"><dt>**DMO \_ E- \_ Typ \_ nicht \_ akzeptiert**</dt> <dt>0x80040205</dt></span><span class="sxs-lookup"><span data-stu-id="da4f1-119"><dt>**DMO\_E\_TYPE\_NOT\_ACCEPTED**</dt> <dt>0x80040205</dt></span></span> </dl>  | <span data-ttu-id="da4f1-120">Der Medientyp wurde nicht akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="da4f1-120">Media type was not accepted.</span></span><br/>                                                                                                                             |
| <span id="DMO_E_NO_MORE_ITEMS"></span><span id="dmo_e_no_more_items"></span><dl> <span data-ttu-id="da4f1-121"><dt>**DMO \_ E \_ keine \_ weiteren \_ Elemente**</dt> <dt>0x80040206</dt></span><span class="sxs-lookup"><span data-stu-id="da4f1-121"><dt>**DMO\_E\_NO\_MORE\_ITEMS**</dt> <dt>0x80040206</dt></span></span> </dl>              | <span data-ttu-id="da4f1-122">Der Medientyp Index liegt außerhalb des zulässigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="da4f1-122">Media-type index is out of range.</span></span><br/>                                                                                                                        |



## <a name="requirements"></a><span data-ttu-id="da4f1-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da4f1-123">Requirements</span></span>



| <span data-ttu-id="da4f1-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da4f1-124">Requirement</span></span> | <span data-ttu-id="da4f1-125">Wert</span><span class="sxs-lookup"><span data-stu-id="da4f1-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="da4f1-126">Header</span><span class="sxs-lookup"><span data-stu-id="da4f1-126">Header</span></span><br/> | <dl> <span data-ttu-id="da4f1-127"><dt>Mediaerr. h</dt></span><span class="sxs-lookup"><span data-stu-id="da4f1-127"><dt>Mediaerr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da4f1-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da4f1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da4f1-129">DMO-Konstanten</span><span class="sxs-lookup"><span data-stu-id="da4f1-129">DMO Constants</span></span>](dmo-constants.md)
</dt> </dl>

 

 




