---
title: TB_ISBUTTONCHECKED Meldung (kommstrg. h)
description: Bestimmt, ob die angegebene Schaltfläche in einer Symbolleiste aktiviert ist.
ms.assetid: ce576951-8db6-4854-8457-211ece018ce8
keywords:
- Windows-Steuerelemente für TB_ISBUTTONCHECKED Meldung
topic_type:
- apiref
api_name:
- TB_ISBUTTONCHECKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb9bc573478ea55ce8e0bda48ff16679b135fc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517591"
---
# <a name="tb_isbuttonchecked-message"></a><span data-ttu-id="a6531-104">TB \_ isbuttoncheckmeldung</span><span class="sxs-lookup"><span data-stu-id="a6531-104">TB\_ISBUTTONCHECKED message</span></span>

<span data-ttu-id="a6531-105">Bestimmt, ob die angegebene Schaltfläche in einer Symbolleiste aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a6531-105">Determines whether the specified button in a toolbar is checked.</span></span>

## <a name="parameters"></a><span data-ttu-id="a6531-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6531-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6531-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a6531-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a6531-108">Der Befehls Bezeichner der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="a6531-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="a6531-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a6531-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a6531-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="a6531-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6531-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a6531-111">Return value</span></span>

<span data-ttu-id="a6531-112">Gibt einen Wert ungleich 0 (null) zurück, wenn die Schaltfläche aktiviert ist, andernfalls.</span><span class="sxs-lookup"><span data-stu-id="a6531-112">Returns nonzero if the button is checked, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6531-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6531-113">Requirements</span></span>



| <span data-ttu-id="a6531-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a6531-114">Requirement</span></span> | <span data-ttu-id="a6531-115">Wert</span><span class="sxs-lookup"><span data-stu-id="a6531-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a6531-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a6531-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a6531-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a6531-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a6531-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a6531-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a6531-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a6531-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a6531-120">Header</span><span class="sxs-lookup"><span data-stu-id="a6531-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6531-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6531-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





