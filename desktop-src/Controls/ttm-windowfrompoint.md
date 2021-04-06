---
title: TTM_WINDOWFROMPOINT Meldung (kommstrg. h)
description: Ermöglicht es einer Unterklassen Prozedur, eine QuickInfo für ein anderes Fenster als das unter dem Mauszeiger anzuzeigen.
ms.assetid: f3bf6917-1745-4e4f-a9c1-8fe86b2b3906
keywords:
- Windows-Steuerelemente für TTM_WINDOWFROMPOINT Meldung
topic_type:
- apiref
api_name:
- TTM_WINDOWFROMPOINT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68679f6b6c2477a8279c22f11d0d300e44c8370d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742257"
---
# <a name="ttm_windowfrompoint-message"></a><span data-ttu-id="5c658-104">TTM \_ WindowFromPoint-Meldung</span><span class="sxs-lookup"><span data-stu-id="5c658-104">TTM\_WINDOWFROMPOINT message</span></span>

<span data-ttu-id="5c658-105">Ermöglicht es einer Unterklassen Prozedur, eine QuickInfo für ein anderes Fenster als das unter dem Mauszeiger anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5c658-105">Allows a subclass procedure to cause a tooltip to display text for a window other than the one beneath the mouse cursor.</span></span>

## <a name="parameters"></a><span data-ttu-id="5c658-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c658-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c658-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5c658-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5c658-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="5c658-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5c658-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5c658-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5c658-110">Zeiger auf eine [**Punkt**](/previous-versions//dd162805(v=vs.85)) Struktur, die den zu überprüfenden Punkt definiert.</span><span class="sxs-lookup"><span data-stu-id="5c658-110">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that defines the point to be checked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c658-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5c658-111">Return value</span></span>

<span data-ttu-id="5c658-112">Der Rückgabewert ist das Handle für das Fenster, das den Punkt enthält, oder **null** , wenn am angegebenen Punkt kein Fenster vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5c658-112">The return value is the handle to the window that contains the point, or **NULL** if no window exists at the specified point.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c658-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5c658-113">Remarks</span></span>

<span data-ttu-id="5c658-114">Diese Nachricht soll von einer Anwendung verarbeitet werden, die eine QuickInfo Unterklassen unterteilt.</span><span class="sxs-lookup"><span data-stu-id="5c658-114">This message is intended to be processed by an application that subclasses a tooltip.</span></span> <span data-ttu-id="5c658-115">Sie ist nicht für das Senden durch eine Anwendung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="5c658-115">It is not intended to be sent by an application.</span></span> <span data-ttu-id="5c658-116">Eine QuickInfo sendet diese Nachricht an sich selbst, bevor Sie den Text für ein Fenster anzeigt.</span><span class="sxs-lookup"><span data-stu-id="5c658-116">A tooltip sends this message to itself before displaying the text for a window.</span></span> <span data-ttu-id="5c658-117">Durch Ändern der Koordinaten des durch *LPARAM* angegebenen Punkts kann die Unterklassen Prozedur bewirken, dass die QuickInfo Text für ein anderes Fenster als das unter dem Mauszeiger anzeigt.</span><span class="sxs-lookup"><span data-stu-id="5c658-117">By changing the coordinates of the point specified by *lParam*, the subclass procedure can cause the tooltip to display text for a window other than the one beneath the mouse cursor.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c658-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c658-118">Requirements</span></span>



| <span data-ttu-id="5c658-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5c658-119">Requirement</span></span> | <span data-ttu-id="5c658-120">Wert</span><span class="sxs-lookup"><span data-stu-id="5c658-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5c658-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5c658-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5c658-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5c658-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5c658-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5c658-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5c658-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5c658-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5c658-125">Header</span><span class="sxs-lookup"><span data-stu-id="5c658-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c658-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c658-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

