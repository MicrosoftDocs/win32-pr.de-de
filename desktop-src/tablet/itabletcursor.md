---
description: Stellt ein tablettstiftobjekt dar.
ms.assetid: c55945b7-59df-49b5-b25f-fa96056889fc
title: Itabletcursor-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: eecbebc7090fb57d3794f3d056c24fba61fa5c61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868683"
---
# <a name="itabletcursor-interface"></a><span data-ttu-id="e1b36-103">Itabletcursor-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="e1b36-103">ITabletCursor interface</span></span>

<span data-ttu-id="e1b36-104">Stellt ein tablettstiftobjekt dar.</span><span class="sxs-lookup"><span data-stu-id="e1b36-104">Represents a stylus object.</span></span>

## <a name="members"></a><span data-ttu-id="e1b36-105">Member</span><span class="sxs-lookup"><span data-stu-id="e1b36-105">Members</span></span>

<span data-ttu-id="e1b36-106">Die **itabletcursor** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e1b36-106">The **ITabletCursor** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e1b36-107">**Itabletcursor** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e1b36-107">**ITabletCursor** also has these types of members:</span></span>

-   [<span data-ttu-id="e1b36-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="e1b36-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e1b36-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="e1b36-109">Methods</span></span>

<span data-ttu-id="e1b36-110">Die **itabletcursor** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="e1b36-110">The **ITabletCursor** interface has these methods.</span></span>



| <span data-ttu-id="e1b36-111">Methode</span><span class="sxs-lookup"><span data-stu-id="e1b36-111">Method</span></span>                                                 | <span data-ttu-id="e1b36-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e1b36-112">Description</span></span>                                                            |
|:-------------------------------------------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="e1b36-113">**Getbutton**</span><span class="sxs-lookup"><span data-stu-id="e1b36-113">**GetButton**</span></span>](itabletcursor-getbutton.md)           | <span data-ttu-id="e1b36-114">Ruft das angegebene Schaltflächen Objekt aus einem Tablet Tablettstift ab.</span><span class="sxs-lookup"><span data-stu-id="e1b36-114">Retrieves the specified button object from a tablet stylus.</span></span><br/> |
| [<span data-ttu-id="e1b36-115">**Getbuttoncount**</span><span class="sxs-lookup"><span data-stu-id="e1b36-115">**GetButtonCount**</span></span>](itabletcursor-getbuttoncount.md) | <span data-ttu-id="e1b36-116">Ruft die Anzahl der Schaltflächen auf dem Tablettstift ab.</span><span class="sxs-lookup"><span data-stu-id="e1b36-116">Retrieves the number of buttons on the tablet stylus.</span></span><br/>       |
| [<span data-ttu-id="e1b36-117">**GetId**</span><span class="sxs-lookup"><span data-stu-id="e1b36-117">**GetId**</span></span>](itabletcursor-getid.md)                   | <span data-ttu-id="e1b36-118">Ruft den tablettstiftbezeichner ab.</span><span class="sxs-lookup"><span data-stu-id="e1b36-118">Retrieves the stylus identifier.</span></span><br/>                            |
| [<span data-ttu-id="e1b36-119">**GetName**</span><span class="sxs-lookup"><span data-stu-id="e1b36-119">**GetName**</span></span>](itabletcursor-getname.md)               | <span data-ttu-id="e1b36-120">Ruft den Namen des Tablettstifts ab.</span><span class="sxs-lookup"><span data-stu-id="e1b36-120">Retrieves the name of the tablet stylus.</span></span><br/>                    |
| [<span data-ttu-id="e1b36-121">**Isinvertierte**</span><span class="sxs-lookup"><span data-stu-id="e1b36-121">**IsInverted**</span></span>](itabletcursor-isinverted.md)         | <span data-ttu-id="e1b36-122">Gibt an, ob der Tablettstift aufwärts unten ist.</span><span class="sxs-lookup"><span data-stu-id="e1b36-122">Indicates if the stylus is upside down.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="e1b36-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e1b36-123">Remarks</span></span>

<span data-ttu-id="e1b36-124">Verwenden Sie diese Schnittstelle nicht.</span><span class="sxs-lookup"><span data-stu-id="e1b36-124">Do not use this interface.</span></span>

<span data-ttu-id="e1b36-125">Im folgenden Code wird beschrieben, wie die **itabletcursor** -Schnittstelle definiert wird.</span><span class="sxs-lookup"><span data-stu-id="e1b36-125">The following code describes how the **ITabletCursor** interface is defined.</span></span>

``` syntax
[
    object,
    uuid(EF9953C6-B472-4B02-9D22-D0E247ADE0E8,
    pointer_default(unique)
]
interface ITabletCursor : IUnknown
{
    HRESULT GetName(
        [out] LPWSTR *ppwszName);

    HRESULT IsInverted();

    HRESULT GetId(
        [out] CURSOR_ID *pCid);

    HRESULT GetTablet(
        [out] ITablet **ppTablet);

    HRESULT GetButtonCount(
        [out] ULONG *pcButtons);

    HRESULT GetButton(
        [in] ULONG iButton,
        [out] ITabletCursorButton **ppButton);
};

     
```

## <a name="requirements"></a><span data-ttu-id="e1b36-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e1b36-126">Requirements</span></span>



| <span data-ttu-id="e1b36-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e1b36-127">Requirement</span></span> | <span data-ttu-id="e1b36-128">Wert</span><span class="sxs-lookup"><span data-stu-id="e1b36-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1b36-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e1b36-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e1b36-130">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e1b36-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e1b36-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e1b36-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e1b36-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e1b36-132">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e1b36-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e1b36-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="e1b36-134"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e1b36-134"><dt>Wisptis.exe</dt></span></span> </dl> |



 

