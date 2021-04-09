---
title: TB_REPLACEBITMAP Meldung (kommstrg. h)
description: Ersetzt eine vorhandene Bitmap durch eine neue Bitmap.
ms.assetid: abad5c7a-ebdd-46b5-a465-fe64ff8eb127
keywords:
- Windows-Steuerelemente für TB_REPLACEBITMAP Meldung
topic_type:
- apiref
api_name:
- TB_REPLACEBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0216d73f70f9bef8230d7e725834d63d60012798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859099"
---
# <a name="tb_replacebitmap-message"></a><span data-ttu-id="55b8d-104">TB \_ replacebitmap-Meldung</span><span class="sxs-lookup"><span data-stu-id="55b8d-104">TB\_REPLACEBITMAP message</span></span>

<span data-ttu-id="55b8d-105">Ersetzt eine vorhandene Bitmap durch eine neue Bitmap.</span><span class="sxs-lookup"><span data-stu-id="55b8d-105">Replaces an existing bitmap with a new bitmap.</span></span>

## <a name="parameters"></a><span data-ttu-id="55b8d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="55b8d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55b8d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="55b8d-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="55b8d-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="55b8d-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="55b8d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="55b8d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="55b8d-110">Zeiger auf eine [**tbreplacebitmap**](/windows/desktop/api/Commctrl/ns-commctrl-tbreplacebitmap) -Struktur, die die Informationen der zu ersetzenden Bitmap und der neuen Bitmap enthält.</span><span class="sxs-lookup"><span data-stu-id="55b8d-110">Pointer to a [**TBREPLACEBITMAP**](/windows/desktop/api/Commctrl/ns-commctrl-tbreplacebitmap) structure that contains the information of the bitmap to be replaced and the new bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55b8d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="55b8d-111">Return value</span></span>

<span data-ttu-id="55b8d-112">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="55b8d-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="55b8d-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="55b8d-113">Requirements</span></span>



| <span data-ttu-id="55b8d-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="55b8d-114">Requirement</span></span> | <span data-ttu-id="55b8d-115">Wert</span><span class="sxs-lookup"><span data-stu-id="55b8d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="55b8d-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="55b8d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="55b8d-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="55b8d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="55b8d-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="55b8d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="55b8d-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="55b8d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="55b8d-120">Header</span><span class="sxs-lookup"><span data-stu-id="55b8d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="55b8d-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="55b8d-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





