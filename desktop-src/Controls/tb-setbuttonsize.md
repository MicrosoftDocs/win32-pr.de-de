---
title: TB_SETBUTTONSIZE Meldung (kommstrg. h)
description: Legt die Größe der Schaltflächen auf einer Symbolleiste fest.
ms.assetid: ef6beed7-a3d6-4379-b9c1-c64a5e33ce78
keywords:
- Windows-Steuerelemente für TB_SETBUTTONSIZE Meldung
topic_type:
- apiref
api_name:
- TB_SETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db17b943c8a7cc8e71735d08718ece02a8c2582
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345295"
---
# <a name="tb_setbuttonsize-message"></a><span data-ttu-id="23577-104">TB \_ setbuttonsize-Meldung</span><span class="sxs-lookup"><span data-stu-id="23577-104">TB\_SETBUTTONSIZE message</span></span>

<span data-ttu-id="23577-105">Legt die Größe der Schaltflächen auf einer Symbolleiste fest.</span><span class="sxs-lookup"><span data-stu-id="23577-105">Sets the size of buttons on a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="23577-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="23577-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23577-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="23577-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="23577-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="23577-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="23577-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="23577-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="23577-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt die Breite der Schaltflächen in Pixel an.</span><span class="sxs-lookup"><span data-stu-id="23577-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the width, in pixels, of the buttons.</span></span> <span data-ttu-id="23577-111">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt die Höhe der Schaltflächen in Pixel an.</span><span class="sxs-lookup"><span data-stu-id="23577-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the height, in pixels, of the buttons.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23577-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="23577-112">Return value</span></span>

<span data-ttu-id="23577-113">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="23577-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="23577-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="23577-114">Remarks</span></span>

<span data-ttu-id="23577-115">**TB \_ Setbuttonsize** sollte in der Regel nach dem Hinzufügen von Schaltflächen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="23577-115">**TB\_SETBUTTONSIZE** should generally be called after adding buttons.</span></span>

<span data-ttu-id="23577-116">Legen Sie mit " [**TB \_ setbuttonwidth**](tb-setbuttonwidth.md) " die maximale und minimale zulässige Breite für Schaltflächen fest, bevor Sie hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="23577-116">Use [**TB\_SETBUTTONWIDTH**](tb-setbuttonwidth.md) to set the maximum and minimum allowed widths for buttons before they are added.</span></span> <span data-ttu-id="23577-117">Legen Sie die tatsächliche Größe von Schaltflächen mit **TB \_ setbuttonsize** fest.</span><span class="sxs-lookup"><span data-stu-id="23577-117">Use **TB\_SETBUTTONSIZE** to set the actual size of buttons.</span></span>

## <a name="examples"></a><span data-ttu-id="23577-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="23577-118">Examples</span></span>

<span data-ttu-id="23577-119">Im folgenden Beispielcode wird die Breite von Schaltflächen auf 80 Pixel und die Höhe auf 30 Pixel festgelegt.</span><span class="sxs-lookup"><span data-stu-id="23577-119">The following example code sets the width of buttons to 80 pixels and the height to 30 pixels.</span></span>


```C++
// hWndToolbar is a handle to the toolbar window.
SendMessage(hWndToolbar, TB_SETBUTTONSIZE, 0, MAKELPARAM(80, 30);
```



## <a name="requirements"></a><span data-ttu-id="23577-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="23577-120">Requirements</span></span>



| <span data-ttu-id="23577-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="23577-121">Requirement</span></span> | <span data-ttu-id="23577-122">Wert</span><span class="sxs-lookup"><span data-stu-id="23577-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="23577-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="23577-123">Minimum supported client</span></span><br/> | <span data-ttu-id="23577-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="23577-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="23577-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="23577-125">Minimum supported server</span></span><br/> | <span data-ttu-id="23577-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="23577-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="23577-127">Header</span><span class="sxs-lookup"><span data-stu-id="23577-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="23577-128"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="23577-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

