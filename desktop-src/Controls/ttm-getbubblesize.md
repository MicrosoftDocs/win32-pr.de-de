---
title: TTM_GETBUBBLESIZE Meldung (kommstrg. h)
description: Gibt die Breite und Höhe eines QuickInfo-Steuer Elements zurück.
ms.assetid: 6afb971e-f05d-4b7a-b63d-3672bfcc32dc
keywords:
- Windows-Steuerelemente für TTM_GETBUBBLESIZE Meldung
topic_type:
- apiref
api_name:
- TTM_GETBUBBLESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48b48bda0f795473cb48303e88bbf3c1c35df7cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103749"
---
# <a name="ttm_getbubblesize-message"></a><span data-ttu-id="fee83-104">TTM \_ getbubblesize-Meldung</span><span class="sxs-lookup"><span data-stu-id="fee83-104">TTM\_GETBUBBLESIZE message</span></span>

<span data-ttu-id="fee83-105">Gibt die Breite und Höhe eines QuickInfo-Steuer Elements zurück.</span><span class="sxs-lookup"><span data-stu-id="fee83-105">Returns the width and height of a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="fee83-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fee83-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fee83-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fee83-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="fee83-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="fee83-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="fee83-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fee83-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fee83-110">Zeiger auf die [**QuickInfo-toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="fee83-110">Pointer to the tooltip [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fee83-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fee83-111">Return value</span></span>

<span data-ttu-id="fee83-112">Gibt die Breite der QuickInfo im unteren Wort und die Höhe im großen Wort zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="fee83-112">Returns the width of the tooltip in the low word and the height in the high word if successful.</span></span> <span data-ttu-id="fee83-113">Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fee83-113">Otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fee83-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fee83-114">Remarks</span></span>

<span data-ttu-id="fee83-115">Wenn die "ttf \_ Track"-und "ttf absolute"- \_ Flags im **uFlags** -Member der [**QuickInfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur festgelegt sind, kann diese Meldung verwendet werden, um die QuickInfo korrekt zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="fee83-115">If the TTF\_TRACK and TTF\_ABSOLUTE flags are set in the **uFlags** member of the tooltip [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure, this message can be used to help position the tooltip accurately.</span></span>

## <a name="requirements"></a><span data-ttu-id="fee83-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fee83-116">Requirements</span></span>



| <span data-ttu-id="fee83-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fee83-117">Requirement</span></span> | <span data-ttu-id="fee83-118">Wert</span><span class="sxs-lookup"><span data-stu-id="fee83-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fee83-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fee83-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fee83-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fee83-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fee83-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fee83-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fee83-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fee83-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fee83-123">Header</span><span class="sxs-lookup"><span data-stu-id="fee83-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fee83-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="fee83-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





