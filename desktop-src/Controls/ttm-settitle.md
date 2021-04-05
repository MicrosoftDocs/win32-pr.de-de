---
title: TTM_SETTITLE Meldung (kommstrg. h)
description: Fügt einer QuickInfo ein Standard Symbol und eine Titel Zeichenfolge hinzu.
ms.assetid: e745a592-eef7-4e0d-8939-a48b52c4ab9f
keywords:
- Windows-Steuerelemente für TTM_SETTITLE Meldung
topic_type:
- apiref
api_name:
- TTM_SETTITLE
- TTM_SETTITLEA
- TTM_SETTITLEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7972a9d40347995e9d641e7fc8706f9ad4c58bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859237"
---
# <a name="ttm_settitle-message"></a><span data-ttu-id="a1921-104">TTM- \_ SetTitle-Meldung</span><span class="sxs-lookup"><span data-stu-id="a1921-104">TTM\_SETTITLE message</span></span>

<span data-ttu-id="a1921-105">Fügt einer QuickInfo ein Standard Symbol und eine Titel Zeichenfolge hinzu.</span><span class="sxs-lookup"><span data-stu-id="a1921-105">Adds a standard icon and title string to a tooltip.</span></span>

## <a name="parameters"></a><span data-ttu-id="a1921-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1921-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1921-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a1921-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a1921-108">Legen Sie *wParam* auf einen der folgenden Werte fest, um das Symbol anzugeben, das angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a1921-108">Set *wParam* to one of the following values to specify the icon to be displayed.</span></span> <span data-ttu-id="a1921-109">Ab Windows XP SP2 kann dieser Parameter auch einen **HICON** -Wert enthalten.</span><span class="sxs-lookup"><span data-stu-id="a1921-109">As of Windows XP SP2 and later, this parameter can also contain an **HICON** value.</span></span> <span data-ttu-id="a1921-110">Jeder Wert, der größer als der TTI- \_ Fehler ist, wird als **HICON** angenommen.</span><span class="sxs-lookup"><span data-stu-id="a1921-110">Any value greater than TTI\_ERROR is assumed to be an **HICON**.</span></span>



| <span data-ttu-id="a1921-111">Wert</span><span class="sxs-lookup"><span data-stu-id="a1921-111">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="a1921-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a1921-112">Meaning</span></span>                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| <span id="TTI_NONE"></span><span id="tti_none"></span><dl> <span data-ttu-id="a1921-113"><dt>**TTI \_ None**</dt></span><span class="sxs-lookup"><span data-stu-id="a1921-113"><dt>**TTI\_NONE**</dt></span></span> </dl>                             | <span data-ttu-id="a1921-114">Kein Symbol.</span><span class="sxs-lookup"><span data-stu-id="a1921-114">No icon.</span></span><br/>         |
| <span id="TTI_INFO"></span><span id="tti_info"></span><dl> <span data-ttu-id="a1921-115"><dt>**TTI- \_ Informationen**</dt></span><span class="sxs-lookup"><span data-stu-id="a1921-115"><dt>**TTI\_INFO**</dt></span></span> </dl>                             | <span data-ttu-id="a1921-116">Info-Symbol.</span><span class="sxs-lookup"><span data-stu-id="a1921-116">Info icon.</span></span><br/>       |
| <span id="TTI_WARNING"></span><span id="tti_warning"></span><dl> <span data-ttu-id="a1921-117"><dt>**TTI- \_ Warnung**</dt></span><span class="sxs-lookup"><span data-stu-id="a1921-117"><dt>**TTI\_WARNING**</dt></span></span> </dl>                    | <span data-ttu-id="a1921-118">Warnungssymbol</span><span class="sxs-lookup"><span data-stu-id="a1921-118">Warning icon</span></span><br/>     |
| <span id="TTI_ERROR"></span><span id="tti_error"></span><dl> <span data-ttu-id="a1921-119"><dt>**TTI- \_ Fehler**</dt></span><span class="sxs-lookup"><span data-stu-id="a1921-119"><dt>**TTI\_ERROR**</dt></span></span> </dl>                          | <span data-ttu-id="a1921-120">Fehler Symbol</span><span class="sxs-lookup"><span data-stu-id="a1921-120">Error Icon</span></span><br/>       |
| <span id="TTI_INFO_LARGE"></span><span id="tti_info_large"></span><dl> <span data-ttu-id="a1921-121"><dt>**TTI- \_ Informationen \_ groß**</dt></span><span class="sxs-lookup"><span data-stu-id="a1921-121"><dt>**TTI\_INFO\_LARGE**</dt></span></span> </dl>          | <span data-ttu-id="a1921-122">Symbol "großes Fehler"</span><span class="sxs-lookup"><span data-stu-id="a1921-122">Large error Icon</span></span><br/> |
| <span id="TTI_WARNING_LARGE"></span><span id="tti_warning_large"></span><dl> <span data-ttu-id="a1921-123"><dt>**TTI- \_ Warnung \_ groß**</dt></span><span class="sxs-lookup"><span data-stu-id="a1921-123"><dt>**TTI\_WARNING\_LARGE**</dt></span></span> </dl> | <span data-ttu-id="a1921-124">Symbol "großes Fehler"</span><span class="sxs-lookup"><span data-stu-id="a1921-124">Large error Icon</span></span><br/> |
| <span id="TTI_ERROR_LARGE"></span><span id="tti_error_large"></span><dl> <span data-ttu-id="a1921-125"><dt>**TTI- \_ Fehler \_ groß**</dt></span><span class="sxs-lookup"><span data-stu-id="a1921-125"><dt>**TTI\_ERROR\_LARGE**</dt></span></span> </dl>       | <span data-ttu-id="a1921-126">Symbol "großes Fehler"</span><span class="sxs-lookup"><span data-stu-id="a1921-126">Large error Icon</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a1921-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a1921-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a1921-128">Ein Zeiger auf die Titel Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="a1921-128">Pointer to the title string.</span></span> <span data-ttu-id="a1921-129">Sie müssen *LPARAM* einen Wert zuweisen.</span><span class="sxs-lookup"><span data-stu-id="a1921-129">You must assign a value to *lParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1921-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a1921-130">Return value</span></span>

