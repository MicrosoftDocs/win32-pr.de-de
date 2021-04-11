---
title: HDM_LAYOUT Meldung (kommstrg. h)
description: Ruft Informationen ab, die zum Festlegen der Größe und Position des Header Steuer Elements innerhalb des Ziel Rechtecks des übergeordneten Fensters verwendet werden. Sie können diese Nachricht explizit senden oder das Header \_ Layout-Makro verwenden.
ms.assetid: 0763e483-f01d-4739-8c61-1c52d1aad0b4
keywords:
- Windows-Steuerelemente für HDM_LAYOUT Meldung
topic_type:
- apiref
api_name:
- HDM_LAYOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a70fc46dee52f52862136dbe583db9f6d7a0e13e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040638"
---
# <a name="hdm_layout-message"></a><span data-ttu-id="9de46-105">HDM- \_ layoutmeldung</span><span class="sxs-lookup"><span data-stu-id="9de46-105">HDM\_LAYOUT message</span></span>

<span data-ttu-id="9de46-106">Ruft Informationen ab, die zum Festlegen der Größe und Position des Header Steuer Elements innerhalb des Ziel Rechtecks des übergeordneten Fensters verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9de46-106">Retrieves information used to set the size and position of the header control within the target rectangle of the parent window.</span></span> <span data-ttu-id="9de46-107">Sie können diese Nachricht explizit senden oder das [**Header \_ Layout**](/windows/desktop/api/Commctrl/nf-commctrl-header_layout) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="9de46-107">You can send this message explicitly or use the [**Header\_Layout**](/windows/desktop/api/Commctrl/nf-commctrl-header_layout) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9de46-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9de46-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9de46-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9de46-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9de46-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="9de46-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9de46-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9de46-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9de46-112">Ein Zeiger auf eine [**hdlayout**](/windows/win32/api/commctrl/ns-commctrl-hdlayout) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="9de46-112">A pointer to an [**HDLAYOUT**](/windows/win32/api/commctrl/ns-commctrl-hdlayout) structure.</span></span> <span data-ttu-id="9de46-113">Der **PRC** -Member gibt die Koordinaten eines Rechtecks an, und das **pwpos** -Element empfängt die Größe und Position des Header Steuer Elements innerhalb des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="9de46-113">The **prc** member specifies the coordinates of a rectangle, and the **pwpos** member receives the size and position for the header control within the rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9de46-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9de46-114">Return value</span></span>

<span data-ttu-id="9de46-115">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="9de46-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9de46-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9de46-116">Remarks</span></span>

<span data-ttu-id="9de46-117">Der **pwpos** -Member der *LPARAM* -Struktur erhält Größen-und Positionswerte, die für die Positionierung des Steuer Elements am oberen Rand des angegebenen Rechtecks geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="9de46-117">The **pwpos** member of the *lParam* structure receives size and position values appropriate for positioning the control along the top of the specified rectangle.</span></span> <span data-ttu-id="9de46-118">Der Height-Wert ist die Summe der Höhe der horizontalen Rahmen des Steuer Elements und die durchschnittliche Höhe der Zeichen in der Schriftart, die derzeit im Gerätekontext des Steuer Elements ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="9de46-118">The height value is the sum of the heights of the control's horizontal borders and the average height of characters in the font currently selected into the control's device context.</span></span>

<span data-ttu-id="9de46-119">Um das **HDM- \_ Layout** zum Festlegen der Anfangs Größe und Position eines Header Steuer Elements zu verwenden, legen Sie den ursprünglichen Sichtbarkeits Zustand des-Steuer Elements so fest, dass es ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="9de46-119">To use **HDM\_LAYOUT** to set the initial size and position of a header control, set the initial visibility state of the control so that it is hidden.</span></span> <span data-ttu-id="9de46-120">Nach dem Senden des **HDM- \_ Layouts** zum Abrufen der Größen-und Positionswerte verwenden Sie die [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) -Funktion, um die neue Größe, Position und den Sichtbarkeits Zustand festzulegen.</span><span class="sxs-lookup"><span data-stu-id="9de46-120">After sending **HDM\_LAYOUT** to retrieve the size and position values, use the [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) function to set the new size, position, and visibility state.</span></span>

## <a name="requirements"></a><span data-ttu-id="9de46-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9de46-121">Requirements</span></span>



| <span data-ttu-id="9de46-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9de46-122">Requirement</span></span> | <span data-ttu-id="9de46-123">Wert</span><span class="sxs-lookup"><span data-stu-id="9de46-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9de46-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9de46-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9de46-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9de46-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9de46-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9de46-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9de46-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9de46-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9de46-128">Header</span><span class="sxs-lookup"><span data-stu-id="9de46-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="9de46-129"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="9de46-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

