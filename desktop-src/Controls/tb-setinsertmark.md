---
title: TB_SETINSERTMARK Meldung (kommstrg. h)
description: Legt die aktuelle Einfügemarke für die Symbolleiste fest.
ms.assetid: 9a576fca-89cf-4db5-9840-35bfa56af89e
keywords:
- Windows-Steuerelemente für TB_SETINSERTMARK Meldung
topic_type:
- apiref
api_name:
- TB_SETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f65ba83d13cbb45f54833725a46de61a5f0444c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102867"
---
# <a name="tb_setinsertmark-message"></a><span data-ttu-id="b65be-104">TB- \_ Meldung "logtmark"</span><span class="sxs-lookup"><span data-stu-id="b65be-104">TB\_SETINSERTMARK message</span></span>

<span data-ttu-id="b65be-105">Legt die aktuelle Einfügemarke für die Symbolleiste fest.</span><span class="sxs-lookup"><span data-stu-id="b65be-105">Sets the current insertion mark for the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="b65be-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b65be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b65be-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b65be-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b65be-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="b65be-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b65be-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b65be-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b65be-110">Zeiger auf eine [**tbinsertmark**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) -Struktur, die die Einfügemarke enthält.</span><span class="sxs-lookup"><span data-stu-id="b65be-110">Pointer to a [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) structure that contains the insertion mark.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b65be-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b65be-111">Return value</span></span>

<span data-ttu-id="b65be-112">Der Rückgabewert für diese Nachricht wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b65be-112">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="b65be-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b65be-113">Requirements</span></span>



| <span data-ttu-id="b65be-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b65be-114">Requirement</span></span> | <span data-ttu-id="b65be-115">Wert</span><span class="sxs-lookup"><span data-stu-id="b65be-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b65be-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b65be-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b65be-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b65be-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b65be-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b65be-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b65be-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b65be-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b65be-120">Header</span><span class="sxs-lookup"><span data-stu-id="b65be-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b65be-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="b65be-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b65be-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b65be-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b65be-123">**TB \_ getinsertmark**</span><span class="sxs-lookup"><span data-stu-id="b65be-123">**TB\_GETINSERTMARK**</span></span>](tb-getinsertmark.md)
</dt> </dl>

 

 





