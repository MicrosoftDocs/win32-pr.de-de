---
title: TB_SETMAXTEXTROWS Meldung (kommstrg. h)
description: Legt die maximale Anzahl der auf einer Symbolleisten Schaltfläche angezeigten Textzeilen fest.
ms.assetid: a14d74e8-cc21-482d-9bca-38dc7c0528ec
keywords:
- Windows-Steuerelemente für TB_SETMAXTEXTROWS Meldung
topic_type:
- apiref
api_name:
- TB_SETMAXTEXTROWS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0984c0b73280ec90c4e659d3bb3b4cc89cdcf4c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949596"
---
# <a name="tb_setmaxtextrows-message"></a><span data-ttu-id="d9da8-104">TB \_ setmaxtextrows-Nachricht</span><span class="sxs-lookup"><span data-stu-id="d9da8-104">TB\_SETMAXTEXTROWS message</span></span>

<span data-ttu-id="d9da8-105">Legt die maximale Anzahl der auf einer Symbolleisten Schaltfläche angezeigten Textzeilen fest.</span><span class="sxs-lookup"><span data-stu-id="d9da8-105">Sets the maximum number of text rows displayed on a toolbar button.</span></span>

## <a name="parameters"></a><span data-ttu-id="d9da8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9da8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9da8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d9da8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d9da8-108">Maximale Anzahl von Textzeilen, die angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="d9da8-108">Maximum number of rows of text that can be displayed.</span></span>

</dd> <dt>

<span data-ttu-id="d9da8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d9da8-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d9da8-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="d9da8-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9da8-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d9da8-111">Return value</span></span>

<span data-ttu-id="d9da8-112">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="d9da8-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9da8-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d9da8-113">Remarks</span></span>

<span data-ttu-id="d9da8-114">Um das Umbruch von Text zu bewirken, müssen Sie die maximale Schaltflächen breite festlegen, indem Sie eine [**TB- \_ setbuttonwidth**](tb-setbuttonwidth.md) -Nachricht senden.</span><span class="sxs-lookup"><span data-stu-id="d9da8-114">To cause text to wrap, you must set the maximum button width by sending a [**TB\_SETBUTTONWIDTH**](tb-setbuttonwidth.md) message.</span></span> <span data-ttu-id="d9da8-115">Der Text wird bei einem Wort Umbruch umschlossen. Zeilenumbrüche (" \\ n") im Text werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d9da8-115">The text wraps at a word break; line breaks ("\\n") in the text are ignored.</span></span> <span data-ttu-id="d9da8-116">Der Text in den tbstyle- \_ Listen Symbolleisten wird immer in einer einzelnen Zeile angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d9da8-116">Text in TBSTYLE\_LIST toolbars is always shown on a single line.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9da8-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9da8-117">Requirements</span></span>



| <span data-ttu-id="d9da8-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d9da8-118">Requirement</span></span> | <span data-ttu-id="d9da8-119">Wert</span><span class="sxs-lookup"><span data-stu-id="d9da8-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d9da8-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d9da8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d9da8-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9da8-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d9da8-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d9da8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d9da8-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9da8-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d9da8-124">Header</span><span class="sxs-lookup"><span data-stu-id="d9da8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9da8-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9da8-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





