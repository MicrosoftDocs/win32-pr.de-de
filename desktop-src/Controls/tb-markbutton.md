---
title: TB_MARKBUTTON Meldung (kommstrg. h)
description: Legt den Hervorhebungs Zustand einer angegebenen Schaltfläche in einem Symbolleisten-Steuerelement fest.
ms.assetid: cba0e2d2-40a7-4e20-a1ef-d5f5444c96d9
keywords:
- Windows-Steuerelemente für TB_MARKBUTTON Meldung
topic_type:
- apiref
api_name:
- TB_MARKBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d42983f5fb0ef6e62716cefa2fa8db4fca87fa4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040842"
---
# <a name="tb_markbutton-message"></a><span data-ttu-id="4a8ab-104">TB- \_ markbutton-Meldung</span><span class="sxs-lookup"><span data-stu-id="4a8ab-104">TB\_MARKBUTTON message</span></span>

<span data-ttu-id="4a8ab-105">Legt den Hervorhebungs Zustand einer angegebenen Schaltfläche in einem Symbolleisten-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="4a8ab-105">Sets the highlight state of a given button in a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4a8ab-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a8ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a8ab-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4a8ab-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4a8ab-108">Befehls Bezeichner für eine Symbolleisten-Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="4a8ab-108">Command identifier for a toolbar button.</span></span>

</dd> <dt>

<span data-ttu-id="4a8ab-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4a8ab-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4a8ab-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist ein **boolescher** Wert, der den neuen Hervorhebungs Zustand angibt.</span><span class="sxs-lookup"><span data-stu-id="4a8ab-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates the new highlight state.</span></span> <span data-ttu-id="4a8ab-111">**True** gibt an, dass die Schaltfläche hervorgehoben ist.</span><span class="sxs-lookup"><span data-stu-id="4a8ab-111">If **TRUE**, the button is highlighted.</span></span> <span data-ttu-id="4a8ab-112">Wenn der Wert **false** ist, wird die Schaltfläche auf den Standardzustand festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4a8ab-112">If **FALSE**, the button is set to its default state.</span></span>

<span data-ttu-id="4a8ab-113">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="4a8ab-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a8ab-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4a8ab-114">Return value</span></span>

<span data-ttu-id="4a8ab-115">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="4a8ab-115">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a8ab-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a8ab-116">Requirements</span></span>



| <span data-ttu-id="4a8ab-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4a8ab-117">Requirement</span></span> | <span data-ttu-id="4a8ab-118">Wert</span><span class="sxs-lookup"><span data-stu-id="4a8ab-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4a8ab-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4a8ab-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4a8ab-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4a8ab-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4a8ab-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4a8ab-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4a8ab-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4a8ab-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4a8ab-123">Header</span><span class="sxs-lookup"><span data-stu-id="4a8ab-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a8ab-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a8ab-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

