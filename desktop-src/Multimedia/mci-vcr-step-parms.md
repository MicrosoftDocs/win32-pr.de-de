---
title: MCI_VCR_STEP_PARMS Struktur (VCR. h)
description: Die Struktur der MCI- \_ VCR- \_ Schritt- \_ Parameter enthält Parameter für den MCI- \_ Schritt Befehl für Video-Kassetten-Recorder.
ms.assetid: 57751de6-d174-418f-8167-402d3ead4e24
keywords:
- MCI_VCR_STEP_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_STEP_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a616b31500a2c814edb3dd443586131ed0ffae7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040219"
---
# <a name="mci_vcr_step_parms-structure"></a><span data-ttu-id="6d4c8-104">Struktur von MCI- \_ VCR- \_ Schritt- \_ Parametern</span><span class="sxs-lookup"><span data-stu-id="6d4c8-104">MCI\_VCR\_STEP\_PARMS structure</span></span>

<span data-ttu-id="6d4c8-105">Die Struktur der **MCI- \_ VCR- \_ Schritt \_** -Parameter enthält Parameter für den [**MCI- \_ Schritt**](mci-step.md) Befehl für Video-Kassetten-Recorder.</span><span class="sxs-lookup"><span data-stu-id="6d4c8-105">The **MCI\_VCR\_STEP\_PARMS** structure contains parameters for the [**MCI\_STEP**](mci-step.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d4c8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d4c8-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_STEP_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrames;
} MCI_VCR_STEP_PARMS;
```



## <a name="members"></a><span data-ttu-id="6d4c8-107">Member</span><span class="sxs-lookup"><span data-stu-id="6d4c8-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="6d4c8-108">**dwcallback**</span><span class="sxs-lookup"><span data-stu-id="6d4c8-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="6d4c8-109">Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="6d4c8-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="6d4c8-110">**dwframes**</span><span class="sxs-lookup"><span data-stu-id="6d4c8-110">**dwFrames**</span></span>
</dt> <dd>

<span data-ttu-id="6d4c8-111">Die Anzahl der zu über springenden Frames (die Länge eines einzelnen Schritts), wenn der [**MCI- \_ Schritt**](mci-step.md) Befehl den Inhalt vorwärts oder rückwärts durchläuft.</span><span class="sxs-lookup"><span data-stu-id="6d4c8-111">Number of frames to jump (the length of a single step) as the [**MCI\_STEP**](mci-step.md) command steps forward or backward through the content.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6d4c8-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d4c8-112">Remarks</span></span>

<span data-ttu-id="6d4c8-113">Wenn Sie den Elementen in dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter von [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) fest, um die Elemente zu validieren.</span><span class="sxs-lookup"><span data-stu-id="6d4c8-113">When assigning data to the members in this structure, set the corresponding flags in the *fdwCommand* parameter of [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d4c8-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d4c8-114">Requirements</span></span>



| <span data-ttu-id="6d4c8-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6d4c8-115">Requirement</span></span> | <span data-ttu-id="6d4c8-116">Wert</span><span class="sxs-lookup"><span data-stu-id="6d4c8-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6d4c8-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6d4c8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6d4c8-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6d4c8-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6d4c8-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6d4c8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6d4c8-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6d4c8-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6d4c8-121">Header</span><span class="sxs-lookup"><span data-stu-id="6d4c8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d4c8-122"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d4c8-122"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d4c8-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d4c8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d4c8-124">**MCI**</span><span class="sxs-lookup"><span data-stu-id="6d4c8-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="6d4c8-125">**MCI-Strukturen**</span><span class="sxs-lookup"><span data-stu-id="6d4c8-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="6d4c8-126">**MCI- \_ Schritt**</span><span class="sxs-lookup"><span data-stu-id="6d4c8-126">**MCI\_STEP**</span></span>](mci-step.md)
</dt> <dt>

<span data-ttu-id="6d4c8-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6d4c8-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

