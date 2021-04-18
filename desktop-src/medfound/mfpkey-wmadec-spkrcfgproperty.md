---
description: Gibt die Sprecher Konfiguration auf dem Client Computer an.
ms.assetid: a0353e70-0741-4705-95e0-e76ebd8ba977
title: MFPKEY_WMADEC_SPKRCFG-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05ed96e4f722c1b3bd7c98178cd7f93a6c2e01df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528568"
---
# <a name="mfpkey_wmadec_spkrcfg-property"></a><span data-ttu-id="b4ecb-103">Mfpkey \_ wmadec \_ spkrcfg (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b4ecb-103">MFPKEY\_WMADEC\_SPKRCFG Property</span></span>

<span data-ttu-id="b4ecb-104">Gibt die Sprecher Konfiguration auf dem Client Computer an.</span><span class="sxs-lookup"><span data-stu-id="b4ecb-104">Specifies the speaker configuration on the client computer.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="b4ecb-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="b4ecb-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="b4ecb-106">g \_ wszwmacspeakerconfig</span><span class="sxs-lookup"><span data-stu-id="b4ecb-106">g\_wszWMACSpeakerConfig</span></span>

## <a name="data-type"></a><span data-ttu-id="b4ecb-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b4ecb-107">Data Type</span></span>

<span data-ttu-id="b4ecb-108">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="b4ecb-108">**VT\_UI4**</span></span>

## <a name="default-value"></a><span data-ttu-id="b4ecb-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="b4ecb-109">Default Value</span></span>

<span data-ttu-id="b4ecb-110">Es wird keine bestimmte Sprecher Konfiguration angenommen.</span><span class="sxs-lookup"><span data-stu-id="b4ecb-110">No specific speaker configuration is assumed.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4ecb-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b4ecb-111">Remarks</span></span>

<span data-ttu-id="b4ecb-112">Sie sollten diesen Wert auf eine der Konstanten oder Werte in der folgenden Tabelle festlegen.</span><span class="sxs-lookup"><span data-stu-id="b4ecb-112">You should set this value to one of the constants or values in the following table.</span></span> <span data-ttu-id="b4ecb-113">Die Konstanten sind in Microsoft DirectSound definiert und werden hier zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="b4ecb-113">The constants are defined in Microsoft DirectSound, and are listed here for convenience.</span></span> <span data-ttu-id="b4ecb-114">Um diese Konstanten Namen für den Compiler aufzulösen, müssen Sie DSound. h einschließen.</span><span class="sxs-lookup"><span data-stu-id="b4ecb-114">To resolve these constant names for your compiler, you must include dsound.h.</span></span>



