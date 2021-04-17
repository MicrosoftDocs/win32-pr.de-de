---
title: MCI_VCR_SEEK_PARMS Struktur (VCR. h)
description: Die Struktur der MCI- \_ VCR- \_ Such \_ Parameter enthält Parameter für den MCI- \_ Suchbefehl für Video-Kassetten-Recorder.
ms.assetid: 40a9cef0-abdb-4698-b11e-5c3f67ea846b
keywords:
- MCI_VCR_SEEK_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_SEEK_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 302011a3e4bf10eb3a81db4a163f94f4322dea98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476005"
---
# <a name="mci_vcr_seek_parms-structure"></a><span data-ttu-id="2b3d5-104">Struktur der MCI- \_ VCR- \_ Such \_ Teilwerte</span><span class="sxs-lookup"><span data-stu-id="2b3d5-104">MCI\_VCR\_SEEK\_PARMS structure</span></span>

<span data-ttu-id="2b3d5-105">Die Struktur der **MCI- \_ VCR- \_ Such \_** Parameter enthält Parameter für den [**MCI- \_ Such**](mci-seek.md) Befehl für Video-Kassetten-Recorder.</span><span class="sxs-lookup"><span data-stu-id="2b3d5-105">The **MCI\_VCR\_SEEK\_PARMS** structure contains parameters for the [**MCI\_SEEK**](mci-seek.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b3d5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b3d5-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_SEEK_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTo;
  DWORD     dwMark;
  DWORD     dwAt;
} MCI_VCR_SEEK_PARMS;
```



## <a name="members"></a><span data-ttu-id="2b3d5-107">Member</span><span class="sxs-lookup"><span data-stu-id="2b3d5-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="2b3d5-108">**dwcallback**</span><span class="sxs-lookup"><span data-stu-id="2b3d5-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="2b3d5-109">Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="2b3d5-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="2b3d5-110">**dwto**</span><span class="sxs-lookup"><span data-stu-id="2b3d5-110">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="2b3d5-111">Position, an der gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="2b3d5-111">Position to seek to.</span></span>

</dd> <dt>

<span data-ttu-id="2b3d5-112">**dwmark**</span><span class="sxs-lookup"><span data-stu-id="2b3d5-112">**dwMark**</span></span>
</dt> <dd>

<span data-ttu-id="2b3d5-113">Nummerierte Markierung, nach der gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="2b3d5-113">Numbered mark to seek for.</span></span>

</dd> <dt>

<span data-ttu-id="2b3d5-114">**dwat**</span><span class="sxs-lookup"><span data-stu-id="2b3d5-114">**dwAt**</span></span>
</dt> <dd>

<span data-ttu-id="2b3d5-115">Zeitpunkt, zu dem die Suche beginnt.</span><span class="sxs-lookup"><span data-stu-id="2b3d5-115">Time when seek begins.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2b3d5-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2b3d5-116">Remarks</span></span>

<span data-ttu-id="2b3d5-117">Positionen werden im aktuellen Zeitformat angegeben.</span><span class="sxs-lookup"><span data-stu-id="2b3d5-117">Positions are specified in the current time format.</span></span>

<span data-ttu-id="2b3d5-118">Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="2b3d5-118">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b3d5-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b3d5-119">Requirements</span></span>



| <span data-ttu-id="2b3d5-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2b3d5-120">Requirement</span></span> | <span data-ttu-id="2b3d5-121">Wert</span><span class="sxs-lookup"><span data-stu-id="2b3d5-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2b3d5-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2b3d5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2b3d5-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2b3d5-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2b3d5-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2b3d5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2b3d5-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2b3d5-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2b3d5-126">Header</span><span class="sxs-lookup"><span data-stu-id="2b3d5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b3d5-127"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b3d5-127"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b3d5-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b3d5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b3d5-129">**MCI**</span><span class="sxs-lookup"><span data-stu-id="2b3d5-129">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="2b3d5-130">**MCI-Strukturen**</span><span class="sxs-lookup"><span data-stu-id="2b3d5-130">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="2b3d5-131">**MCI- \_ Suche**</span><span class="sxs-lookup"><span data-stu-id="2b3d5-131">**MCI\_SEEK**</span></span>](mci-seek.md)
</dt> <dt>

<span data-ttu-id="2b3d5-132">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2b3d5-132">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

