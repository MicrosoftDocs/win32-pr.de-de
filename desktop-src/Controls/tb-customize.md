---
title: TB_CUSTOMIZE Meldung (kommstrg. h)
description: Zeigt das Dialogfeld Symbolleiste anpassen an.
ms.assetid: 45249467-d585-4ffd-8bbe-e39739059c40
keywords:
- Windows-Steuerelemente für TB_CUSTOMIZE Meldung
topic_type:
- apiref
api_name:
- TB_CUSTOMIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dada0ef195e898b7a46487a2d775e46d6af854ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345532"
---
# <a name="tb_customize-message"></a><span data-ttu-id="ef180-104">TB anpassbare \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="ef180-104">TB\_CUSTOMIZE message</span></span>

<span data-ttu-id="ef180-105">Zeigt das Dialogfeld **Symbolleiste anpassen** an.</span><span class="sxs-lookup"><span data-stu-id="ef180-105">Displays the **Customize Toolbar** dialog box.</span></span>

## <a name="parameters"></a><span data-ttu-id="ef180-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef180-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef180-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ef180-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ef180-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="ef180-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ef180-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ef180-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ef180-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="ef180-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef180-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ef180-111">Return value</span></span>

<span data-ttu-id="ef180-112">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="ef180-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef180-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef180-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ef180-114">Die Symbolleiste muss die [TBN \_ queryinsert](tbn-queryinsert.md) -und [TBN \_ querydelete](tbn-querydelete.md) -Benachrichtigungen verarbeiten, damit das Dialogfeld **Symbolleiste anpassen** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ef180-114">The toolbar must handle the [TBN\_QUERYINSERT](tbn-queryinsert.md) and [TBN\_QUERYDELETE](tbn-querydelete.md) notifications for the **Customize Toolbar** dialog box to appear.</span></span> <span data-ttu-id="ef180-115">Wenn die Symbolleiste diese Benachrichtigungen nicht verarbeitet, hat die **\_ Anpassung von TB** keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="ef180-115">If the toolbar does not handle those notifications, **TB\_CUSTOMIZE** has no effect.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ef180-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef180-116">Requirements</span></span>



| <span data-ttu-id="ef180-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef180-117">Requirement</span></span> | <span data-ttu-id="ef180-118">Wert</span><span class="sxs-lookup"><span data-stu-id="ef180-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ef180-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ef180-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ef180-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef180-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ef180-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ef180-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ef180-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef180-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ef180-123">Header</span><span class="sxs-lookup"><span data-stu-id="ef180-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef180-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef180-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





