---
title: TB_ISBUTTONHIDDEN Meldung (kommstrg. h)
description: Bestimmt, ob die angegebene Schaltfläche in einer Symbolleiste ausgeblendet ist.
ms.assetid: 3372a64f-8209-4e3f-a6a9-8fe2e7e87ff2
keywords:
- Windows-Steuerelemente für TB_ISBUTTONHIDDEN Meldung
topic_type:
- apiref
api_name:
- TB_ISBUTTONHIDDEN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db36f289a05fecfb2a0795965820324a9ce68057
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957248"
---
# <a name="tb_isbuttonhidden-message"></a><span data-ttu-id="35e0d-104">TB \_ isbuttonhidden-Nachricht</span><span class="sxs-lookup"><span data-stu-id="35e0d-104">TB\_ISBUTTONHIDDEN message</span></span>

<span data-ttu-id="35e0d-105">Bestimmt, ob die angegebene Schaltfläche in einer Symbolleiste ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="35e0d-105">Determines whether the specified button in a toolbar is hidden.</span></span>

## <a name="parameters"></a><span data-ttu-id="35e0d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="35e0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35e0d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="35e0d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35e0d-108">Der Befehls Bezeichner der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="35e0d-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="35e0d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="35e0d-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="35e0d-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="35e0d-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35e0d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="35e0d-111">Return value</span></span>

<span data-ttu-id="35e0d-112">Gibt einen Wert ungleich 0 (null) zurück, wenn die Schaltfläche ausgeblendet ist, andernfalls.</span><span class="sxs-lookup"><span data-stu-id="35e0d-112">Returns nonzero if the button is hidden, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="35e0d-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="35e0d-113">Requirements</span></span>



| <span data-ttu-id="35e0d-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="35e0d-114">Requirement</span></span> | <span data-ttu-id="35e0d-115">Wert</span><span class="sxs-lookup"><span data-stu-id="35e0d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="35e0d-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="35e0d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="35e0d-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="35e0d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="35e0d-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="35e0d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="35e0d-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="35e0d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="35e0d-120">Header</span><span class="sxs-lookup"><span data-stu-id="35e0d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="35e0d-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="35e0d-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





