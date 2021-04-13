---
title: TB_AUTOSIZE Meldung (kommstrg. h)
description: Bewirkt, dass die Größe einer Symbolleiste geändert wird.
ms.assetid: 11aff184-6f18-43a2-9bdc-462fc5ba1680
keywords:
- Windows-Steuerelemente für TB_AUTOSIZE Meldung
topic_type:
- apiref
api_name:
- TB_AUTOSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5f901463888338fd9cadf67472232efe9a25f29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519311"
---
# <a name="tb_autosize-message"></a><span data-ttu-id="25073-104">TB \_ AutoSize-Nachricht</span><span class="sxs-lookup"><span data-stu-id="25073-104">TB\_AUTOSIZE message</span></span>

<span data-ttu-id="25073-105">Bewirkt, dass die Größe einer Symbolleiste geändert wird.</span><span class="sxs-lookup"><span data-stu-id="25073-105">Causes a toolbar to be resized.</span></span>

## <a name="parameters"></a><span data-ttu-id="25073-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="25073-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25073-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="25073-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="25073-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="25073-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="25073-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="25073-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="25073-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="25073-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25073-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="25073-111">Return value</span></span>

<span data-ttu-id="25073-112">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="25073-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="25073-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="25073-113">Remarks</span></span>

<span data-ttu-id="25073-114">Eine Anwendung sendet die **TB \_ AutoSize** -Nachricht, nachdem die Größe einer Symbolleiste geändert wurde, indem entweder die Schaltfläche oder die Bitmapgröße festgelegt oder Zeichen folgen zum ersten Mal hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="25073-114">An application sends the **TB\_AUTOSIZE** message after causing the size of a toolbar to change either by setting the button or bitmap size or by adding strings for the first time.</span></span>

## <a name="requirements"></a><span data-ttu-id="25073-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25073-115">Requirements</span></span>



| <span data-ttu-id="25073-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="25073-116">Requirement</span></span> | <span data-ttu-id="25073-117">Wert</span><span class="sxs-lookup"><span data-stu-id="25073-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="25073-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="25073-118">Minimum supported client</span></span><br/> | <span data-ttu-id="25073-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="25073-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="25073-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="25073-120">Minimum supported server</span></span><br/> | <span data-ttu-id="25073-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="25073-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="25073-122">Header</span><span class="sxs-lookup"><span data-stu-id="25073-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="25073-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="25073-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





