---
title: EM_LINEFROMCHAR Meldung (Winuser. h)
description: Ruft den Index der Zeile ab, die den angegebenen Zeichen Index in einem mehrzeiligen Bearbeitungs Steuerelement enthält.
ms.assetid: e8e9217b-3f0c-478d-b44d-2a51868dbc5a
keywords:
- Windows-Steuerelemente für EM_LINEFROMCHAR Meldung
topic_type:
- apiref
api_name:
- EM_LINEFROMCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0dfe0c6c2ed0f9d77817fddde75fa18b64d485f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103374"
---
# <a name="em_linefromchar-message"></a><span data-ttu-id="95afe-104">EM \_ linefromchar-Nachricht</span><span class="sxs-lookup"><span data-stu-id="95afe-104">EM\_LINEFROMCHAR message</span></span>

<span data-ttu-id="95afe-105">Ruft den Index der Zeile ab, die den angegebenen Zeichen Index in einem mehrzeiligen Bearbeitungs Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="95afe-105">Gets the index of the line that contains the specified character index in a multiline edit control.</span></span> <span data-ttu-id="95afe-106">Ein Zeichen Index ist der null basierte Index des Zeichens vom Anfang des Bearbeitungs Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="95afe-106">A character index is the zero-based index of the character from the beginning of the edit control.</span></span> <span data-ttu-id="95afe-107">Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.</span><span class="sxs-lookup"><span data-stu-id="95afe-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="95afe-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="95afe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95afe-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="95afe-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95afe-110">Der Zeichen Index des Zeichens, das in der Zeile enthalten ist, deren Zahl abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="95afe-110">The character index of the character contained in the line whose number is to be retrieved.</span></span> <span data-ttu-id="95afe-111">Wenn dieser Parameter-1 ist, ruft **EM \_ linefromchar** entweder die Zeilennummer der aktuellen Zeile (die Zeile mit der Einfügemarke) oder, wenn eine Auswahl vorliegt, die Zeilennummer der Zeile ab, die den Anfang der Auswahl enthält.</span><span class="sxs-lookup"><span data-stu-id="95afe-111">If this parameter is -1, **EM\_LINEFROMCHAR** retrieves either the line number of the current line (the line containing the caret) or, if there is a selection, the line number of the line containing the beginning of the selection.</span></span>

</dd> <dt>

<span data-ttu-id="95afe-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="95afe-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95afe-113">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="95afe-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95afe-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="95afe-114">Return value</span></span>

<span data-ttu-id="95afe-115">Der Rückgabewert ist die null basierte Zeilennummer der Zeile, die den von *wParam* angegebenen Zeichen Index enthält.</span><span class="sxs-lookup"><span data-stu-id="95afe-115">The return value is the zero-based line number of the line containing the character index specified by *wParam*.</span></span>

## <a name="remarks"></a><span data-ttu-id="95afe-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95afe-116">Remarks</span></span>

<span data-ttu-id="95afe-117">Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="95afe-117">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="95afe-118">Wenn der Zeichen Index größer als 64.000 ist, verwenden Sie die Nachricht [**EM \_ exlinefromchar**](em-exlinefromchar.md) .</span><span class="sxs-lookup"><span data-stu-id="95afe-118">If the character index is greater than 64,000, use the [**EM\_EXLINEFROMCHAR**](em-exlinefromchar.md) message.</span></span> <span data-ttu-id="95afe-119">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="95afe-119">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="95afe-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95afe-120">Requirements</span></span>



| <span data-ttu-id="95afe-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95afe-121">Requirement</span></span> | <span data-ttu-id="95afe-122">Wert</span><span class="sxs-lookup"><span data-stu-id="95afe-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95afe-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="95afe-123">Minimum supported client</span></span><br/> | <span data-ttu-id="95afe-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95afe-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="95afe-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="95afe-125">Minimum supported server</span></span><br/> | <span data-ttu-id="95afe-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95afe-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="95afe-127">Header</span><span class="sxs-lookup"><span data-stu-id="95afe-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="95afe-128"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="95afe-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95afe-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95afe-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="95afe-130">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="95afe-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="95afe-131">**EM \_ exlinefromchar**</span><span class="sxs-lookup"><span data-stu-id="95afe-131">**EM\_EXLINEFROMCHAR**</span></span>](em-exlinefromchar.md)
</dt> <dt>

[<span data-ttu-id="95afe-132">**EM \_ Linan DEX**</span><span class="sxs-lookup"><span data-stu-id="95afe-132">**EM\_LINEINDEX**</span></span>](em-lineindex.md)
</dt> </dl>

 

 





