---
title: DTM_GETIDEALSIZE Meldung (kommstrg. h)
description: Ruft die Größe ab, die zum Anzeigen des Steuer Elements ohne Clipping benötigt wird. Senden Sie diese Nachricht explizit oder mithilfe des "DateTime \_ getidealsize"-Makros.
ms.assetid: 15ec26a1-645b-4a96-af66-1031e1a46c6c
keywords:
- Windows-Steuerelemente für DTM_GETIDEALSIZE Meldung
topic_type:
- apiref
api_name:
- DTM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a979883f431fea4627f52fe19c3716341e3f2328
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104213708"
---
# <a name="dtm_getidealsize-message"></a><span data-ttu-id="62c24-105">DTM- \_ getidealsize-Nachricht</span><span class="sxs-lookup"><span data-stu-id="62c24-105">DTM\_GETIDEALSIZE message</span></span>

<span data-ttu-id="62c24-106">Ruft die Größe ab, die zum Anzeigen des Steuer Elements ohne Clipping benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="62c24-106">Gets the size needed to display the control without clipping.</span></span> <span data-ttu-id="62c24-107">Senden Sie diese Nachricht explizit oder mithilfe des " [**DateTime \_ getidealsize**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize) "-Makros.</span><span class="sxs-lookup"><span data-stu-id="62c24-107">Send this message explicitly or by using the [**DateTime\_GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="62c24-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="62c24-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62c24-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="62c24-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="62c24-110">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="62c24-110">Not used.</span></span> <span data-ttu-id="62c24-111">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="62c24-111">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="62c24-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="62c24-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="62c24-113">Ein Zeiger auf eine [**Größen**](/previous-versions//dd145106(v=vs.85)) Struktur, die die ideale Größe erhält.</span><span class="sxs-lookup"><span data-stu-id="62c24-113">A pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure to receive the ideal size.</span></span> <span data-ttu-id="62c24-114">Die aufrufenden Anwendung ist für die Zuordnung dieser Struktur verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="62c24-114">The calling application is responsible for allocating this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62c24-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="62c24-115">Return value</span></span>

<span data-ttu-id="62c24-116">Gibt **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="62c24-116">Returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="62c24-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="62c24-117">Requirements</span></span>



| <span data-ttu-id="62c24-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="62c24-118">Requirement</span></span> | <span data-ttu-id="62c24-119">Wert</span><span class="sxs-lookup"><span data-stu-id="62c24-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="62c24-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="62c24-120">Minimum supported client</span></span><br/> | <span data-ttu-id="62c24-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="62c24-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="62c24-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="62c24-122">Minimum supported server</span></span><br/> | <span data-ttu-id="62c24-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="62c24-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="62c24-124">Header</span><span class="sxs-lookup"><span data-stu-id="62c24-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="62c24-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="62c24-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

