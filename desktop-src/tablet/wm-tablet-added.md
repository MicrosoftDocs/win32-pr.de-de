---
description: Die \_ hinzugefügte WM-Tablet- \_ Nachricht wird gesendet, wenn Windows ein Tablet-Gerät hinzugefügt wird.
ms.assetid: 74323b34-2364-47eb-b8ac-b97546e43b32
title: WM_TABLET_ADDED Meldung (tpcshrd. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a721f83cbab3c520a5502fa2f1262de9a26b25a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346931"
---
# <a name="wm_tablet_added-message"></a><span data-ttu-id="37074-103">\_Hinzugefügte WM-Tablette \_</span><span class="sxs-lookup"><span data-stu-id="37074-103">WM\_TABLET\_ADDED message</span></span>

<span data-ttu-id="37074-104">Die **\_ \_ hinzugefügte WM-Tablet** -Nachricht wird gesendet, wenn Windows ein Tablet-Gerät hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="37074-104">The **WM\_TABLET\_ADDED** message is posted when a tablet device is added to Windows.</span></span>


```C++
#define WM_TABLET_DEFBASE  0x02C0
#define WM_TABLET_ADDED    (WM_TABLET_DEFBASE + 8)      
```



## <a name="parameters"></a><span data-ttu-id="37074-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="37074-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37074-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="37074-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="37074-107">Der Index des hinzugefügten Tablettgeräts.</span><span class="sxs-lookup"><span data-stu-id="37074-107">Index of tablet device being added</span></span>

</dd> <dt>

<span data-ttu-id="37074-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="37074-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="37074-109">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="37074-109">Unused.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="37074-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37074-110">Remarks</span></span>

<span data-ttu-id="37074-111">Diese Nachricht wird an alle Fenster der obersten Ebene im System gesendet, darunter deaktivierte oder nicht sichtbare, nicht im Besitz befindliche Fenster, überlappende Fenster und Popup Fenster. die Meldung wird jedoch nicht an untergeordnete Fenster gesendet.</span><span class="sxs-lookup"><span data-stu-id="37074-111">This message is sent to all top-level windows in the system, including disabled or invisible unowned windows, overlapped windows, and pop-up windows; but the message is not sent to child windows.</span></span>

<span data-ttu-id="37074-112">Die Indizes, die in *wParam* übergeben werden, sind mit dem Index verknüpft, der von der [**itabletmanager:: gettablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85)) -Methode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="37074-112">The indexes passed in *wParam* are related to the index used by the [**ITabletManager::GetTablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85)) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="37074-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="37074-113">Requirements</span></span>



| <span data-ttu-id="37074-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="37074-114">Requirement</span></span> | <span data-ttu-id="37074-115">Wert</span><span class="sxs-lookup"><span data-stu-id="37074-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="37074-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="37074-116">Minimum supported client</span></span><br/> | <span data-ttu-id="37074-117">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37074-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="37074-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="37074-118">Minimum supported server</span></span><br/> | <span data-ttu-id="37074-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="37074-119">None supported</span></span><br/>                                                            |
| <span data-ttu-id="37074-120">Header</span><span class="sxs-lookup"><span data-stu-id="37074-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="37074-121"><dt>Tpcshrd. h</dt></span><span class="sxs-lookup"><span data-stu-id="37074-121"><dt>Tpcshrd.h</dt></span></span> </dl> |



 

 
