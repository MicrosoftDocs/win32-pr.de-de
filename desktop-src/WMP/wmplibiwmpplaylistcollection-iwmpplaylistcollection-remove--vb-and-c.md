---
title: Iwmpplaylistcollection-Methode entfernen
description: Mit der Remove-Methode wird eine Wiedergabeliste aus der Bibliothek entfernt. | Iwmpplaylistcollection-Methode entfernen
ms.assetid: 40c8ee1d-13fa-40d9-9532-4dc8383c4eb3
keywords:
- Methode "Windows Media Player entfernen"
- Remove-Methode, Windows Media Player, iwmpplaylistcollection-Schnittstelle
- Iwmpplaylistcollection-Schnittstelle, Windows Media Player, Methode entfernen
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.remove
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c99fbaa2f60c769599bd6173b8e38f4d99e9f42d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352177"
---
# <a name="iwmpplaylistcollectionremove-method"></a><span data-ttu-id="e01cd-107">Iwmpplaylistcollection:: Remove-Methode</span><span class="sxs-lookup"><span data-stu-id="e01cd-107">IWMPPlaylistCollection::remove method</span></span>

<span data-ttu-id="e01cd-108">Mit der **Remove** -Methode wird eine Wiedergabeliste aus der Bibliothek entfernt.</span><span class="sxs-lookup"><span data-stu-id="e01cd-108">The **remove** method removes a playlist from the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="e01cd-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e01cd-109">Syntax</span></span>


```CSharp
public void remove(
  IWMPPlaylist pItem
);
```


```VB

Public Sub remove( _
  ByVal pItem As IWMPPlaylist _
)
Implements IWMPPlaylistCollection.remove
```





## <a name="parameters"></a><span data-ttu-id="e01cd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e01cd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e01cd-111">*pitem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e01cd-111">*pItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e01cd-112">Eine **WMPLib. iwmpwiedergabe** -Schnittstelle für die Wiedergabeliste, die von dieser Methode entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="e01cd-112">A **WMPLib.IWMPPlaylist** interface for the playlist that this method will remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e01cd-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e01cd-113">Return value</span></span>

<span data-ttu-id="e01cd-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e01cd-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e01cd-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e01cd-115">Remarks</span></span>

<span data-ttu-id="e01cd-116">Vor dem Aufrufen dieser Methode müssen Sie über Vollzugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="e01cd-116">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="e01cd-117">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="e01cd-117">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e01cd-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e01cd-118">Requirements</span></span>



| <span data-ttu-id="e01cd-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e01cd-119">Requirement</span></span> | <span data-ttu-id="e01cd-120">Wert</span><span class="sxs-lookup"><span data-stu-id="e01cd-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e01cd-121">Version</span><span class="sxs-lookup"><span data-stu-id="e01cd-121">Version</span></span><br/>   | <span data-ttu-id="e01cd-122">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="e01cd-122">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="e01cd-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="e01cd-123">Namespace</span></span><br/> | <span data-ttu-id="e01cd-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="e01cd-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="e01cd-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="e01cd-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e01cd-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e01cd-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e01cd-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e01cd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e01cd-128">**Iwmpwiedergabe-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e01cd-128">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e01cd-129">**Iwmpplaylistcollection-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e01cd-129">**IWMPPlaylistCollection Interface (VB and C#)**</span></span>](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





