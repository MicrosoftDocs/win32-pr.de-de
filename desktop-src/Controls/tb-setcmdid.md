---
title: TB_SETCMDID Meldung (kommstrg. h)
description: Legt den Befehls Bezeichner einer Symbolleisten Schaltfläche fest.
ms.assetid: 0674c905-2d9d-45d3-b565-2f3bcd7d6383
keywords:
- Windows-Steuerelemente für TB_SETCMDID Meldung
topic_type:
- apiref
api_name:
- TB_SETCMDID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f91cc4fd4d70e912bed3163cdf783e8e17ab463
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338733"
---
# <a name="tb_setcmdid-message"></a><span data-ttu-id="1f56e-104">TB \_ setcmdid-Meldung</span><span class="sxs-lookup"><span data-stu-id="1f56e-104">TB\_SETCMDID message</span></span>

<span data-ttu-id="1f56e-105">Legt den Befehls Bezeichner einer Symbolleisten Schaltfläche fest.</span><span class="sxs-lookup"><span data-stu-id="1f56e-105">Sets the command identifier of a toolbar button.</span></span>

## <a name="parameters"></a><span data-ttu-id="1f56e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f56e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f56e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1f56e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1f56e-108">NULL basierter Index der Schaltfläche, deren Befehls Bezeichner festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1f56e-108">Zero-based index of the button whose command identifier is to be set.</span></span>

</dd> <dt>

<span data-ttu-id="1f56e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1f56e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1f56e-110">Befehls Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="1f56e-110">Command identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f56e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1f56e-111">Return value</span></span>

<span data-ttu-id="1f56e-112">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="1f56e-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f56e-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1f56e-113">Requirements</span></span>



| <span data-ttu-id="1f56e-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1f56e-114">Requirement</span></span> | <span data-ttu-id="1f56e-115">Wert</span><span class="sxs-lookup"><span data-stu-id="1f56e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1f56e-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1f56e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1f56e-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1f56e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1f56e-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1f56e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1f56e-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1f56e-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1f56e-120">Header</span><span class="sxs-lookup"><span data-stu-id="1f56e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f56e-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f56e-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





