---
title: EM_LINESCROLL Meldung (Winuser. h)
description: Scrollt den Text in einem mehrzeiligen Bearbeitungs Steuerelement.
ms.assetid: 5398082d-f1ef-4a3a-9e5a-83cf286adbf1
keywords:
- Windows-Steuerelemente für EM_LINESCROLL Meldung
topic_type:
- apiref
api_name:
- EM_LINESCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 646e225ef269ccddca2cdc29caf635d94c1671e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040803"
---
# <a name="em_linescroll-message"></a><span data-ttu-id="2da3b-104">EM \_ linescroll-Nachricht</span><span class="sxs-lookup"><span data-stu-id="2da3b-104">EM\_LINESCROLL message</span></span>

<span data-ttu-id="2da3b-105">Scrollt den Text in einem mehrzeiligen Bearbeitungs Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="2da3b-105">Scrolls the text in a multiline edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="2da3b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2da3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2da3b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2da3b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2da3b-108">Steuer **Elemente bearbeiten:** Die Anzahl der Zeichen, die horizontal durchlaufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2da3b-108">**Edit controls:** The number of characters to scroll horizontally.</span></span>

<span data-ttu-id="2da3b-109">**Rich Edit-Steuerelemente:** Dieser Parameter wird nicht verwendet. Er muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="2da3b-109">**Rich edit controls:** This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2da3b-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2da3b-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2da3b-111">Die Anzahl der Zeilen, für die vertikale Bildläufe durchführen</span><span class="sxs-lookup"><span data-stu-id="2da3b-111">The number of lines to scroll vertically.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2da3b-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2da3b-112">Return value</span></span>

<span data-ttu-id="2da3b-113">Wenn die Nachricht an ein mehrzeilige Bearbeitungs Steuerelement gesendet wird, ist der Rückgabewert " **true**".</span><span class="sxs-lookup"><span data-stu-id="2da3b-113">If the message is sent to a multiline edit control, the return value is **TRUE**.</span></span>

<span data-ttu-id="2da3b-114">Wenn die Nachricht an ein einzeilige Bearbeitungs Steuerelement gesendet wird, ist der Rückgabewert **false**.</span><span class="sxs-lookup"><span data-stu-id="2da3b-114">If the message is sent to a single-line edit control, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2da3b-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2da3b-115">Remarks</span></span>

<span data-ttu-id="2da3b-116">Das-Steuerelement scrollt nicht vertikal nach der letzten Textzeile im Bearbeitungs Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="2da3b-116">The control does not scroll vertically past the last line of text in the edit control.</span></span> <span data-ttu-id="2da3b-117">Wenn die aktuelle Zeile zuzüglich der durch den *LPARAM* -Parameter angegebenen Anzahl von Zeilen die Gesamtzahl der Zeilen im Bearbeitungs Steuerelement überschreitet, wird der Wert so angepasst, dass die letzte Zeile des Bearbeitungs Steuer Elements auf den oberen Rand des Fensters zum Bearbeiten von Steuerelementen gescrollt wird.</span><span class="sxs-lookup"><span data-stu-id="2da3b-117">If the current line plus the number of lines specified by the *lParam* parameter exceeds the total number of lines in the edit control, the value is adjusted so that the last line of the edit control is scrolled to the top of the edit-control window.</span></span>

<span data-ttu-id="2da3b-118">Steuer **Elemente bearbeiten:** Die **\_ gelinescroll** -Nachricht scrollt den Text vertikal oder horizontal in einem mehrzeiligen Bearbeitungs Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="2da3b-118">**Edit controls:** The **EM\_LINESCROLL** message scrolls the text vertically or horizontally in a multiline edit control.</span></span> <span data-ttu-id="2da3b-119">Die **EM \_ linescroll** -Nachricht kann verwendet werden, um einen horizontalen Bildlauf nach dem letzten Zeichen einer beliebigen Zeile durchführen.</span><span class="sxs-lookup"><span data-stu-id="2da3b-119">The **EM\_LINESCROLL** message can be used to scroll horizontally past the last character of any line.</span></span>

<span data-ttu-id="2da3b-120">Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2da3b-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="2da3b-121">Die **\_ gelinescroll** -Nachricht führt einen vertikalen Bildlauf in einem mehrzeiligen Bearbeitungs Steuerelement aus.</span><span class="sxs-lookup"><span data-stu-id="2da3b-121">The **EM\_LINESCROLL** message scrolls the text vertically in a multiline edit control.</span></span> <span data-ttu-id="2da3b-122">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="2da3b-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2da3b-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2da3b-123">Requirements</span></span>



| <span data-ttu-id="2da3b-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2da3b-124">Requirement</span></span> | <span data-ttu-id="2da3b-125">Wert</span><span class="sxs-lookup"><span data-stu-id="2da3b-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2da3b-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2da3b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2da3b-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2da3b-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2da3b-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2da3b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2da3b-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2da3b-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2da3b-130">Header</span><span class="sxs-lookup"><span data-stu-id="2da3b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="2da3b-131"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="2da3b-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





