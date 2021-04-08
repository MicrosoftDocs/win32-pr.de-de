---
title: TB_MAPACCELERATOR Meldung (kommstrg. h)
description: Bestimmt die ID der Schaltfläche, die dem angegebenen Zugriffstasten Zeichen entspricht.
ms.assetid: 724b593d-39af-4301-b721-0332844677b1
keywords:
- Windows-Steuerelemente für TB_MAPACCELERATOR Meldung
topic_type:
- apiref
api_name:
- TB_MAPACCELERATOR
- TB_MAPACCELERATORA
- TB_MAPACCELERATORW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 029584d9e1614a3a135da5ebd3f4f446795fd9ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742657"
---
# <a name="tb_mapaccelerator-message"></a><span data-ttu-id="f1dae-104">TB \_ mapaccelerator-Meldung</span><span class="sxs-lookup"><span data-stu-id="f1dae-104">TB\_MAPACCELERATOR message</span></span>

<span data-ttu-id="f1dae-105">Bestimmt die ID der Schaltfläche, die dem angegebenen Zugriffstasten Zeichen entspricht.</span><span class="sxs-lookup"><span data-stu-id="f1dae-105">Determines the ID of the button that corresponds to the specified accelerator character.</span></span>

## <a name="parameters"></a><span data-ttu-id="f1dae-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1dae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1dae-107">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f1dae-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1dae-108">Das Zugriffstasten Zeichen.</span><span class="sxs-lookup"><span data-stu-id="f1dae-108">The accelerator character.</span></span>

</dd> <dt>

<span data-ttu-id="f1dae-109">*LPARAM* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f1dae-109">*lParam* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1dae-110">Zeiger auf einen **uint**.</span><span class="sxs-lookup"><span data-stu-id="f1dae-110">Pointer to a **UINT**.</span></span> <span data-ttu-id="f1dae-111">Bei erfolgreicher Rückgabe enthält dieser Parameter die ID der Schaltfläche, die über *wParam* als Zugriffstasten verfügt.</span><span class="sxs-lookup"><span data-stu-id="f1dae-111">On return, if successful, this parameter will hold the id of the button that has *wParam* as its accelerator character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1dae-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f1dae-112">Return value</span></span>

<span data-ttu-id="f1dae-113">Gibt einen Wert ungleich 0 (null) zurück, wenn eine der Schaltflächen über *wParam* als Zugriffstaste verfügt, andernfalls 0 (null).</span><span class="sxs-lookup"><span data-stu-id="f1dae-113">Returns a nonzero value if one of the buttons has *wParam* as its accelerator character, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1dae-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f1dae-114">Requirements</span></span>



| <span data-ttu-id="f1dae-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f1dae-115">Requirement</span></span> | <span data-ttu-id="f1dae-116">Wert</span><span class="sxs-lookup"><span data-stu-id="f1dae-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f1dae-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f1dae-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f1dae-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f1dae-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f1dae-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f1dae-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f1dae-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f1dae-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f1dae-121">Header</span><span class="sxs-lookup"><span data-stu-id="f1dae-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1dae-122"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1dae-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="f1dae-123">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="f1dae-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f1dae-124">**TB \_ Mapacceleratorw** (Unicode) und **TB \_ mapacceleratora** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f1dae-124">**TB\_MAPACCELERATORW** (Unicode) and **TB\_MAPACCELERATORA** (ANSI)</span></span><br/>       |



 

 





