---
title: Iwmpplaylistarray-Element Methode
description: Die Item-Methode gibt eine iwmpwiedergabe-Schnittstelle zurück, die die Wiedergabeliste am angegebenen Index darstellt.
ms.assetid: 5cb4b89f-b679-4d92-a5f9-5d0fe686775d
keywords:
- Element-Methoden Fenster Media Player
- Element-Methode, Windows Media Player, iwmpplaylistarray-Schnittstelle
- Iwmpplaylistarray Interface, Windows Media Player, Element-Methode
topic_type:
- apiref
api_name:
- IWMPPlaylistArray.Item
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 660e919ef51bbb9584971f25bdf92296d331de23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354667"
---
# <a name="iwmpplaylistarrayitem-method"></a><span data-ttu-id="e8fac-106">Iwmpplaylistarray:: Item-Methode</span><span class="sxs-lookup"><span data-stu-id="e8fac-106">IWMPPlaylistArray::Item method</span></span>

<span data-ttu-id="e8fac-107">Die **Item** -Methode gibt eine **iwmpwiedergabe** -Schnittstelle zurück, die die Wiedergabeliste am angegebenen Index darstellt.</span><span class="sxs-lookup"><span data-stu-id="e8fac-107">The **Item** method returns an **IWMPPlaylist** interface representing the playlist at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8fac-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8fac-108">Syntax</span></span>


```CSharp
public IWMPPlaylist Item(
  System.Int32 lIndex
);
```


```VB

Public Function Item( _
  ByVal lIndex As System.Int32 _
) As IWMPPlaylist
Implements IWMPPlaylistArray.Item
```





## <a name="parameters"></a><span data-ttu-id="e8fac-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8fac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8fac-110">*Lindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e8fac-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8fac-111">Ein **System. Int32** -Wert, der den Index enthält, der die Wiedergabeliste angibt, die die Methode abrufen soll.</span><span class="sxs-lookup"><span data-stu-id="e8fac-111">A **System.Int32** containing the index that identifies the playlist that the method should retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8fac-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e8fac-112">Return value</span></span>

<span data-ttu-id="e8fac-113">Eine **WMPLib. iwmpwiedergabe** -Schnittstelle für die abgerufene Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="e8fac-113">A **WMPLib.IWMPPlaylist** interface for the retrieved playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8fac-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e8fac-114">Remarks</span></span>

<span data-ttu-id="e8fac-115">Vor dem Aufrufen dieser Methode müssen Sie über Lesezugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="e8fac-115">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="e8fac-116">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="e8fac-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e8fac-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8fac-117">Requirements</span></span>



| <span data-ttu-id="e8fac-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e8fac-118">Requirement</span></span> | <span data-ttu-id="e8fac-119">Wert</span><span class="sxs-lookup"><span data-stu-id="e8fac-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8fac-120">Version</span><span class="sxs-lookup"><span data-stu-id="e8fac-120">Version</span></span><br/>   | <span data-ttu-id="e8fac-121">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="e8fac-121">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="e8fac-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="e8fac-122">Namespace</span></span><br/> | <span data-ttu-id="e8fac-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="e8fac-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="e8fac-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="e8fac-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e8fac-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e8fac-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8fac-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8fac-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8fac-127">**Iwmpwiedergabe-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e8fac-127">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e8fac-128">**Iwmpplaylistarray-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e8fac-128">**IWMPPlaylistArray Interface (VB and C#)**</span></span>](iwmpplaylistarray--vb-and-c.md)
</dt> </dl>

 

 





