---
title: TB_SETROWS Meldung (kommstrg. h)
description: Legt die Anzahl der Zeilen von Schaltflächen in einer Symbolleiste fest.
ms.assetid: d8ea7b80-d23e-4593-8eb1-d23808173fc9
keywords:
- Windows-Steuerelemente für TB_SETROWS Meldung
topic_type:
- apiref
api_name:
- TB_SETROWS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d0065a3f5f6a277713e368177886ebd064ea132
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104041012"
---
# <a name="tb_setrows-message"></a><span data-ttu-id="52bb5-104">TB- \_ Nachricht (loggt)</span><span class="sxs-lookup"><span data-stu-id="52bb5-104">TB\_SETROWS message</span></span>

<span data-ttu-id="52bb5-105">Legt die Anzahl der Zeilen von Schaltflächen in einer Symbolleiste fest.</span><span class="sxs-lookup"><span data-stu-id="52bb5-105">Sets the number of rows of buttons in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="52bb5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="52bb5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52bb5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="52bb5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="52bb5-108">Der [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) -Wert gibt die Anzahl der angeforderten Zeilen an.</span><span class="sxs-lookup"><span data-stu-id="52bb5-108">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the number of rows requested.</span></span> <span data-ttu-id="52bb5-109">Die Mindestanzahl von Zeilen ist 1, und die maximale Anzahl von Zeilen entspricht der Anzahl der Schaltflächen auf der Symbolleiste.</span><span class="sxs-lookup"><span data-stu-id="52bb5-109">The minimum number of rows is one, and the maximum number of rows is equal to the number of buttons in the toolbar.</span></span>

<span data-ttu-id="52bb5-110">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) ist ein **boolescher** Wert, der angibt, ob mehr Zeilen als angefordert erstellt werden sollen, wenn das System nicht die Anzahl der Zeilen erstellen kann, die von *wParam* angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="52bb5-110">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is a **BOOL** that indicates whether to create more rows than requested when the system cannot create the number of rows specified by *wParam*.</span></span> <span data-ttu-id="52bb5-111">**True** gibt an, dass das System weitere Zeilen erstellt.</span><span class="sxs-lookup"><span data-stu-id="52bb5-111">If **TRUE**, the system creates more rows.</span></span> <span data-ttu-id="52bb5-112">Wenn der Wert **false** ist, erstellt das System weniger Zeilen.</span><span class="sxs-lookup"><span data-stu-id="52bb5-112">If **FALSE**, the system creates fewer rows.</span></span>

</dd> <dt>

<span data-ttu-id="52bb5-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="52bb5-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="52bb5-114">Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die das umschließende Rechteck der Symbolleiste empfängt, nachdem die Zeilen festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="52bb5-114">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the bounding rectangle of the toolbar after the rows are set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52bb5-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="52bb5-115">Return value</span></span>

<span data-ttu-id="52bb5-116">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="52bb5-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="52bb5-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52bb5-117">Remarks</span></span>

<span data-ttu-id="52bb5-118">Da das System beim Festlegen der Zeilen Anzahl keine Schaltflächen Gruppen aufbricht, kann sich die resultierende Anzahl von Zeilen von der angeforderten Anzahl unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="52bb5-118">Because the system does not break up button groups when setting the number of rows, the resulting number of rows might differ from the number requested.</span></span>

## <a name="requirements"></a><span data-ttu-id="52bb5-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="52bb5-119">Requirements</span></span>



| <span data-ttu-id="52bb5-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="52bb5-120">Requirement</span></span> | <span data-ttu-id="52bb5-121">Wert</span><span class="sxs-lookup"><span data-stu-id="52bb5-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="52bb5-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="52bb5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="52bb5-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="52bb5-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="52bb5-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="52bb5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="52bb5-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="52bb5-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="52bb5-126">Header</span><span class="sxs-lookup"><span data-stu-id="52bb5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="52bb5-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="52bb5-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

