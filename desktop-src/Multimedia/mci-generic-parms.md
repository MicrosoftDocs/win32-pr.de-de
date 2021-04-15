---
title: MCI_GENERIC_PARMS-Struktur (mciapi. h)
description: Die generische MCI- \_ \_ Struktur enthält das Handle des Fensters, das Benachrichtigungs Meldungen empfängt. Diese Struktur wird für MCI-befehlsnachrichten verwendet, die leere Parameterlisten aufweisen.
ms.assetid: 706e406c-d263-4347-932c-e5f125acfe0f
keywords:
- MCI_GENERIC_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_GENERIC_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1f96482ed5ec7e27253f234031cd099600bf1b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476230"
---
# <a name="mci_generic_parms-structure"></a><span data-ttu-id="4bd3d-105">Generische MCI- \_ \_ paramemstruktur</span><span class="sxs-lookup"><span data-stu-id="4bd3d-105">MCI\_GENERIC\_PARMS structure</span></span>

<span data-ttu-id="4bd3d-106">Die **\_ generische \_ MCI** -Struktur enthält das Handle des Fensters, das Benachrichtigungs Meldungen empfängt.</span><span class="sxs-lookup"><span data-stu-id="4bd3d-106">The **MCI\_GENERIC\_PARMS** structure contains the handle of the window that receives notification messages.</span></span> <span data-ttu-id="4bd3d-107">Diese Struktur wird für MCI-befehlsnachrichten verwendet, die leere Parameterlisten aufweisen.</span><span class="sxs-lookup"><span data-stu-id="4bd3d-107">This structure is used for MCI command messages that have empty parameter lists.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bd3d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4bd3d-108">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
} MCI_GENERIC_PARMS;
```



## <a name="members"></a><span data-ttu-id="4bd3d-109">Member</span><span class="sxs-lookup"><span data-stu-id="4bd3d-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="4bd3d-110">**dwcallback**</span><span class="sxs-lookup"><span data-stu-id="4bd3d-110">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="4bd3d-111">Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="4bd3d-111">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4bd3d-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4bd3d-112">Remarks</span></span>

<span data-ttu-id="4bd3d-113">Die **MCI \_ \_** --, Close-und **MCI- \_ Merkmals \_** Struktur-Strukturen sind identisch mit der **generischen MCI-Struktur von \_ \_ para** Metern.</span><span class="sxs-lookup"><span data-stu-id="4bd3d-113">The **MCI\_CLOSE\_PARMS** and **MCI\_REALIZE\_PARMS** structures are identical to the **MCI\_GENERIC\_PARMS** structure.</span></span>

<span data-ttu-id="4bd3d-114">Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="4bd3d-114">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bd3d-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4bd3d-115">Requirements</span></span>



| <span data-ttu-id="4bd3d-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4bd3d-116">Requirement</span></span> | <span data-ttu-id="4bd3d-117">Wert</span><span class="sxs-lookup"><span data-stu-id="4bd3d-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4bd3d-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4bd3d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4bd3d-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4bd3d-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="4bd3d-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4bd3d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4bd3d-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4bd3d-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4bd3d-122">Header</span><span class="sxs-lookup"><span data-stu-id="4bd3d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4bd3d-123"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bd3d-123"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bd3d-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4bd3d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bd3d-125">**MCI**</span><span class="sxs-lookup"><span data-stu-id="4bd3d-125">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="4bd3d-126">**MCI-Strukturen**</span><span class="sxs-lookup"><span data-stu-id="4bd3d-126">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

<span data-ttu-id="4bd3d-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4bd3d-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

