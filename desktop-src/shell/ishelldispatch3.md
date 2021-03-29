---
description: Erweitert das IShellDispatch2-Objekt.
ms.assetid: 89d0aa4d-844d-497d-82bb-bcc2bcf9c78b
title: IShellDispatch3-Objekt (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch3
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 501b1396bd08ad8fd06f25da9b7030d4ce28d1e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978008"
---
# <a name="ishelldispatch3-object"></a><span data-ttu-id="11739-103">IShellDispatch3-Objekt</span><span class="sxs-lookup"><span data-stu-id="11739-103">IShellDispatch3 object</span></span>

<span data-ttu-id="11739-104">Erweitert das [**IShellDispatch2**](ishelldispatch2-object.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="11739-104">Extends the [**IShellDispatch2**](ishelldispatch2-object.md) object.</span></span> <span data-ttu-id="11739-105">**IShellDispatch3** unterstützt eine neue Methode zusätzlich zu den Eigenschaften und Methoden, die von **IShellDispatch2** unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="11739-105">**IShellDispatch3** supports one new method in addition to the properties and methods supported by **IShellDispatch2**.</span></span>

> [!Note]  
> <span data-ttu-id="11739-106">**IShellDispatch3** wird implementiert, und der Zugriff erfolgt über das [**Shellobjekt**](shell.md) .</span><span class="sxs-lookup"><span data-stu-id="11739-106">**IShellDispatch3** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="11739-107">Member</span><span class="sxs-lookup"><span data-stu-id="11739-107">Members</span></span>

<span data-ttu-id="11739-108">Das **IShellDispatch3** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="11739-108">The **IShellDispatch3** object has these types of members:</span></span>

-   [<span data-ttu-id="11739-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="11739-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="11739-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="11739-110">Methods</span></span>

<span data-ttu-id="11739-111">Das **IShellDispatch3** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="11739-111">The **IShellDispatch3** object has these methods.</span></span>



| <span data-ttu-id="11739-112">Methode</span><span class="sxs-lookup"><span data-stu-id="11739-112">Method</span></span>                                             | <span data-ttu-id="11739-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11739-113">Description</span></span>                                                  |
|:---------------------------------------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="11739-114">**Addtor**</span><span class="sxs-lookup"><span data-stu-id="11739-114">**AddToRecent**</span></span>](ishelldispatch3-addtorecent.md) | <span data-ttu-id="11739-115">Fügt der Liste der zuletzt verwendeten (MRU) eine Datei hinzu.</span><span class="sxs-lookup"><span data-stu-id="11739-115">Adds a file to the most recently used (MRU) list.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="11739-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="11739-116">Remarks</span></span>

<span data-ttu-id="11739-117">Eine Erläuterung der Windows-Dienste finden Sie in der Dokumentation zu [Diensten](../services/services.md) .</span><span class="sxs-lookup"><span data-stu-id="11739-117">For a discussion of Windows services, see the [Services](../services/services.md) documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="11739-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="11739-118">Requirements</span></span>



| <span data-ttu-id="11739-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11739-119">Requirement</span></span> | <span data-ttu-id="11739-120">Wert</span><span class="sxs-lookup"><span data-stu-id="11739-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11739-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="11739-121">Minimum supported client</span></span><br/> | <span data-ttu-id="11739-122">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11739-122">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="11739-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="11739-123">Minimum supported server</span></span><br/> | <span data-ttu-id="11739-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11739-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="11739-125">Header</span><span class="sxs-lookup"><span data-stu-id="11739-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="11739-126"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="11739-126"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="11739-127">IDL</span><span class="sxs-lookup"><span data-stu-id="11739-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="11739-128"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="11739-128"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="11739-129">DLL</span><span class="sxs-lookup"><span data-stu-id="11739-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11739-130"><dt>Shell32.dll (Version 6,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="11739-130"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11739-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="11739-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11739-132">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="11739-132">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="11739-133">**Shellobjekt**</span><span class="sxs-lookup"><span data-stu-id="11739-133">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="11739-134">**Ishelldispatch**</span><span class="sxs-lookup"><span data-stu-id="11739-134">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="11739-135">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="11739-135">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)
</dt> </dl>

 

 
