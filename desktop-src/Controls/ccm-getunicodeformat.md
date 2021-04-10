---
title: CCM_GETUNICODEFORMAT Meldung (kommstrg. h)
description: Ruft das Unicode-Zeichenformat Flag für das-Steuerelement ab.
ms.assetid: 8a23cd1c-549e-4d48-891a-b37dbf5c524b
keywords:
- Windows-Steuerelemente für CCM_GETUNICODEFORMAT Meldung
topic_type:
- apiref
api_name:
- CCM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 095d49ccc57faa05e86d12df130b12ce3d542bf6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104516"
---
# <a name="ccm_getunicodeformat-message"></a><span data-ttu-id="ce9e8-104">CCM \_ getunicodeformat-Meldung</span><span class="sxs-lookup"><span data-stu-id="ce9e8-104">CCM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="ce9e8-105">Ruft das Unicode-Zeichenformat Flag für das-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="ce9e8-105">Gets the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ce9e8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce9e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce9e8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ce9e8-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ce9e8-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="ce9e8-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ce9e8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ce9e8-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ce9e8-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="ce9e8-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce9e8-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ce9e8-111">Return value</span></span>

<span data-ttu-id="ce9e8-112">Gibt das Unicode-formatflag für das-Steuerelement zurück.</span><span class="sxs-lookup"><span data-stu-id="ce9e8-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="ce9e8-113">Wenn dieser Wert ungleich 0 (null) ist, verwendet das Steuerelement Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="ce9e8-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="ce9e8-114">Wenn dieser Wert 0 (null) ist, verwendet das Steuerelement ANSI-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="ce9e8-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce9e8-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce9e8-115">Requirements</span></span>



| <span data-ttu-id="ce9e8-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce9e8-116">Requirement</span></span> | <span data-ttu-id="ce9e8-117">Wert</span><span class="sxs-lookup"><span data-stu-id="ce9e8-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ce9e8-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ce9e8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ce9e8-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce9e8-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ce9e8-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ce9e8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ce9e8-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce9e8-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ce9e8-122">Header</span><span class="sxs-lookup"><span data-stu-id="ce9e8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce9e8-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce9e8-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce9e8-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce9e8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce9e8-125">**CCM- \_ Code Format**</span><span class="sxs-lookup"><span data-stu-id="ce9e8-125">**CCM\_SETUNICODEFORMAT**</span></span>](ccm-setunicodeformat.md)
</dt> </dl>

 

 





