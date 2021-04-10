---
title: PGN_HOTITEMCHANGE Meldung (kommstrg. h)
description: Benachrichtigt das übergeordnete Fenster eines Pager-Steuer Elements, dass sich das heiße (hervorgehobene) Element geändert hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 0f59677c-0251-49f4-b909-6fac6d93f354
keywords:
- Windows-Steuerelemente für PGN_HOTITEMCHANGE Meldung
topic_type:
- apiref
api_name:
- PGN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 573f3dd93a6e4b0b3db6682d36804416d6f6f1e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040501"
---
# <a name="pgn_hotitemchange-message"></a><span data-ttu-id="be1f9-105">PGN- \_ Nachricht zum Ändern der Nachricht</span><span class="sxs-lookup"><span data-stu-id="be1f9-105">PGN\_HOTITEMCHANGE message</span></span>

<span data-ttu-id="be1f9-106">Benachrichtigt das übergeordnete Fenster eines Pager-Steuer Elements, dass sich das heiße (hervorgehobene) Element geändert hat.</span><span class="sxs-lookup"><span data-stu-id="be1f9-106">Notifies a pager control's parent window that the hot (highlighted) item has change.</span></span> <span data-ttu-id="be1f9-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="be1f9-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PGN_HOTITEMCHANGE

    pnmPGHotItem = (LPNMPGHOTITEM) lParam;
```



## <a name="parameters"></a><span data-ttu-id="be1f9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="be1f9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be1f9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="be1f9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="be1f9-110">Zeiger auf eine [**nmpghotitem**](/windows/win32/api/commctrl/ns-commctrl-nmpghotitem) -Struktur, die Informationen zu diesem Benachrichtigungs Code enthält.</span><span class="sxs-lookup"><span data-stu-id="be1f9-110">Pointer to a [**NMPGHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmpghotitem) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be1f9-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="be1f9-111">Return value</span></span>

<span data-ttu-id="be1f9-112">Gibt 0 (null) zurück, um das Element hervorzuheben, bzw</span><span class="sxs-lookup"><span data-stu-id="be1f9-112">Return zero to highlight the item or nonzero to prevent highlighting.</span></span>

## <a name="remarks"></a><span data-ttu-id="be1f9-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="be1f9-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="be1f9-114">Zur Verwendung dieses Benachrichtigungs Codes müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="be1f9-114">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="be1f9-115">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="be1f9-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="be1f9-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be1f9-116">Requirements</span></span>



| <span data-ttu-id="be1f9-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be1f9-117">Requirement</span></span> | <span data-ttu-id="be1f9-118">Wert</span><span class="sxs-lookup"><span data-stu-id="be1f9-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="be1f9-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="be1f9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="be1f9-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="be1f9-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="be1f9-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="be1f9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="be1f9-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="be1f9-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="be1f9-123">Header</span><span class="sxs-lookup"><span data-stu-id="be1f9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="be1f9-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="be1f9-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





