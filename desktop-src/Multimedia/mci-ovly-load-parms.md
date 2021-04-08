---
title: MCI_OVLY_LOAD_PARMS-Struktur (MMSYSTEM. h)
description: Die Struktur für den MCI- \_ OVLY- \_ Ladevorgang \_ enthält Informationen zum MCI \_ -Lade Befehl für Video Überlagerungs Geräte.
ms.assetid: 701c27da-72bf-493d-a679-9e0bd210215d
keywords:
- MCI_OVLY_LOAD_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_OVLY_LOAD_PARMS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2029e92f7991f1ae5d8d0bdbabc76eef456a36ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040078"
---
# <a name="mci_ovly_load_parms-structure"></a><span data-ttu-id="d94d8-104">Struktur von MCI- \_ OVLY- \_ Lade- \_ Parametern</span><span class="sxs-lookup"><span data-stu-id="d94d8-104">MCI\_OVLY\_LOAD\_PARMS structure</span></span>

<span data-ttu-id="d94d8-105">Die Struktur für den **MCI- \_ OVLY- \_ Lade \_** Vorgang enthält Informationen zum [**MCI- \_ Lade**](mci-load.md) Befehl für Video Überlagerungs Geräte.</span><span class="sxs-lookup"><span data-stu-id="d94d8-105">The **MCI\_OVLY\_LOAD\_PARMS** structure contains information for the [**MCI\_LOAD**](mci-load.md) command for video-overlay devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="d94d8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d94d8-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpfilename;
  RECT      rc;
} MCI_OVLY_LOAD_PARMS;
```



## <a name="members"></a><span data-ttu-id="d94d8-107">Member</span><span class="sxs-lookup"><span data-stu-id="d94d8-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="d94d8-108">**dwcallback**</span><span class="sxs-lookup"><span data-stu-id="d94d8-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="d94d8-109">Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="d94d8-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="d94d8-110">**lpFileName**</span><span class="sxs-lookup"><span data-stu-id="d94d8-110">**lpfilename**</span></span>
</dt> <dd>

<span data-ttu-id="d94d8-111">Der Name der zu ladenden Datei.</span><span class="sxs-lookup"><span data-stu-id="d94d8-111">Name of file to load.</span></span>

</dd> <dt>

<span data-ttu-id="d94d8-112">**RC**</span><span class="sxs-lookup"><span data-stu-id="d94d8-112">**rc**</span></span>
</dt> <dd>

<span data-ttu-id="d94d8-113">Identifiziert den Bereich des zu aktualisierenden Video Puffers.</span><span class="sxs-lookup"><span data-stu-id="d94d8-113">Identifies the area of the video buffer to update.</span></span> <span data-ttu-id="d94d8-114">[Rect](/previous-versions//ms536136(v=vs.85)) -Strukturen werden in MCI anders behandelt als in anderen Teilen von Windows. in MCI enthält **RC. Right** die Breite des Rechtecks und **RC. Bottom** enthält die Höhe des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="d94d8-114">[RECT](/previous-versions//ms536136(v=vs.85)) structures are handled differently in MCI than in other parts of Windows; in MCI, **rc.right** contains the width of the rectangle and **rc.bottom** contains its height.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d94d8-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d94d8-115">Remarks</span></span>

<span data-ttu-id="d94d8-116">Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="d94d8-116">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="d94d8-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d94d8-117">Requirements</span></span>



| <span data-ttu-id="d94d8-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d94d8-118">Requirement</span></span> | <span data-ttu-id="d94d8-119">Wert</span><span class="sxs-lookup"><span data-stu-id="d94d8-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d94d8-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d94d8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d94d8-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d94d8-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="d94d8-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d94d8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d94d8-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d94d8-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d94d8-124">Header</span><span class="sxs-lookup"><span data-stu-id="d94d8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d94d8-125"><dt>MMSYSTEM. h</dt></span><span class="sxs-lookup"><span data-stu-id="d94d8-125"><dt>Mmsystem.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d94d8-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d94d8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d94d8-127">**MCI**</span><span class="sxs-lookup"><span data-stu-id="d94d8-127">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d94d8-128">**MCI-Strukturen**</span><span class="sxs-lookup"><span data-stu-id="d94d8-128">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="d94d8-129">**MCI- \_ Auslastung**</span><span class="sxs-lookup"><span data-stu-id="d94d8-129">**MCI\_LOAD**</span></span>](mci-load.md)
</dt> <dt>

<span data-ttu-id="d94d8-130">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d94d8-130">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="d94d8-131">[Rect](/previous-versions//ms536136(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d94d8-131">[RECT](/previous-versions//ms536136(v=vs.85))</span></span>
</dt> </dl>

 

