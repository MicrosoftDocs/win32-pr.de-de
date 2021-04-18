---
description: Gibt die durchschnittliche Volumeebene von Audioinhalten an.
ms.assetid: eabb36ff-300f-4ed1-aca3-9415627ac1a7
title: MFPKEY_WMADRC_AVGREF-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf18c37b00f84cc3ae3fdf1f44b2fbefcc56d9f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354572"
---
# <a name="mfpkey_wmadrc_avgref-property"></a><span data-ttu-id="403e0-103">Eigenschaft "mfpkey \_ wmadrc \_ avgref"</span><span class="sxs-lookup"><span data-stu-id="403e0-103">MFPKEY\_WMADRC\_AVGREF Property</span></span>

<span data-ttu-id="403e0-104">Gibt die durchschnittliche Volumeebene von Audioinhalten an.</span><span class="sxs-lookup"><span data-stu-id="403e0-104">Specifies the average volume level of audio content.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="403e0-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="403e0-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="403e0-106">g \_ wszwmadrcaveragereferenzierung</span><span class="sxs-lookup"><span data-stu-id="403e0-106">g\_wszWMADRCAverageReference</span></span>

## <a name="data-type"></a><span data-ttu-id="403e0-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="403e0-107">Data Type</span></span>

<span data-ttu-id="403e0-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="403e0-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="403e0-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="403e0-109">Remarks</span></span>

<span data-ttu-id="403e0-110">Sie können diesen Wert aus dem Encoder nach der Verarbeitung des Inhalts erhalten.</span><span class="sxs-lookup"><span data-stu-id="403e0-110">You can get this value from the encoder after the content is processed.</span></span> <span data-ttu-id="403e0-111">Dieser Wert kann auch für den Decoder für das dynamische Bereichs Steuerelement festgelegt werden, aber er wirkt sich nur dann aus, wenn die Eigenschaft " [mfpkey \_ wmadec \_ drcmode](mfpkey-wmadec-drcmodeproperty.md) " festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="403e0-111">This value can also be set on the decoder for the purpose of dynamic range control, but it will have an effect only if the [MFPKEY\_WMADEC\_DRCMODE](mfpkey-wmadec-drcmodeproperty.md) property is set.</span></span>

<span data-ttu-id="403e0-112">Weitere Informationen zum dynamischen Bereichs Steuerelement finden Sie im Webartikel [Windows Media Audio Professional-Codec-Features](/previous-versions/ms867218(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="403e0-112">For more information on dynamic range control see the web article [Windows Media Audio Professional Codec Features](/previous-versions/ms867218(v=msdn.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="403e0-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="403e0-113">Requirements</span></span>



| <span data-ttu-id="403e0-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="403e0-114">Requirement</span></span> | <span data-ttu-id="403e0-115">Wert</span><span class="sxs-lookup"><span data-stu-id="403e0-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="403e0-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="403e0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="403e0-117">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="403e0-117">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="403e0-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="403e0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="403e0-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="403e0-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="403e0-120">Header</span><span class="sxs-lookup"><span data-stu-id="403e0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="403e0-121"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="403e0-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="403e0-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="403e0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="403e0-123">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="403e0-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
