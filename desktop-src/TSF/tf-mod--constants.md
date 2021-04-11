---
title: TF_MOD_ Konstanten (msctf. h)
description: Die TF \_ mod \_ \-Konstanten geben schlüsselmodifizierer in der TF \_ preservedkey-Struktur an.
ms.assetid: 4642ef17-34bd-4482-a9e9-0fbed7b574b1
topic_type:
- apiref
api_name:
- TF_MOD_ALT
- TF_MOD_CONTROL
- TF_MOD_SHIFT
- TF_MOD_RALT
- TF_MOD_RCONTROL
- TF_MOD_RSHIFT
- TF_MOD_LALT
- TF_MOD_LCONTROL
- TF_MOD_LSHIFT
- TF_MOD_ON_KEYUP
- TF_MOD_IGNORE_ALL_MODIFIER
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e67e081d9a0f8714410861c7c36f9f751bad8d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040569"
---
# <a name="tf_mod_-constants"></a><span data-ttu-id="1e38e-103">TF- \_ mod- \_ \* Konstanten</span><span class="sxs-lookup"><span data-stu-id="1e38e-103">TF\_MOD\_\* Constants</span></span>

<span data-ttu-id="1e38e-104">Die TF \_ mod- \_ \* Konstanten geben schlüsselmodifizierer in der [tf \_ preservedkey](/windows/desktop/api/Msctf/ns-msctf-tf_preservedkey) -Struktur an.</span><span class="sxs-lookup"><span data-stu-id="1e38e-104">The TF\_MOD\_\* constants specify key modifiers in the [TF\_PRESERVEDKEY](/windows/desktop/api/Msctf/ns-msctf-tf_preservedkey) structure.</span></span>



