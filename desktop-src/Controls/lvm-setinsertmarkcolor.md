---
title: LVM_SETINSERTMARKCOLOR Meldung (kommstrg. h)
description: Legt die Farbe der Einfügemarke fest.
ms.assetid: dce2c266-672b-4682-ba23-51d9a8e1102b
keywords:
- Windows-Steuerelemente für LVM_SETINSERTMARKCOLOR Meldung
topic_type:
- apiref
api_name:
- LVM_SETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 260d21d083e2c70d8e82a27628e42596bd1b37eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949419"
---
# <a name="lvm_setinsertmarkcolor-message"></a><span data-ttu-id="0b85c-104">LVM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="0b85c-104">LVM\_SETINSERTMARKCOLOR message</span></span>

<span data-ttu-id="0b85c-105">Legt die Farbe der Einfügemarke fest.</span><span class="sxs-lookup"><span data-stu-id="0b85c-105">Sets the color of the insertion point.</span></span>

## <a name="parameters"></a><span data-ttu-id="0b85c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b85c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b85c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0b85c-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0b85c-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="0b85c-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0b85c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0b85c-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0b85c-110">**COLORREF** -Struktur, die die Farbe zum Festlegen der Einfügemarke angibt.</span><span class="sxs-lookup"><span data-stu-id="0b85c-110">**COLORREF** structure that specifies the color to set the insertion point.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b85c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0b85c-111">Return value</span></span>

<span data-ttu-id="0b85c-112">Gibt die auf die vorherige Farbe festgelegte **COLORREF** -Struktur zurück.</span><span class="sxs-lookup"><span data-stu-id="0b85c-112">Returns **COLORREF** structure set to the previous color.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b85c-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b85c-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0b85c-114">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="0b85c-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="0b85c-115">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0b85c-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0b85c-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b85c-116">Requirements</span></span>



| <span data-ttu-id="0b85c-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0b85c-117">Requirement</span></span> | <span data-ttu-id="0b85c-118">Wert</span><span class="sxs-lookup"><span data-stu-id="0b85c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0b85c-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0b85c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0b85c-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0b85c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0b85c-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0b85c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0b85c-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0b85c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0b85c-123">Header</span><span class="sxs-lookup"><span data-stu-id="0b85c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b85c-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b85c-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





