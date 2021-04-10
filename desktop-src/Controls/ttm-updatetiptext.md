---
title: TTM_UPDATETIPTEXT Meldung (kommstrg. h)
description: Legt den QuickInfo-Text für ein Tool fest.
ms.assetid: 2a7432dd-76f9-42b4-b639-178dce1d89ef
keywords:
- Windows-Steuerelemente für TTM_UPDATETIPTEXT Meldung
topic_type:
- apiref
api_name:
- TTM_UPDATETIPTEXT
- TTM_UPDATETIPTEXTA
- TTM_UPDATETIPTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6c94b14ec83c190ce019ecba1413d2fa05f0103
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104433"
---
# <a name="ttm_updatetiptext-message"></a><span data-ttu-id="50c21-104">TTM- \_ updatetiptext-Nachricht</span><span class="sxs-lookup"><span data-stu-id="50c21-104">TTM\_UPDATETIPTEXT message</span></span>

<span data-ttu-id="50c21-105">Legt den QuickInfo-Text für ein Tool fest.</span><span class="sxs-lookup"><span data-stu-id="50c21-105">Sets the tooltip text for a tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="50c21-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="50c21-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50c21-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="50c21-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="50c21-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="50c21-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="50c21-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="50c21-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="50c21-110">Zeiger auf eine [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="50c21-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="50c21-111">Die **hInst** -und **lpszText** -Member müssen den Instanzhandle und die Adresse des Texts angeben.</span><span class="sxs-lookup"><span data-stu-id="50c21-111">The **hinst** and **lpszText** members must specify the instance handle and the address of the text.</span></span> <span data-ttu-id="50c21-112">Das zu aktualisierenden Tool wird durch die **HWND** -und **UID** -Mitglieder identifiziert</span><span class="sxs-lookup"><span data-stu-id="50c21-112">The **hwnd** and **uId** members identify the tool to update.</span></span> <span data-ttu-id="50c21-113">Der **CBSIZE** -Member dieser Struktur muss ausgefüllt werden, bevor diese Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="50c21-113">The **cbSize** member of this structure must be filled in before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50c21-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="50c21-114">Return value</span></span>

<span data-ttu-id="50c21-115">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="50c21-115">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="50c21-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50c21-116">Requirements</span></span>



| <span data-ttu-id="50c21-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="50c21-117">Requirement</span></span> | <span data-ttu-id="50c21-118">Wert</span><span class="sxs-lookup"><span data-stu-id="50c21-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="50c21-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="50c21-119">Minimum supported client</span></span><br/> | <span data-ttu-id="50c21-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50c21-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="50c21-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="50c21-121">Minimum supported server</span></span><br/> | <span data-ttu-id="50c21-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50c21-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="50c21-123">Header</span><span class="sxs-lookup"><span data-stu-id="50c21-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="50c21-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="50c21-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="50c21-125">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="50c21-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="50c21-126">**TTM \_ Updatetiptextw** (Unicode) und **TTM \_ updatetiptexta** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="50c21-126">**TTM\_UPDATETIPTEXTW** (Unicode) and **TTM\_UPDATETIPTEXTA** (ANSI)</span></span><br/>       |



 

 





