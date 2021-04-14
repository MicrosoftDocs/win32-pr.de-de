---
title: MM_MCISIGNAL Meldung (MMSYSTEM. h)
description: Die mm \_ mcisignal-Nachricht wird an ein Fenster gesendet, um eine Anwendung zu benachrichtigen, dass ein MCI-Gerät eine in einem vorherigen Signal (MCI-Signal)-Befehl definierte Position erreicht hat \_ .
ms.assetid: 12512d23-9a89-4e38-9ec5-88845766f4f6
keywords:
- MM_MCISIGNAL-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_MCISIGNAL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d42d4d39f31b82c7461a5bd8d8561b0da1b6bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392093"
---
# <a name="mm_mcisignal-message"></a><span data-ttu-id="395f1-104">MM- \_ mcisignal-Meldung</span><span class="sxs-lookup"><span data-stu-id="395f1-104">MM\_MCISIGNAL message</span></span>

<span data-ttu-id="395f1-105">Die **mm \_ mcisignal** -Nachricht wird an ein Fenster gesendet, um eine Anwendung zu benachrichtigen, dass ein MCI-Gerät eine in einem vorherigen [**Signal**](signal.md) ( [**MCI- \_ Signal**](mci-signal.md))-Befehl definierte Position erreicht hat.</span><span class="sxs-lookup"><span data-stu-id="395f1-105">The **MM\_MCISIGNAL** message is sent to a window to notify an application that an MCI device has reached a position defined in a previous [**signal**](signal.md) ( [**MCI\_SIGNAL**](mci-signal.md)) command.</span></span>


```C++
MM_MCISIGNAL 
wParam = (WPARAM) wID      
lParam = (LONG) lUserParm  
```



## <a name="parameters"></a><span data-ttu-id="395f1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="395f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="395f1-107"><span id="wID"></span><span id="wid"></span><span id="WID"></span>*wID*</span><span class="sxs-lookup"><span data-stu-id="395f1-107"><span id="wID"></span><span id="wid"></span><span id="WID"></span>*wID*</span></span>
</dt> <dd>

<span data-ttu-id="395f1-108">Der Bezeichner des Geräts, von dem die Signal Meldung initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="395f1-108">Identifier of the device initiating the signal message.</span></span>

</dd> <dt>

<span data-ttu-id="395f1-109"><span id="lUserParm"></span><span id="luserparm"></span><span id="LUSERPARM"></span>*luserparamem*</span><span class="sxs-lookup"><span data-stu-id="395f1-109"><span id="lUserParm"></span><span id="luserparm"></span><span id="LUSERPARM"></span>*lUserParm*</span></span>
</dt> <dd>

<span data-ttu-id="395f1-110">Der Wert, der im **dwuserparamem** -Member der **MCI \_ DGV-Signal \_ parametriams \_** -Struktur übermittelt wird, wenn der **Signal** -Befehl diese Rückruffunktion definiert hat.</span><span class="sxs-lookup"><span data-stu-id="395f1-110">Value passed in the **dwUserParm** member of the **MCI\_DGV\_SIGNAL\_PARAMS** structure when the **signal** command has defined this callback function.</span></span> <span data-ttu-id="395f1-111">Alternativ kann Sie auch den Positionswert enthalten.</span><span class="sxs-lookup"><span data-stu-id="395f1-111">Alternatively, it might contain the position value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="395f1-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="395f1-112">Requirements</span></span>



| <span data-ttu-id="395f1-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="395f1-113">Requirement</span></span> | <span data-ttu-id="395f1-114">Wert</span><span class="sxs-lookup"><span data-stu-id="395f1-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="395f1-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="395f1-115">Minimum supported client</span></span><br/> | <span data-ttu-id="395f1-116">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="395f1-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="395f1-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="395f1-117">Minimum supported server</span></span><br/> | <span data-ttu-id="395f1-118">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="395f1-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="395f1-119">Header</span><span class="sxs-lookup"><span data-stu-id="395f1-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="395f1-120"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="395f1-120"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="395f1-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="395f1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="395f1-122">MCI</span><span class="sxs-lookup"><span data-stu-id="395f1-122">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="395f1-123">MCI-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="395f1-123">MCI Messages</span></span>](mci-messages.md)
</dt> <dt>

[<span data-ttu-id="395f1-124">**aussendet**</span><span class="sxs-lookup"><span data-stu-id="395f1-124">**signal**</span></span>](signal.md)
</dt> </dl>

 

 





