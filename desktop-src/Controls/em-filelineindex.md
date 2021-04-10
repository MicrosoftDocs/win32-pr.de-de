---
title: EM_FILELINEINDEX Meldung (kommstrg. h)
description: Ruft den Zeichen Index des ersten Zeichens einer angegebenen Zeile in einem mehrzeiligen Bearbeitungs Steuerelement ab, unabhängig davon, wie Linien auf dem Bildschirm angezeigt werden.
ms.assetid: vs|controls|~\controls\editcontrols\editcontrolreference\editcontrolmessages\em_lineindex.htm
keywords:
- Windows-Steuerelemente für EM_FILELINEINDEX Meldung
topic_type:
- apiref
api_name:
- EM_FILELINEINDEX
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4ce5f5ca07fc9fb9869898965422c7c8a6aa3fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104228"
---
# <a name="em_filelineindex-message-commctrlh"></a><span data-ttu-id="48074-104">EM_FILELINEINDEX Meldung (kommstrg. h)</span><span class="sxs-lookup"><span data-stu-id="48074-104">EM_FILELINEINDEX message (CommCtrl.h)</span></span>

<span data-ttu-id="48074-105">Ruft den Zeichen Index des ersten Zeichens einer angegebenen Zeile in einem mehrzeiligen Bearbeitungs Steuerelement ab, unabhängig davon, wie Linien auf dem Bildschirm angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="48074-105">Gets the character index of the first character of a specified line in a multiline edit control, independently of how lines are displayed on the screen..</span></span> <span data-ttu-id="48074-106">Ein Zeichen Index ist der null basierte Index des Zeichens vom Anfang des Bearbeitungs Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="48074-106">A character index is the zero-based index of the character from the beginning of the edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="48074-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="48074-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48074-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="48074-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="48074-109">Die null basierte Zeilennummer.</span><span class="sxs-lookup"><span data-stu-id="48074-109">The zero-based line number.</span></span> <span data-ttu-id="48074-110">Der Wert-1 gibt die aktuelle Zeilennummer an (die Zeile, die die Einfügemarke enthält).</span><span class="sxs-lookup"><span data-stu-id="48074-110">A value of -1 specifies the current line number (the line that contains the caret).</span></span>

</dd> <dt>

<span data-ttu-id="48074-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="48074-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="48074-112">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="48074-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48074-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="48074-113">Return value</span></span>

<span data-ttu-id="48074-114">Der Rückgabewert ist der Zeichen Index der im *wParam* -Parameter angegebenen Zeile, unabhängig davon, wie Linien auf dem Bildschirm angezeigt werden, oder es ist-1, wenn die angegebene Zeilennummer größer als die Anzahl der Zeilen im Bearbeitungs Steuerelement ist.</span><span class="sxs-lookup"><span data-stu-id="48074-114">The return value is the character index of the line specified in the *wParam* parameter, independently of how lines are displayed on the screen, or it is -1 if the specified line number is greater than the number of lines in the edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="48074-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48074-115">Requirements</span></span>



| <span data-ttu-id="48074-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48074-116">Requirement</span></span> | <span data-ttu-id="48074-117">Wert</span><span class="sxs-lookup"><span data-stu-id="48074-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48074-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="48074-118">Minimum supported client</span></span><br/> | <span data-ttu-id="48074-119">Nur Windows 10, 1809 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48074-119">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="48074-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="48074-120">Minimum supported server</span></span><br/> | <span data-ttu-id="48074-121">Nur Windows Server 2019 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48074-121">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="48074-122">Header</span><span class="sxs-lookup"><span data-stu-id="48074-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="48074-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="48074-123"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48074-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48074-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48074-125">**EM \_ filelinefromchar**</span><span class="sxs-lookup"><span data-stu-id="48074-125">**EM\_FILELINEFROMCHAR**</span></span>](em-filelinefromchar.md)
</dt> </dl>

 

 





