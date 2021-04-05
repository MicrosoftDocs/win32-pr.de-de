---
title: TCM_GETROWCOUNT Meldung (kommstrg. h)
description: Ruft die aktuelle Anzahl der Zeilen von Registerkarten in einem Registerkarten-Steuerelement ab. Sie können diese Nachricht explizit oder mithilfe des tabctrl \_ GetRowCount-Makros senden.
ms.assetid: ef104374-1030-46c3-876e-083df73854ab
keywords:
- Windows-Steuerelemente für TCM_GETROWCOUNT Meldung
topic_type:
- apiref
api_name:
- TCM_GETROWCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9bc3d9985591a08b96be2f21d55b8a6cade9b7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859197"
---
# <a name="tcm_getrowcount-message"></a><span data-ttu-id="d74cf-105">TCM \_ GetRowCount-Nachricht</span><span class="sxs-lookup"><span data-stu-id="d74cf-105">TCM\_GETROWCOUNT message</span></span>

<span data-ttu-id="d74cf-106">Ruft die aktuelle Anzahl der Zeilen von Registerkarten in einem Registerkarten-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="d74cf-106">Retrieves the current number of rows of tabs in a tab control.</span></span> <span data-ttu-id="d74cf-107">Sie können diese Nachricht explizit oder mithilfe des [**tabctrl \_ GetRowCount**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getrowcount) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="d74cf-107">You can send this message explicitly or by using the [**TabCtrl\_GetRowCount**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getrowcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d74cf-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d74cf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d74cf-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d74cf-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d74cf-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="d74cf-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d74cf-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d74cf-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d74cf-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="d74cf-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d74cf-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d74cf-113">Return value</span></span>

<span data-ttu-id="d74cf-114">Gibt die Anzahl der Zeilen von Registerkarten zurück.</span><span class="sxs-lookup"><span data-stu-id="d74cf-114">Returns the number of rows of tabs.</span></span>

## <a name="remarks"></a><span data-ttu-id="d74cf-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d74cf-115">Remarks</span></span>

<span data-ttu-id="d74cf-116">Nur Registerkarten-Steuerelemente, die den [**\_ mehrzeiligen TCS**](tab-control-styles.md) -Stil aufweisen, können mehrere Zeilen mit Registerkarten aufweisen</span><span class="sxs-lookup"><span data-stu-id="d74cf-116">Only tab controls that have the [**TCS\_MULTILINE**](tab-control-styles.md) style can have multiple rows of tabs.</span></span>

## <a name="requirements"></a><span data-ttu-id="d74cf-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d74cf-117">Requirements</span></span>



| <span data-ttu-id="d74cf-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d74cf-118">Requirement</span></span> | <span data-ttu-id="d74cf-119">Wert</span><span class="sxs-lookup"><span data-stu-id="d74cf-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d74cf-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d74cf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d74cf-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d74cf-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d74cf-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d74cf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d74cf-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d74cf-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d74cf-124">Header</span><span class="sxs-lookup"><span data-stu-id="d74cf-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d74cf-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="d74cf-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





