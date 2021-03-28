---
description: Erweitert das IShellDispatch3-Objekt.
title: IShellDispatch4-Objekt (Shldisp. h)
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
ms.openlocfilehash: 0bdada12a48f9c48749b614e6b45ff5427e62b4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527323"
---
# <a name="ishelldispatch4-object"></a><span data-ttu-id="2511d-103">IShellDispatch4-Objekt</span><span class="sxs-lookup"><span data-stu-id="2511d-103">IShellDispatch4 object</span></span>

<span data-ttu-id="2511d-104">Erweitert das [**IShellDispatch3**](ishelldispatch3.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="2511d-104">Extends the [**IShellDispatch3**](ishelldispatch3.md) object.</span></span> <span data-ttu-id="2511d-105">Zusätzlich zu den Eigenschaften und Methoden, die von **IShellDispatch3** unterstützt werden, unterstützt **IShellDispatch4** vier zusätzliche Methoden.</span><span class="sxs-lookup"><span data-stu-id="2511d-105">In addition to the properties and methods supported by **IShellDispatch3**, **IShellDispatch4** supports four additional methods.</span></span>

> [!Note]  
> <span data-ttu-id="2511d-106">**IShellDispatch4** wird implementiert, und der Zugriff erfolgt über das [**Shellobjekt**](shell.md) .</span><span class="sxs-lookup"><span data-stu-id="2511d-106">**IShellDispatch4** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="2511d-107">Member</span><span class="sxs-lookup"><span data-stu-id="2511d-107">Members</span></span>

<span data-ttu-id="2511d-108">Das **IShellDispatch4** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2511d-108">The **IShellDispatch4** object has these types of members:</span></span>

-   [<span data-ttu-id="2511d-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="2511d-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2511d-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="2511d-110">Methods</span></span>

<span data-ttu-id="2511d-111">Das **IShellDispatch4** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="2511d-111">The **IShellDispatch4** object has these methods.</span></span>



| <span data-ttu-id="2511d-112">Methode</span><span class="sxs-lookup"><span data-stu-id="2511d-112">Method</span></span>                                                     | <span data-ttu-id="2511d-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2511d-113">Description</span></span>                                                         |
|:-----------------------------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="2511d-114">**Explorerpolicy**</span><span class="sxs-lookup"><span data-stu-id="2511d-114">**ExplorerPolicy**</span></span>](ishelldispatch4-explorerpolicy.md)   | <span data-ttu-id="2511d-115">Ruft den Wert für eine angegebene Internet Explorer-Richtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="2511d-115">Gets the value for a specified Internet Explorer policy.</span></span><br/> |
| [<span data-ttu-id="2511d-116">**GetSetting**</span><span class="sxs-lookup"><span data-stu-id="2511d-116">**GetSetting**</span></span>](ishelldispatch4-getsetting.md)           | <span data-ttu-id="2511d-117">Ruft eine globale shelleinstellung ab.</span><span class="sxs-lookup"><span data-stu-id="2511d-117">Retrieves a global Shell setting.</span></span><br/>                        |
| [<span data-ttu-id="2511d-118">**ToggleDesktop**</span><span class="sxs-lookup"><span data-stu-id="2511d-118">**ToggleDesktop**</span></span>](ishelldispatch4-toggledesktop.md)     | <span data-ttu-id="2511d-119">Zeigt den Desktop an oder blendet ihn aus.</span><span class="sxs-lookup"><span data-stu-id="2511d-119">Displays or hides the desktop.</span></span><br/>                           |
| [<span data-ttu-id="2511d-120">**WindowsSecurity**</span><span class="sxs-lookup"><span data-stu-id="2511d-120">**WindowsSecurity**</span></span>](ishelldispatch4-windowssecurity.md) | <span data-ttu-id="2511d-121">Zeigt das Dialogfeld **Windows-Sicherheit** an.</span><span class="sxs-lookup"><span data-stu-id="2511d-121">Displays the **Windows Security** dialog box.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="2511d-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2511d-122">Remarks</span></span>

<span data-ttu-id="2511d-123">Eine Erläuterung der Windows-Dienste finden Sie in der Dokumentation zu [Diensten](../services/services.md) .</span><span class="sxs-lookup"><span data-stu-id="2511d-123">For a discussion of Windows services, see the [Services](../services/services.md) documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="2511d-124">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="2511d-124">Requirements</span></span>



| <span data-ttu-id="2511d-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2511d-125">Requirement</span></span> | <span data-ttu-id="2511d-126">Wert</span><span class="sxs-lookup"><span data-stu-id="2511d-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2511d-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2511d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2511d-128">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2511d-128">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="2511d-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2511d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2511d-130">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2511d-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="2511d-131">Header</span><span class="sxs-lookup"><span data-stu-id="2511d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="2511d-132"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2511d-132"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="2511d-133">IDL</span><span class="sxs-lookup"><span data-stu-id="2511d-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2511d-134"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2511d-134"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="2511d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="2511d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2511d-136"><dt>Shell32.dll (Version 6,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="2511d-136"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2511d-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2511d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2511d-138">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="2511d-138">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="2511d-139">**Shellobjekt**</span><span class="sxs-lookup"><span data-stu-id="2511d-139">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="2511d-140">**Ishelldispatch**</span><span class="sxs-lookup"><span data-stu-id="2511d-140">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="2511d-141">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="2511d-141">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)
</dt> <dt>

[<span data-ttu-id="2511d-142">**IShellDispatch3**</span><span class="sxs-lookup"><span data-stu-id="2511d-142">**IShellDispatch3**</span></span>](ishelldispatch3.md)
</dt> </dl>

 

 
