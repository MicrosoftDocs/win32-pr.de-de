---
title: TTM_GETCURRENTTOOL Meldung (kommstrg. h)
description: Ruft die Informationen für das aktuelle Tool in einem QuickInfo-Steuerelement ab.
ms.assetid: acb254cf-064c-4ed8-b488-a3138b648405
keywords:
- Windows-Steuerelemente für TTM_GETCURRENTTOOL Meldung
topic_type:
- apiref
api_name:
- TTM_GETCURRENTTOOL
- TTM_GETCURRENTTOOLA
- TTM_GETCURRENTTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fa6218bcb4ad9aa43c7ffba0d332786956d9a62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956490"
---
# <a name="ttm_getcurrenttool-message"></a><span data-ttu-id="46d87-104">TTM \_ getcurrenttool-Meldung</span><span class="sxs-lookup"><span data-stu-id="46d87-104">TTM\_GETCURRENTTOOL message</span></span>

<span data-ttu-id="46d87-105">Ruft die Informationen für das aktuelle Tool in einem QuickInfo-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="46d87-105">Retrieves the information for the current tool in a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="46d87-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="46d87-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46d87-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="46d87-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="46d87-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="46d87-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="46d87-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="46d87-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="46d87-110">Ein Zeiger auf eine [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur, die Informationen über das aktuelle Tool empfängt.</span><span class="sxs-lookup"><span data-stu-id="46d87-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure that receives information about the current tool.</span></span> <span data-ttu-id="46d87-111">Wenn dieser Wert **null** ist, gibt der Rückgabewert an, dass das aktuelle Tool vorhanden ist, ohne dass die Tool Informationen tatsächlich abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="46d87-111">If this value is **NULL**, the return value indicates the existence of the current tool without actually retrieving the tool information.</span></span> <span data-ttu-id="46d87-112">Wenn dieser Wert nicht **null** ist, muss das **CBSIZE** -Element der **toolinfo** -Struktur ausgefüllt werden, bevor diese Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="46d87-112">If this value is not **NULL**, the **cbSize** member of the **TOOLINFO** structure must be filled in before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46d87-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="46d87-113">Return value</span></span>

<span data-ttu-id="46d87-114">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="46d87-114">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="46d87-115">Wenn *LPARAM* gleich **null** ist, gibt einen Wert ungleich 0 (null) zurück, wenn ein aktuelles Tool vorhanden ist, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="46d87-115">If *lParam* is **NULL**, returns nonzero if a current tool exists, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="46d87-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46d87-116">Requirements</span></span>



| <span data-ttu-id="46d87-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46d87-117">Requirement</span></span> | <span data-ttu-id="46d87-118">Wert</span><span class="sxs-lookup"><span data-stu-id="46d87-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="46d87-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="46d87-119">Minimum supported client</span></span><br/> | <span data-ttu-id="46d87-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="46d87-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="46d87-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="46d87-121">Minimum supported server</span></span><br/> | <span data-ttu-id="46d87-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="46d87-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="46d87-123">Header</span><span class="sxs-lookup"><span data-stu-id="46d87-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="46d87-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="46d87-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="46d87-125">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="46d87-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="46d87-126">**TTM \_ Getcurrenttoolw** (Unicode) und **TTM \_ getcurrenttola** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="46d87-126">**TTM\_GETCURRENTTOOLW** (Unicode) and **TTM\_GETCURRENTTOOLA** (ANSI)</span></span><br/>     |



 

 





