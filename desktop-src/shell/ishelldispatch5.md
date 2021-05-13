---
description: Erweitert das IShellDispatch4-Objekt.
title: IShellDispatch5-Objekt (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch5
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9170340a-0f11-4ec9-877d-fb7fef9888b2
ms.openlocfilehash: 26c3112faa748aa443526fbe9cb493af67502cd7
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843001"
---
# <a name="ishelldispatch5-object"></a><span data-ttu-id="cdd6d-103">IShellDispatch5-Objekt</span><span class="sxs-lookup"><span data-stu-id="cdd6d-103">IShellDispatch5 object</span></span>

<span data-ttu-id="cdd6d-104">Erweitert das [**IShellDispatch4-Objekt.**](ishelldispatch4.md)</span><span class="sxs-lookup"><span data-stu-id="cdd6d-104">Extends the [**IShellDispatch4**](ishelldispatch4.md) object.</span></span> <span data-ttu-id="cdd6d-105">Zusätzlich zu den von **IShellDispatch4** unterstützten Eigenschaften und Methoden fügt **IShellDispatch5** eine Methode hinzu, die geöffnete Fenster in einem 3D-Stapel anzeigt.</span><span class="sxs-lookup"><span data-stu-id="cdd6d-105">In addition to the properties and methods supported by **IShellDispatch4**, **IShellDispatch5** adds a method that displays open windows in a 3D stack.</span></span>

> [!Note]  
> <span data-ttu-id="cdd6d-106">**IShellDispatch5** wird implementiert und über das [**Shell-Objekt**](shell.md) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="cdd6d-106">**IShellDispatch5** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="cdd6d-107">Member</span><span class="sxs-lookup"><span data-stu-id="cdd6d-107">Members</span></span>

<span data-ttu-id="cdd6d-108">Das **IShellDispatch5-Objekt** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="cdd6d-108">The **IShellDispatch5** object has these types of members:</span></span>

-   [<span data-ttu-id="cdd6d-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="cdd6d-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cdd6d-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="cdd6d-110">Methods</span></span>

<span data-ttu-id="cdd6d-111">Das **IShellDispatch5-Objekt** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="cdd6d-111">The **IShellDispatch5** object has these methods.</span></span>



| <span data-ttu-id="cdd6d-112">Methode</span><span class="sxs-lookup"><span data-stu-id="cdd6d-112">Method</span></span>                                                   | <span data-ttu-id="cdd6d-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cdd6d-113">Description</span></span>                                                                    |
|:---------------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="cdd6d-114">**WindowSwitcher**</span><span class="sxs-lookup"><span data-stu-id="cdd6d-114">**WindowSwitcher**</span></span>](ishelldispatch5-windowswitcher.md) | <span data-ttu-id="cdd6d-115">Zeigt die geöffneten Fenster in einem 3D-Stapel an, den Sie durchlaufen können.</span><span class="sxs-lookup"><span data-stu-id="cdd6d-115">Displays your open windows in a 3D stack that you can flip through.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cdd6d-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cdd6d-116">Requirements</span></span>



| <span data-ttu-id="cdd6d-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cdd6d-117">Requirement</span></span> | <span data-ttu-id="cdd6d-118">Wert</span><span class="sxs-lookup"><span data-stu-id="cdd6d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdd6d-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cdd6d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cdd6d-120">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cdd6d-120">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="cdd6d-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cdd6d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cdd6d-122">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cdd6d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="cdd6d-123">Header</span><span class="sxs-lookup"><span data-stu-id="cdd6d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdd6d-124"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="cdd6d-124"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="cdd6d-125">Idl</span><span class="sxs-lookup"><span data-stu-id="cdd6d-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cdd6d-126"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="cdd6d-126"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="cdd6d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="cdd6d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cdd6d-128"><dt>Shell32.dll (Version 6.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="cdd6d-128"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdd6d-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cdd6d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdd6d-130">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="cdd6d-130">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="cdd6d-131">**Shell-Objekt**</span><span class="sxs-lookup"><span data-stu-id="cdd6d-131">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="cdd6d-132">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="cdd6d-132">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="cdd6d-133">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="cdd6d-133">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)
</dt> <dt>

[<span data-ttu-id="cdd6d-134">**IShellDispatch3**</span><span class="sxs-lookup"><span data-stu-id="cdd6d-134">**IShellDispatch3**</span></span>](ishelldispatch3.md)
</dt> <dt>

[<span data-ttu-id="cdd6d-135">**IShellDispatch4**</span><span class="sxs-lookup"><span data-stu-id="cdd6d-135">**IShellDispatch4**</span></span>](ishelldispatch4.md)
</dt> </dl>

 

 
