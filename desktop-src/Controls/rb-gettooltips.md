---
title: RB_GETTOOLTIPS Meldung (kommstrg. h)
description: Ruft das Handle für ein QuickInfo-Steuerelement ab, das dem Grund leisten-Steuerelement zugeordnet ist.
ms.assetid: 87897b00-857f-4a8a-ae16-a48abf4c411d
keywords:
- Windows-Steuerelemente für RB_GETTOOLTIPS Meldung
topic_type:
- apiref
api_name:
- RB_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 703b500e7009ca5f5cad46dc72d5deebeebca047
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104438"
---
# <a name="rb_gettooltips-message"></a><span data-ttu-id="2e3ec-104">RB \_ gettooltips-Meldung</span><span class="sxs-lookup"><span data-stu-id="2e3ec-104">RB\_GETTOOLTIPS message</span></span>

<span data-ttu-id="2e3ec-105">Ruft das Handle für ein QuickInfo-Steuerelement ab, das dem Grund leisten-Steuerelement zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2e3ec-105">Retrieves the handle to any tooltip control associated with the rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="2e3ec-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e3ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e3ec-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2e3ec-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2e3ec-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="2e3ec-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2e3ec-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2e3ec-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2e3ec-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="2e3ec-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e3ec-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2e3ec-111">Return value</span></span>

<span data-ttu-id="2e3ec-112">Gibt einen **HWND** -Wert zurück, der das Handle für das QuickInfo-Steuerelement ist, das dem Grund leisten-Steuerelement zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="2e3ec-112">Returns an **HWND** value that is the handle to the tooltip control associated with the rebar control, or zero if no tooltip control is associated with the rebar control.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e3ec-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e3ec-113">Requirements</span></span>



| <span data-ttu-id="2e3ec-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e3ec-114">Requirement</span></span> | <span data-ttu-id="2e3ec-115">Wert</span><span class="sxs-lookup"><span data-stu-id="2e3ec-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2e3ec-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2e3ec-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2e3ec-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2e3ec-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2e3ec-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2e3ec-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2e3ec-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2e3ec-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2e3ec-120">Header</span><span class="sxs-lookup"><span data-stu-id="2e3ec-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e3ec-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e3ec-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





