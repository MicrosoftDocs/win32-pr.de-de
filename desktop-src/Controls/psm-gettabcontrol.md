---
title: PSM_GETTABCONTROL Meldung (prsht. h)
description: Ruft das Handle für das Registerkarten-Steuerelement eines Eigenschaften Blatts ab. Sie können diese Nachricht explizit oder mithilfe des propsheet \_ gettabcontrol-Makros senden.
ms.assetid: 5ddea541-c8e0-4357-b08e-3b5e64be377f
keywords:
- Windows-Steuerelemente für PSM_GETTABCONTROL Meldung
topic_type:
- apiref
api_name:
- PSM_GETTABCONTROL
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab296159cac4dbfb4ef894d90d31bcd74d6ca2e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518527"
---
# <a name="psm_gettabcontrol-message"></a><span data-ttu-id="e8056-105">PSM \_ gettabcontrol-Meldung</span><span class="sxs-lookup"><span data-stu-id="e8056-105">PSM\_GETTABCONTROL message</span></span>

<span data-ttu-id="e8056-106">Ruft das Handle für das Registerkarten-Steuerelement eines Eigenschaften Blatts ab.</span><span class="sxs-lookup"><span data-stu-id="e8056-106">Retrieves the handle to the tab control of a property sheet.</span></span> <span data-ttu-id="e8056-107">Sie können diese Nachricht explizit oder mithilfe des [**propsheet \_ gettabcontrol**](/windows/desktop/api/Prsht/nf-prsht-propsheet_gettabcontrol) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="e8056-107">You can send this message explicitly or by using the [**PropSheet\_GetTabControl**](/windows/desktop/api/Prsht/nf-prsht-propsheet_gettabcontrol) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e8056-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8056-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8056-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e8056-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e8056-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="e8056-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e8056-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e8056-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e8056-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="e8056-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8056-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e8056-113">Return value</span></span>

<span data-ttu-id="e8056-114">Gibt das Handle für das Registerkarten-Steuerelement zurück.</span><span class="sxs-lookup"><span data-stu-id="e8056-114">Returns the handle to the tab control.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8056-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e8056-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e8056-116">Diese Meldung wird nicht unterstützt, wenn der Aero Wizard Style ([**PSH \_ aerowizard**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e8056-116">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e8056-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8056-117">Requirements</span></span>



| <span data-ttu-id="e8056-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e8056-118">Requirement</span></span> | <span data-ttu-id="e8056-119">Wert</span><span class="sxs-lookup"><span data-stu-id="e8056-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e8056-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e8056-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e8056-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e8056-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e8056-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e8056-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e8056-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e8056-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e8056-124">Header</span><span class="sxs-lookup"><span data-stu-id="e8056-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8056-125"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8056-125"><dt>Prsht.h</dt></span></span> </dl> |



 

 





