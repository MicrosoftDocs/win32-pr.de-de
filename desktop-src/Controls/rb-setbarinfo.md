---
title: RB_SETBARINFO Meldung (kommstrg. h)
description: Legt die Eigenschaften eines Grund leisten-Steuer Elements fest.
ms.assetid: e4413d46-574f-4ccd-b5fd-3ba6c1e3924b
keywords:
- Windows-Steuerelemente für RB_SETBARINFO Meldung
topic_type:
- apiref
api_name:
- RB_SETBARINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b360bc0b4d14963619aad8f769634d7dd0ad17e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040162"
---
# <a name="rb_setbarinfo-message"></a><span data-ttu-id="fdf88-104">RB- \_ setbarinfo-Meldung</span><span class="sxs-lookup"><span data-stu-id="fdf88-104">RB\_SETBARINFO message</span></span>

<span data-ttu-id="fdf88-105">Legt die Eigenschaften eines Grund leisten-Steuer Elements fest.</span><span class="sxs-lookup"><span data-stu-id="fdf88-105">Sets the characteristics of a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="fdf88-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fdf88-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdf88-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fdf88-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="fdf88-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="fdf88-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="fdf88-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fdf88-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fdf88-110">Ein Zeiger auf eine [**rebarinfo**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) -Struktur, die die festzulegenden Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="fdf88-110">Pointer to a [**REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) structure that contains the information to be set.</span></span> <span data-ttu-id="fdf88-111">Sie müssen den **CBSIZE** -Member dieser Struktur auf **sizeof**(rebarinfo) festlegen, bevor Sie diese Nachricht senden.</span><span class="sxs-lookup"><span data-stu-id="fdf88-111">You must set the **cbSize** member of this structure to **sizeof**(REBARINFO) before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdf88-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fdf88-112">Return value</span></span>

<span data-ttu-id="fdf88-113">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="fdf88-113">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdf88-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fdf88-114">Requirements</span></span>



| <span data-ttu-id="fdf88-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fdf88-115">Requirement</span></span> | <span data-ttu-id="fdf88-116">Wert</span><span class="sxs-lookup"><span data-stu-id="fdf88-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fdf88-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fdf88-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fdf88-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fdf88-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fdf88-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fdf88-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fdf88-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fdf88-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fdf88-121">Header</span><span class="sxs-lookup"><span data-stu-id="fdf88-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdf88-122"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdf88-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





