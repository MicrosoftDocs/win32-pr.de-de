---
title: TB_ISBUTTONINDETERMINATE Meldung (kommstrg. h)
description: Bestimmt, ob die angegebene Schaltfläche in einer Symbolleiste unbestimmt ist.
ms.assetid: b4d759b3-cdbc-417b-9da4-4ed9edc38c0e
keywords:
- Windows-Steuerelemente für TB_ISBUTTONINDETERMINATE Meldung
topic_type:
- apiref
api_name:
- TB_ISBUTTONINDETERMINATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29fc024efcad9f0f48ae4882b019269903c249bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040363"
---
# <a name="tb_isbuttonindeterminate-message"></a><span data-ttu-id="09a33-104">TB \_ isbuttonindeend-Nachricht</span><span class="sxs-lookup"><span data-stu-id="09a33-104">TB\_ISBUTTONINDETERMINATE message</span></span>

<span data-ttu-id="09a33-105">Bestimmt, ob die angegebene Schaltfläche in einer Symbolleiste unbestimmt ist.</span><span class="sxs-lookup"><span data-stu-id="09a33-105">Determines whether the specified button in a toolbar is indeterminate.</span></span>

## <a name="parameters"></a><span data-ttu-id="09a33-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="09a33-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09a33-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="09a33-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="09a33-108">Der Befehls Bezeichner der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="09a33-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="09a33-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="09a33-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="09a33-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="09a33-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09a33-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="09a33-111">Return value</span></span>

<span data-ttu-id="09a33-112">Gibt einen Wert ungleich 0 (null) zurück, wenn die Schaltfläche unbestimmt ist, andernfalls NULL</span><span class="sxs-lookup"><span data-stu-id="09a33-112">Returns nonzero if the button is indeterminate, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="09a33-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="09a33-113">Requirements</span></span>



| <span data-ttu-id="09a33-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="09a33-114">Requirement</span></span> | <span data-ttu-id="09a33-115">Wert</span><span class="sxs-lookup"><span data-stu-id="09a33-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="09a33-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="09a33-116">Minimum supported client</span></span><br/> | <span data-ttu-id="09a33-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="09a33-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="09a33-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="09a33-118">Minimum supported server</span></span><br/> | <span data-ttu-id="09a33-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="09a33-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="09a33-120">Header</span><span class="sxs-lookup"><span data-stu-id="09a33-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="09a33-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="09a33-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





