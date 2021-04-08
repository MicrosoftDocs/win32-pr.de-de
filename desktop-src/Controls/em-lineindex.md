---
title: EM_LINEINDEX Meldung (Winuser. h)
description: Ruft den Zeichen Index des ersten Zeichens einer angegebenen Zeile in einem mehrzeiligen Bearbeitungs Steuerelement ab.
ms.assetid: vs|controls|~\controls\editcontrols\editcontrolreference\editcontrolmessages\em_lineindex.htm
keywords:
- Windows-Steuerelemente für EM_LINEINDEX Meldung
topic_type:
- apiref
api_name:
- EM_LINEINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611d4ff892f95287c45166ae55ff2389f454512c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949711"
---
# <a name="em_lineindex-message-winuserh"></a><span data-ttu-id="0bf11-104">EM_LINEINDEX Meldung (Winuser. h)</span><span class="sxs-lookup"><span data-stu-id="0bf11-104">EM_LINEINDEX message (Winuser.h)</span></span>

<span data-ttu-id="0bf11-105">Ruft den Zeichen Index des ersten Zeichens einer angegebenen Zeile in einem mehrzeiligen Bearbeitungs Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="0bf11-105">Gets the character index of the first character of a specified line in a multiline edit control.</span></span> <span data-ttu-id="0bf11-106">Ein Zeichen Index ist der null basierte Index des Zeichens vom Anfang des Bearbeitungs Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="0bf11-106">A character index is the zero-based index of the character from the beginning of the edit control.</span></span> <span data-ttu-id="0bf11-107">Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.</span><span class="sxs-lookup"><span data-stu-id="0bf11-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="0bf11-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0bf11-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bf11-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0bf11-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0bf11-110">Die null basierte Zeilennummer.</span><span class="sxs-lookup"><span data-stu-id="0bf11-110">The zero-based line number.</span></span> <span data-ttu-id="0bf11-111">Der Wert-1 gibt die aktuelle Zeilennummer an (die Zeile, die die Einfügemarke enthält).</span><span class="sxs-lookup"><span data-stu-id="0bf11-111">A value of -1 specifies the current line number (the line that contains the caret).</span></span>

</dd> <dt>

<span data-ttu-id="0bf11-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0bf11-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0bf11-113">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0bf11-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bf11-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0bf11-114">Return value</span></span>

<span data-ttu-id="0bf11-115">Der Rückgabewert ist der Zeichen Index der im *wParam* -Parameter angegebenen Zeile, oder es ist-1, wenn die angegebene Zeilennummer größer als die Anzahl der Zeilen im Bearbeitungs Steuerelement ist.</span><span class="sxs-lookup"><span data-stu-id="0bf11-115">The return value is the character index of the line specified in the *wParam* parameter, or it is -1 if the specified line number is greater than the number of lines in the edit control.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bf11-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0bf11-116">Remarks</span></span>

<span data-ttu-id="0bf11-117">Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0bf11-117">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="0bf11-118">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="0bf11-118">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0bf11-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0bf11-119">Requirements</span></span>



| <span data-ttu-id="0bf11-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0bf11-120">Requirement</span></span> | <span data-ttu-id="0bf11-121">Wert</span><span class="sxs-lookup"><span data-stu-id="0bf11-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bf11-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0bf11-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0bf11-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0bf11-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0bf11-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0bf11-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0bf11-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0bf11-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0bf11-126">Header</span><span class="sxs-lookup"><span data-stu-id="0bf11-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0bf11-127"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="0bf11-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bf11-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0bf11-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bf11-129">**EM \_ linefromchar**</span><span class="sxs-lookup"><span data-stu-id="0bf11-129">**EM\_LINEFROMCHAR**</span></span>](em-linefromchar.md)
</dt> </dl>

 

 





