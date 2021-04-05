---
title: MCI_VCR_CUE_PARMS Struktur (VCR. h)
description: Die Struktur der MCI- \_ VCR-Hinweis \_ \_ Parameter enthält Parameter für den MCI-Hinweis \_ Befehl für Video-Kassetten-Recorder.
ms.assetid: b2ac0c43-93ea-41c9-b886-542bda57b59e
keywords:
- MCI_VCR_CUE_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_CUE_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eeae20495281640718f95066476f0f3ac89dc6f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859222"
---
# <a name="mci_vcr_cue_parms-structure"></a><span data-ttu-id="2d70e-104">Struktur von MCI VCR-Hinweis- \_ \_ \_ Parametern</span><span class="sxs-lookup"><span data-stu-id="2d70e-104">MCI\_VCR\_CUE\_PARMS structure</span></span>

<span data-ttu-id="2d70e-105">Die Struktur der **MCI- \_ VCR \_ \_** -Hinweis Parameter enthält Parameter für den [**MCI \_**](mci-cue.md) -Hinweis Befehl für Video-Kassetten-Recorder.</span><span class="sxs-lookup"><span data-stu-id="2d70e-105">The **MCI\_VCR\_CUE\_PARMS** structure contains parameters for the [**MCI\_CUE**](mci-cue.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d70e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d70e-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_CUE_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
} MCI_VCR_CUE_PARMS;
```



## <a name="members"></a><span data-ttu-id="2d70e-107">Member</span><span class="sxs-lookup"><span data-stu-id="2d70e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="2d70e-108">**dwcallback**</span><span class="sxs-lookup"><span data-stu-id="2d70e-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="2d70e-109">Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="2d70e-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="2d70e-110">**dwfrom**</span><span class="sxs-lookup"><span data-stu-id="2d70e-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="2d70e-111">Die Position, an der Sie sich orientieren</span><span class="sxs-lookup"><span data-stu-id="2d70e-111">Position to cue from.</span></span>

</dd> <dt>

<span data-ttu-id="2d70e-112">**dwto**</span><span class="sxs-lookup"><span data-stu-id="2d70e-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="2d70e-113">Positions Position</span><span class="sxs-lookup"><span data-stu-id="2d70e-113">Position to cue to.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2d70e-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2d70e-114">Remarks</span></span>

<span data-ttu-id="2d70e-115">Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="2d70e-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d70e-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2d70e-116">Requirements</span></span>



| <span data-ttu-id="2d70e-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2d70e-117">Requirement</span></span> | <span data-ttu-id="2d70e-118">Wert</span><span class="sxs-lookup"><span data-stu-id="2d70e-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2d70e-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2d70e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2d70e-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2d70e-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2d70e-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2d70e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2d70e-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2d70e-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2d70e-123">Header</span><span class="sxs-lookup"><span data-stu-id="2d70e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d70e-124"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d70e-124"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d70e-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d70e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d70e-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="2d70e-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="2d70e-127">**MCI-Strukturen**</span><span class="sxs-lookup"><span data-stu-id="2d70e-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="2d70e-128">**MCI \_ -Hinweis**</span><span class="sxs-lookup"><span data-stu-id="2d70e-128">**MCI\_CUE**</span></span>](mci-cue.md)
</dt> <dt>

<span data-ttu-id="2d70e-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2d70e-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

