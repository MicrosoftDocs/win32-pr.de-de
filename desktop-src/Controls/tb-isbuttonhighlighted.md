---
title: TB_ISBUTTONHIGHLIGHTED Meldung (kommstrg. h)
description: Überprüft den Hervorhebungs Zustand einer Symbolleisten-Schaltfläche.
ms.assetid: d5aab670-a989-46f2-b4f8-d8a8968cbe07
keywords:
- Windows-Steuerelemente für TB_ISBUTTONHIGHLIGHTED Meldung
topic_type:
- apiref
api_name:
- TB_ISBUTTONHIGHLIGHTED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f53e25058fee8fa5dcac218a641277ac46aed4e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040364"
---
# <a name="tb_isbuttonhighlighted-message"></a><span data-ttu-id="3c5aa-104">TB \_ isbuttonmarkierte Meldung</span><span class="sxs-lookup"><span data-stu-id="3c5aa-104">TB\_ISBUTTONHIGHLIGHTED message</span></span>

<span data-ttu-id="3c5aa-105">Überprüft den Hervorhebungs Zustand einer Symbolleisten-Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-105">Checks the highlight state of a toolbar button.</span></span>

## <a name="parameters"></a><span data-ttu-id="3c5aa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c5aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c5aa-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3c5aa-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3c5aa-108">Befehls Bezeichner für eine Symbolleisten-Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-108">Command identifier for a toolbar button.</span></span>

</dd> <dt>

<span data-ttu-id="3c5aa-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3c5aa-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3c5aa-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c5aa-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3c5aa-111">Return value</span></span>

<span data-ttu-id="3c5aa-112">Gibt einen Wert ungleich 0 (null) zurück, wenn die Schaltfläche markiert ist, andernfalls NULL</span><span class="sxs-lookup"><span data-stu-id="3c5aa-112">Returns nonzero if the button is highlighted, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c5aa-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c5aa-113">Requirements</span></span>



| <span data-ttu-id="3c5aa-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c5aa-114">Requirement</span></span> | <span data-ttu-id="3c5aa-115">Wert</span><span class="sxs-lookup"><span data-stu-id="3c5aa-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3c5aa-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3c5aa-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3c5aa-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c5aa-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3c5aa-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3c5aa-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3c5aa-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c5aa-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3c5aa-120">Header</span><span class="sxs-lookup"><span data-stu-id="3c5aa-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c5aa-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c5aa-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





