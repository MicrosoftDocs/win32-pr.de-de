---
title: LVN_BEGINSCROLL Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, wenn ein scrollvorgang gestartet wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 67123db1-118c-43d7-8511-12a3c4413958
keywords:
- Windows-Steuerelemente für LVN_BEGINSCROLL Benachrichtigungs
topic_type:
- apiref
api_name:
- LVN_BEGINSCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae09a05525ac6e9f08d8cc7a0b7de6ef51329baa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475363"
---
# <a name="lvn_beginscroll-notification-code"></a><span data-ttu-id="6d2bd-105">LVN \_ beginscroll-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="6d2bd-105">LVN\_BEGINSCROLL notification code</span></span>

<span data-ttu-id="6d2bd-106">Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, wenn ein scrollvorgang gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="6d2bd-106">Notifies a list-view control's parent window when a scrolling operation starts.</span></span> <span data-ttu-id="6d2bd-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="6d2bd-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_BEGINSCROLL

    pnmLVScroll = (LPNMLVSCROLL) lParam;
```



## <a name="parameters"></a><span data-ttu-id="6d2bd-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d2bd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d2bd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6d2bd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6d2bd-110">Ein Zeiger auf eine [**nmlvscroll**](/windows/win32/api/commctrl/ns-commctrl-nmlvscroll) -Struktur, die die horizontale oder vertikale Position von enthält, an der der scrollvorgang beginnt.</span><span class="sxs-lookup"><span data-stu-id="6d2bd-110">Pointer to a [**NMLVSCROLL**](/windows/win32/api/commctrl/ns-commctrl-nmlvscroll) structure that contains the horizontal or vertical position of where the scroll operation starts.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d2bd-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6d2bd-111">Return value</span></span>

<span data-ttu-id="6d2bd-112">Der Rückgabewert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6d2bd-112">Return value not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d2bd-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d2bd-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6d2bd-114">Zur Verwendung dieses Benachrichtigungs Codes müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="6d2bd-114">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="6d2bd-115">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6d2bd-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6d2bd-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d2bd-116">Requirements</span></span>



| <span data-ttu-id="6d2bd-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6d2bd-117">Requirement</span></span> | <span data-ttu-id="6d2bd-118">Wert</span><span class="sxs-lookup"><span data-stu-id="6d2bd-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6d2bd-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6d2bd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6d2bd-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6d2bd-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6d2bd-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6d2bd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6d2bd-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6d2bd-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6d2bd-123">Header</span><span class="sxs-lookup"><span data-stu-id="6d2bd-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d2bd-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d2bd-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





