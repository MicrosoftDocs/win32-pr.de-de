---
title: WMT_RIGHTS-Enumeration (wmdrmsdk. h)
description: Definiert die Rechte, die in einer DRM-Lizenz angegeben werden können.
ms.assetid: 9c034ca0-83e9-4a4c-8e98-96e2a95fd97c
keywords:
- WMT_RIGHTS-Enumeration Windows Media-Format
- Enumeration Windows Media-Format
topic_type:
- apiref
api_name:
- WMT_RIGHTS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 644cff9c94876fab11bc9fbe181ac0375d9444fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369356"
---
# <a name="wmt_rights-enumeration"></a><span data-ttu-id="46393-105">WMT- \_ Rechte Enumeration</span><span class="sxs-lookup"><span data-stu-id="46393-105">WMT\_RIGHTS enumeration</span></span>

<span data-ttu-id="46393-106">Der Enumerationstyp **WMT- \_ Rechte** definiert die Rechte, die in einer DRM-Lizenz angegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="46393-106">The **WMT\_RIGHTS** enumeration type defines the rights that may be specified in a DRM license.</span></span>

## <a name="syntax"></a><span data-ttu-id="46393-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="46393-107">Syntax</span></span>


```C++
typedef enum WMT_RIGHTS { 
  WMT_RIGHT_PLAYBACK                 = 0x00000001,
  WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE  = 0x00000002,
  WMT_RIGHT_COPY_TO_CD               = 0x00000008,
  WMT_RIGHT_COPY_TO_SDMI_DEVICE      = 0x00000010,
  WMT_RIGHT_ONE_TIME                 = 0x00000020,
  WMT_RIGHT_SAVE_STREAM_PROTECTED    = 0x00000040,
  WMT_RIGHT_COPY                     = 0x00000080,
  WMT_RIGHT_COLLABORATIVE_PLAY       = 0x00000100,
  WMT_RIGHT_SDMI_TRIGGER             = 0x00010000,
  WMT_RIGHT_SDMI_NOMORECOPIES        = 0x00020000
} ;
```



## <a name="constants"></a><span data-ttu-id="46393-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="46393-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="46393-109"><span id="WMT_RIGHT_PLAYBACK"></span><span id="wmt_right_playback"></span>**WMT \_ right- \_ Wiedergabe**</span><span class="sxs-lookup"><span data-stu-id="46393-109"><span id="WMT_RIGHT_PLAYBACK"></span><span id="wmt_right_playback"></span>**WMT\_RIGHT\_PLAYBACK**</span></span>
</dt> <dd>

<span data-ttu-id="46393-110">Gibt die Berechtigung an, Inhalte ohne Einschränkung wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="46393-110">Specifies the right to play content without restriction.</span></span>

</dd> <dt>

<span data-ttu-id="46393-111"><span id="WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE"></span><span id="wmt_right_copy_to_non_sdmi_device"></span>**WMT- \_ Rechte \_ Kopie \_ auf nicht- \_ \_ SDMI- \_ Gerät**</span><span class="sxs-lookup"><span data-stu-id="46393-111"><span id="WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE"></span><span id="wmt_right_copy_to_non_sdmi_device"></span>**WMT\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE**</span></span>
</dt> <dd>

<span data-ttu-id="46393-112">Gibt die Berechtigung an, Inhalte auf ein Gerät zu kopieren, das mit der Secure Digital Music Initiative (SDMI) nicht kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="46393-112">Specifies the right to copy content to a device not compliant with the Secure Digital Music Initiative (SDMI).</span></span>

</dd> <dt>

<span data-ttu-id="46393-113"><span id="WMT_RIGHT_COPY_TO_CD"></span><span id="wmt_right_copy_to_cd"></span>**WMT- \_ Rechte \_ Kopie \_ auf \_ CD**</span><span class="sxs-lookup"><span data-stu-id="46393-113"><span id="WMT_RIGHT_COPY_TO_CD"></span><span id="wmt_right_copy_to_cd"></span>**WMT\_RIGHT\_COPY\_TO\_CD**</span></span>
</dt> <dd>

