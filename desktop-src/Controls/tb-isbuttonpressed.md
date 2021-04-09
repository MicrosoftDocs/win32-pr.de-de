---
title: TB_ISBUTTONPRESSED Meldung (kommstrg. h)
description: Bestimmt, ob die angegebene Schaltfläche in einer Symbolleiste gedrückt ist.
ms.assetid: b8e2434c-24c2-47eb-b243-ffdaf31d5b8f
keywords:
- Windows-Steuerelemente für TB_ISBUTTONPRESSED Meldung
topic_type:
- apiref
api_name:
- TB_ISBUTTONPRESSED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfc2e6ec7b56ce205f3d89bc22a7c9dbbee90b1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103226"
---
# <a name="tb_isbuttonpressed-message"></a><span data-ttu-id="1e880-104">TB \_ isbuttonpressed-Meldung</span><span class="sxs-lookup"><span data-stu-id="1e880-104">TB\_ISBUTTONPRESSED message</span></span>

<span data-ttu-id="1e880-105">Bestimmt, ob die angegebene Schaltfläche in einer Symbolleiste gedrückt ist.</span><span class="sxs-lookup"><span data-stu-id="1e880-105">Determines whether the specified button in a toolbar is pressed.</span></span>

## <a name="parameters"></a><span data-ttu-id="1e880-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e880-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e880-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1e880-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e880-108">Der Befehls Bezeichner der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="1e880-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="1e880-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1e880-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="1e880-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="1e880-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e880-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1e880-111">Return value</span></span>

<span data-ttu-id="1e880-112">Gibt einen Wert ungleich 0 (null) zurück, wenn die Schaltfläche gedrückt wird, andernfalls 0</span><span class="sxs-lookup"><span data-stu-id="1e880-112">Returns nonzero if the button is pressed, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e880-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e880-113">Requirements</span></span>



| <span data-ttu-id="1e880-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1e880-114">Requirement</span></span> | <span data-ttu-id="1e880-115">Wert</span><span class="sxs-lookup"><span data-stu-id="1e880-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1e880-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1e880-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1e880-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1e880-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1e880-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1e880-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1e880-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1e880-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1e880-120">Header</span><span class="sxs-lookup"><span data-stu-id="1e880-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e880-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e880-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





