---
title: TB_ISBUTTONENABLED Meldung (kommstrg. h)
description: Bestimmt, ob die angegebene Schaltfläche in einer Symbolleiste aktiviert ist.
ms.assetid: 055ed89a-2f3a-4174-b249-c6e68afbad31
keywords:
- Windows-Steuerelemente für TB_ISBUTTONENABLED Meldung
topic_type:
- apiref
api_name:
- TB_ISBUTTONENABLED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1647d158f0e19ce9dc110a475990cfcc9deff770
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858782"
---
# <a name="tb_isbuttonenabled-message"></a><span data-ttu-id="a0c2d-104">TB \_ isbuttonaktivierte Meldung</span><span class="sxs-lookup"><span data-stu-id="a0c2d-104">TB\_ISBUTTONENABLED message</span></span>

<span data-ttu-id="a0c2d-105">Bestimmt, ob die angegebene Schaltfläche in einer Symbolleiste aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-105">Determines whether the specified button in a toolbar is enabled.</span></span>

## <a name="parameters"></a><span data-ttu-id="a0c2d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0c2d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0c2d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a0c2d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a0c2d-108">Der Befehls Bezeichner der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="a0c2d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a0c2d-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a0c2d-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0c2d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a0c2d-111">Return value</span></span>

<span data-ttu-id="a0c2d-112">Gibt einen Wert ungleich 0 (null) zurück, wenn die Schaltfläche aktiviert ist, andernfalls.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-112">Returns nonzero if the button is enabled, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0c2d-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a0c2d-113">Requirements</span></span>



| <span data-ttu-id="a0c2d-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a0c2d-114">Requirement</span></span> | <span data-ttu-id="a0c2d-115">Wert</span><span class="sxs-lookup"><span data-stu-id="a0c2d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a0c2d-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a0c2d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a0c2d-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a0c2d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a0c2d-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a0c2d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a0c2d-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a0c2d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a0c2d-120">Header</span><span class="sxs-lookup"><span data-stu-id="a0c2d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0c2d-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0c2d-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





