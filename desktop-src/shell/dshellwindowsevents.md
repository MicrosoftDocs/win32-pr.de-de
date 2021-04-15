---
description: Empfängt IShellWindows-Fenster Registrierungs Ereignisse.
ms.assetid: c340296d-f8eb-43a1-809d-912ea7412fe2
title: Dshellwindowsevents-Objekt (Exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DShellWindowsEvents
api_type:
- COM
api_location:
- Shdocvw.dll
ms.openlocfilehash: 7df1571556b5f2942f181b4c88b22ff3bc83f273
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "104983013"
---
# <a name="dshellwindowsevents-object"></a><span data-ttu-id="6d452-103">Dshellwindowsevents-Objekt</span><span class="sxs-lookup"><span data-stu-id="6d452-103">DShellWindowsEvents object</span></span>

<span data-ttu-id="6d452-104">Empfängt [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) -Fenster Registrierungs Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="6d452-104">Receives [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) window registration events.</span></span>

## <a name="members"></a><span data-ttu-id="6d452-105">Member</span><span class="sxs-lookup"><span data-stu-id="6d452-105">Members</span></span>

<span data-ttu-id="6d452-106">Das **dshellwindowsevents** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6d452-106">The **DShellWindowsEvents** object has these types of members:</span></span>

-   [<span data-ttu-id="6d452-107">Methoden</span><span class="sxs-lookup"><span data-stu-id="6d452-107">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6d452-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="6d452-108">Methods</span></span>

<span data-ttu-id="6d452-109">Das **dshellwindowsevents** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="6d452-109">The **DShellWindowsEvents** object has these methods.</span></span>



| <span data-ttu-id="6d452-110">Methode</span><span class="sxs-lookup"><span data-stu-id="6d452-110">Method</span></span>                                                           | <span data-ttu-id="6d452-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6d452-111">Description</span></span>                                                       |
|:-----------------------------------------------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="6d452-112">**Windowregistered**</span><span class="sxs-lookup"><span data-stu-id="6d452-112">**WindowRegistered**</span></span>](dshellwindowsevents-windowregistered.md) | <span data-ttu-id="6d452-113">Wird aufgerufen, wenn ein Fenster als Shellfenster registriert wird.</span><span class="sxs-lookup"><span data-stu-id="6d452-113">Called when a window is registered as a Shell window.</span></span> <br/> |
| [<span data-ttu-id="6d452-114">**Windows-gesperrt**</span><span class="sxs-lookup"><span data-stu-id="6d452-114">**WindowRevoked**</span></span>](dshellwindowsevents-windowrevoked.md)       | <span data-ttu-id="6d452-115">Wird aufgerufen, wenn die Registrierung eines shellfensters widerrufen wird.</span><span class="sxs-lookup"><span data-stu-id="6d452-115">Called when a Shell window's registration is revoked.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="6d452-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d452-116">Remarks</span></span>

<span data-ttu-id="6d452-117">Verwenden Sie **dshellwindowsvents** , um zu überwachen, wann ein Shellfenster registriert oder widerrufen wird.</span><span class="sxs-lookup"><span data-stu-id="6d452-117">Use **DShellWindowsEvents** to monitor when a Shell window is registered or revoked.</span></span> <span data-ttu-id="6d452-118">Weitere Informationen finden Sie unter [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows).</span><span class="sxs-lookup"><span data-stu-id="6d452-118">For more information, see [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows).</span></span>

## <a name="requirements"></a><span data-ttu-id="6d452-119">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="6d452-119">Requirements</span></span>



| <span data-ttu-id="6d452-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6d452-120">Requirement</span></span> | <span data-ttu-id="6d452-121">Wert</span><span class="sxs-lookup"><span data-stu-id="6d452-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d452-122">Produkt</span><span class="sxs-lookup"><span data-stu-id="6d452-122">Product</span></span><br/> | <span data-ttu-id="6d452-123">Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="6d452-123">Internet Explorer 5</span></span><br/>                                                                                           |
| <span data-ttu-id="6d452-124">Header</span><span class="sxs-lookup"><span data-stu-id="6d452-124">Header</span></span><br/>  | <dl> <span data-ttu-id="6d452-125"><dt>Exdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d452-125"><dt>Exdisp.h</dt></span></span> </dl>                                      |
| <span data-ttu-id="6d452-126">DLL</span><span class="sxs-lookup"><span data-stu-id="6d452-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="6d452-127"><dt>Shdocvw.dll (Version 5.00.2014.0216 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="6d452-127"><dt>Shdocvw.dll (version 5.00.2014.0216 or later)</dt></span></span> </dl> |
| <span data-ttu-id="6d452-128">IID</span><span class="sxs-lookup"><span data-stu-id="6d452-128">IID</span></span><br/>     | <span data-ttu-id="6d452-129">IID \_ IShellWindows</span><span class="sxs-lookup"><span data-stu-id="6d452-129">IID\_IShellWindows</span></span><br/>                                                                                            |



## <a name="see-also"></a><span data-ttu-id="6d452-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6d452-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d452-131">**Shellwindows**</span><span class="sxs-lookup"><span data-stu-id="6d452-131">**ShellWindows**</span></span>](shellwindows.md)
</dt> </dl>

 

 




