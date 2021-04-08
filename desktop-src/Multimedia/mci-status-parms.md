---
title: MCI_STATUS_PARMS-Struktur (mciapi. h)
description: Die Struktur des MCI- \_ Status \_ Parametern enthält Informationen zum MCI- \_ Status Befehl.
ms.assetid: c4897b34-4184-46aa-af17-2127edfbf82d
keywords:
- MCI_STATUS_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_STATUS_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8295f2e747752889c10083c6bb794ba2df7ac273
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949533"
---
# <a name="mci_status_parms-structure"></a><span data-ttu-id="4bd2b-104">Struktur von MCI- \_ Status- \_ Parametern</span><span class="sxs-lookup"><span data-stu-id="4bd2b-104">MCI\_STATUS\_PARMS structure</span></span>

<span data-ttu-id="4bd2b-105">Die Struktur des **MCI- \_ Status \_ Parametern** enthält Informationen zum [**MCI- \_ Status**](mci-status.md) Befehl.</span><span class="sxs-lookup"><span data-stu-id="4bd2b-105">The **MCI\_STATUS\_PARMS** structure contains information for the [**MCI\_STATUS**](mci-status.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bd2b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4bd2b-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD_PTR dwReturn;
  DWORD     dwItem;
  DWORD     dwTrack;
} MCI_STATUS_PARMS;
```



## <a name="members"></a><span data-ttu-id="4bd2b-107">Member</span><span class="sxs-lookup"><span data-stu-id="4bd2b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="4bd2b-108">**dwcallback**</span><span class="sxs-lookup"><span data-stu-id="4bd2b-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="4bd2b-109">Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="4bd2b-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="4bd2b-110">**dwreturn**</span><span class="sxs-lookup"><span data-stu-id="4bd2b-110">**dwReturn**</span></span>
</dt> <dd>

<span data-ttu-id="4bd2b-111">Enthält Informationen zur Rückgabe.</span><span class="sxs-lookup"><span data-stu-id="4bd2b-111">Contains information on return.</span></span>

</dd> <dt>

<span data-ttu-id="4bd2b-112">**dwitem**</span><span class="sxs-lookup"><span data-stu-id="4bd2b-112">**dwItem**</span></span>
</dt> <dd>

<span data-ttu-id="4bd2b-113">Die Funktion, die abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="4bd2b-113">Capability being queried.</span></span>

</dd> <dt>

<span data-ttu-id="4bd2b-114">**dwtrack**</span><span class="sxs-lookup"><span data-stu-id="4bd2b-114">**dwTrack**</span></span>
</dt> <dd>

<span data-ttu-id="4bd2b-115">Länge oder Anzahl der Spuren.</span><span class="sxs-lookup"><span data-stu-id="4bd2b-115">Length or number of tracks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4bd2b-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4bd2b-116">Remarks</span></span>

<span data-ttu-id="4bd2b-117">Das MCI \_ - \_ statuselementflag muss im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion festgelegt werden, um das **dwitem** -Element zu validieren, das eine der Konstanten enthalten muss, die angeben, welche Status Informationen angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="4bd2b-117">The MCI\_STATUS\_ITEM flag must be set in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the **dwItem** member, which should contain one of the constants indicating what status information is being requested.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bd2b-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4bd2b-118">Requirements</span></span>



| <span data-ttu-id="4bd2b-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4bd2b-119">Requirement</span></span> | <span data-ttu-id="4bd2b-120">Wert</span><span class="sxs-lookup"><span data-stu-id="4bd2b-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4bd2b-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4bd2b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4bd2b-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4bd2b-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="4bd2b-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4bd2b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4bd2b-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4bd2b-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4bd2b-125">Header</span><span class="sxs-lookup"><span data-stu-id="4bd2b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4bd2b-126"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bd2b-126"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bd2b-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4bd2b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bd2b-128">**MCI**</span><span class="sxs-lookup"><span data-stu-id="4bd2b-128">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="4bd2b-129">**MCI-Strukturen**</span><span class="sxs-lookup"><span data-stu-id="4bd2b-129">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="4bd2b-130">**MCI- \_ Status**</span><span class="sxs-lookup"><span data-stu-id="4bd2b-130">**MCI\_STATUS**</span></span>](mci-status.md)
</dt> <dt>

<span data-ttu-id="4bd2b-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4bd2b-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

