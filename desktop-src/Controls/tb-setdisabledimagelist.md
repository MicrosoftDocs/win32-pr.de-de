---
title: TB_SETDISABLEDIMAGELIST Meldung (kommstrg. h)
description: Legt die Bildliste fest, die das Symbolleisten-Steuerelement zum Anzeigen deaktivierter Schaltflächen verwendet.
ms.assetid: 1e76b3cf-2d06-48c8-8298-ef6caf3d85c3
keywords:
- Windows-Steuerelemente für TB_SETDISABLEDIMAGELIST Meldung
topic_type:
- apiref
api_name:
- TB_SETDISABLEDIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7cc8c9ec1fdc9658413da5991fa109e7bef27a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040841"
---
# <a name="tb_setdisabledimagelist-message"></a><span data-ttu-id="2f80b-104">TB \_ SetDisabledImageList-Meldung</span><span class="sxs-lookup"><span data-stu-id="2f80b-104">TB\_SETDISABLEDIMAGELIST message</span></span>

<span data-ttu-id="2f80b-105">Legt die Bildliste fest, die das Symbolleisten-Steuerelement zum Anzeigen deaktivierter Schaltflächen verwendet.</span><span class="sxs-lookup"><span data-stu-id="2f80b-105">Sets the image list that the toolbar control will use to display disabled buttons.</span></span>

## <a name="parameters"></a><span data-ttu-id="2f80b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f80b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f80b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2f80b-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2f80b-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="2f80b-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2f80b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2f80b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2f80b-110">Handle für die Bildliste, die festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="2f80b-110">Handle to the image list that will be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f80b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2f80b-111">Return value</span></span>

<span data-ttu-id="2f80b-112">Gibt das Handle für die Bildliste zurück, die zuvor zum Anzeigen deaktivierter Schaltflächen verwendet wurde, oder **null** , wenn zuvor keine Bildliste festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="2f80b-112">Returns the handle to the image list previously used to display disabled buttons, or **NULL** if no image list was previously set.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f80b-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f80b-113">Requirements</span></span>



| <span data-ttu-id="2f80b-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2f80b-114">Requirement</span></span> | <span data-ttu-id="2f80b-115">Wert</span><span class="sxs-lookup"><span data-stu-id="2f80b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2f80b-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2f80b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2f80b-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f80b-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2f80b-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2f80b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2f80b-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f80b-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2f80b-120">Header</span><span class="sxs-lookup"><span data-stu-id="2f80b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f80b-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f80b-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





