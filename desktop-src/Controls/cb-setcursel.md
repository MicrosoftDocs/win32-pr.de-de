---
title: CB_SETCURSEL Meldung (Winuser. h)
description: Eine Anwendung sendet eine CB \_ setcurrsel-Nachricht, um eine Zeichenfolge in der Liste eines Kombinations Felds auszuwählen.
ms.assetid: d4ce3811-6e0a-4952-97cf-ba6efde0de0d
keywords:
- Windows-Steuerelemente für CB_SETCURSEL Meldung
topic_type:
- apiref
api_name:
- CB_SETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bd130204e6dc8bb4166c21bc9c4d52950182c5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040591"
---
# <a name="cb_setcursel-message"></a><span data-ttu-id="49be9-104">CB- \_ setcurrsel-Meldung</span><span class="sxs-lookup"><span data-stu-id="49be9-104">CB\_SETCURSEL message</span></span>

<span data-ttu-id="49be9-105">Eine Anwendung sendet eine **CB \_ setcurrsel** -Nachricht, um eine Zeichenfolge in der Liste eines Kombinations Felds auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="49be9-105">An application sends a **CB\_SETCURSEL** message to select a string in the list of a combo box.</span></span> <span data-ttu-id="49be9-106">Bei Bedarf führt die Liste einen Bildlauf in der Zeichenfolge durch.</span><span class="sxs-lookup"><span data-stu-id="49be9-106">If necessary, the list scrolls the string into view.</span></span> <span data-ttu-id="49be9-107">Der Text im Bearbeitungs Steuerelement des Kombinations Felds ändert sich, um die neue Auswahl widerzuspiegeln, und jede vorherige Auswahl in der Liste wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="49be9-107">The text in the edit control of the combo box changes to reflect the new selection, and any previous selection in the list is removed.</span></span>

## <a name="parameters"></a><span data-ttu-id="49be9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="49be9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49be9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="49be9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49be9-110">Gibt den NULL basierten Index der auszuwählen Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="49be9-110">Specifies the zero-based index of the string to select.</span></span> <span data-ttu-id="49be9-111">Wenn dieser Parameter-1 ist, wird jede aktuelle Auswahl in der Liste entfernt, und das Bearbeitungs Steuerelement wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="49be9-111">If this parameter is -1, any current selection in the list is removed and the edit control is cleared.</span></span>

</dd> <dt>

<span data-ttu-id="49be9-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="49be9-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49be9-113">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="49be9-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49be9-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="49be9-114">Return value</span></span>

<span data-ttu-id="49be9-115">Wenn die Nachricht erfolgreich ist, ist der Rückgabewert der Index des ausgewählten Elements.</span><span class="sxs-lookup"><span data-stu-id="49be9-115">If the message is successful, the return value is the index of the item selected.</span></span> <span data-ttu-id="49be9-116">Wenn *wParam* größer als die Anzahl der Elemente in der Liste ist oder wenn *wParam* den Wert-1 aufweist, ist der Rückgabewert CB \_ Err, und die Auswahl wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="49be9-116">If *wParam* is greater than the number of items in the list or if *wParam* is -1, the return value is CB\_ERR and the selection is cleared.</span></span>

## <a name="requirements"></a><span data-ttu-id="49be9-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49be9-117">Requirements</span></span>



| <span data-ttu-id="49be9-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="49be9-118">Requirement</span></span> | <span data-ttu-id="49be9-119">Wert</span><span class="sxs-lookup"><span data-stu-id="49be9-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49be9-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="49be9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="49be9-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="49be9-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="49be9-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="49be9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="49be9-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="49be9-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="49be9-124">Header</span><span class="sxs-lookup"><span data-stu-id="49be9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="49be9-125"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="49be9-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49be9-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49be9-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="49be9-127">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="49be9-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="49be9-128">**CB- \_ FindString**</span><span class="sxs-lookup"><span data-stu-id="49be9-128">**CB\_FINDSTRING**</span></span>](cb-findstring.md)
</dt> <dt>

[<span data-ttu-id="49be9-129">**CB \_ getcurrsel**</span><span class="sxs-lookup"><span data-stu-id="49be9-129">**CB\_GETCURSEL**</span></span>](cb-getcursel.md)
</dt> <dt>

[<span data-ttu-id="49be9-130">**CB- \_ SelectString**</span><span class="sxs-lookup"><span data-stu-id="49be9-130">**CB\_SELECTSTRING**</span></span>](cb-selectstring.md)
</dt> </dl>

 

 





