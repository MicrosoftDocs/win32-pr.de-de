---
title: MCI_VD_STEP_PARMS-Struktur (mciapi. h)
description: Die Struktur der MCI- \_ VD- \_ Schritt-Parametern \_ enthält Informationen zum MCI- \_ Schritt Befehl für Videodisk-Geräte.
ms.assetid: 5345468c-b195-485a-8101-4a076410f26a
keywords:
- MCI_VD_STEP_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VD_STEP_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b8b368046375f87a897d002c362624fed3ea105
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517813"
---
# <a name="mci_vd_step_parms-structure"></a><span data-ttu-id="2df1a-104">Struktur von MCI- \_ VD- \_ Schritt- \_ Parametern</span><span class="sxs-lookup"><span data-stu-id="2df1a-104">MCI\_VD\_STEP\_PARMS structure</span></span>

<span data-ttu-id="2df1a-105">Die Struktur der **MCI- \_ VD-Schritt- \_ \_ Parametern** enthält Informationen zum [**MCI- \_ Schritt**](mci-step.md) Befehl für Videodisk-Geräte.</span><span class="sxs-lookup"><span data-stu-id="2df1a-105">The **MCI\_VD\_STEP\_PARMS** structure contains information for the [**MCI\_STEP**](mci-step.md) command for videodisc devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="2df1a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2df1a-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrames;
} MCI_VD_STEP_PARMS;
```



## <a name="members"></a><span data-ttu-id="2df1a-107">Member</span><span class="sxs-lookup"><span data-stu-id="2df1a-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="2df1a-108">**dwcallback**</span><span class="sxs-lookup"><span data-stu-id="2df1a-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="2df1a-109">Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="2df1a-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="2df1a-110">**dwframes**</span><span class="sxs-lookup"><span data-stu-id="2df1a-110">**dwFrames**</span></span>
</dt> <dd>

<span data-ttu-id="2df1a-111">Anzahl der zu schrifenden Frames.</span><span class="sxs-lookup"><span data-stu-id="2df1a-111">Number of frames to step.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2df1a-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2df1a-112">Remarks</span></span>

<span data-ttu-id="2df1a-113">Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="2df1a-113">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="2df1a-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2df1a-114">Requirements</span></span>



| <span data-ttu-id="2df1a-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2df1a-115">Requirement</span></span> | <span data-ttu-id="2df1a-116">Wert</span><span class="sxs-lookup"><span data-stu-id="2df1a-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2df1a-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2df1a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2df1a-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2df1a-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2df1a-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2df1a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2df1a-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2df1a-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2df1a-121">Header</span><span class="sxs-lookup"><span data-stu-id="2df1a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2df1a-122"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2df1a-122"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2df1a-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2df1a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2df1a-124">**MCI**</span><span class="sxs-lookup"><span data-stu-id="2df1a-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="2df1a-125">**MCI-Strukturen**</span><span class="sxs-lookup"><span data-stu-id="2df1a-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="2df1a-126">**MCI- \_ Schritt**</span><span class="sxs-lookup"><span data-stu-id="2df1a-126">**MCI\_STEP**</span></span>](mci-step.md)
</dt> <dt>

<span data-ttu-id="2df1a-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2df1a-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