<span data-ttu-id="46393-114">Gibt die Berechtigung an, Inhalte auf eine CD zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="46393-114">Specifies the right to copy content to a CD.</span></span>

</dd> <dt>

<span data-ttu-id="46393-115"><span id="WMT_RIGHT_COPY_TO_SDMI_DEVICE"></span><span id="wmt_right_copy_to_sdmi_device"></span>**WMT- \_ Rechte \_ Kopie \_ auf \_ SDMI- \_ Gerät kopieren**</span><span class="sxs-lookup"><span data-stu-id="46393-115"><span id="WMT_RIGHT_COPY_TO_SDMI_DEVICE"></span><span id="wmt_right_copy_to_sdmi_device"></span>**WMT\_RIGHT\_COPY\_TO\_SDMI\_DEVICE**</span></span>
</dt> <dd>

<span data-ttu-id="46393-116">Gibt die Berechtigung an, Inhalte auf ein Gerät zu kopieren, das mit dem SDMI kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="46393-116">Specifies the right to copy content to a device compliant with the SDMI.</span></span>

</dd> <dt>

<span data-ttu-id="46393-117"><span id="WMT_RIGHT_ONE_TIME"></span><span id="wmt_right_one_time"></span>**WMT \_ right \_ einmalig \_**</span><span class="sxs-lookup"><span data-stu-id="46393-117"><span id="WMT_RIGHT_ONE_TIME"></span><span id="wmt_right_one_time"></span>**WMT\_RIGHT\_ONE\_TIME**</span></span>
</dt> <dd>

<span data-ttu-id="46393-118">Gibt die Berechtigung an, den Inhalt nur einmal wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="46393-118">Specifies the right to play content one time only.</span></span>

</dd> <dt>

<span data-ttu-id="46393-119"><span id="WMT_RIGHT_SAVE_STREAM_PROTECTED"></span><span id="wmt_right_save_stream_protected"></span>**WMT \_ right \_ Save \_ Stream \_ Protected**</span><span class="sxs-lookup"><span data-stu-id="46393-119"><span id="WMT_RIGHT_SAVE_STREAM_PROTECTED"></span><span id="wmt_right_save_stream_protected"></span>**WMT\_RIGHT\_SAVE\_STREAM\_PROTECTED**</span></span>
</dt> <dd>

<span data-ttu-id="46393-120">Gibt die Berechtigung an, Inhalte von einem Server zu speichern.</span><span class="sxs-lookup"><span data-stu-id="46393-120">Specifies the right to save content from a server.</span></span>

</dd> <dt>

<span data-ttu-id="46393-121"><span id="WMT_RIGHT_COPY"></span><span id="wmt_right_copy"></span>**WMT- \_ Rechte \_ Kopie**</span><span class="sxs-lookup"><span data-stu-id="46393-121"><span id="WMT_RIGHT_COPY"></span><span id="wmt_right_copy"></span>**WMT\_RIGHT\_COPY**</span></span>
</dt> <dd>

<span data-ttu-id="46393-122">Gibt die Berechtigung an, Inhalte zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="46393-122">Specifies the right to copy content.</span></span> <span data-ttu-id="46393-123">Windows Media DRM 10 regelt die Geräte, auf die der Inhalt kopiert werden kann, mithilfe von "Output Protection Levels (opls)".</span><span class="sxs-lookup"><span data-stu-id="46393-123">Windows Media DRM 10 regulates the devices to which the content can be copied by using output protection levels (OPLs).</span></span>

</dd> <dt>

<span data-ttu-id="46393-124"><span id="WMT_RIGHT_COLLABORATIVE_PLAY"></span><span id="wmt_right_collaborative_play"></span>**WMT \_ right \_ COLLABORATIVE \_ Play**</span><span class="sxs-lookup"><span data-stu-id="46393-124"><span id="WMT_RIGHT_COLLABORATIVE_PLAY"></span><span id="wmt_right_collaborative_play"></span>**WMT\_RIGHT\_COLLABORATIVE\_PLAY**</span></span>
</dt> <dd>

