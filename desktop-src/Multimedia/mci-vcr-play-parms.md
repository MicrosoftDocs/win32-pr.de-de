---
title: MCI_VCR_PLAY_PARMS Struktur (VCR. h)
description: Die MCI- \_ VCR- \_ Wiedergabe \_ Parameter Struktur enthält Parameter für den MCI \_ -Wiedergabe Befehl für Video-Kassetten-Recorder.
ms.assetid: e180c203-3113-4fdb-bcf1-ea3e45e646e2
keywords:
- MCI_VCR_PLAY_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_PLAY_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae15eedc69accc88ef7a58a6d7ad435e872de7ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956576"
---
# <a name="mci_vcr_play_parms-structure"></a><span data-ttu-id="c112a-104">MCI \_ VCR-Wiedergabe-Parametern- \_ \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="c112a-104">MCI\_VCR\_PLAY\_PARMS structure</span></span>

<span data-ttu-id="c112a-105">Die **MCI- \_ VCR- \_ Wiedergabe \_** Parameter Struktur enthält Parameter für den [**MCI- \_ Wiedergabe**](mci-play.md) Befehl für Video-Kassetten-Recorder.</span><span class="sxs-lookup"><span data-stu-id="c112a-105">The **MCI\_VCR\_PLAY\_PARMS** structure contains parameters for the [**MCI\_PLAY**](mci-play.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="c112a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c112a-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_PLAY_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwAt;
} MCI_VCR_PLAY_PARMS;
```



## <a name="members"></a><span data-ttu-id="c112a-107">Member</span><span class="sxs-lookup"><span data-stu-id="c112a-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c112a-108">**dwcallback**</span><span class="sxs-lookup"><span data-stu-id="c112a-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="c112a-109">Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="c112a-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="c112a-110">**dwfrom**</span><span class="sxs-lookup"><span data-stu-id="c112a-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="c112a-111">Wiedergabe Position</span><span class="sxs-lookup"><span data-stu-id="c112a-111">Position to play from.</span></span>

</dd> <dt>

<span data-ttu-id="c112a-112">**dwto**</span><span class="sxs-lookup"><span data-stu-id="c112a-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="c112a-113">Position der Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="c112a-113">Position to play to.</span></span>

</dd> <dt>

<span data-ttu-id="c112a-114">**dwat**</span><span class="sxs-lookup"><span data-stu-id="c112a-114">**dwAt**</span></span>
</dt> <dd>

<span data-ttu-id="c112a-115">Der Uhrzeitwert, der sich auf den Befehl [**MCI \_ Play**](mci-play.md) oder [**\_ MCI**](mci-cue.md) -Hinweis auswirkt.</span><span class="sxs-lookup"><span data-stu-id="c112a-115">Time value that affects the [**MCI\_PLAY**](mci-play.md) or [**MCI\_CUE**](mci-cue.md) command.</span></span> <span data-ttu-id="c112a-116">Bei der Wiedergabe von [**MCI \_ ist**](mci-play-parms.md)dies der Zeitpunkt, zu dem die Wiedergabe beginnt.</span><span class="sxs-lookup"><span data-stu-id="c112a-116">For [**MCI\_PLAY**](mci-play-parms.md), this is the time when playback begins.</span></span> <span data-ttu-id="c112a-117">Bei **MCI \_**-Hinweis ist dies die Zeit, zu der das cubegerät die in **dwfrom** angegebene Position erreicht.</span><span class="sxs-lookup"><span data-stu-id="c112a-117">For **MCI\_CUE**, this is the time when the cued device reaches the position given in **dwFrom**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c112a-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c112a-118">Remarks</span></span>

<span data-ttu-id="c112a-119">Positionen werden im aktuellen Zeitformat angegeben.</span><span class="sxs-lookup"><span data-stu-id="c112a-119">Positions are specified in the current time format.</span></span>

<span data-ttu-id="c112a-120">Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="c112a-120">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="c112a-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c112a-121">Requirements</span></span>



| <span data-ttu-id="c112a-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c112a-122">Requirement</span></span> | <span data-ttu-id="c112a-123">Wert</span><span class="sxs-lookup"><span data-stu-id="c112a-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c112a-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c112a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c112a-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c112a-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c112a-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c112a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c112a-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c112a-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c112a-128">Header</span><span class="sxs-lookup"><span data-stu-id="c112a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c112a-129"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="c112a-129"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c112a-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c112a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c112a-131">**MCI**</span><span class="sxs-lookup"><span data-stu-id="c112a-131">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c112a-132">**MCI-Strukturen**</span><span class="sxs-lookup"><span data-stu-id="c112a-132">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="c112a-133">**MCI \_ -Hinweis**</span><span class="sxs-lookup"><span data-stu-id="c112a-133">**MCI\_CUE**</span></span>](mci-cue.md)
</dt> <dt>

[<span data-ttu-id="c112a-134">**MCI- \_ Play**</span><span class="sxs-lookup"><span data-stu-id="c112a-134">**MCI\_PLAY**</span></span>](mci-play.md)
</dt> <dt>

<span data-ttu-id="c112a-135">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c112a-135">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

