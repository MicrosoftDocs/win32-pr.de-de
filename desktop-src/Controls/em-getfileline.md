---
title: EM_GETFILELINE Meldung (kommstrg. h)
description: Kopiert eine Textzeile aus einem Bearbeitungs Steuerelement, unabhängig davon, wie Linien auf dem Bildschirm angezeigt werden, und platziert Sie in einem angegebenen Puffer.
ms.assetid: ff56d2c6-5013-46c6-90d8-ee2bdc9074b1
keywords:
- Windows-Steuerelemente für EM_GETFILELINE Meldung
topic_type:
- apiref
api_name:
- EM_GETLINE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 6b3be3ea4ae883fc808f7ddc8fb60f0d93bcd6ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477919"
---
# <a name="em_getfileline-message-commctrlh"></a><span data-ttu-id="0d6aa-104">EM_GETFILELINE Meldung (kommstrg. h)</span><span class="sxs-lookup"><span data-stu-id="0d6aa-104">EM_GETFILELINE message (CommCtrl.h)</span></span>

<span data-ttu-id="0d6aa-105">Kopiert eine Textzeile aus einem Bearbeitungs Steuerelement, unabhängig davon, wie Linien auf dem Bildschirm angezeigt werden, und platziert Sie in einem angegebenen Puffer.</span><span class="sxs-lookup"><span data-stu-id="0d6aa-105">Copies a line of text from an edit control, independently of how lines are displayed on the screen, and places it in a specified buffer.</span></span>

## <a name="parameters"></a><span data-ttu-id="0d6aa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d6aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d6aa-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0d6aa-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0d6aa-108">Der null basierte Index der Zeile, die aus einem mehrzeiligen Bearbeitungs Steuerelement abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="0d6aa-108">The zero-based index of the line to retrieve from a multiline edit control.</span></span> <span data-ttu-id="0d6aa-109">Der Wert 0 (null) gibt die oberste Zeile an.</span><span class="sxs-lookup"><span data-stu-id="0d6aa-109">A value of zero specifies the topmost line.</span></span> <span data-ttu-id="0d6aa-110">Dieser Parameter wird von einem einzeiligen Bearbeitungs Steuerelement ignoriert.</span><span class="sxs-lookup"><span data-stu-id="0d6aa-110">This parameter is ignored by a single-line edit control.</span></span>

</dd> <dt>

<span data-ttu-id="0d6aa-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0d6aa-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0d6aa-112">Ein Zeiger auf den Puffer, der eine Kopie der Zeile empfängt.</span><span class="sxs-lookup"><span data-stu-id="0d6aa-112">A pointer to the buffer that receives a copy of the line.</span></span> <span data-ttu-id="0d6aa-113">Legen Sie vor dem Senden der Nachricht das erste Wort dieses Puffers auf die Größe des Puffers in **TCHAR** s fest.</span><span class="sxs-lookup"><span data-stu-id="0d6aa-113">Before sending the message, set the first word of this buffer to the size, in **TCHAR** s, of the buffer.</span></span> <span data-ttu-id="0d6aa-114">Bei ANSI-Text ist dies die Anzahl der Bytes. bei Unicode-Text ist dies die Anzahl der Zeichen.</span><span class="sxs-lookup"><span data-stu-id="0d6aa-114">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="0d6aa-115">Die Größe im ersten Wort wird von der kopierten Zeile überschrieben.</span><span class="sxs-lookup"><span data-stu-id="0d6aa-115">The size in the first word is overwritten by the copied line.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d6aa-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0d6aa-116">Return value</span></span>

<span data-ttu-id="0d6aa-117">Der Rückgabewert ist die Anzahl der kopierten **TCHAR**-s.</span><span class="sxs-lookup"><span data-stu-id="0d6aa-117">The return value is the number of **TCHAR** s copied.</span></span> <span data-ttu-id="0d6aa-118">Der Rückgabewert ist 0 (null), wenn die durch den *wParam* -Parameter angegebene Zeilennummer größer als die Anzahl der Zeilen im Bearbeitungs Steuerelement ist.</span><span class="sxs-lookup"><span data-stu-id="0d6aa-118">The return value is zero if the line number specified by the *wParam* parameter is greater than the number of lines in the edit control.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d6aa-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0d6aa-119">Remarks</span></span>

<span data-ttu-id="0d6aa-120">Die kopierte Zeile enthält kein abschließende Null Zeichen.</span><span class="sxs-lookup"><span data-stu-id="0d6aa-120">The copied line does not contain a terminating null character.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d6aa-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0d6aa-121">Requirements</span></span>



| <span data-ttu-id="0d6aa-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0d6aa-122">Requirement</span></span> | <span data-ttu-id="0d6aa-123">Wert</span><span class="sxs-lookup"><span data-stu-id="0d6aa-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d6aa-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0d6aa-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0d6aa-125">Nur Windows 10, 1809 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0d6aa-125">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0d6aa-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0d6aa-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0d6aa-127">Nur Windows Server 2019 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0d6aa-127">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0d6aa-128">Header</span><span class="sxs-lookup"><span data-stu-id="0d6aa-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d6aa-129"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d6aa-129"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d6aa-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d6aa-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="0d6aa-131">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="0d6aa-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0d6aa-132">**EM \_ filelinelength**</span><span class="sxs-lookup"><span data-stu-id="0d6aa-132">**EM\_FILELINELENGTH**</span></span>](em-filelinelength.md)
</dt> <dt>

[<span data-ttu-id="0d6aa-133">**\_Getfileline bearbeiten**</span><span class="sxs-lookup"><span data-stu-id="0d6aa-133">**Edit\_GetFileLine**</span></span>](/windows/win32/api/commctrl/nf-commctrl-edit_getfileline)
</dt> <dt>

<span data-ttu-id="0d6aa-134">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="0d6aa-134">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="0d6aa-135">**WM \_ gettext**</span><span class="sxs-lookup"><span data-stu-id="0d6aa-135">**WM\_GETTEXT**</span></span>](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