<span data-ttu-id="46393-125">Gibt die Berechtigung an, Inhalte als Teil eines Online Szenarios wiederzugeben, in dem mehrere Teilnehmer in einer freigegebenen Wiedergabeliste auf Titel aus Ihrer Sammlung mitwirken können.</span><span class="sxs-lookup"><span data-stu-id="46393-125">Specifies the right to play content as part of an online scenario where multiple participants can contribute songs from their collection to a shared playlist.</span></span>

</dd> <dt>

<span data-ttu-id="46393-126"><span id="WMT_RIGHT_SDMI_TRIGGER"></span><span id="wmt_right_sdmi_trigger"></span>**WMT \_ right- \_ SDMI-Auslösung \_**</span><span class="sxs-lookup"><span data-stu-id="46393-126"><span id="WMT_RIGHT_SDMI_TRIGGER"></span><span id="wmt_right_sdmi_trigger"></span>**WMT\_RIGHT\_SDMI\_TRIGGER**</span></span>
</dt> <dd>

<span data-ttu-id="46393-127">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="46393-127">Reserved for future use.</span></span> <span data-ttu-id="46393-128">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="46393-128">Do not use.</span></span>

</dd> <dt>

<span data-ttu-id="46393-129"><span id="WMT_RIGHT_SDMI_NOMORECOPIES"></span><span id="wmt_right_sdmi_nomorecopies"></span>**WMT \_ right \_ SDMI \_ nomorecopies**</span><span class="sxs-lookup"><span data-stu-id="46393-129"><span id="WMT_RIGHT_SDMI_NOMORECOPIES"></span><span id="wmt_right_sdmi_nomorecopies"></span>**WMT\_RIGHT\_SDMI\_NOMORECOPIES**</span></span>
</dt> <dd>

<span data-ttu-id="46393-130">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="46393-130">Reserved for future use.</span></span> <span data-ttu-id="46393-131">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="46393-131">Do not use.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="46393-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46393-132">Remarks</span></span>

<span data-ttu-id="46393-133">Diese Werte sind Bitflags, sodass eine oder mehrere festgelegt werden können, indem Sie mit dem bitweisen **or** -Operator kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="46393-133">These values are bit flags, so one or more can be set by combining them with the bitwise **OR** operator.</span></span>

<span data-ttu-id="46393-134">Bei der Verwendung von Windows Media DRM 10 werden **WMT- \_ Rechte \_ auf ein nicht- \_ \_ \_ SDMI- \_ Gerät kopiert**, die **WMT-Rechte Kopie auf das \_ \_ \_ \_ SDMI- \_ Gerät** und die **WMT-Rechte Kopie \_ \_ \_ auf \_ CD** ersetzt durch die **WMT- \_ Rechte \_ Kopie**.</span><span class="sxs-lookup"><span data-stu-id="46393-134">When using Windows Media DRM 10, **WMT\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE**, **WMT\_RIGHT\_COPY\_TO\_SDMI\_DEVICE**, and **WMT\_RIGHT\_COPY\_TO\_CD** are superseded by **WMT\_RIGHT\_COPY**.</span></span> <span data-ttu-id="46393-135">Einschränkungen auf den Geräten, auf die der Inhalt kopiert werden kann, werden mithilfe von "Output Protection Levels (opls)" angegeben.</span><span class="sxs-lookup"><span data-stu-id="46393-135">Limitations on the devices to which the content may be copied are specified by using output protection levels (OPLs).</span></span>

## <a name="requirements"></a><span data-ttu-id="46393-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46393-136">Requirements</span></span>



| <span data-ttu-id="46393-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46393-137">Requirement</span></span> | <span data-ttu-id="46393-138">Wert</span><span class="sxs-lookup"><span data-stu-id="46393-138">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="46393-139">Header</span><span class="sxs-lookup"><span data-stu-id="46393-139">Header</span></span><br/> | <dl> <span data-ttu-id="46393-140"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="46393-140"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46393-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46393-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46393-142">**Enumerationstypen**</span><span class="sxs-lookup"><span data-stu-id="46393-142">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





