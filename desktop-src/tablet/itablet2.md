---
description: Erweitert die iTablet-Schnittstelle.
ms.assetid: dd4f3b2e-7f63-4d5b-b50e-64458719c17a
title: ITablet2-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet2
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: b402695aa278105ad57209f3ff33e66ccaf8c746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363326"
---
# <a name="itablet2-interface"></a><span data-ttu-id="dbac4-103">ITablet2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="dbac4-103">ITablet2 interface</span></span>

<span data-ttu-id="dbac4-104">Erweitert die [**iTablet-Schnittstelle**](itablet.md).</span><span class="sxs-lookup"><span data-stu-id="dbac4-104">Extends the [**ITablet Interface**](itablet.md).</span></span>

## <a name="members"></a><span data-ttu-id="dbac4-105">Member</span><span class="sxs-lookup"><span data-stu-id="dbac4-105">Members</span></span>

<span data-ttu-id="dbac4-106">Die **ITablet2** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="dbac4-106">The **ITablet2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="dbac4-107">**ITablet2** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="dbac4-107">**ITablet2** also has these types of members:</span></span>

-   [<span data-ttu-id="dbac4-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="dbac4-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="dbac4-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="dbac4-109">Methods</span></span>

<span data-ttu-id="dbac4-110">Die **ITablet2** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="dbac4-110">The **ITablet2** interface has these methods.</span></span>



| <span data-ttu-id="dbac4-111">Methode</span><span class="sxs-lookup"><span data-stu-id="dbac4-111">Method</span></span>                                          | <span data-ttu-id="dbac4-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dbac4-112">Description</span></span>                                                                                              |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dbac4-113">**Getdevicekind**</span><span class="sxs-lookup"><span data-stu-id="dbac4-113">**GetDeviceKind**</span></span>](itablet2-getdevicekind.md) | <span data-ttu-id="dbac4-114">Gibt den Typ des Hardware Geräts zurück, das das Tablet-Objekt darstellt, z. b. Maus, Stift oder Fingereingabe</span><span class="sxs-lookup"><span data-stu-id="dbac4-114">Returns the type of hardware device the tablet object represents such as mouse, pen or touch.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dbac4-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dbac4-115">Remarks</span></span>

<span data-ttu-id="dbac4-116">Diese Schnittstelle wurde in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="dbac4-116">This interface was introduced in Windows Vista.</span></span>

<span data-ttu-id="dbac4-117">Entwickler sollten diese Schnittstelle nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="dbac4-117">Developers should not use this interface.</span></span>

<span data-ttu-id="dbac4-118">Im folgenden Code wird beschrieben, wie die **ITablet2** -Schnittstelle definiert wird.</span><span class="sxs-lookup"><span data-stu-id="dbac4-118">The following code describes how the **ITablet2** interface is defined.</span></span>

``` syntax
[
    object,
    uuid(C247F616-BBEB-406A-AED3-F75E656599AE),
    pointer_default(unique)
]
interface ITablet2 : IUnknown
{
    HRESULT GetDeviceKind([out] TABLET_DEVICE_KIND *pKind);

    HRESULT GetMatchingScreenRect([out] RECT *prcInput);
};
```

## <a name="requirements"></a><span data-ttu-id="dbac4-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dbac4-119">Requirements</span></span>



| <span data-ttu-id="dbac4-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dbac4-120">Requirement</span></span> | <span data-ttu-id="dbac4-121">Wert</span><span class="sxs-lookup"><span data-stu-id="dbac4-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbac4-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dbac4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="dbac4-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dbac4-123">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="dbac4-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dbac4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="dbac4-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="dbac4-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="dbac4-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dbac4-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="dbac4-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dbac4-127"><dt>Wisptis.exe</dt></span></span> </dl> |



 

