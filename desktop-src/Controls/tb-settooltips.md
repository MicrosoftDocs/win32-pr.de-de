---
title: TB_SETTOOLTIPS Meldung (kommstrg. h)
description: Verknüpft ein QuickInfo-Steuerelement mit einer Symbolleiste.
ms.assetid: a645f1f2-9333-4e25-985a-107cffb9b97f
keywords:
- Windows-Steuerelemente für TB_SETTOOLTIPS Meldung
topic_type:
- apiref
api_name:
- TB_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 781565658d2c362ca32e36736d6e2d80c3641514
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040362"
---
# <a name="tb_settooltips-message"></a><span data-ttu-id="a36cf-104">TB \_ SetToolTips-Meldung</span><span class="sxs-lookup"><span data-stu-id="a36cf-104">TB\_SETTOOLTIPS message</span></span>

<span data-ttu-id="a36cf-105">Verknüpft ein QuickInfo-Steuerelement mit einer Symbolleiste.</span><span class="sxs-lookup"><span data-stu-id="a36cf-105">Associates a tooltip control with a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="a36cf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a36cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a36cf-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a36cf-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a36cf-108">Handle für das QuickInfo-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="a36cf-108">Handle to the tooltip control.</span></span>

</dd> <dt>

<span data-ttu-id="a36cf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a36cf-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a36cf-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="a36cf-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a36cf-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a36cf-111">Return value</span></span>

<span data-ttu-id="a36cf-112">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="a36cf-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a36cf-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a36cf-113">Remarks</span></span>

<span data-ttu-id="a36cf-114">Alle Schaltflächen, die einer Symbolleiste vor dem Senden der **TB- \_ SetToolTips** -Nachricht hinzugefügt werden, werden nicht beim QuickInfo-Steuerelement registriert</span><span class="sxs-lookup"><span data-stu-id="a36cf-114">Any buttons added to a toolbar before sending the **TB\_SETTOOLTIPS** message will not be registered with the tooltip control.</span></span>

## <a name="requirements"></a><span data-ttu-id="a36cf-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a36cf-115">Requirements</span></span>



| <span data-ttu-id="a36cf-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a36cf-116">Requirement</span></span> | <span data-ttu-id="a36cf-117">Wert</span><span class="sxs-lookup"><span data-stu-id="a36cf-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a36cf-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a36cf-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a36cf-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a36cf-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a36cf-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a36cf-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a36cf-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a36cf-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a36cf-122">Header</span><span class="sxs-lookup"><span data-stu-id="a36cf-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a36cf-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="a36cf-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