| <span data-ttu-id="1e38e-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="1e38e-105">Constant/value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="1e38e-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1e38e-106">Description</span></span>                                                                                                                                                                          |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_MOD_ALT"></span><span id="tf_mod_alt"></span><dl> <span data-ttu-id="1e38e-107"><dt>**Tf \_ MOD \_ alt**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="1e38e-107"><dt>**TF\_MOD\_ALT**</dt> <dt>0x0001</dt></span></span> </dl>                                                   | <span data-ttu-id="1e38e-108">Jeder der Alt-Taste wird gedrückt.</span><span class="sxs-lookup"><span data-stu-id="1e38e-108">Either of the ALT keys is pressed</span></span><br/>                                                                                                                                         |
| <span id="TF_MOD_CONTROL"></span><span id="tf_mod_control"></span><dl> <span data-ttu-id="1e38e-109"><dt>**Tf \_ MOD- \_ Steuer**</dt> Element <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="1e38e-109"><dt>**TF\_MOD\_CONTROL**</dt> <dt>0x0002</dt></span></span> </dl>                                       | <span data-ttu-id="1e38e-110">Eine der STRG-Taste wird gedrückt.</span><span class="sxs-lookup"><span data-stu-id="1e38e-110">Either of the CTRL keys is pressed</span></span><br/>                                                                                                                                        |
| <span id="TF_MOD_SHIFT"></span><span id="tf_mod_shift"></span><dl> <span data-ttu-id="1e38e-111"><dt>**Tf \_ MOD \_ Shift**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="1e38e-111"><dt>**TF\_MOD\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>                                             | <span data-ttu-id="1e38e-112">Beide Umschalt Tasten werden gedrückt.</span><span class="sxs-lookup"><span data-stu-id="1e38e-112">Either of the SHIFT keys is pressed</span></span><br/>                                                                                                                                       |
| <span id="TF_MOD_RALT"></span><span id="tf_mod_ralt"></span><dl> <span data-ttu-id="1e38e-113"><dt>**Tf \_ MOD \_ Ralt**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="1e38e-113"><dt>**TF\_MOD\_RALT**</dt> <dt>0x0008</dt></span></span> </dl>                                                | <span data-ttu-id="1e38e-114">Die Rechte ALT-Taste wird gedrückt.</span><span class="sxs-lookup"><span data-stu-id="1e38e-114">The right ALT key is pressed</span></span><br/>                                                                                                                                              |
| <span id="TF_MOD_RCONTROL"></span><span id="tf_mod_rcontrol"></span><dl> <span data-ttu-id="1e38e-115"><dt>**Tf \_ MOD \_ rcontrol**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="1e38e-115"><dt>**TF\_MOD\_RCONTROL**</dt> <dt>0x0010</dt></span></span> </dl>                                    | <span data-ttu-id="1e38e-116">Die Rechte STRG-Taste wird gedrückt.</span><span class="sxs-lookup"><span data-stu-id="1e38e-116">The right CTRL key is pressed</span></span><br/>                                                                                                                                             |
| <span id="TF_MOD_RSHIFT"></span><span id="tf_mod_rshift"></span><dl> <span data-ttu-id="1e38e-117"><dt>**Tf \_ MOD \_ rshift**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="1e38e-117"><dt>**TF\_MOD\_RSHIFT**</dt> <dt>0x0020</dt></span></span> </dl>                                          | <span data-ttu-id="1e38e-118">Die Rechte UMSCHALTTASTE wird gedrückt.</span><span class="sxs-lookup"><span data-stu-id="1e38e-118">The right SHIFT key is pressed</span></span><br/>                                                                                                                                            |
| <span id="TF_MOD_LALT"></span><span id="tf_mod_lalt"></span><dl> <span data-ttu-id="1e38e-119"><dt>**Tf \_ MOD \_ LAlt**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="1e38e-119"><dt>**TF\_MOD\_LALT**</dt> <dt>0x0040</dt></span></span> </dl>                                                | <span data-ttu-id="1e38e-120">Die linke ALT-Taste wird gedrückt.</span><span class="sxs-lookup"><span data-stu-id="1e38e-120">The left ALT key is pressed</span></span><br/>                                                                                                                                               |
| <span id="TF_MOD_LCONTROL"></span><span id="tf_mod_lcontrol"></span><dl> <span data-ttu-id="1e38e-121"><dt>**Tf \_ MOD \_ lcontrol**</dt> <dt>0x0080</dt></span><span class="sxs-lookup"><span data-stu-id="1e38e-121"><dt>**TF\_MOD\_LCONTROL**</dt> <dt>0x0080</dt></span></span> </dl>                                    | <span data-ttu-id="1e38e-122">Die linke STRG-Taste wird gedrückt.</span><span class="sxs-lookup"><span data-stu-id="1e38e-122">The left CTRL key is pressed</span></span><br/>                                                                                                                                              |
| <span id="TF_MOD_LSHIFT"></span><span id="tf_mod_lshift"></span><dl> <span data-ttu-id="1e38e-123"><dt>**Tf \_ MOD \_ LShift**</dt> <dt>0x0100</dt></span><span class="sxs-lookup"><span data-stu-id="1e38e-123"><dt>**TF\_MOD\_LSHIFT**</dt> <dt>0x0100</dt></span></span> </dl>                                          | <span data-ttu-id="1e38e-124">Die Linke UMSCHALTTASTE wird gedrückt.</span><span class="sxs-lookup"><span data-stu-id="1e38e-124">The left SHIFT key is pressed</span></span><br/>                                                                                                                                             |
| <span id="TF_MOD_ON_KEYUP"></span><span id="tf_mod_on_keyup"></span><dl> <span data-ttu-id="1e38e-125"><dt>**Tf \_ MOD \_ für \_ KeyUp**</dt> <dt>0x0200</dt></span><span class="sxs-lookup"><span data-stu-id="1e38e-125"><dt>**TF\_MOD\_ON\_KEYUP**</dt> <dt>0x0200</dt></span></span> </dl>                                   | <span data-ttu-id="1e38e-126">Das Ereignis wird ausgelöst, wenn der Schlüssel freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1e38e-126">The event will be fired when the key is released.</span></span> <span data-ttu-id="1e38e-127">Ohne dieses Flag wird das-Ereignis ausgelöst, wenn die Taste gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="1e38e-127">Without this flag, the event is fired when the key is pressed.</span></span><br/>                                                          |
| <span id="TF_MOD_IGNORE_ALL_MODIFIER"></span><span id="tf_mod_ignore_all_modifier"></span><dl> <span data-ttu-id="1e38e-128"><dt>**Tf \_ MOD \_ \_ alle \_ Modifizierer**</dt> <dt>0x0400</dt> ignorieren</span><span class="sxs-lookup"><span data-stu-id="1e38e-128"><dt>**TF\_MOD\_IGNORE\_ALL\_MODIFIER**</dt> <dt>0x0400</dt></span></span> </dl> | <span data-ttu-id="1e38e-129">Der Zustand der Alt-Taste, der STRG-Taste und der UMSCHALTTASTE wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="1e38e-129">The state of the ALT, CTRL, and SHIFT keys is ignored.</span></span> <span data-ttu-id="1e38e-130">Dies bedeutet, dass das Ereignis beim Drücken der virtuellen Taste ausgelöst wird, unabhängig davon, welche Modifizierertasten gedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="1e38e-130">This means the event will be fired when the virtual key is pressed, regardless of which modifier keys are pressed.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="1e38e-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e38e-131">Requirements</span></span>



| <span data-ttu-id="1e38e-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1e38e-132">Requirement</span></span> | <span data-ttu-id="1e38e-133">Wert</span><span class="sxs-lookup"><span data-stu-id="1e38e-133">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1e38e-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1e38e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="1e38e-135">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1e38e-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1e38e-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1e38e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="1e38e-137">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1e38e-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1e38e-138">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="1e38e-138">Redistributable</span></span><br/>          | <span data-ttu-id="1e38e-139">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1e38e-139">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="1e38e-140">Header</span><span class="sxs-lookup"><span data-stu-id="1e38e-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e38e-141"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e38e-141"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="1e38e-142">IDL</span><span class="sxs-lookup"><span data-stu-id="1e38e-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1e38e-143"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1e38e-143"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e38e-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e38e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e38e-145">TF \_ preservedkey</span><span class="sxs-lookup"><span data-stu-id="1e38e-145">TF\_PRESERVEDKEY</span></span>](/windows/desktop/api/Msctf/ns-msctf-tf_preservedkey)
</dt> </dl>

 

 





