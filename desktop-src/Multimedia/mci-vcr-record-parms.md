---
title: MCI_VCR_RECORD_PARMS Struktur (VCR. h)
description: Die Struktur der MCI- \_ VCR- \_ Daten Satz \_ Parameter enthält Parameter für den MCI- \_ Datensatz-Befehl für Video-Kassetten-Recorder.
ms.assetid: a95a6dab-9854-4c44-989a-032dff680106
keywords:
- MCI_VCR_RECORD_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_RECORD_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4089b6b7977959b5eb0d0ac60dd4e612b17b823d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339142"
---
# <a name="mci_vcr_record_parms-structure"></a><span data-ttu-id="68668-104">Struktur von MCI \_ VCR- \_ Daten Satz- \_ Parametern</span><span class="sxs-lookup"><span data-stu-id="68668-104">MCI\_VCR\_RECORD\_PARMS structure</span></span>

<span data-ttu-id="68668-105">Die Struktur der **MCI- \_ VCR- \_ Daten Satz \_** Parameter enthält Parameter für den [**MCI- \_ Datensatz**](mci-record.md) -Befehl für Video-Kassetten-Recorder.</span><span class="sxs-lookup"><span data-stu-id="68668-105">The **MCI\_VCR\_RECORD\_PARMS** structure contains parameters for the [**MCI\_RECORD**](mci-record.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="68668-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="68668-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_RECORD_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwAt;
} MCI_VCR_RECORD_PARMS;
```



## <a name="members"></a><span data-ttu-id="68668-107">Member</span><span class="sxs-lookup"><span data-stu-id="68668-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="68668-108">**dwcallback**</span><span class="sxs-lookup"><span data-stu-id="68668-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="68668-109">Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="68668-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="68668-110">**dwfrom**</span><span class="sxs-lookup"><span data-stu-id="68668-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="68668-111">Wiedergabe Position</span><span class="sxs-lookup"><span data-stu-id="68668-111">Position to play from.</span></span>

</dd> <dt>

<span data-ttu-id="68668-112">**dwto**</span><span class="sxs-lookup"><span data-stu-id="68668-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="68668-113">Position der Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="68668-113">Position to play to.</span></span>

</dd> <dt>

<span data-ttu-id="68668-114">**dwat**</span><span class="sxs-lookup"><span data-stu-id="68668-114">**dwAt**</span></span>
</dt> <dd>

<span data-ttu-id="68668-115">Zeitwert, der sich auf den [**MCI- \_ Datensatz**](mci-record.md) oder den [**MCI \_**](mci-cue.md) -Hinweis Befehl auswirkt.</span><span class="sxs-lookup"><span data-stu-id="68668-115">Time value that affects the [**MCI\_RECORD**](mci-record.md) or [**MCI\_CUE**](mci-cue.md) command.</span></span> <span data-ttu-id="68668-116">Bei einem **MCI- \_ Datensatz** ist dies der Zeitpunkt, zu dem die Aufzeichnung beginnt.</span><span class="sxs-lookup"><span data-stu-id="68668-116">For **MCI\_RECORD**, this is the time when recording begins.</span></span> <span data-ttu-id="68668-117">Bei **MCI \_**-Hinweis ist dies die Zeit, zu der das cubegerät die in **dwfrom** angegebene Position erreicht.</span><span class="sxs-lookup"><span data-stu-id="68668-117">For **MCI\_CUE**, this is the time when the cued device reaches the position given in **dwFrom**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="68668-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="68668-118">Remarks</span></span>

<span data-ttu-id="68668-119">Positionen werden im aktuellen Zeitformat angegeben.</span><span class="sxs-lookup"><span data-stu-id="68668-119">Positions are specified in the current time format.</span></span>

<span data-ttu-id="68668-120">Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="68668-120">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="68668-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68668-121">Requirements</span></span>



| <span data-ttu-id="68668-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="68668-122">Requirement</span></span> | <span data-ttu-id="68668-123">Wert</span><span class="sxs-lookup"><span data-stu-id="68668-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="68668-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="68668-124">Minimum supported client</span></span><br/> | <span data-ttu-id="68668-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="68668-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="68668-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="68668-126">Minimum supported server</span></span><br/> | <span data-ttu-id="68668-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="68668-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="68668-128">Header</span><span class="sxs-lookup"><span data-stu-id="68668-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="68668-129"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="68668-129"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68668-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68668-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68668-131">**MCI**</span><span class="sxs-lookup"><span data-stu-id="68668-131">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="68668-132">**MCI-Strukturen**</span><span class="sxs-lookup"><span data-stu-id="68668-132">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="68668-133">**MCI \_ -Hinweis**</span><span class="sxs-lookup"><span data-stu-id="68668-133">**MCI\_CUE**</span></span>](mci-cue.md)
</dt> <dt>

[<span data-ttu-id="68668-134">**MCI- \_ Datensatz**</span><span class="sxs-lookup"><span data-stu-id="68668-134">**MCI\_RECORD**</span></span>](mci-record.md)
</dt> <dt>

<span data-ttu-id="68668-135">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="68668-135">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

