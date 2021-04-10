---
title: BCN_HOTITEMCHANGE Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt den Besitzer des Button-Steuer Elements, dass die Maus in den Client Bereich des Schaltflächen-Steuer Elements wechselt oder diesen verlässt. Das Schaltflächen-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs \_ Meldung.
ms.assetid: 92882e21-b69d-4326-94e9-ae69a0d00a83
keywords:
- Windows-Steuerelemente für BCN_HOTITEMCHANGE Benachrichtigungs
topic_type:
- apiref
api_name:
- BCN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67ba6a7e64e95b45d0883b5adf34b384bccac8c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040448"
---
# <a name="bcn_hotitemchange-notification-code"></a><span data-ttu-id="677cf-105">BCN-Warnungs \_ Änderungs Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="677cf-105">BCN\_HOTITEMCHANGE notification code</span></span>

<span data-ttu-id="677cf-106">Benachrichtigt den Besitzer des Button-Steuer Elements, dass die Maus in den Client Bereich des Schaltflächen-Steuer Elements wechselt oder diesen verlässt.</span><span class="sxs-lookup"><span data-stu-id="677cf-106">Notifies the button control owner that the mouse is entering or leaving the client area of the button control.</span></span> <span data-ttu-id="677cf-107">Das Schaltflächen-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs Meldung. [**\_**](wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="677cf-107">The button control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
BCN_HOTITEMCHANGE

    pnmbchotitem = (NMBCHOTITEM*) lParam;
```



## <a name="parameters"></a><span data-ttu-id="677cf-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="677cf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="677cf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="677cf-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="677cf-110">Ein Zeiger auf eine [**nmbchotitem**](/windows/win32/api/commctrl/ns-commctrl-nmbchotitem) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="677cf-110">A pointer to a [**NMBCHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmbchotitem) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="677cf-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="677cf-111">Return value</span></span>

<span data-ttu-id="677cf-112">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="677cf-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="677cf-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="677cf-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="677cf-114">Zur Verwendung dieses Benachrichtigungs Codes müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="677cf-114">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="677cf-115">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="677cf-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="677cf-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="677cf-116">Requirements</span></span>



| <span data-ttu-id="677cf-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="677cf-117">Requirement</span></span> | <span data-ttu-id="677cf-118">Wert</span><span class="sxs-lookup"><span data-stu-id="677cf-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="677cf-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="677cf-119">Minimum supported client</span></span><br/> | <span data-ttu-id="677cf-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="677cf-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="677cf-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="677cf-121">Minimum supported server</span></span><br/> | <span data-ttu-id="677cf-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="677cf-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="677cf-123">Header</span><span class="sxs-lookup"><span data-stu-id="677cf-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="677cf-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="677cf-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





