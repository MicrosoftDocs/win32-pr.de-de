---
title: EM_FILELINELENGTH Meldung (kommstrg. h)
description: Ruft die Länge einer Zeile in einem Bearbeitungs Steuerelement (in Zeichen) unabhängig von der Anzeige von Linien auf dem Bildschirm ab.
ms.assetid: cfb0632c-9ba9-4864-939a-dbbaed6c177e
keywords:
- Windows-Steuerelemente für EM_FILELINELENGTH Meldung
topic_type:
- apiref
api_name:
- EM_FILELINELENGTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4aa50f4d9b49253a558095be78e0e781d7d4c7f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517984"
---
# <a name="em_filelinelength-message"></a><span data-ttu-id="2c9fc-104">EM \_ filelinelength-Meldung</span><span class="sxs-lookup"><span data-stu-id="2c9fc-104">EM\_FILELINELENGTH message</span></span>

<span data-ttu-id="2c9fc-105">Ruft die Länge einer Zeile in einem Bearbeitungs Steuerelement (in Zeichen) unabhängig von der Anzeige von Linien auf dem Bildschirm ab.</span><span class="sxs-lookup"><span data-stu-id="2c9fc-105">Retrieves the length, in characters, of a line in an edit control, independently of how lines are displayed on the screen.</span></span>

## <a name="parameters"></a><span data-ttu-id="2c9fc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c9fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c9fc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2c9fc-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c9fc-108">Der Zeichen Index eines Zeichens in der Zeile, deren Länge abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="2c9fc-108">The character index of a character in the line whose length is to be retrieved.</span></span> <span data-ttu-id="2c9fc-109">Wenn dieser Parameter größer als die Anzahl der Zeichen im-Steuerelement ist, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="2c9fc-109">If this parameter is greater than the number of characters in the control, the return value is zero.</span></span>

<span data-ttu-id="2c9fc-110">Dieser Parameter kann-1 sein.</span><span class="sxs-lookup"><span data-stu-id="2c9fc-110">This parameter can be -1.</span></span> <span data-ttu-id="2c9fc-111">In diesem Fall gibt die Nachricht die Anzahl der nicht ausgewählten Zeichen in Zeilen zurück, die ausgewählte Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="2c9fc-111">In this case, the message returns the number of unselected characters on lines containing selected characters.</span></span> <span data-ttu-id="2c9fc-112">Wenn die Auswahl z. b. vom vierten Zeichen einer Zeile bis zum achten Zeichen vom Ende der nächsten Zeile aus verlängert wird, wäre der Rückgabewert 10 (drei Zeichen in der ersten Zeile und sieben bei der nächsten Zeile).</span><span class="sxs-lookup"><span data-stu-id="2c9fc-112">For example, if the selection extended from the fourth character of one line through the eighth character from the end of the next line, the return value would be 10 (three characters on the first line and seven on the next).</span></span>

</dd> <dt>

<span data-ttu-id="2c9fc-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2c9fc-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c9fc-114">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="2c9fc-114">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c9fc-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2c9fc-115">Return value</span></span>

<span data-ttu-id="2c9fc-116">Für mehrzeilige Bearbeitungs Steuerelemente ist der Rückgabewert die Länge in **TCHAR** s der durch den *wParam* -Parameter angegebenen Zeile, unabhängig davon, wie Zeilen auf dem Bildschirm angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2c9fc-116">For multiline edit controls, the return value is the length, in **TCHAR** s, of the line specified by the *wParam* parameter, independently of how lines are displayed on the screen.</span></span> <span data-ttu-id="2c9fc-117">Das Wagen Rücklauf Zeichen oder das Zeilenvorschub Zeichen am Ende der Zeile ist nicht enthalten.</span><span class="sxs-lookup"><span data-stu-id="2c9fc-117">It does not include the carriage-return or linefeed character at the end of the line.</span></span>

<span data-ttu-id="2c9fc-118">Für einzeilige Bearbeitungs Steuerelemente ist der Rückgabewert die Länge des Texts im Bearbeitungs Steuerelement in **TCHAR** s.</span><span class="sxs-lookup"><span data-stu-id="2c9fc-118">For single-line edit controls, the return value is the length, in **TCHAR** s, of the text in the edit control.</span></span>

<span data-ttu-id="2c9fc-119">Wenn *wParam* größer als die Anzahl der Zeichen im-Steuerelement ist, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="2c9fc-119">If *wParam* is greater than the number of characters in the control, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c9fc-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2c9fc-120">Remarks</span></span>

<span data-ttu-id="2c9fc-121">Verwenden Sie die [**EM \_ filelineindex**](em-lineindex.md) -Nachricht, um einen Zeichen Index für eine bestimmte Zeilennummer innerhalb eines mehrzeiligen Bearbeitungs Steuer Elements abzurufen, unabhängig davon, wie Linien auf dem Bildschirm angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2c9fc-121">Use the [**EM\_FILELINEINDEX**](em-lineindex.md) message to retrieve a character index for a given line number within a multiline edit control, independently of how lines are displayed on the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c9fc-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c9fc-122">Requirements</span></span>



| <span data-ttu-id="2c9fc-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c9fc-123">Requirement</span></span> | <span data-ttu-id="2c9fc-124">Wert</span><span class="sxs-lookup"><span data-stu-id="2c9fc-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c9fc-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2c9fc-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2c9fc-126">Nur Windows 10, 1809 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c9fc-126">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2c9fc-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2c9fc-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2c9fc-128">Nur Windows Server 2019 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c9fc-128">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2c9fc-129">Header</span><span class="sxs-lookup"><span data-stu-id="2c9fc-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c9fc-130"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c9fc-130"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c9fc-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c9fc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c9fc-132">**EM \_ filelineingedex**</span><span class="sxs-lookup"><span data-stu-id="2c9fc-132">**EM\_FILELINEINDEX**</span></span>](em-filelineindex.md)
</dt> </dl>

 

 





