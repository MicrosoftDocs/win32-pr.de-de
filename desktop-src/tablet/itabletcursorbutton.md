---
description: Stellt allgemeine Informationen über eine Schaltfläche auf einem Tablettstiftgerät dar.
ms.assetid: 20c9f8bb-8f8d-4469-baff-b9001c8adb3b
title: Itabletcursor Button-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursorButton
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: c8f13e46699c1bea42bd8f8a7f78313aeba68aaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346868"
---
# <a name="itabletcursorbutton-interface"></a><span data-ttu-id="76f27-103">Itabletcursor Button-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="76f27-103">ITabletCursorButton interface</span></span>

<span data-ttu-id="76f27-104">Stellt allgemeine Informationen über eine Schaltfläche auf einem Tablettstiftgerät dar.</span><span class="sxs-lookup"><span data-stu-id="76f27-104">Represents general information about a button on a stylus device.</span></span>

## <a name="members"></a><span data-ttu-id="76f27-105">Member</span><span class="sxs-lookup"><span data-stu-id="76f27-105">Members</span></span>

<span data-ttu-id="76f27-106">Die **itabletcursor Button** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="76f27-106">The **ITabletCursorButton** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="76f27-107">**Itabletcursor Button** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="76f27-107">**ITabletCursorButton** also has these types of members:</span></span>

-   [<span data-ttu-id="76f27-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="76f27-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="76f27-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="76f27-109">Methods</span></span>

<span data-ttu-id="76f27-110">Die Schnittstelle **itabletcursor Button** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="76f27-110">The **ITabletCursorButton** interface has these methods.</span></span>



| <span data-ttu-id="76f27-111">Methode</span><span class="sxs-lookup"><span data-stu-id="76f27-111">Method</span></span>                                         | <span data-ttu-id="76f27-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="76f27-112">Description</span></span>                                                      |
|:-----------------------------------------------|:-----------------------------------------------------------------|
| [<span data-ttu-id="76f27-113">**GetGuid**</span><span class="sxs-lookup"><span data-stu-id="76f27-113">**GetGuid**</span></span>](itabletcursorbutton-getguid.md) | <span data-ttu-id="76f27-114">Ruft den eindeutigen Bezeichner der Tablettstiftschaltfläche ab.</span><span class="sxs-lookup"><span data-stu-id="76f27-114">Retrieves the unique identifier of the stylus button.</span></span><br/> |
| [<span data-ttu-id="76f27-115">**GetName**</span><span class="sxs-lookup"><span data-stu-id="76f27-115">**GetName**</span></span>](itabletcursorbutton-getname.md) | <span data-ttu-id="76f27-116">Ruft den Namen der Tablettstiftschaltfläche ab.</span><span class="sxs-lookup"><span data-stu-id="76f27-116">Retrieves the name of the stylus button.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="76f27-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76f27-117">Remarks</span></span>

<span data-ttu-id="76f27-118">Entwickler sollten diese Schnittstelle nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="76f27-118">Developers should not use this interface.</span></span>

<span data-ttu-id="76f27-119">Der folgende Code zeigt, wie die **itabletcursor Button** -Schnittstelle definiert wird.</span><span class="sxs-lookup"><span data-stu-id="76f27-119">The following code shows how the **ITabletCursorButton** interface is defined.</span></span>

``` syntax
[
    object,
    uuid(997A992E-8B6C-4945-BC17-A1EE563B3AB7),
    pointer_default(unique)
]
interface ITabletCursorButton : IUnknown
{
    HRESULT GetName(
        [out] LPWSTR *ppwszName);

    HRESULT GetGuid(
        [out] GUID *pguidBtn);
};
```

## <a name="requirements"></a><span data-ttu-id="76f27-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76f27-120">Requirements</span></span>



| <span data-ttu-id="76f27-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76f27-121">Requirement</span></span> | <span data-ttu-id="76f27-122">Wert</span><span class="sxs-lookup"><span data-stu-id="76f27-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="76f27-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="76f27-123">Minimum supported client</span></span><br/> | <span data-ttu-id="76f27-124">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76f27-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="76f27-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="76f27-125">Minimum supported server</span></span><br/> | <span data-ttu-id="76f27-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="76f27-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="76f27-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="76f27-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="76f27-128"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="76f27-128"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76f27-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76f27-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76f27-130">**Itabletcursor Button-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="76f27-130">**ITabletCursorButton Interface**</span></span>](itabletcursorbutton.md)
</dt> </dl>

 

