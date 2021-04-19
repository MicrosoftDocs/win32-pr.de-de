---
description: Die ITablet3-Schnittstelle ermöglicht multifingerabfragen für Eingaben.
ms.assetid: 949f2d83-7761-4d60-b8fe-5a9ac7567238
title: ITablet3-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: f37d70888ccedf0fe941f0387c064aba37dc287e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360816"
---
# <a name="itablet3-interface"></a><span data-ttu-id="44084-103">ITablet3-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="44084-103">ITablet3 interface</span></span>

<span data-ttu-id="44084-104">Die ITablet3-Schnittstelle ermöglicht multifingerabfragen für Eingaben.</span><span class="sxs-lookup"><span data-stu-id="44084-104">The ITablet3 interface enables multitouch querying for input.</span></span>

## <a name="members"></a><span data-ttu-id="44084-105">Member</span><span class="sxs-lookup"><span data-stu-id="44084-105">Members</span></span>

<span data-ttu-id="44084-106">Die **ITablet3** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="44084-106">The **ITablet3** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="44084-107">**ITablet3** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="44084-107">**ITablet3** also has these types of members:</span></span>

-   [<span data-ttu-id="44084-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="44084-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="44084-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="44084-109">Methods</span></span>

<span data-ttu-id="44084-110">Die **ITablet3** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="44084-110">The **ITablet3** interface has these methods.</span></span>



| <span data-ttu-id="44084-111">Methode</span><span class="sxs-lookup"><span data-stu-id="44084-111">Method</span></span>                                                  | <span data-ttu-id="44084-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="44084-112">Description</span></span>                                                         |
|:--------------------------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="44084-113">**Getmaximumcursors**</span><span class="sxs-lookup"><span data-stu-id="44084-113">**GetMaximumCursors**</span></span>](itablet3-getmaximumcursors.md) | <span data-ttu-id="44084-114">Ruft die maximal unterstützte Anzahl von Eingaben ab.</span><span class="sxs-lookup"><span data-stu-id="44084-114">Retrieves the maximum number of inputs supported.</span></span><br/>        |
| [<span data-ttu-id="44084-115">**ismultiberühren**</span><span class="sxs-lookup"><span data-stu-id="44084-115">**isMultiTouch**</span></span>](itablet3-ismultitouch.md)           | <span data-ttu-id="44084-116">Gibt an, ob multiberühren für dieses Objekt aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="44084-116">Indicates whether multitouch is enabled for this object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="44084-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="44084-117">Remarks</span></span>

<span data-ttu-id="44084-118">Entwickler sollten diese Schnittstelle nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="44084-118">Developers should not use this interface</span></span>

<span data-ttu-id="44084-119">Im folgenden Code wird beschrieben, wie die **ITablet3** -Schnittstelle definiert wird.</span><span class="sxs-lookup"><span data-stu-id="44084-119">The following code describes how the **ITablet3** interface is defined.</span></span>

``` syntax
[
  object,
  uuid(AC0E3951-0A2F-448E-88D0-49DA0C453460)
  pointer_default(unique)
]
interface ITablet3 : IUnknown
{
    HRESULT IsMultiTouch([out] BOOL *pIsMultiTouch);

    HRESULT GetMaximumCursors([out] ULONG *pMaximumCursors);
};
  
```

## <a name="requirements"></a><span data-ttu-id="44084-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44084-120">Requirements</span></span>



| <span data-ttu-id="44084-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="44084-121">Requirement</span></span> | <span data-ttu-id="44084-122">Wert</span><span class="sxs-lookup"><span data-stu-id="44084-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="44084-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="44084-123">Minimum supported client</span></span><br/> | <span data-ttu-id="44084-124">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="44084-124">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="44084-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="44084-125">Minimum supported server</span></span><br/> | <span data-ttu-id="44084-126">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="44084-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="44084-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="44084-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="44084-128"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="44084-128"><dt>Wisptis.exe</dt></span></span> </dl> |



 

