---
description: Erweitert das IShellDispatch4-Objekt.
title: IShellDispatch5-Objekt (Shldisp. h)
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
ms.openlocfilehash: cbf3e960d7bfb9cd15411142cc036a21a9995ff9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977968"
---
# <a name="ishelldispatch5-object"></a><span data-ttu-id="43cf7-103">IShellDispatch5-Objekt</span><span class="sxs-lookup"><span data-stu-id="43cf7-103">IShellDispatch5 object</span></span>

<span data-ttu-id="43cf7-104">Erweitert das [**IShellDispatch4**](ishelldispatch4.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="43cf7-104">Extends the [**IShellDispatch4**](ishelldispatch4.md) object.</span></span> <span data-ttu-id="43cf7-105">Zusätzlich zu den Eigenschaften und Methoden, die von **IShellDispatch4** unterstützt werden, fügt **IShellDispatch5** eine Methode hinzu, die geöffnete Fenster in einem 3D-Stapel anzeigt.</span><span class="sxs-lookup"><span data-stu-id="43cf7-105">In addition to the properties and methods supported by **IShellDispatch4**, **IShellDispatch5** adds a method that displays open windows in a 3D stack.</span></span>

> [!Note]  
> <span data-ttu-id="43cf7-106">**IShellDispatch5** wird implementiert, und der Zugriff erfolgt über das [**Shellobjekt**](shell.md) .</span><span class="sxs-lookup"><span data-stu-id="43cf7-106">**IShellDispatch5** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="43cf7-107">Member</span><span class="sxs-lookup"><span data-stu-id="43cf7-107">Members</span></span>

<span data-ttu-id="43cf7-108">Das **IShellDispatch5** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="43cf7-108">The **IShellDispatch5** object has these types of members:</span></span>

-   [<span data-ttu-id="43cf7-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="43cf7-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="43cf7-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="43cf7-110">Methods</span></span>

<span data-ttu-id="43cf7-111">Das **IShellDispatch5** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="43cf7-111">The **IShellDispatch5** object has these methods.</span></span>



| <span data-ttu-id="43cf7-112">Methode</span><span class="sxs-lookup"><span data-stu-id="43cf7-112">Method</span></span>                                                   | <span data-ttu-id="43cf7-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="43cf7-113">Description</span></span>                                                                    |
|:---------------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="43cf7-114">**Windowswitcher**</span><span class="sxs-lookup"><span data-stu-id="43cf7-114">**WindowSwitcher**</span></span>](ishelldispatch5-windowswitcher.md) | <span data-ttu-id="43cf7-115">Zeigt die geöffneten Fenster in einem 3D-Stapel an, den Sie durchlaufen können.</span><span class="sxs-lookup"><span data-stu-id="43cf7-115">Displays your open windows in a 3D stack that you can flip through.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="43cf7-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="43cf7-116">Requirements</span></span>



| <span data-ttu-id="43cf7-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="43cf7-117">Requirement</span></span> | <span data-ttu-id="43cf7-118">Wert</span><span class="sxs-lookup"><span data-stu-id="43cf7-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43cf7-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="43cf7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="43cf7-120">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43cf7-120">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="43cf7-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="43cf7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="43cf7-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43cf7-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="43cf7-123">Header</span><span class="sxs-lookup"><span data-stu-id="43cf7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="43cf7-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="43cf7-124"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="43cf7-125">IDL</span><span class="sxs-lookup"><span data-stu-id="43cf7-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="43cf7-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="43cf7-126"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="43cf7-127">DLL</span><span class="sxs-lookup"><span data-stu-id="43cf7-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43cf7-128"><dt>Shell32.dll (Version 6,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="43cf7-128"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43cf7-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="43cf7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43cf7-130">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="43cf7-130">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="43cf7-131">**Shellobjekt**</span><span class="sxs-lookup"><span data-stu-id="43cf7-131">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="43cf7-132">**Ishelldispatch**</span><span class="sxs-lookup"><span data-stu-id="43cf7-132">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="43cf7-133">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="43cf7-133">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)
</dt> <dt>

[<span data-ttu-id="43cf7-134">**IShellDispatch3**</span><span class="sxs-lookup"><span data-stu-id="43cf7-134">**IShellDispatch3**</span></span>](ishelldispatch3.md)
</dt> <dt>

[<span data-ttu-id="43cf7-135">**IShellDispatch4**</span><span class="sxs-lookup"><span data-stu-id="43cf7-135">**IShellDispatch4**</span></span>](ishelldispatch4.md)
</dt> </dl>

 

 
