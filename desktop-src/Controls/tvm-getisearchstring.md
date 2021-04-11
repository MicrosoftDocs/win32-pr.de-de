---
title: TVM_GETISEARCHSTRING Meldung (kommstrg. h)
description: Ruft die inkrementelle Such Zeichenfolge für ein Strukturansicht-Steuerelement ab.
ms.assetid: 71f9a9b6-e124-4655-80fc-dd23f441496d
keywords:
- Windows-Steuerelemente für TVM_GETISEARCHSTRING Meldung
topic_type:
- apiref
api_name:
- TVM_GETISEARCHSTRING
- TVM_GETISEARCHSTRINGA
- TVM_GETISEARCHSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa968d78a1a99dd3b1eb90055cf2c1d2de51db86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105957"
---
# <a name="tvm_getisearchstring-message"></a><span data-ttu-id="eb4f7-104">TVM- \_ getisearchstring-Meldung</span><span class="sxs-lookup"><span data-stu-id="eb4f7-104">TVM\_GETISEARCHSTRING message</span></span>

<span data-ttu-id="eb4f7-105">Ruft die inkrementelle Such Zeichenfolge für ein Strukturansicht-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="eb4f7-105">Retrieves the incremental search string for a tree-view control.</span></span> <span data-ttu-id="eb4f7-106">Das Strukturansicht-Steuerelement verwendet die inkrementelle Such Zeichenfolge, um auf der Grundlage der vom Benutzer eingegebenen Zeichen ein Element auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="eb4f7-106">The tree-view control uses the incremental search string to select an item based on characters typed by the user.</span></span> <span data-ttu-id="eb4f7-107">Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ getisearchstring**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getisearchstring) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="eb4f7-107">You can send this message explicitly or by using the [**TreeView\_GetISearchString**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getisearchstring) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="eb4f7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb4f7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb4f7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eb4f7-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="eb4f7-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="eb4f7-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="eb4f7-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eb4f7-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eb4f7-112">Zeiger auf den Puffer, der die inkrementelle Such Zeichenfolge empfängt</span><span class="sxs-lookup"><span data-stu-id="eb4f7-112">Pointer to the buffer that receives the incremental search string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb4f7-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eb4f7-113">Return value</span></span>

<span data-ttu-id="eb4f7-114">Gibt die Anzahl der Zeichen in der inkrementellen Such Zeichenfolge zurück</span><span class="sxs-lookup"><span data-stu-id="eb4f7-114">Returns the number of characters in the incremental search string.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb4f7-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eb4f7-115">Remarks</span></span>

<span data-ttu-id="eb4f7-116">**Sicherheitswarnung:** Wenn Sie diese Meldung falsch verwenden, kann dies die Sicherheit des Programms beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="eb4f7-116">**Security Warning:** Using this message incorrectly might compromise the security of your program.</span></span> <span data-ttu-id="eb4f7-117">Sie müssen einen ausreichend großen Puffer zuordnen, um die Zeichenfolge zu speichern.</span><span class="sxs-lookup"><span data-stu-id="eb4f7-117">You must allocate a large enough buffer to hold the string.</span></span> <span data-ttu-id="eb4f7-118">Nennen Sie zuerst die Nachricht, die **null** in *LPARAM* übergibt.</span><span class="sxs-lookup"><span data-stu-id="eb4f7-118">First call the message passing **NULL** in *lParam*.</span></span> <span data-ttu-id="eb4f7-119">Dadurch wird die Anzahl von Zeichen zurückgegeben, die erforderlich sind, ausgenommen **null**.</span><span class="sxs-lookup"><span data-stu-id="eb4f7-119">This returns the number of characters, excluding **NULL**, that are required.</span></span> <span data-ttu-id="eb4f7-120">Rufen Sie dann die Nachricht ein zweites Mal auf, um die Zeichenfolge abzurufen.</span><span class="sxs-lookup"><span data-stu-id="eb4f7-120">Then call the message a second time to retrieve the string.</span></span> <span data-ttu-id="eb4f7-121">Überprüfen Sie die [Sicherheitsaspekte: Microsoft Windows](sec-comctls.md) -Steuerelemente, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="eb4f7-121">You should review [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

<span data-ttu-id="eb4f7-122">Wenn sich das Strukturansicht-Steuerelement nicht im inkrementellen Suchmodus befindet, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="eb4f7-122">If the tree-view control is not in incremental search mode, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb4f7-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb4f7-123">Requirements</span></span>



| <span data-ttu-id="eb4f7-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eb4f7-124">Requirement</span></span> | <span data-ttu-id="eb4f7-125">Wert</span><span class="sxs-lookup"><span data-stu-id="eb4f7-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eb4f7-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eb4f7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="eb4f7-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eb4f7-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eb4f7-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eb4f7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="eb4f7-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eb4f7-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eb4f7-130">Header</span><span class="sxs-lookup"><span data-stu-id="eb4f7-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb4f7-131"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb4f7-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="eb4f7-132">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="eb4f7-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="eb4f7-133">**TVM \_ Getisearchstringw** (Unicode) und **TVM \_ getisearchstrauinga** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="eb4f7-133">**TVM\_GETISEARCHSTRINGW** (Unicode) and **TVM\_GETISEARCHSTRINGA** (ANSI)</span></span><br/> |



 

 





