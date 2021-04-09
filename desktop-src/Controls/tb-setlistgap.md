---
title: TB_SETLISTGAP Meldung (kommstrg. h)
description: Legt den Abstand zwischen den Symbolleisten-Schaltflächen auf einer bestimmten Symbolleiste fest.
ms.assetid: ca8ba6e4-cf70-41ca-ac61-cd13671d4010
keywords:
- Windows-Steuerelemente für TB_SETLISTGAP Meldung
topic_type:
- apiref
api_name:
- TB_SETLISTGAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 224a709b7beefcfdf49ea7838f905977487aca8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858634"
---
# <a name="tb_setlistgap-message"></a><span data-ttu-id="78dd7-104">TB \_ setlistgap-Nachricht</span><span class="sxs-lookup"><span data-stu-id="78dd7-104">TB\_SETLISTGAP message</span></span>

<span data-ttu-id="78dd7-105">Legt den Abstand zwischen den Symbolleisten-Schaltflächen auf einer bestimmten Symbolleiste fest.</span><span class="sxs-lookup"><span data-stu-id="78dd7-105">Sets the distance between the toolbar buttons on a specific toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="78dd7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="78dd7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78dd7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="78dd7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="78dd7-108">Die Lücke zwischen den Schaltflächen auf der Symbolleiste in Pixel.</span><span class="sxs-lookup"><span data-stu-id="78dd7-108">The gap, in pixels, between buttons on the toolbar.</span></span>

</dd> <dt>

<span data-ttu-id="78dd7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="78dd7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="78dd7-110">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="78dd7-110">Ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78dd7-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="78dd7-111">Return value</span></span>

<span data-ttu-id="78dd7-112">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="78dd7-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="78dd7-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78dd7-113">Remarks</span></span>

<span data-ttu-id="78dd7-114">Die Lücke zwischen Schaltflächen gilt nur für das Symbolleisten-Steuerelement, das diese Nachricht empfängt.</span><span class="sxs-lookup"><span data-stu-id="78dd7-114">The gap between buttons only applies to the toolbar control window that receives this message.</span></span> <span data-ttu-id="78dd7-115">Der Empfang dieser Nachricht löst eine neupaint der Symbolleiste aus, wenn die Symbolleiste momentan sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="78dd7-115">Receipt of this message triggers a repaint of the toolbar, if the toolbar is currently visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="78dd7-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="78dd7-116">Requirements</span></span>



| <span data-ttu-id="78dd7-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="78dd7-117">Requirement</span></span> | <span data-ttu-id="78dd7-118">Wert</span><span class="sxs-lookup"><span data-stu-id="78dd7-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="78dd7-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="78dd7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="78dd7-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="78dd7-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="78dd7-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="78dd7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="78dd7-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="78dd7-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="78dd7-123">Header</span><span class="sxs-lookup"><span data-stu-id="78dd7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="78dd7-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="78dd7-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





