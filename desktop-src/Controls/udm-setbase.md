---
title: UDM_SETBASE Meldung (kommstrg. h)
description: Legt die Basis für ein auf-ab-Steuerelement fest. Der Basiswert bestimmt, ob das Buddy-Fenster Zahlen in Dezimal-oder hexadezimal Ziffern anzeigt. Hexadezimale Zahlen sind immer unsigniert, und Dezimalzahlen werden signiert.
ms.assetid: c76cdec1-e73b-4b4b-89be-9a00ff2ea172
keywords:
- Windows-Steuerelemente für UDM_SETBASE Meldung
topic_type:
- apiref
api_name:
- UDM_SETBASE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d6bcd7d6154b4ba732e5ffbbec889b326ec8176
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956792"
---
# <a name="udm_setbase-message"></a><span data-ttu-id="3fefc-106">UDM- \_ setbase-Nachricht</span><span class="sxs-lookup"><span data-stu-id="3fefc-106">UDM\_SETBASE message</span></span>

<span data-ttu-id="3fefc-107">Legt die Basis für ein auf-ab-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="3fefc-107">Sets the radix base for an up-down control.</span></span> <span data-ttu-id="3fefc-108">Der Basiswert bestimmt, ob das Buddy-Fenster Zahlen in Dezimal-oder hexadezimal Ziffern anzeigt.</span><span class="sxs-lookup"><span data-stu-id="3fefc-108">The base value determines whether the buddy window displays numbers in decimal or hexadecimal digits.</span></span> <span data-ttu-id="3fefc-109">Hexadezimale Zahlen sind immer unsigniert, und Dezimalzahlen werden signiert.</span><span class="sxs-lookup"><span data-stu-id="3fefc-109">Hexadecimal numbers are always unsigned, and decimal numbers are signed.</span></span>

## <a name="parameters"></a><span data-ttu-id="3fefc-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3fefc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fefc-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3fefc-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3fefc-112">Neuer Basiswert für das Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="3fefc-112">New base value for the control.</span></span> <span data-ttu-id="3fefc-113">Dieser Parameter kann für "Decimal" oder "16" für hexadezimale 10 lauten.</span><span class="sxs-lookup"><span data-stu-id="3fefc-113">This parameter can be 10 for decimal or 16 for hexadecimal.</span></span>

</dd> <dt>

<span data-ttu-id="3fefc-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3fefc-114">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3fefc-115">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="3fefc-115">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fefc-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3fefc-116">Return value</span></span>

<span data-ttu-id="3fefc-117">Der Rückgabewert ist der vorherige Basiswert.</span><span class="sxs-lookup"><span data-stu-id="3fefc-117">The return value is the previous base value.</span></span> <span data-ttu-id="3fefc-118">Wenn eine ungültige Basis angegeben wird, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="3fefc-118">If an invalid base is given, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fefc-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3fefc-119">Requirements</span></span>



| <span data-ttu-id="3fefc-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3fefc-120">Requirement</span></span> | <span data-ttu-id="3fefc-121">Wert</span><span class="sxs-lookup"><span data-stu-id="3fefc-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3fefc-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3fefc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3fefc-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3fefc-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3fefc-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3fefc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3fefc-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3fefc-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3fefc-126">Header</span><span class="sxs-lookup"><span data-stu-id="3fefc-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fefc-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fefc-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





