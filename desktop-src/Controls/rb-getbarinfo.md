---
title: RB_GETBARINFO Meldung (kommstrg. h)
description: Ruft Informationen zum Grund leisten-Steuerelement und der von ihm verwendeten Bildliste ab.
ms.assetid: d3d56b95-7540-4e45-bb2e-b9d41cfcca0d
keywords:
- Windows-Steuerelemente für RB_GETBARINFO Meldung
topic_type:
- apiref
api_name:
- RB_GETBARINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d224c7c826bad0d5d6ae76ce5a4c2266632fa8a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040793"
---
# <a name="rb_getbarinfo-message"></a><span data-ttu-id="ce6a2-104">RB \_ getbarinfo-Meldung</span><span class="sxs-lookup"><span data-stu-id="ce6a2-104">RB\_GETBARINFO message</span></span>

<span data-ttu-id="ce6a2-105">Ruft Informationen zum Grund leisten-Steuerelement und der von ihm verwendeten Bildliste ab.</span><span class="sxs-lookup"><span data-stu-id="ce6a2-105">Retrieves information about the rebar control and the image list it uses.</span></span>

## <a name="parameters"></a><span data-ttu-id="ce6a2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce6a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce6a2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ce6a2-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ce6a2-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="ce6a2-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ce6a2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ce6a2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ce6a2-110">Zeiger auf eine [**rebarinfo**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) -Struktur, die die Informationen zum Info leisten-Steuerelement empfängt.</span><span class="sxs-lookup"><span data-stu-id="ce6a2-110">Pointer to a [**REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) structure that will receive the rebar control information.</span></span> <span data-ttu-id="ce6a2-111">Sie müssen den **CBSIZE** -Member dieser Struktur auf **sizeof**(rebarinfo) festlegen, bevor Sie diese Nachricht senden.</span><span class="sxs-lookup"><span data-stu-id="ce6a2-111">You must set the **cbSize** member of this structure to **sizeof**(REBARINFO) before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce6a2-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ce6a2-112">Return value</span></span>

<span data-ttu-id="ce6a2-113">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="ce6a2-113">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce6a2-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce6a2-114">Requirements</span></span>



| <span data-ttu-id="ce6a2-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce6a2-115">Requirement</span></span> | <span data-ttu-id="ce6a2-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ce6a2-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ce6a2-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ce6a2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ce6a2-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce6a2-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ce6a2-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ce6a2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ce6a2-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce6a2-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ce6a2-121">Header</span><span class="sxs-lookup"><span data-stu-id="ce6a2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce6a2-122"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce6a2-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





