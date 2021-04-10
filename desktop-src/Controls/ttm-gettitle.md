---
title: TTM_GETTITLE Meldung (kommstrg. h)
description: Ruft Informationen über den Titel eines QuickInfo-Steuer Elements ab.
ms.assetid: d8992dd1-1610-44e8-8c0f-8ae1ac4b5898
keywords:
- Windows-Steuerelemente für TTM_GETTITLE Meldung
topic_type:
- apiref
api_name:
- TTM_GETTITLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0048925ed3dc267ac07b10b85e2ea1ca1449996c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956486"
---
# <a name="ttm_gettitle-message"></a><span data-ttu-id="53b18-104">TTM \_ getTitle-Nachricht</span><span class="sxs-lookup"><span data-stu-id="53b18-104">TTM\_GETTITLE message</span></span>

<span data-ttu-id="53b18-105">Ruft Informationen über den Titel eines QuickInfo-Steuer Elements ab.</span><span class="sxs-lookup"><span data-stu-id="53b18-105">Retrieve information concerning the title of a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="53b18-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="53b18-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53b18-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="53b18-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="53b18-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="53b18-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="53b18-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="53b18-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53b18-110">Ein Zeiger auf eine [**ttgettitle**](/windows/desktop/api/Commctrl/ns-commctrl-ttgettitle) -Struktur, die Informationen über einen QuickInfo-Titel enthält.</span><span class="sxs-lookup"><span data-stu-id="53b18-110">Pointer to a [**TTGETTITLE**](/windows/desktop/api/Commctrl/ns-commctrl-ttgettitle) structure that contains information about a tooltip title.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53b18-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="53b18-111">Return value</span></span>

<span data-ttu-id="53b18-112">Der Rückgabewert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="53b18-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="53b18-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="53b18-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="53b18-114">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="53b18-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="53b18-115">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="53b18-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="53b18-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53b18-116">Requirements</span></span>



| <span data-ttu-id="53b18-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="53b18-117">Requirement</span></span> | <span data-ttu-id="53b18-118">Wert</span><span class="sxs-lookup"><span data-stu-id="53b18-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="53b18-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="53b18-119">Minimum supported client</span></span><br/> | <span data-ttu-id="53b18-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="53b18-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="53b18-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="53b18-121">Minimum supported server</span></span><br/> | <span data-ttu-id="53b18-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="53b18-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="53b18-123">Header</span><span class="sxs-lookup"><span data-stu-id="53b18-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="53b18-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="53b18-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





