---
title: EM_FILELINEFROMCHAR Meldung (kommstrg. h)
description: Ruft den Index der Zeile ab, die den angegebenen Zeichen Index in einem mehrzeiligen Bearbeitungs Steuerelement enthält, unabhängig davon, wie Linien auf dem Bildschirm angezeigt werden.
ms.assetid: e8e9217b-3f0c-478d-b44d-2a51868dbc5a
keywords:
- Windows-Steuerelemente für EM_FILELINEFROMCHAR Meldung
topic_type:
- apiref
api_name:
- EM_FILELINEFROMCHAR
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a083d7e12822eacfb1e29a7d4bfd2ea705f2d32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477331"
---
# <a name="em_filelinefromchar-message"></a><span data-ttu-id="cd311-104">EM \_ filelinefromchar-Meldung</span><span class="sxs-lookup"><span data-stu-id="cd311-104">EM\_FILELINEFROMCHAR message</span></span>

<span data-ttu-id="cd311-105">Ruft den Index der Zeile ab, die den angegebenen Zeichen Index in einem mehrzeiligen Bearbeitungs Steuerelement enthält, unabhängig davon, wie Linien auf dem Bildschirm angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="cd311-105">Gets the index of the line that contains the specified character index in a multiline edit control, independently of how lines are displayed on the screen.</span></span> <span data-ttu-id="cd311-106">Ein Zeichen Index ist der null basierte Index des Zeichens vom Anfang des Bearbeitungs Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="cd311-106">A character index is the zero-based index of the character from the beginning of the edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="cd311-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd311-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd311-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cd311-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd311-109">Der Zeichen Index des Zeichens, das in der Zeile enthalten ist, deren Zahl abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="cd311-109">The character index of the character contained in the line whose number is to be retrieved.</span></span> <span data-ttu-id="cd311-110">Wenn dieser Parameter-1 ist, ruft **EM \_ filelinefromchar** entweder die Zeilennummer der aktuellen Zeile (die Zeile mit der Einfügemarke) oder, wenn eine Auswahl vorliegt, die Zeilennummer der Zeile ab, die den Anfang der Auswahl enthält.</span><span class="sxs-lookup"><span data-stu-id="cd311-110">If this parameter is -1, **EM\_FILELINEFROMCHAR** retrieves either the line number of the current line (the line containing the caret) or, if there is a selection, the line number of the line containing the beginning of the selection.</span></span>

</dd> <dt>

<span data-ttu-id="cd311-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cd311-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd311-112">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="cd311-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd311-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cd311-113">Return value</span></span>

<span data-ttu-id="cd311-114">Der Rückgabewert ist die null basierte Zeilennummer der Zeile, die den von *wParam* angegebenen Zeichen Index enthält, unabhängig davon, wie Linien auf dem Bildschirm angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="cd311-114">The return value is the zero-based line number of the line containing the character index specified by *wParam*, independently of how lines are displayed on the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd311-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd311-115">Requirements</span></span>



| <span data-ttu-id="cd311-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cd311-116">Requirement</span></span> | <span data-ttu-id="cd311-117">Wert</span><span class="sxs-lookup"><span data-stu-id="cd311-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd311-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cd311-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cd311-119">Nur Windows 10, 1809 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cd311-119">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cd311-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cd311-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cd311-121">Nur Windows Server 2019 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cd311-121">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cd311-122">Header</span><span class="sxs-lookup"><span data-stu-id="cd311-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd311-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd311-123"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd311-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd311-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="cd311-125">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="cd311-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cd311-126">**EM \_ filelineingedex**</span><span class="sxs-lookup"><span data-stu-id="cd311-126">**EM\_FILELINEINDEX**</span></span>](em-filelineindex.md)
</dt> </dl>

 

 





