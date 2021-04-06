---
title: MCM_GETCALENDARGRIDINFO Meldung (kommstrg. h)
description: Ruft Informationen zu einem Kalender Raster ab.
ms.assetid: 6b385362-f963-4041-bc9f-d2b7a890c9b4
keywords:
- Windows-Steuerelemente für MCM_GETCALENDARGRIDINFO Meldung
topic_type:
- apiref
api_name:
- MCM_GETCALENDARGRIDINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 506f6193ab32d059bb85fa4583441bfbe027f224
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743993"
---
# <a name="mcm_getcalendargridinfo-message"></a><span data-ttu-id="da38f-104">MCM \_ getcalendargridinfo-Meldung</span><span class="sxs-lookup"><span data-stu-id="da38f-104">MCM\_GETCALENDARGRIDINFO message</span></span>

<span data-ttu-id="da38f-105">Ruft Informationen zu einem Kalender Raster ab.</span><span class="sxs-lookup"><span data-stu-id="da38f-105">Gets information about a calendar grid.</span></span>

## <a name="parameters"></a><span data-ttu-id="da38f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="da38f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da38f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="da38f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da38f-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="da38f-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="da38f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="da38f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da38f-110">Zeiger auf eine [**mcgridinfo**](/windows/win32/api/commctrl/ns-commctrl-mcgridinfo) -Struktur, die Informationen über das Kalender Raster enthält.</span><span class="sxs-lookup"><span data-stu-id="da38f-110">Pointer to an [**MCGRIDINFO**](/windows/win32/api/commctrl/ns-commctrl-mcgridinfo) structure that contains information about the calendar grid.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da38f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="da38f-111">Return value</span></span>

<span data-ttu-id="da38f-112">**True** , wenn erfolgreich, andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="da38f-112">**TRUE** if successful, otherwise **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="da38f-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da38f-113">Requirements</span></span>



| <span data-ttu-id="da38f-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da38f-114">Requirement</span></span> | <span data-ttu-id="da38f-115">Wert</span><span class="sxs-lookup"><span data-stu-id="da38f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="da38f-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="da38f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="da38f-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da38f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="da38f-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="da38f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="da38f-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da38f-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="da38f-120">Header</span><span class="sxs-lookup"><span data-stu-id="da38f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="da38f-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="da38f-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





