---
title: TB_GETINSERTMARK Meldung (kommstrg. h)
description: Ruft die aktuelle Einfügemarke für die Symbolleiste ab.
ms.assetid: b22770a4-e859-451d-a726-279bbc49b984
keywords:
- Windows-Steuerelemente für TB_GETINSERTMARK Meldung
topic_type:
- apiref
api_name:
- TB_GETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b45a4cafbd49c709e9ca5b8e9afeda51323de491
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040232"
---
# <a name="tb_getinsertmark-message"></a><span data-ttu-id="39da8-104">TB \_ getinsertmark-Nachricht</span><span class="sxs-lookup"><span data-stu-id="39da8-104">TB\_GETINSERTMARK message</span></span>

<span data-ttu-id="39da8-105">Ruft die aktuelle Einfügemarke für die Symbolleiste ab.</span><span class="sxs-lookup"><span data-stu-id="39da8-105">Retrieves the current insertion mark for the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="39da8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="39da8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39da8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="39da8-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="39da8-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="39da8-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="39da8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="39da8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39da8-110">Zeiger auf eine [**tbinsertmark**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) -Struktur, die die Einfügemarke empfängt.</span><span class="sxs-lookup"><span data-stu-id="39da8-110">Pointer to a [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) structure that receives the insertion mark.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39da8-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="39da8-111">Return value</span></span>

<span data-ttu-id="39da8-112">Gibt immer **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="39da8-112">Always returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="39da8-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39da8-113">Requirements</span></span>



| <span data-ttu-id="39da8-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39da8-114">Requirement</span></span> | <span data-ttu-id="39da8-115">Wert</span><span class="sxs-lookup"><span data-stu-id="39da8-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39da8-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="39da8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="39da8-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39da8-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="39da8-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="39da8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="39da8-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39da8-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="39da8-120">Header</span><span class="sxs-lookup"><span data-stu-id="39da8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="39da8-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="39da8-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39da8-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39da8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39da8-123">**TB- \_ Einfügemarke**</span><span class="sxs-lookup"><span data-stu-id="39da8-123">**TB\_SETINSERTMARK**</span></span>](tb-setinsertmark.md)
</dt> </dl>

 

 