<span data-ttu-id="a1921-131">Gibt bei Erfolg **true** zurück, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="a1921-131">Returns **TRUE** if successful, **FALSE** if not.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1921-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a1921-132">Remarks</span></span>

<span data-ttu-id="a1921-133">Der Titel einer QuickInfo wird über dem Text in einer anderen Schriftart angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a1921-133">The title of a tooltip appears above the text, in a different font.</span></span> <span data-ttu-id="a1921-134">Es reicht nicht aus, einen Titel zu haben. die QuickInfo muss ebenfalls über Text verfügen, oder Sie wird nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a1921-134">It is not sufficient to have a title; the tooltip must have text as well, or it is not displayed.</span></span>

<span data-ttu-id="a1921-135">Wenn *wParam* ein **HICON** enthält, wird eine Kopie des Symbols im QuickInfo-Fenster erstellt.</span><span class="sxs-lookup"><span data-stu-id="a1921-135">When *wParam* contains an **HICON**, a copy of the icon is created by the tooltip window.</span></span>

<span data-ttu-id="a1921-136">Wenn **TTM \_ SetTitle** aufgerufen wird, darf die Zeichenfolge, auf die von *LPARAM* verwiesen wird, nicht länger als 100 **tchars** sein, einschließlich der abschließenden **null**-Werte.</span><span class="sxs-lookup"><span data-stu-id="a1921-136">When calling **TTM\_SETTITLE**, the string pointed to by *lParam* must not exceed 100 **TCHARs** in length, including the terminating **NULL**.</span></span>

## <a name="examples"></a><span data-ttu-id="a1921-137">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a1921-137">Examples</span></span>

<span data-ttu-id="a1921-138">Im folgenden Beispiel wird gezeigt, wie ein Titel und ein System Symbol zu einer QuickInfo hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="a1921-138">The following example shows how to add a title and a system icon to a tooltip.</span></span>


```C++
// hwndTip is the handle of the tooltip window.
HICON hIcon = LoadIcon(NULL, IDI_INFORMATION);
SendMessage(hwndTip, TTM_SETTITLE, (WPARAM)hIcon, L"Title text");
DestroyIcon(hIcon);
```



## <a name="requirements"></a><span data-ttu-id="a1921-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a1921-139">Requirements</span></span>



| <span data-ttu-id="a1921-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a1921-140">Requirement</span></span> | <span data-ttu-id="a1921-141">Wert</span><span class="sxs-lookup"><span data-stu-id="a1921-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a1921-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a1921-142">Minimum supported client</span></span><br/> | <span data-ttu-id="a1921-143">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a1921-143">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a1921-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a1921-144">Minimum supported server</span></span><br/> | <span data-ttu-id="a1921-145">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a1921-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a1921-146">Header</span><span class="sxs-lookup"><span data-stu-id="a1921-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1921-147"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1921-147"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="a1921-148">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="a1921-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a1921-149">**TTM \_ Settitlew** (Unicode) und **TTM \_ settitlea** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a1921-149">**TTM\_SETTITLEW** (Unicode) and **TTM\_SETTITLEA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="a1921-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1921-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1921-151">Info-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="a1921-151">About Tooltip Controls</span></span>](tooltip-controls.md)
</dt> </dl>

 

 





