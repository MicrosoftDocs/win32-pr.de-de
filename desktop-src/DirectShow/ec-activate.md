---
description: Ein Videofenster wird aktiviert oder deaktiviert.
ms.assetid: 2e004899-bb2b-4127-b606-e2a979275836
title: EC_ACTIVATE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81e48adb3ae98af172664b807386c615d34b6b22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359390"
---
# <a name="ec_activate"></a><span data-ttu-id="166b0-103">Aktivieren von EC \_</span><span class="sxs-lookup"><span data-stu-id="166b0-103">EC\_ACTIVATE</span></span>

<span data-ttu-id="166b0-104">Ein Videofenster wird aktiviert oder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="166b0-104">A video window is being activated or deactivated.</span></span>

## <a name="parameters"></a><span data-ttu-id="166b0-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="166b0-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="166b0-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="166b0-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="166b0-107">(**Bool**) **True** , wenn das Fenster aktiviert ist, oder **false** , wenn das Fenster deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="166b0-107">(**BOOL**) **TRUE** if the window is activated, or **FALSE** if the window is deactivated.</span></span>

</dd> <dt>

<span data-ttu-id="166b0-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="166b0-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="166b0-109">(**IUnknown** \* ) Ein Zeiger auf die [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Schnittstelle des Renderers.</span><span class="sxs-lookup"><span data-stu-id="166b0-109">(**IUnknown**\*) Pointer to the renderer's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="166b0-110">Standardaktion</span><span class="sxs-lookup"><span data-stu-id="166b0-110">Default Action</span></span>

<span data-ttu-id="166b0-111">Der Filter Graph-Manager legt den Fokus über die [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) -Schnittstelle fest.</span><span class="sxs-lookup"><span data-stu-id="166b0-111">The filter graph manager sets the focus, through the [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) interface.</span></span> <span data-ttu-id="166b0-112">Die Ereignis Benachrichtigung wird nicht an die Anwendung gesendet.</span><span class="sxs-lookup"><span data-stu-id="166b0-112">It does not send the event notification to the application.</span></span>

## <a name="remarks"></a><span data-ttu-id="166b0-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="166b0-113">Remarks</span></span>

<span data-ttu-id="166b0-114">Ein Videorenderer sendet dieses Ereignis, wenn das Fenster aktiviert oder deaktiviert wird (d. h., wenn es eine WM \_ activateapp-Nachricht empfängt).</span><span class="sxs-lookup"><span data-stu-id="166b0-114">A video renderer sends this event whenever its window is activated or deactivated (that is, when it receives a WM\_ACTIVATEAPP message).</span></span> <span data-ttu-id="166b0-115">Die Fenster Aktivierung oder-Deaktivierung kann auftreten, da der Fokus im Fenster erreicht oder verloren gegangen ist oder der Renderer zwischen dem Vollbildmodus und dem Fenstermodus gewechselt hat.</span><span class="sxs-lookup"><span data-stu-id="166b0-115">Window activation or deactivation can occur because the window has gained or lost focus, or because the renderer has switched between full-screen mode and windowed mode.</span></span>

<span data-ttu-id="166b0-116">Dieses Ereignis ermöglicht es dem Filter Graph-Manager, Ressourcen zuzuordnen, die von Fenster Fokus abhängen, z. b. Audiogeräte.</span><span class="sxs-lookup"><span data-stu-id="166b0-116">This event enables the filter graph manager to allocate resources that depend on window focus, such as audio devices.</span></span>

## <a name="requirements"></a><span data-ttu-id="166b0-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="166b0-117">Requirements</span></span>



| <span data-ttu-id="166b0-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="166b0-118">Requirement</span></span> | <span data-ttu-id="166b0-119">Wert</span><span class="sxs-lookup"><span data-stu-id="166b0-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="166b0-120">Header</span><span class="sxs-lookup"><span data-stu-id="166b0-120">Header</span></span><br/> | <dl> <span data-ttu-id="166b0-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="166b0-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="166b0-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="166b0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="166b0-123">Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="166b0-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="166b0-124">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="166b0-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




