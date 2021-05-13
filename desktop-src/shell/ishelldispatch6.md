---
description: Erweitert das IShellDispatch5-Objekt.
title: IShellDispatch6-Objekt (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch6
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 540A5CFD-1520-4B61-B461-E893EFA27115
ms.openlocfilehash: de27322324dc8a25bdc679374e625f94a1d1a2ae
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843031"
---
# <a name="ishelldispatch6-object"></a><span data-ttu-id="7129e-103">IShellDispatch6-Objekt</span><span class="sxs-lookup"><span data-stu-id="7129e-103">IShellDispatch6 object</span></span>

<span data-ttu-id="7129e-104">Erweitert das [**IShellDispatch5-Objekt.**](ishelldispatch5.md)</span><span class="sxs-lookup"><span data-stu-id="7129e-104">Extends the [**IShellDispatch5**](ishelldispatch5.md) object.</span></span> <span data-ttu-id="7129e-105">Zusätzlich zu den Eigenschaften und Methoden, die von **IShellDispatch5** unterstützt werden, fügt **IShellDispatch6** eine Methode hinzu, die den Bereich Apps-Suche anzeigt.</span><span class="sxs-lookup"><span data-stu-id="7129e-105">In addition to the properties and methods supported by **IShellDispatch5**, **IShellDispatch6** adds a method that displays the Apps Search pane.</span></span>

> [!Note]  
> <span data-ttu-id="7129e-106">**IShellDispatch6 wird** implementiert und über das [**Shell-Objekt aufgerufen.**](shell.md)</span><span class="sxs-lookup"><span data-stu-id="7129e-106">**IShellDispatch6** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="7129e-107">Member</span><span class="sxs-lookup"><span data-stu-id="7129e-107">Members</span></span>

<span data-ttu-id="7129e-108">Das **IShellDispatch6-Objekt** verfügt über die folgenden Membertypen:</span><span class="sxs-lookup"><span data-stu-id="7129e-108">The **IShellDispatch6** object has these types of members:</span></span>

-   [<span data-ttu-id="7129e-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="7129e-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7129e-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="7129e-110">Methods</span></span>

<span data-ttu-id="7129e-111">Das **IShellDispatch6-Objekt** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="7129e-111">The **IShellDispatch6** object has these methods.</span></span>



| <span data-ttu-id="7129e-112">Methode</span><span class="sxs-lookup"><span data-stu-id="7129e-112">Method</span></span>                                                 | <span data-ttu-id="7129e-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7129e-113">Description</span></span>                                                                                                                  |
|:-------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7129e-114">**SearchCommand**</span><span class="sxs-lookup"><span data-stu-id="7129e-114">**SearchCommand**</span></span>](ishelldispatch6-searchcommand.md) | <span data-ttu-id="7129e-115">Zeigt den Bereich Apps-Suche an, der normalerweise angezeigt wird, wenn Sie beginnen, einen Suchbegriff aus dem Startbildschirm.</span><span class="sxs-lookup"><span data-stu-id="7129e-115">Displays the Apps Search pane, which normally appears when you begin to type a search term from the Start screen.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7129e-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7129e-116">Requirements</span></span>



| <span data-ttu-id="7129e-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7129e-117">Requirement</span></span> | <span data-ttu-id="7129e-118">Wert</span><span class="sxs-lookup"><span data-stu-id="7129e-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7129e-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7129e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7129e-120">Windows 8 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7129e-120">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7129e-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7129e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7129e-122">Nur Windows Server \[ 2012-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7129e-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7129e-123">Header</span><span class="sxs-lookup"><span data-stu-id="7129e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7129e-124"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="7129e-124"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7129e-125">Idl</span><span class="sxs-lookup"><span data-stu-id="7129e-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7129e-126"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="7129e-126"><dt>Shldisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="7129e-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7129e-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7129e-128"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7129e-128"><dt>Shell32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7129e-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7129e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7129e-130">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="7129e-130">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="7129e-131">**Shell-Objekt**</span><span class="sxs-lookup"><span data-stu-id="7129e-131">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="7129e-132">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="7129e-132">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="7129e-133">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="7129e-133">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)
</dt> <dt>

[<span data-ttu-id="7129e-134">**IShellDispatch3**</span><span class="sxs-lookup"><span data-stu-id="7129e-134">**IShellDispatch3**</span></span>](ishelldispatch3.md)
</dt> <dt>

[<span data-ttu-id="7129e-135">**IShellDispatch4**</span><span class="sxs-lookup"><span data-stu-id="7129e-135">**IShellDispatch4**</span></span>](ishelldispatch4.md)
</dt> <dt>

[<span data-ttu-id="7129e-136">**IShellDispatch5**</span><span class="sxs-lookup"><span data-stu-id="7129e-136">**IShellDispatch5**</span></span>](ishelldispatch5.md)
</dt> </dl>

 

 
