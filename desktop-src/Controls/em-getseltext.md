---
title: EM_GETSELTEXT Meldung (RichEdit. h)
description: Ruft den aktuell ausgewählten Text in einem Rich-Edit-Steuerelement ab.
ms.assetid: 56af77c3-f2d7-4b5d-895f-a67c141459e3
keywords:
- Windows-Steuerelemente für EM_GETSELTEXT Meldung
topic_type:
- apiref
api_name:
- EM_GETSELTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acde2c0677fa04ff6d7991bca56bad0c08a6f5ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858851"
---
# <a name="em_getseltext-message"></a><span data-ttu-id="6002b-104">EM \_ GetSelText-Nachricht</span><span class="sxs-lookup"><span data-stu-id="6002b-104">EM\_GETSELTEXT message</span></span>

<span data-ttu-id="6002b-105">Ruft den aktuell ausgewählten Text in einem Rich-Edit-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="6002b-105">Retrieves the currently selected text in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="6002b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6002b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6002b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6002b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6002b-108">Dieser Parameter wird nicht verwendet. Er muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="6002b-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6002b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6002b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6002b-110">Zeiger auf einen Puffer, der den ausgewählten Text empfängt.</span><span class="sxs-lookup"><span data-stu-id="6002b-110">Pointer to a buffer that receives the selected text.</span></span> <span data-ttu-id="6002b-111">Die aufrufenden Anwendung muss sicherstellen, dass der Puffer groß genug ist, um den ausgewählten Text zu speichern.</span><span class="sxs-lookup"><span data-stu-id="6002b-111">The calling application must ensure that the buffer is large enough to hold the selected text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6002b-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6002b-112">Return value</span></span>

<span data-ttu-id="6002b-113">Diese Meldung gibt die Anzahl der kopierten Zeichen ohne das abschließende Null Zeichen zurück.</span><span class="sxs-lookup"><span data-stu-id="6002b-113">This message returns the number of characters copied, not including the terminating null character.</span></span>

## <a name="requirements"></a><span data-ttu-id="6002b-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6002b-114">Requirements</span></span>



| <span data-ttu-id="6002b-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6002b-115">Requirement</span></span> | <span data-ttu-id="6002b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="6002b-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6002b-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6002b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6002b-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6002b-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6002b-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6002b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6002b-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6002b-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6002b-121">Header</span><span class="sxs-lookup"><span data-stu-id="6002b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6002b-122"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6002b-122"><dt>Richedit.h</dt></span></span> </dl> |



 

 





