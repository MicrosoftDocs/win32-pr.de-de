---
title: CCM_SETVERSION Meldung (kommstrg. h)
description: Diese Meldung wird verwendet, um das Steuerelement zu informieren, dass Sie ein Verhalten erwarten, das mit einer bestimmten Version verknüpft ist.
ms.assetid: f87b20bc-0139-4d0a-b38c-32c75743d6f6
keywords:
- Windows-Steuerelemente für CCM_SETVERSION Meldung
topic_type:
- apiref
api_name:
- CCM_SETVERSION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 349935173c41cd9c90a016ef3d2f3c77df8f159c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040770"
---
# <a name="ccm_setversion-message"></a><span data-ttu-id="52c03-104">CCM- \_ setVersion-Meldung</span><span class="sxs-lookup"><span data-stu-id="52c03-104">CCM\_SETVERSION message</span></span>

<span data-ttu-id="52c03-105">Diese Meldung wird verwendet, um das Steuerelement zu informieren, dass Sie ein Verhalten erwarten, das mit einer bestimmten Version verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="52c03-105">This message is used to inform the control that you are expecting a behavior associated with a particular version.</span></span>

## <a name="parameters"></a><span data-ttu-id="52c03-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="52c03-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52c03-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="52c03-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="52c03-108">Die Versionsnummer.</span><span class="sxs-lookup"><span data-stu-id="52c03-108">The version number.</span></span>

</dd> <dt>

<span data-ttu-id="52c03-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="52c03-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="52c03-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="52c03-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52c03-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="52c03-111">Return value</span></span>

<span data-ttu-id="52c03-112">Gibt die in der vorherigen ccm- **\_ setVersion** -Meldung angegebene Version zurück.</span><span class="sxs-lookup"><span data-stu-id="52c03-112">Returns the version specified in the previous **CCM\_SETVERSION** message.</span></span> <span data-ttu-id="52c03-113">Wenn *wParam* auf einen Wert festgelegt ist, der höher als die aktuelle dll-Version ist, wird-1 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="52c03-113">If *wParam* is set to a value greater than the current DLL version, it returns -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="52c03-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52c03-114">Remarks</span></span>

<span data-ttu-id="52c03-115">In einigen Fällen kann sich ein Steuerelement abhängig von der jeweiligen Version anders Verhalten.</span><span class="sxs-lookup"><span data-stu-id="52c03-115">In a few cases, a control may behave differently, depending on the version.</span></span> <span data-ttu-id="52c03-116">Dies gilt hauptsächlich für Fehler, die in späteren Versionen behoben wurden.</span><span class="sxs-lookup"><span data-stu-id="52c03-116">This primarily applies to bugs that were fixed in later versions.</span></span> <span data-ttu-id="52c03-117">Die **ccm- \_ setVersion** -Meldung ermöglicht Ihnen, das Steuerelement zu informieren, welches Verhalten erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="52c03-117">The **CCM\_SETVERSION** message enables you to inform the control which behavior is expected.</span></span> <span data-ttu-id="52c03-118">Sie können ermitteln, welche Version Sie angegeben haben, indem Sie eine [**ccm- \_ GetVersion**](ccm-getversion.md) -Nachricht senden.</span><span class="sxs-lookup"><span data-stu-id="52c03-118">You can determine which version you have specified by sending a [**CCM\_GETVERSION**](ccm-getversion.md) message.</span></span> <span data-ttu-id="52c03-119">Ein Beispiel für die Verwendung dieser Nachricht finden Sie unter [benutzerdefiniertes Zeichnen mit List-View und Tree-View Steuerelementen](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="52c03-119">For an example of how to use this message, see [Custom Draw With List-View and Tree-View Controls](custom-draw.md).</span></span>

<span data-ttu-id="52c03-120">Wenn Sie ComCtl32.dll Version 6 installiert haben, gibt die **ccm- \_ setVersion** -Nachricht unabhängig von dem Wert, den Sie in *wParam* festlegen, Version 6 zurück.</span><span class="sxs-lookup"><span data-stu-id="52c03-120">If you have ComCtl32.dll version 6 installed, regardless of what value you set in *wParam*, the **CCM\_SETVERSION** message returns version 6.</span></span>

> [!Note]  
> <span data-ttu-id="52c03-121">Mit dieser Meldung wird nur die Versionsnummer für das Steuerelement festgelegt, an das das Steuerelement gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="52c03-121">This message only sets the version number for the control to which it is sent.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="52c03-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="52c03-122">Requirements</span></span>



| <span data-ttu-id="52c03-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="52c03-123">Requirement</span></span> | <span data-ttu-id="52c03-124">Wert</span><span class="sxs-lookup"><span data-stu-id="52c03-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="52c03-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="52c03-125">Minimum supported client</span></span><br/> | <span data-ttu-id="52c03-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="52c03-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="52c03-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="52c03-127">Minimum supported server</span></span><br/> | <span data-ttu-id="52c03-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="52c03-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="52c03-129">Header</span><span class="sxs-lookup"><span data-stu-id="52c03-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="52c03-130"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="52c03-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





