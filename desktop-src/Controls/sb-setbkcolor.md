---
title: SB_SETBKCOLOR Meldung (kommstrg. h)
description: Legt die Hintergrundfarbe in einer Statusleiste fest.
ms.assetid: 49bcd816-e3e2-45f4-8845-ef67789b8a01
keywords:
- Windows-Steuerelemente für SB_SETBKCOLOR Meldung
topic_type:
- apiref
api_name:
- SB_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc08687c6d228074bc3e4dd7c8442a1c1e35a835
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392115"
---
# <a name="sb_setbkcolor-message"></a><span data-ttu-id="2a302-104">SB- \_ SetBkColor-Nachricht</span><span class="sxs-lookup"><span data-stu-id="2a302-104">SB\_SETBKCOLOR message</span></span>

<span data-ttu-id="2a302-105">Legt die Hintergrundfarbe in einer Statusleiste fest.</span><span class="sxs-lookup"><span data-stu-id="2a302-105">Sets the background color in a status bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="2a302-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2a302-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a302-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2a302-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2a302-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="2a302-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2a302-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2a302-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a302-110">[**COLORREF**](/windows/desktop/gdi/colorref) -Wert, der die neue Hintergrundfarbe angibt.</span><span class="sxs-lookup"><span data-stu-id="2a302-110">[**COLORREF**](/windows/desktop/gdi/colorref) value that specifies the new background color.</span></span> <span data-ttu-id="2a302-111">Geben Sie den CLR- \_ Standardwert an, damit die Statusleiste die Standard Hintergrundfarbe verwendet.</span><span class="sxs-lookup"><span data-stu-id="2a302-111">Specify the CLR\_DEFAULT value to cause the status bar to use its default background color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a302-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2a302-112">Return value</span></span>

<span data-ttu-id="2a302-113">Gibt die vorherige Hintergrundfarbe bzw. CLR-Standardwert zurück, \_ Wenn die Hintergrundfarbe die Standardfarbe ist.</span><span class="sxs-lookup"><span data-stu-id="2a302-113">Returns the previous background color, or CLR\_DEFAULT if the background color is the default color.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a302-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a302-114">Requirements</span></span>



| <span data-ttu-id="2a302-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2a302-115">Requirement</span></span> | <span data-ttu-id="2a302-116">Wert</span><span class="sxs-lookup"><span data-stu-id="2a302-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2a302-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2a302-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2a302-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2a302-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2a302-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2a302-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2a302-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2a302-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2a302-121">Header</span><span class="sxs-lookup"><span data-stu-id="2a302-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a302-122"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a302-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

