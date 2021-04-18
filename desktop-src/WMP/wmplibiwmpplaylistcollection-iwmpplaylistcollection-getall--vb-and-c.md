---
title: Iwmpplaylistcollection GetAll-Methode
description: Die GetAll-Methode gibt eine iwmpplaylistarray-Schnittstelle zurück, die Zugriff auf alle Wiedergabelisten in der Bibliothek bietet.
ms.assetid: d36dbc5c-ccb0-400a-ab5b-918598c218f1
keywords:
- GetAll-Methoden Fenster Media Player
- GetAll-Methode, Windows Media Player, iwmpplaylistcollection-Schnittstelle
- Iwmpplaylistcollection-Schnittstelle, Windows Media Player, GetAll-Methode
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.getAll
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4260f5c960650cf6c04a1dd8b39d887f711fb8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371210"
---
# <a name="iwmpplaylistcollectiongetall-method"></a><span data-ttu-id="edd90-106">Iwmpplaylistcollection:: GetAll-Methode</span><span class="sxs-lookup"><span data-stu-id="edd90-106">IWMPPlaylistCollection::getAll method</span></span>

<span data-ttu-id="edd90-107">Die **GetAll** -Methode gibt eine **iwmpplaylistarray** -Schnittstelle zurück, die Zugriff auf alle Wiedergabelisten in der Bibliothek bietet.</span><span class="sxs-lookup"><span data-stu-id="edd90-107">The **getAll** method returns an **IWMPPlaylistArray** interface that provides access to all of the playlists in the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="edd90-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="edd90-108">Syntax</span></span>


```CSharp
public IWMPPlaylistArray getAll();
```


```VB

Public Function getAll() As IWMPPlaylistArray
Implements IWMPPlaylistCollection.getAll
```





## <a name="parameters"></a><span data-ttu-id="edd90-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="edd90-109">Parameters</span></span>

<span data-ttu-id="edd90-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="edd90-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="edd90-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="edd90-111">Return value</span></span>

<span data-ttu-id="edd90-112">Eine **WMPLib. iwmpplaylistarray** -Schnittstelle für das abgerufene Array von Wiedergabelisten.</span><span class="sxs-lookup"><span data-stu-id="edd90-112">A **WMPLib.IWMPPlaylistArray** interface for the retrieved array of playlists.</span></span>

## <a name="remarks"></a><span data-ttu-id="edd90-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="edd90-113">Remarks</span></span>

<span data-ttu-id="edd90-114">Vor dem Aufrufen dieser Methode müssen Sie über Lesezugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="edd90-114">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="edd90-115">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="edd90-115">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="edd90-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="edd90-116">Requirements</span></span>



| <span data-ttu-id="edd90-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="edd90-117">Requirement</span></span> | <span data-ttu-id="edd90-118">Wert</span><span class="sxs-lookup"><span data-stu-id="edd90-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edd90-119">Version</span><span class="sxs-lookup"><span data-stu-id="edd90-119">Version</span></span><br/>   | <span data-ttu-id="edd90-120">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="edd90-120">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="edd90-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="edd90-121">Namespace</span></span><br/> | <span data-ttu-id="edd90-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="edd90-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="edd90-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="edd90-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="edd90-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="edd90-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edd90-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="edd90-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edd90-126">**Iwmpplaylistarray-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="edd90-126">**IWMPPlaylistArray Interface (VB and C#)**</span></span>](iwmpplaylistarray--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="edd90-127">**Iwmpplaylistcollection-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="edd90-127">**IWMPPlaylistCollection Interface (VB and C#)**</span></span>](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





