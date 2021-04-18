---
description: Die vom WM- \_ Tablet \_ gelöschte Nachricht wird gepostet, wenn ein Tablet-Gerät aus Windows entfernt wird.
ms.assetid: af5be7f0-a213-49a1-800e-c922281522c8
title: WM_TABLET_DELETED Meldung (tpcshrd. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da8ade03d199f8ee7a258b9db2aeea039fd725e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354467"
---
# <a name="wm_tablet_deleted-message"></a><span data-ttu-id="4946e-103">Vom WM- \_ Tablet \_ gelöschte Nachricht</span><span class="sxs-lookup"><span data-stu-id="4946e-103">WM\_TABLET\_DELETED message</span></span>

<span data-ttu-id="4946e-104">Die vom **WM- \_ Tablet \_ Gelöschte** Nachricht wird gepostet, wenn ein Tablet-Gerät aus Windows entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="4946e-104">The **WM\_TABLET\_DELETED** message is posted when a tablet device is removed from Windows.</span></span>


```C++
#define WM_TABLET_DEFBASE   0x02C0
#define WM_TABLET_DELETED   (WM_TABLET_DEFBASE + 9)     
```



## <a name="parameters"></a><span data-ttu-id="4946e-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="4946e-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4946e-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4946e-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4946e-107">Der Index des zu entfernenden Tablet-Geräts.</span><span class="sxs-lookup"><span data-stu-id="4946e-107">Index of tablet device being removed.</span></span>

</dd> <dt>

<span data-ttu-id="4946e-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4946e-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4946e-109">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4946e-109">Unused.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4946e-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4946e-110">Remarks</span></span>

<span data-ttu-id="4946e-111">Diese Nachricht wird an alle Fenster der obersten Ebene im System gesendet, darunter deaktivierte oder nicht sichtbare, nicht im Besitz befindliche Fenster, überlappende Fenster und Popup Fenster. die Meldung wird jedoch nicht an untergeordnete Fenster gesendet.</span><span class="sxs-lookup"><span data-stu-id="4946e-111">This message is sent to all top-level windows in the system, including disabled or invisible unowned windows, overlapped windows, and pop-up windows; but the message is not sent to child windows.</span></span>

<span data-ttu-id="4946e-112">Die Indizes, die in *wParam* übergeben werden, sind mit dem Index verknüpft, der von der [**itabletmanager:: gettablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85)) -Methode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4946e-112">The indexes passed in *wParam* are related to the index used by the [**ITabletManager::GetTablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85)) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4946e-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4946e-113">Requirements</span></span>



| <span data-ttu-id="4946e-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4946e-114">Requirement</span></span> | <span data-ttu-id="4946e-115">Wert</span><span class="sxs-lookup"><span data-stu-id="4946e-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4946e-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4946e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4946e-117">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4946e-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="4946e-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4946e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4946e-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4946e-119">None supported</span></span><br/>                                                            |
| <span data-ttu-id="4946e-120">Header</span><span class="sxs-lookup"><span data-stu-id="4946e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4946e-121"><dt>Tpcshrd. h</dt></span><span class="sxs-lookup"><span data-stu-id="4946e-121"><dt>Tpcshrd.h</dt></span></span> </dl> |



 

 
