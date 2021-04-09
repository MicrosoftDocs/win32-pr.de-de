---
title: LVN_ENDSCROLL Meldung (kommstrg. h)
description: Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, wenn ein scrollvorgang beendet wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 2838dcd0-ac0f-48c7-94ba-dc36febedb94
keywords:
- Windows-Steuerelemente für LVN_ENDSCROLL Meldung
topic_type:
- apiref
api_name:
- LVN_ENDSCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b9dcdcff2d0bcfc28e1818d5add6d37838e5f9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859347"
---
# <a name="lvn_endscroll-message"></a><span data-ttu-id="44f8b-105">LVN- \_ endscrollnachricht</span><span class="sxs-lookup"><span data-stu-id="44f8b-105">LVN\_ENDSCROLL message</span></span>

<span data-ttu-id="44f8b-106">Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, wenn ein scrollvorgang beendet wird.</span><span class="sxs-lookup"><span data-stu-id="44f8b-106">Notifies a list-view control's parent window when a scrolling operation ends.</span></span> <span data-ttu-id="44f8b-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="44f8b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ENDSCROLL

    pnmLVScroll = (LPNMLVSCROLL) lParam;
```



## <a name="parameters"></a><span data-ttu-id="44f8b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="44f8b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44f8b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="44f8b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="44f8b-110">Ein Zeiger auf eine [**nmlvscroll**](/windows/win32/api/commctrl/ns-commctrl-nmlvscroll) -Struktur, die die horizontale oder vertikale Position von enthält, an der der scrollvorgang endet.</span><span class="sxs-lookup"><span data-stu-id="44f8b-110">Pointer to a [**NMLVSCROLL**](/windows/win32/api/commctrl/ns-commctrl-nmlvscroll) structure that contains the horizontal or vertical position of where the scroll operation ends.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44f8b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="44f8b-111">Return value</span></span>

<span data-ttu-id="44f8b-112">Der Rückgabewert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="44f8b-112">Return value not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="44f8b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="44f8b-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="44f8b-114">Zur Verwendung dieses Benachrichtigungs Codes müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="44f8b-114">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="44f8b-115">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="44f8b-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="44f8b-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44f8b-116">Requirements</span></span>



| <span data-ttu-id="44f8b-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="44f8b-117">Requirement</span></span> | <span data-ttu-id="44f8b-118">Wert</span><span class="sxs-lookup"><span data-stu-id="44f8b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="44f8b-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="44f8b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="44f8b-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="44f8b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="44f8b-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="44f8b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="44f8b-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="44f8b-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="44f8b-123">Header</span><span class="sxs-lookup"><span data-stu-id="44f8b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="44f8b-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="44f8b-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





