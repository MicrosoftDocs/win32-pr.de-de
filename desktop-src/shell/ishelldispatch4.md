---
description: Erweitert das IShellDispatch3-Objekt.
title: IShellDispatch4-Objekt (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 4fe37e38-ee71-41f0-b620-35fdc18f9dbb
ms.openlocfilehash: daec9c922a0bac05154c1108f236ddf336a2e380
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843061"
---
# <a name="ishelldispatch4-object"></a><span data-ttu-id="8d203-103">IShellDispatch4-Objekt</span><span class="sxs-lookup"><span data-stu-id="8d203-103">IShellDispatch4 object</span></span>

<span data-ttu-id="8d203-104">Erweitert das [**IShellDispatch3-Objekt.**](ishelldispatch3.md)</span><span class="sxs-lookup"><span data-stu-id="8d203-104">Extends the [**IShellDispatch3**](ishelldispatch3.md) object.</span></span> <span data-ttu-id="8d203-105">Zusätzlich zu den Eigenschaften und Methoden, die von **IShellDispatch3** unterstützt werden, unterstützt **IShellDispatch4** vier zusätzliche Methoden.</span><span class="sxs-lookup"><span data-stu-id="8d203-105">In addition to the properties and methods supported by **IShellDispatch3**, **IShellDispatch4** supports four additional methods.</span></span>

> [!Note]  
> <span data-ttu-id="8d203-106">**IShellDispatch4 wird** implementiert und über das [**Shell-Objekt aufgerufen.**](shell.md)</span><span class="sxs-lookup"><span data-stu-id="8d203-106">**IShellDispatch4** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="8d203-107">Member</span><span class="sxs-lookup"><span data-stu-id="8d203-107">Members</span></span>

<span data-ttu-id="8d203-108">Das **IShellDispatch4-Objekt** verfügt über die folgenden Membertypen:</span><span class="sxs-lookup"><span data-stu-id="8d203-108">The **IShellDispatch4** object has these types of members:</span></span>

-   [<span data-ttu-id="8d203-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="8d203-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8d203-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="8d203-110">Methods</span></span>

<span data-ttu-id="8d203-111">Das **IShellDispatch4-Objekt** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="8d203-111">The **IShellDispatch4** object has these methods.</span></span>



| <span data-ttu-id="8d203-112">Methode</span><span class="sxs-lookup"><span data-stu-id="8d203-112">Method</span></span>                                                     | <span data-ttu-id="8d203-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8d203-113">Description</span></span>                                                         |
|:-----------------------------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="8d203-114">**ExplorerPolicy**</span><span class="sxs-lookup"><span data-stu-id="8d203-114">**ExplorerPolicy**</span></span>](ishelldispatch4-explorerpolicy.md)   | <span data-ttu-id="8d203-115">Ruft den Wert für eine angegebene Internet Explorer ab.</span><span class="sxs-lookup"><span data-stu-id="8d203-115">Gets the value for a specified Internet Explorer policy.</span></span><br/> |
| [<span data-ttu-id="8d203-116">**Getsetting**</span><span class="sxs-lookup"><span data-stu-id="8d203-116">**GetSetting**</span></span>](ishelldispatch4-getsetting.md)           | <span data-ttu-id="8d203-117">Ruft eine globale Shelleinstellung ab.</span><span class="sxs-lookup"><span data-stu-id="8d203-117">Retrieves a global Shell setting.</span></span><br/>                        |
| [<span data-ttu-id="8d203-118">**ToggleDesktop**</span><span class="sxs-lookup"><span data-stu-id="8d203-118">**ToggleDesktop**</span></span>](ishelldispatch4-toggledesktop.md)     | <span data-ttu-id="8d203-119">Zeigt den Desktop an oder blendet den Desktop aus.</span><span class="sxs-lookup"><span data-stu-id="8d203-119">Displays or hides the desktop.</span></span><br/>                           |
| [<span data-ttu-id="8d203-120">**WindowsSecurity**</span><span class="sxs-lookup"><span data-stu-id="8d203-120">**WindowsSecurity**</span></span>](ishelldispatch4-windowssecurity.md) | <span data-ttu-id="8d203-121">Zeigt das **Windows-Sicherheit** An.</span><span class="sxs-lookup"><span data-stu-id="8d203-121">Displays the **Windows Security** dialog box.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="8d203-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8d203-122">Remarks</span></span>

<span data-ttu-id="8d203-123">Eine Erörterung der Windows-Dienste finden Sie in der [Dokumentation zu Diensten.](../services/services.md)</span><span class="sxs-lookup"><span data-stu-id="8d203-123">For a discussion of Windows services, see the [Services](../services/services.md) documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d203-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8d203-124">Requirements</span></span>



| <span data-ttu-id="8d203-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8d203-125">Requirement</span></span> | <span data-ttu-id="8d203-126">Wert</span><span class="sxs-lookup"><span data-stu-id="8d203-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d203-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8d203-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8d203-128">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8d203-128">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="8d203-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8d203-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8d203-130">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8d203-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="8d203-131">Header</span><span class="sxs-lookup"><span data-stu-id="8d203-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d203-132"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="8d203-132"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="8d203-133">Idl</span><span class="sxs-lookup"><span data-stu-id="8d203-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8d203-134"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="8d203-134"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="8d203-135">DLL</span><span class="sxs-lookup"><span data-stu-id="8d203-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d203-136"><dt>Shell32.dll (Version 6.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="8d203-136"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d203-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d203-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d203-138">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="8d203-138">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="8d203-139">**Shell-Objekt**</span><span class="sxs-lookup"><span data-stu-id="8d203-139">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="8d203-140">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="8d203-140">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="8d203-141">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="8d203-141">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)
</dt> <dt>

[<span data-ttu-id="8d203-142">**IShellDispatch3**</span><span class="sxs-lookup"><span data-stu-id="8d203-142">**IShellDispatch3**</span></span>](ishelldispatch3.md)
</dt> </dl>

 

 
