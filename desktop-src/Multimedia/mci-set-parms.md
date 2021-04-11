---
title: MCI_SET_PARMS-Struktur (mciapi. h)
description: Die Struktur der MCI- \_ Set- \_ Parametern enthält Informationen für den MCI- \_ Befehl Set.
ms.assetid: 58811a0f-dc89-4303-b2b2-c98933ebab80
keywords:
- MCI_SET_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SET_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 971affd319ecae817b9c1159ab0f307d0c2a5c91
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040296"
---
# <a name="mci_set_parms-structure"></a><span data-ttu-id="079de-104">Struktur von MCI- \_ Set- \_ Parametern</span><span class="sxs-lookup"><span data-stu-id="079de-104">MCI\_SET\_PARMS structure</span></span>

<span data-ttu-id="079de-105">Die Struktur der **MCI- \_ Set- \_ Parametern** enthält Informationen für den [**MCI-Befehl \_ Set**](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="079de-105">The **MCI\_SET\_PARMS** structure contains information for the [**MCI\_SET**](mci-set.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="079de-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="079de-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
} MCI_SET_PARMS;
```



## <a name="members"></a><span data-ttu-id="079de-107">Member</span><span class="sxs-lookup"><span data-stu-id="079de-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="079de-108">**dwcallback**</span><span class="sxs-lookup"><span data-stu-id="079de-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="079de-109">Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="079de-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="079de-110">**dwtimeformat**</span><span class="sxs-lookup"><span data-stu-id="079de-110">**dwTimeFormat**</span></span>
</dt> <dd>

<span data-ttu-id="079de-111">Das Zeitformat für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="079de-111">Time format for device.</span></span>

</dd> <dt>

<span data-ttu-id="079de-112">**dwaudiodatei**</span><span class="sxs-lookup"><span data-stu-id="079de-112">**dwAudio**</span></span>
</dt> <dd>

<span data-ttu-id="079de-113">Audioausgabechannel.</span><span class="sxs-lookup"><span data-stu-id="079de-113">Audio output channel.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="079de-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="079de-114">Remarks</span></span>

<span data-ttu-id="079de-115">Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="079de-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="079de-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="079de-116">Requirements</span></span>



| <span data-ttu-id="079de-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="079de-117">Requirement</span></span> | <span data-ttu-id="079de-118">Wert</span><span class="sxs-lookup"><span data-stu-id="079de-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="079de-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="079de-119">Minimum supported client</span></span><br/> | <span data-ttu-id="079de-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="079de-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="079de-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="079de-121">Minimum supported server</span></span><br/> | <span data-ttu-id="079de-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="079de-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="079de-123">Header</span><span class="sxs-lookup"><span data-stu-id="079de-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="079de-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="079de-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="079de-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="079de-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="079de-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="079de-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="079de-127">**MCI-Strukturen**</span><span class="sxs-lookup"><span data-stu-id="079de-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="079de-128">**MCI- \_ Gruppe**</span><span class="sxs-lookup"><span data-stu-id="079de-128">**MCI\_SET**</span></span>](mci-set.md)
</dt> <dt>

<span data-ttu-id="079de-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="079de-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

