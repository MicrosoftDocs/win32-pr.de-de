---
title: TB_SETANCHORHIGHLIGHT Meldung (kommstrg. h)
description: Legt die Anker Hervorhebungs Einstellung für eine Symbolleiste fest.
ms.assetid: d31652d5-e9cf-4bf3-8f90-818eb078fa87
keywords:
- Windows-Steuerelemente für TB_SETANCHORHIGHLIGHT Meldung
topic_type:
- apiref
api_name:
- TB_SETANCHORHIGHLIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 809f71e446f7768d637258152db1dd2d56346dfd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341357"
---
# <a name="tb_setanchorhighlight-message"></a><span data-ttu-id="97c3a-104">TB-Nachricht "- \_ Abmeldung"</span><span class="sxs-lookup"><span data-stu-id="97c3a-104">TB\_SETANCHORHIGHLIGHT message</span></span>

<span data-ttu-id="97c3a-105">Legt die Anker Hervorhebungs Einstellung für eine Symbolleiste fest.</span><span class="sxs-lookup"><span data-stu-id="97c3a-105">Sets the anchor highlight setting for a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="97c3a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="97c3a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97c3a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="97c3a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="97c3a-108">**Boolescher** Wert, der angibt, ob Anker Hervorhebung aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="97c3a-108">**BOOL** value that specifies if anchor highlighting is enabled or disabled.</span></span> <span data-ttu-id="97c3a-109">Wenn dieser Wert ungleich 0 (null) ist, wird die Anker Markierung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="97c3a-109">If this value is nonzero, anchor highlighting will be enabled.</span></span> <span data-ttu-id="97c3a-110">Wenn dieser Wert 0 (null) ist, wird die Anker Markierung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="97c3a-110">If this value is zero, anchor highlighting will be disabled.</span></span>

</dd> <dt>

<span data-ttu-id="97c3a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="97c3a-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="97c3a-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="97c3a-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97c3a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="97c3a-113">Return value</span></span>

<span data-ttu-id="97c3a-114">Gibt die vorherige Anker Hervorhebungs Einstellung zurück.</span><span class="sxs-lookup"><span data-stu-id="97c3a-114">Returns the previous anchor highlight setting.</span></span> <span data-ttu-id="97c3a-115">Wenn dieser Wert ungleich 0 (null) ist, wurde die Anker Markierung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="97c3a-115">If this value is nonzero, anchor highlighting was enabled.</span></span> <span data-ttu-id="97c3a-116">Wenn dieser Wert 0 (null) ist, wurde die Anker Markierung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="97c3a-116">If this value is zero, anchor highlighting was disabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="97c3a-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="97c3a-117">Remarks</span></span>

<span data-ttu-id="97c3a-118">Die Anker Markierung in einer Symbolleiste bedeutet, dass das letzte markierte Element hervorgehoben bleibt, bis ein anderes Element hervorgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="97c3a-118">Anchor highlighting in a toolbar means that the last highlighted item will remain highlighted until another item is highlighted.</span></span> <span data-ttu-id="97c3a-119">Dies tritt auch auf, wenn der Cursor das Symbolleisten-Steuerelement verlässt.</span><span class="sxs-lookup"><span data-stu-id="97c3a-119">This occurs even if the cursor leaves the toolbar control.</span></span>

## <a name="requirements"></a><span data-ttu-id="97c3a-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97c3a-120">Requirements</span></span>



| <span data-ttu-id="97c3a-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="97c3a-121">Requirement</span></span> | <span data-ttu-id="97c3a-122">Wert</span><span class="sxs-lookup"><span data-stu-id="97c3a-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="97c3a-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="97c3a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="97c3a-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="97c3a-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="97c3a-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="97c3a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="97c3a-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="97c3a-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="97c3a-127">Header</span><span class="sxs-lookup"><span data-stu-id="97c3a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="97c3a-128"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="97c3a-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