| <span data-ttu-id="b4ecb-115">Konstante</span><span class="sxs-lookup"><span data-stu-id="b4ecb-115">Constant</span></span>             | <span data-ttu-id="b4ecb-116">Wert</span><span class="sxs-lookup"><span data-stu-id="b4ecb-116">Value</span></span>      | <span data-ttu-id="b4ecb-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b4ecb-117">Description</span></span>                                                                  |
|----------------------|------------|------------------------------------------------------------------------------|
| <span data-ttu-id="b4ecb-118">dsspeaker- \_ directout</span><span class="sxs-lookup"><span data-stu-id="b4ecb-118">DSSPEAKER\_DIRECTOUT</span></span> | <span data-ttu-id="b4ecb-119">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4ecb-119">0x00000000</span></span> | <span data-ttu-id="b4ecb-120">Die Audiodaten werden direkt durchlaufen, ohne für Referenten konfiguriert zu werden.</span><span class="sxs-lookup"><span data-stu-id="b4ecb-120">The audio is passed through directly, without being configured for speakers.</span></span> |
| <span data-ttu-id="b4ecb-121">dsspeaker- \_ Telefon</span><span class="sxs-lookup"><span data-stu-id="b4ecb-121">DSSPEAKER\_HEADPHONE</span></span> | <span data-ttu-id="b4ecb-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b4ecb-122">0x00000001</span></span> | <span data-ttu-id="b4ecb-123">Der Client Computer ist mit einem Kopfhörer ausgestattet.</span><span class="sxs-lookup"><span data-stu-id="b4ecb-123">The client computer is equipped with headphones.</span></span>                             |
| <span data-ttu-id="b4ecb-124">dsspeaker \_ Mono</span><span class="sxs-lookup"><span data-stu-id="b4ecb-124">DSSPEAKER\_MONO</span></span>      | <span data-ttu-id="b4ecb-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b4ecb-125">0x00000002</span></span> | <span data-ttu-id="b4ecb-126">Der Client Computer ist mit einem monoaural-Redner ausgestattet.</span><span class="sxs-lookup"><span data-stu-id="b4ecb-126">The client computer is equipped with a monoaural speaker.</span></span>                    |
| <span data-ttu-id="b4ecb-127">dsspeaker \_ Quad</span><span class="sxs-lookup"><span data-stu-id="b4ecb-127">DSSPEAKER\_QUAD</span></span>      | <span data-ttu-id="b4ecb-128">0x00000003</span><span class="sxs-lookup"><span data-stu-id="b4ecb-128">0x00000003</span></span> | <span data-ttu-id="b4ecb-129">Der Client Computer ist mit quadratischen sprechenden Referenten ausgestattet.</span><span class="sxs-lookup"><span data-stu-id="b4ecb-129">The client computer is equipped with quadraphonic speakers.</span></span>                  |
| <span data-ttu-id="b4ecb-130">dsspeaker- \_ Stereo</span><span class="sxs-lookup"><span data-stu-id="b4ecb-130">DSSPEAKER\_STEREO</span></span>    | <span data-ttu-id="b4ecb-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="b4ecb-131">0x00000004</span></span> | <span data-ttu-id="b4ecb-132">Der Client Computer ist mit Stereo Referenten ausgestattet.</span><span class="sxs-lookup"><span data-stu-id="b4ecb-132">The client computer is equipped with stereo speakers.</span></span>                        |
| <span data-ttu-id="b4ecb-133">Umschließen von dsspeaker \_</span><span class="sxs-lookup"><span data-stu-id="b4ecb-133">DSSPEAKER\_SURROUND</span></span>  | <span data-ttu-id="b4ecb-134">0x00000005</span><span class="sxs-lookup"><span data-stu-id="b4ecb-134">0x00000005</span></span> | <span data-ttu-id="b4ecb-135">Der Client Computer ist mit vier-Kanal-umschließenden sprechenden ausgestattet.</span><span class="sxs-lookup"><span data-stu-id="b4ecb-135">The client computer is equipped with four-channel surround-sound speakers.</span></span>   |
| <span data-ttu-id="b4ecb-136">Dsspeaker \_ 5point1</span><span class="sxs-lookup"><span data-stu-id="b4ecb-136">DSSPEAKER\_5POINT1</span></span>   | <span data-ttu-id="b4ecb-137">0x00000006</span><span class="sxs-lookup"><span data-stu-id="b4ecb-137">0x00000006</span></span> | <span data-ttu-id="b4ecb-138">Der Client Computer ist mit fünf Referenten und einem Subwoofer ausgestattet.</span><span class="sxs-lookup"><span data-stu-id="b4ecb-138">The client computer is equipped with five speakers and a subwoofer.</span></span>          |
| <span data-ttu-id="b4ecb-139">Dsspeaker \_ 7point1</span><span class="sxs-lookup"><span data-stu-id="b4ecb-139">DSSPEAKER\_7POINT1</span></span>   | <span data-ttu-id="b4ecb-140">0x00000007</span><span class="sxs-lookup"><span data-stu-id="b4ecb-140">0x00000007</span></span> | <span data-ttu-id="b4ecb-141">Der Client Computer ist mit sieben Referenten und einem Subwoofer ausgestattet.</span><span class="sxs-lookup"><span data-stu-id="b4ecb-141">The client computer is equipped with seven speakers and a subwoofer.</span></span>         |



 

<span data-ttu-id="b4ecb-142">Der für diese Eigenschaft festgelegte Wert bestimmt die Ausgabeformate, die vom Codec für Multichannel-Audiodaten aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="b4ecb-142">The value set for this property determines the output formats enumerated by the codec for multichannel audio.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4ecb-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b4ecb-143">Requirements</span></span>



| <span data-ttu-id="b4ecb-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b4ecb-144">Requirement</span></span> | <span data-ttu-id="b4ecb-145">Wert</span><span class="sxs-lookup"><span data-stu-id="b4ecb-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4ecb-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b4ecb-146">Minimum supported client</span></span><br/> | <span data-ttu-id="b4ecb-147">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b4ecb-147">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b4ecb-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b4ecb-148">Minimum supported server</span></span><br/> | <span data-ttu-id="b4ecb-149">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b4ecb-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b4ecb-150">Header</span><span class="sxs-lookup"><span data-stu-id="b4ecb-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4ecb-151"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4ecb-151"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4ecb-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4ecb-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4ecb-153">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b4ecb-153">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




