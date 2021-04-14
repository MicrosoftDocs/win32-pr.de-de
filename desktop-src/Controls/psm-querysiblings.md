---
title: PSM_QUERYSIBLINGS Meldung (prsht. h)
description: Wird an ein Eigenschaften Blatt gesendet, das die Nachricht dann an jede Ihrer Seiten weiterleitet. Sie können diese Nachricht explizit oder mithilfe des propsheet \_ querysiblings-Makros senden.
ms.assetid: 96f48847-b7b8-4d6f-8bde-ada915b7c962
keywords:
- Windows-Steuerelemente für PSM_QUERYSIBLINGS Meldung
topic_type:
- apiref
api_name:
- PSM_QUERYSIBLINGS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea5943fefa906475e34d1cc7acc7f8a86cd99252
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517966"
---
# <a name="psm_querysiblings-message"></a><span data-ttu-id="a1622-105">PSM- \_ querysiblings-Meldung</span><span class="sxs-lookup"><span data-stu-id="a1622-105">PSM\_QUERYSIBLINGS message</span></span>

<span data-ttu-id="a1622-106">Wird an ein Eigenschaften Blatt gesendet, das die Nachricht dann an jede Ihrer Seiten weiterleitet.</span><span class="sxs-lookup"><span data-stu-id="a1622-106">Sent to a property sheet, which then forwards the message to each of its pages.</span></span> <span data-ttu-id="a1622-107">Sie können diese Nachricht explizit oder mithilfe des [**propsheet \_ querysiblings**](/windows/desktop/api/Prsht/nf-prsht-propsheet_querysiblings) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="a1622-107">You can send this message explicitly or by using the [**PropSheet\_QuerySiblings**](/windows/desktop/api/Prsht/nf-prsht-propsheet_querysiblings) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a1622-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1622-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1622-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a1622-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a1622-110">Der erste Anwendungs definierte Parameter.</span><span class="sxs-lookup"><span data-stu-id="a1622-110">First application-defined parameter.</span></span>

</dd> <dt>

<span data-ttu-id="a1622-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a1622-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a1622-112">Der zweite Anwendungs definierte Parameter.</span><span class="sxs-lookup"><span data-stu-id="a1622-112">Second application-defined parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1622-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a1622-113">Return value</span></span>

<span data-ttu-id="a1622-114">Gibt den Wert ungleich 0 (null) von einer Seite im Eigenschaften Blatt zurück, oder NULL, wenn keine Seite einen Wert ungleich 0 (null) zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="a1622-114">Returns the nonzero value from a page in the property sheet, or zero if no page returns a nonzero value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1622-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a1622-115">Remarks</span></span>

<span data-ttu-id="a1622-116">Wenn eine Seite einen Wert ungleich 0 (null) zurückgibt, sendet das Eigenschaften Blatt die Nachricht nicht an nachfolgende Seiten.</span><span class="sxs-lookup"><span data-stu-id="a1622-116">If a page returns a nonzero value, the property sheet does not send the message to subsequent pages.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1622-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a1622-117">Requirements</span></span>



| <span data-ttu-id="a1622-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a1622-118">Requirement</span></span> | <span data-ttu-id="a1622-119">Wert</span><span class="sxs-lookup"><span data-stu-id="a1622-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a1622-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a1622-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a1622-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a1622-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a1622-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a1622-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a1622-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a1622-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a1622-124">Header</span><span class="sxs-lookup"><span data-stu-id="a1622-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1622-125"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1622-125"><dt>Prsht.h</dt></span></span> </dl> |



 

 





