---
title: TB_GETTOOLTIPS Meldung (kommstrg. h)
description: Ruft das Handle für das QuickInfo-Steuerelement ab, das der Symbolleiste zugeordnet ist.
ms.assetid: 1e0edfdc-d0cb-41f3-9178-1239d81d3034
keywords:
- Windows-Steuerelemente für TB_GETTOOLTIPS Meldung
topic_type:
- apiref
api_name:
- TB_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 488212b34f9f1816797f097a5a1f42d2ea4f68c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040690"
---
# <a name="tb_gettooltips-message"></a><span data-ttu-id="d3e8b-104">TB \_ gettooltips-Meldung</span><span class="sxs-lookup"><span data-stu-id="d3e8b-104">TB\_GETTOOLTIPS message</span></span>

<span data-ttu-id="d3e8b-105">Ruft das Handle für das QuickInfo-Steuerelement ab, das der Symbolleiste zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d3e8b-105">Retrieves the handle to the tooltip control, if any, associated with the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="d3e8b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3e8b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3e8b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d3e8b-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d3e8b-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="d3e8b-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d3e8b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d3e8b-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d3e8b-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="d3e8b-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3e8b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d3e8b-111">Return value</span></span>

<span data-ttu-id="d3e8b-112">Gibt das Handle für das QuickInfo-Steuerelement oder **null** zurück, wenn die Symbolleiste keine zugeordnete QuickInfo aufweist.</span><span class="sxs-lookup"><span data-stu-id="d3e8b-112">Returns the handle to the tooltip control, or **NULL** if the toolbar has no associated tooltip.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3e8b-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d3e8b-113">Requirements</span></span>



| <span data-ttu-id="d3e8b-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d3e8b-114">Requirement</span></span> | <span data-ttu-id="d3e8b-115">Wert</span><span class="sxs-lookup"><span data-stu-id="d3e8b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d3e8b-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d3e8b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d3e8b-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3e8b-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d3e8b-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d3e8b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d3e8b-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3e8b-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d3e8b-120">Header</span><span class="sxs-lookup"><span data-stu-id="d3e8b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3e8b-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3e8b-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





