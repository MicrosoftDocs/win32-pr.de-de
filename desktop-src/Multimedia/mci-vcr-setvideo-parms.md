---
title: MCI_VCR_SETVIDEO_PARMS Struktur (VCR. h)
description: Die Struktur der MCI \_ VCR- \_ setvideo \_ -Parameter enthält Parameter für den MCI \_ setvideo-Befehl für Video-Kassetten-Recorder.
ms.assetid: d14b2c9f-6068-4902-8db6-fc081bcd01c0
keywords:
- MCI_VCR_SETVIDEO_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_SETVIDEO_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050e6452b3952a9d15515de01c2ca94a87af2f29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859188"
---
# <a name="mci_vcr_setvideo_parms-structure"></a><span data-ttu-id="6b50a-104">Struktur von MCI \_ VCR- \_ setvideo- \_ Parametern</span><span class="sxs-lookup"><span data-stu-id="6b50a-104">MCI\_VCR\_SETVIDEO\_PARMS structure</span></span>

<span data-ttu-id="6b50a-105">Die Struktur der **MCI \_ VCR- \_ setvideo \_** -Parameter enthält Parameter für den [**MCI \_ setvideo**](mci-setvideo.md) -Befehl für Video-Kassetten-Recorder.</span><span class="sxs-lookup"><span data-stu-id="6b50a-105">The **MCI\_VCR\_SETVIDEO\_PARMS** structure contains parameters for the [**MCI\_SETVIDEO**](mci-setvideo.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b50a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b50a-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_SETVIDEO_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTrack;
  DWORD     dwTo;
  DWORD     dwNumber;
} MCI_VCR_SETVIDEO_PARMS;
```



## <a name="members"></a><span data-ttu-id="6b50a-107">Member</span><span class="sxs-lookup"><span data-stu-id="6b50a-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="6b50a-108">**dwcallback**</span><span class="sxs-lookup"><span data-stu-id="6b50a-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="6b50a-109">Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="6b50a-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="6b50a-110">**dwtrack**</span><span class="sxs-lookup"><span data-stu-id="6b50a-110">**dwTrack**</span></span>
</dt> <dd>

<span data-ttu-id="6b50a-111">Betroffener Titel.</span><span class="sxs-lookup"><span data-stu-id="6b50a-111">Affected track.</span></span>

</dd> <dt>

<span data-ttu-id="6b50a-112">**dwto**</span><span class="sxs-lookup"><span data-stu-id="6b50a-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="6b50a-113">Typ der Eingabe-oder überwachten Eingabe.</span><span class="sxs-lookup"><span data-stu-id="6b50a-113">Type of input or monitored input.</span></span>

</dd> <dt>

<span data-ttu-id="6b50a-114">**dwnumber**</span><span class="sxs-lookup"><span data-stu-id="6b50a-114">**dwNumber**</span></span>
</dt> <dd>

<span data-ttu-id="6b50a-115">Die für zu verwendende Video Eingabe (des Typs, der im **dwto** -Member angegeben ist).</span><span class="sxs-lookup"><span data-stu-id="6b50a-115">Video input (of the type specified in the **dwTo** member) to use.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6b50a-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b50a-116">Remarks</span></span>

<span data-ttu-id="6b50a-117">Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="6b50a-117">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b50a-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b50a-118">Requirements</span></span>



| <span data-ttu-id="6b50a-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b50a-119">Requirement</span></span> | <span data-ttu-id="6b50a-120">Wert</span><span class="sxs-lookup"><span data-stu-id="6b50a-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6b50a-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6b50a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6b50a-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b50a-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6b50a-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6b50a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6b50a-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b50a-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6b50a-125">Header</span><span class="sxs-lookup"><span data-stu-id="6b50a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b50a-126"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b50a-126"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b50a-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b50a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b50a-128">**MCI**</span><span class="sxs-lookup"><span data-stu-id="6b50a-128">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="6b50a-129">**MCI-Strukturen**</span><span class="sxs-lookup"><span data-stu-id="6b50a-129">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="6b50a-130">**MCI- \_ setvideo**</span><span class="sxs-lookup"><span data-stu-id="6b50a-130">**MCI\_SETVIDEO**</span></span>](mci-setvideo.md)
</dt> <dt>

<span data-ttu-id="6b50a-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6b50a-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

