---
title: MCI_VD_PLAY_PARMS-Struktur (mciapi. h)
description: Die Struktur der MCI-" \_ \_ Play-Parser" \_ enthält Positions-und Geschwindigkeitsinformationen für den MCI- \_ Wiedergabe Befehl für Videodisk-Geräte.
ms.assetid: 9fa8418f-3f69-4a9c-b23e-7d2e2c75c7af
keywords:
- MCI_VD_PLAY_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VD_PLAY_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3ab04ba5cf0a2b507370a4b777c19fd60a05c30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040650"
---
# <a name="mci_vd_play_parms-structure"></a><span data-ttu-id="9a49b-104">MCI-VD-Wiedergabe-Parametern- \_ \_ \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="9a49b-104">MCI\_VD\_PLAY\_PARMS structure</span></span>

<span data-ttu-id="9a49b-105">Die Struktur der **MCI-" \_ Play- \_ \_ Parser** " enthält Positions-und Geschwindigkeitsinformationen für den [**MCI- \_ Wiedergabe**](mci-play.md) Befehl für Videodisk-Geräte.</span><span class="sxs-lookup"><span data-stu-id="9a49b-105">The **MCI\_VD\_PLAY\_PARMS** structure contains position and speed information for the [**MCI\_PLAY**](mci-play.md) command for videodisc devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a49b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a49b-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwSpeed;
} MCI_VD_PLAY_PARMS;
```



## <a name="members"></a><span data-ttu-id="9a49b-107">Member</span><span class="sxs-lookup"><span data-stu-id="9a49b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="9a49b-108">**dwcallback**</span><span class="sxs-lookup"><span data-stu-id="9a49b-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="9a49b-109">Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="9a49b-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="9a49b-110">**dwfrom**</span><span class="sxs-lookup"><span data-stu-id="9a49b-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="9a49b-111">Wiedergabe Position</span><span class="sxs-lookup"><span data-stu-id="9a49b-111">Position to play from.</span></span>

</dd> <dt>

<span data-ttu-id="9a49b-112">**dwto**</span><span class="sxs-lookup"><span data-stu-id="9a49b-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="9a49b-113">Position der Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="9a49b-113">Position to play to.</span></span>

</dd> <dt>

<span data-ttu-id="9a49b-114">**dwspeed**</span><span class="sxs-lookup"><span data-stu-id="9a49b-114">**dwSpeed**</span></span>
</dt> <dd>

<span data-ttu-id="9a49b-115">Wiedergabegeschwindigkeit in Frames pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="9a49b-115">Playback speed in frames per second.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9a49b-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9a49b-116">Remarks</span></span>

<span data-ttu-id="9a49b-117">Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="9a49b-117">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

<span data-ttu-id="9a49b-118">Wenn Sie die erweiterten Datenmember nicht verwenden, können Sie die [**MCI- \_ Wiedergabe- \_ Parametern**](mci-play-parms.md) anstelle von **MCI- \_ VD-Play- \_ \_ para** Metern verwenden.</span><span class="sxs-lookup"><span data-stu-id="9a49b-118">You can use the [**MCI\_PLAY\_PARMS**](mci-play-parms.md) structure instead of **MCI\_VD\_PLAY\_PARMS** if you are not using the extended data members.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a49b-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a49b-119">Requirements</span></span>



| <span data-ttu-id="9a49b-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9a49b-120">Requirement</span></span> | <span data-ttu-id="9a49b-121">Wert</span><span class="sxs-lookup"><span data-stu-id="9a49b-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9a49b-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9a49b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9a49b-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9a49b-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9a49b-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9a49b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9a49b-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9a49b-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9a49b-126">Header</span><span class="sxs-lookup"><span data-stu-id="9a49b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a49b-127"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a49b-127"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a49b-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a49b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a49b-129">**MCI**</span><span class="sxs-lookup"><span data-stu-id="9a49b-129">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="9a49b-130">**MCI-Strukturen**</span><span class="sxs-lookup"><span data-stu-id="9a49b-130">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="9a49b-131">**MCI- \_ Play**</span><span class="sxs-lookup"><span data-stu-id="9a49b-131">**MCI\_PLAY**</span></span>](mci-play.md)
</dt> <dt>

[<span data-ttu-id="9a49b-132">**MCI- \_ Wiedergabe- \_ Parser**</span><span class="sxs-lookup"><span data-stu-id="9a49b-132">**MCI\_PLAY\_PARMS**</span></span>](mci-play-parms.md)
</dt> <dt>

<span data-ttu-id="9a49b-133">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9a49b-133">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

