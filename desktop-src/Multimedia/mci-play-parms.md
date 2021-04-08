---
title: MCI_PLAY_PARMS-Struktur (mciapi. h)
description: Die MCI-Wiedergabe-Parametern- \_ \_ Struktur enthält Positionsinformationen für den MCI \_ Play-Befehl.
ms.assetid: f1bacf61-ec14-4391-b227-20b35c0bbbc3
keywords:
- MCI_PLAY_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_PLAY_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f207737d4eb93e280355d0e5041b6e7bfc1b3048
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949399"
---
# <a name="mci_play_parms-structure"></a><span data-ttu-id="99203-104">MCI-Wiedergabe-Parametern- \_ \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="99203-104">MCI\_PLAY\_PARMS structure</span></span>

<span data-ttu-id="99203-105">Die **MCI- \_ Wiedergabe- \_ Parametern** -Struktur enthält Positionsinformationen für den [**MCI \_ Play**](mci-play.md) -Befehl.</span><span class="sxs-lookup"><span data-stu-id="99203-105">The **MCI\_PLAY\_PARMS** structure contains positioning information for the [**MCI\_PLAY**](mci-play.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="99203-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="99203-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
} MCI_PLAY_PARMS;
```



## <a name="members"></a><span data-ttu-id="99203-107">Member</span><span class="sxs-lookup"><span data-stu-id="99203-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="99203-108">**dwcallback**</span><span class="sxs-lookup"><span data-stu-id="99203-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="99203-109">Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="99203-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="99203-110">**dwfrom**</span><span class="sxs-lookup"><span data-stu-id="99203-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="99203-111">Wiedergabe Position</span><span class="sxs-lookup"><span data-stu-id="99203-111">Position to play from.</span></span>

</dd> <dt>

<span data-ttu-id="99203-112">**dwto**</span><span class="sxs-lookup"><span data-stu-id="99203-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="99203-113">Position der Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="99203-113">Position to play to.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="99203-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="99203-114">Remarks</span></span>

<span data-ttu-id="99203-115">Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="99203-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="99203-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="99203-116">Requirements</span></span>



| <span data-ttu-id="99203-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="99203-117">Requirement</span></span> | <span data-ttu-id="99203-118">Wert</span><span class="sxs-lookup"><span data-stu-id="99203-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="99203-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="99203-119">Minimum supported client</span></span><br/> | <span data-ttu-id="99203-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="99203-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="99203-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="99203-121">Minimum supported server</span></span><br/> | <span data-ttu-id="99203-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="99203-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="99203-123">Header</span><span class="sxs-lookup"><span data-stu-id="99203-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="99203-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="99203-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99203-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99203-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99203-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="99203-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="99203-127">**MCI-Strukturen**</span><span class="sxs-lookup"><span data-stu-id="99203-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="99203-128">**MCI- \_ Play**</span><span class="sxs-lookup"><span data-stu-id="99203-128">**MCI\_PLAY**</span></span>](mci-play.md)
</dt> <dt>

<span data-ttu-id="99203-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="99203-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

