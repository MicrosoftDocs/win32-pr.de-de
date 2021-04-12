---
title: MCI_OVLY_RECT_PARMS-Struktur (mciapi. h)
description: Die MCI \_ \_ -Struktur für den OVLY Rect \_ -Inhalt enthält Positionsinformationen für die MCI \_ Put-und MCI \_ -Befehle für Video Überlagerungs Geräte.
ms.assetid: 1cfd8e51-c76f-4a1c-905c-efacbd8146f4
keywords:
- MCI_OVLY_RECT_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_OVLY_RECT_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68a6b51d980b6ca0a3c223f414571a42b2e3ae3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475093"
---
# <a name="mci_ovly_rect_parms-structure"></a><span data-ttu-id="73815-104">MCI \_ OVLY \_ Rect- \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="73815-104">MCI\_OVLY\_RECT\_PARMS structure</span></span>

<span data-ttu-id="73815-105">Die MCI-Struktur für den **\_ OVLY \_ \_ Rect** -Inhalt enthält Positionsinformationen für die [**MCI \_ Put**](mci-put.md) -und [**MCI \_**](mci-where.md) -Befehle für Video Überlagerungs Geräte.</span><span class="sxs-lookup"><span data-stu-id="73815-105">The **MCI\_OVLY\_RECT\_PARMS** structure contains positioning information for the [**MCI\_PUT**](mci-put.md) and [**MCI\_WHERE**](mci-where.md) commands for video-overlay devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="73815-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="73815-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  RECT      rc;
} MCI_OVLY_RECT_PARMS;
```



## <a name="members"></a><span data-ttu-id="73815-107">Member</span><span class="sxs-lookup"><span data-stu-id="73815-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="73815-108">**dwcallback**</span><span class="sxs-lookup"><span data-stu-id="73815-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="73815-109">Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="73815-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="73815-110">**RC**</span><span class="sxs-lookup"><span data-stu-id="73815-110">**rc**</span></span>
</dt> <dd>

<span data-ttu-id="73815-111">Rechteck, das Positionsinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="73815-111">Rectangle containing positioning information.</span></span> <span data-ttu-id="73815-112">[Rect](/previous-versions//ms536136(v=vs.85)) -Strukturen werden in MCI anders behandelt als in anderen Teilen von Windows. in MCI enthält **RC. Right** die Breite des Rechtecks und **RC. Bottom** enthält die Höhe des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="73815-112">[RECT](/previous-versions//ms536136(v=vs.85)) structures are handled differently in MCI than in other parts of Windows; in MCI, **rc.right** contains the width of the rectangle and **rc.bottom** contains its height.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="73815-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73815-113">Remarks</span></span>

<span data-ttu-id="73815-114">Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="73815-114">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="73815-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="73815-115">Requirements</span></span>



| <span data-ttu-id="73815-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="73815-116">Requirement</span></span> | <span data-ttu-id="73815-117">Wert</span><span class="sxs-lookup"><span data-stu-id="73815-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="73815-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="73815-118">Minimum supported client</span></span><br/> | <span data-ttu-id="73815-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73815-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="73815-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="73815-120">Minimum supported server</span></span><br/> | <span data-ttu-id="73815-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73815-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="73815-122">Header</span><span class="sxs-lookup"><span data-stu-id="73815-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="73815-123"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="73815-123"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73815-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73815-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73815-125">**MCI**</span><span class="sxs-lookup"><span data-stu-id="73815-125">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="73815-126">**MCI-Strukturen**</span><span class="sxs-lookup"><span data-stu-id="73815-126">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="73815-127">**MCI- \_ Put**</span><span class="sxs-lookup"><span data-stu-id="73815-127">**MCI\_PUT**</span></span>](mci-put.md)
</dt> <dt>

[<span data-ttu-id="73815-128">**MCI, \_ wobei**</span><span class="sxs-lookup"><span data-stu-id="73815-128">**MCI\_WHERE**</span></span>](mci-where.md)
</dt> <dt>

<span data-ttu-id="73815-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="73815-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="73815-130">[Rect](/previous-versions//ms536136(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="73815-130">[RECT](/previous-versions//ms536136(v=vs.85))</span></span>
</dt> </dl>

 

