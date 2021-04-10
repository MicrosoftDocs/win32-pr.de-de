---
title: MCI_GETDEVCAPS_PARMS-Struktur (mciapi. h)
description: Die Struktur der MCI \_ getdevcaps-Parameter \_ enthält Informationen zur Geräte Funktion für den MCI \_ getdevcaps-Befehl.
ms.assetid: a7b128c5-2121-49cd-b668-3a8466d49a73
keywords:
- MCI_GETDEVCAPS_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_GETDEVCAPS_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a981f6fb9f156cecfa1b4b73046b1b3c654b32e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040301"
---
# <a name="mci_getdevcaps_parms-structure"></a><span data-ttu-id="0153f-104">Struktur von MCI \_ getdevcaps- \_ Parametern</span><span class="sxs-lookup"><span data-stu-id="0153f-104">MCI\_GETDEVCAPS\_PARMS structure</span></span>

<span data-ttu-id="0153f-105">Die Struktur der **MCI \_ getdevcaps \_** -Parameter enthält Informationen zur Geräte Funktion für den [**MCI \_ getdevcaps**](mci-getdevcaps.md) -Befehl.</span><span class="sxs-lookup"><span data-stu-id="0153f-105">The **MCI\_GETDEVCAPS\_PARMS** structure contains device-capability information for the [**MCI\_GETDEVCAPS**](mci-getdevcaps.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="0153f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0153f-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwReturn;
  DWORD     dwItem;
} MCI_GETDEVCAPS_PARMS;
```



## <a name="members"></a><span data-ttu-id="0153f-107">Member</span><span class="sxs-lookup"><span data-stu-id="0153f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="0153f-108">**dwcallback**</span><span class="sxs-lookup"><span data-stu-id="0153f-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="0153f-109">Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="0153f-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="0153f-110">**dwreturn**</span><span class="sxs-lookup"><span data-stu-id="0153f-110">**dwReturn**</span></span>
</dt> <dd>

<span data-ttu-id="0153f-111">Enthält Informationen zum Beenden.</span><span class="sxs-lookup"><span data-stu-id="0153f-111">Contains information on exit.</span></span>

</dd> <dt>

<span data-ttu-id="0153f-112">**dwitem**</span><span class="sxs-lookup"><span data-stu-id="0153f-112">**dwItem**</span></span>
</dt> <dd>

<span data-ttu-id="0153f-113">Die Funktion, die abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="0153f-113">Capability being queried.</span></span> <span data-ttu-id="0153f-114">Dieser Member kann eine der Konstanten sein, die im Referenzmaterial für den [**MCI \_ getdevcaps**](mci-getdevcaps.md) -Befehl aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="0153f-114">This member can be one of the constants listed in the reference material for the [**MCI\_GETDEVCAPS**](mci-getdevcaps.md) command.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0153f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0153f-115">Remarks</span></span>

<span data-ttu-id="0153f-116">Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="0153f-116">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="0153f-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0153f-117">Requirements</span></span>



| <span data-ttu-id="0153f-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0153f-118">Requirement</span></span> | <span data-ttu-id="0153f-119">Wert</span><span class="sxs-lookup"><span data-stu-id="0153f-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0153f-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0153f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0153f-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0153f-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0153f-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0153f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0153f-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0153f-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0153f-124">Header</span><span class="sxs-lookup"><span data-stu-id="0153f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0153f-125"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0153f-125"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0153f-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0153f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0153f-127">**MCI**</span><span class="sxs-lookup"><span data-stu-id="0153f-127">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="0153f-128">**MCI-Strukturen**</span><span class="sxs-lookup"><span data-stu-id="0153f-128">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="0153f-129">**MCI- \_ getdevcaps**</span><span class="sxs-lookup"><span data-stu-id="0153f-129">**MCI\_GETDEVCAPS**</span></span>](mci-getdevcaps.md)
</dt> <dt>

<span data-ttu-id="0153f-130">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0153f-130">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

