---
title: TB_ENABLEBUTTON Meldung (kommstrg. h)
description: Aktiviert oder deaktiviert die angegebene Schaltfläche in einer Symbolleiste.
ms.assetid: d73851ee-f909-4b70-9514-c45cd3a7e999
keywords:
- Windows-Steuerelemente für TB_ENABLEBUTTON Meldung
topic_type:
- apiref
api_name:
- TB_ENABLEBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caf2fe865d49f9c89e31b1701abfcbf7991ae72e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342885"
---
# <a name="tb_enablebutton-message"></a><span data-ttu-id="b155b-104">TB \_ enablebutton-Meldung</span><span class="sxs-lookup"><span data-stu-id="b155b-104">TB\_ENABLEBUTTON message</span></span>

<span data-ttu-id="b155b-105">Aktiviert oder deaktiviert die angegebene Schaltfläche in einer Symbolleiste.</span><span class="sxs-lookup"><span data-stu-id="b155b-105">Enables or disables the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="b155b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b155b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b155b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b155b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b155b-108">Der Befehls Bezeichner der Schaltfläche, die aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b155b-108">Command identifier of the button to enable or disable.</span></span>

</dd> <dt>

<span data-ttu-id="b155b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b155b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b155b-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist ein **boolescher** Wert, der angibt, ob die angegebene Schaltfläche aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b155b-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates whether to enable or disable the specified button.</span></span> <span data-ttu-id="b155b-111">**True** gibt an, dass die Schaltfläche aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b155b-111">If **TRUE**, the button is enabled.</span></span> <span data-ttu-id="b155b-112">Wenn der Wert **false** ist, wird die Schaltfläche deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b155b-112">If **FALSE**, the button is disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b155b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b155b-113">Return value</span></span>

<span data-ttu-id="b155b-114">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="b155b-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b155b-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b155b-115">Remarks</span></span>

<span data-ttu-id="b155b-116">Wenn eine Schaltfläche aktiviert wurde, kann Sie gedrückt und aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="b155b-116">When a button has been enabled, it can be pressed and checked.</span></span>

## <a name="requirements"></a><span data-ttu-id="b155b-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b155b-117">Requirements</span></span>



| <span data-ttu-id="b155b-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b155b-118">Requirement</span></span> | <span data-ttu-id="b155b-119">Wert</span><span class="sxs-lookup"><span data-stu-id="b155b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b155b-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b155b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b155b-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b155b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b155b-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b155b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b155b-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b155b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b155b-124">Header</span><span class="sxs-lookup"><span data-stu-id="b155b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b155b-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="b155b-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

