---
title: Iwmpwiedergabe InsertItem-Methode
description: Die InsertItem-Methode fügt ein Medien Element an einem angegebenen Speicherort in eine Wiedergabeliste ein.
ms.assetid: 6e472f0a-13df-41d9-8e6f-8430d87fe978
keywords:
- InsertItem-Methode, Windows-Media Player
- InsertItem-Methode, Windows Media Player, iwmpwiedergabe-Schnittstelle
- Iwmpwiedergabe Interface, Windows Media Player, InsertItem-Methode
topic_type:
- apiref
api_name:
- IWMPPlaylist.insertItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1ef167a5f3931f34d4cd6fb91b3d044affb9484
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365561"
---
# <a name="iwmpplaylistinsertitem-method"></a><span data-ttu-id="621d0-106">Iwmpwiedergabe:: InsertItem-Methode</span><span class="sxs-lookup"><span data-stu-id="621d0-106">IWMPPlaylist::insertItem method</span></span>

<span data-ttu-id="621d0-107">Die **InsertItem** -Methode fügt ein Medien Element an einem angegebenen Speicherort in eine Wiedergabeliste ein.</span><span class="sxs-lookup"><span data-stu-id="621d0-107">The **insertItem** method inserts a media item at a specified location in a playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="621d0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="621d0-108">Syntax</span></span>


```CSharp
public void insertItem(
  System.Int32 lIndex,
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub insertItem( _
  ByVal lIndex As System.Int32, _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPPlaylist.insertItem
```





## <a name="parameters"></a><span data-ttu-id="621d0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="621d0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="621d0-110">*Lindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="621d0-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="621d0-111">Ein **System. Int32** , bei dem es sich um den NULL basierten Index handelt, an dem das Medien Element in die Wiedergabeliste eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="621d0-111">A **System.Int32** that is the zero-based index at which the media item will be inserted in the playlist.</span></span>

</dd> <dt>

<span data-ttu-id="621d0-112">*piwmpmedia* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="621d0-112">*pIWMPMedia* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="621d0-113">Eine **WMPLib. iwmpmedia** -Schnittstelle, die das einzufügende Medien Element darstellt.</span><span class="sxs-lookup"><span data-stu-id="621d0-113">A **WMPLib.IWMPMedia** interface that represents the media item to be inserted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="621d0-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="621d0-114">Return value</span></span>

<span data-ttu-id="621d0-115">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="621d0-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="621d0-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="621d0-116">Remarks</span></span>

<span data-ttu-id="621d0-117">Für alle Medienelemente nach dem eingefügten Element werden die Indizes um eins erweitert.</span><span class="sxs-lookup"><span data-stu-id="621d0-117">All media items after the inserted item will have their indexes increased by one.</span></span>

<span data-ttu-id="621d0-118">Vor dem Aufrufen dieser Methode müssen Sie über Vollzugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="621d0-118">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="621d0-119">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="621d0-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="621d0-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="621d0-120">Requirements</span></span>



| <span data-ttu-id="621d0-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="621d0-121">Requirement</span></span> | <span data-ttu-id="621d0-122">Wert</span><span class="sxs-lookup"><span data-stu-id="621d0-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="621d0-123">Version</span><span class="sxs-lookup"><span data-stu-id="621d0-123">Version</span></span><br/>   | <span data-ttu-id="621d0-124">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="621d0-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="621d0-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="621d0-125">Namespace</span></span><br/> | <span data-ttu-id="621d0-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="621d0-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="621d0-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="621d0-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="621d0-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="621d0-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="621d0-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="621d0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="621d0-130">**Iwmpmedia-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="621d0-130">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="621d0-131">**Iwmpwiedergabe-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="621d0-131">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="621d0-132">**Iwmpwiedergabe. RemoveItem (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="621d0-132">**IWMPPlaylist.removeItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)
</dt> </dl>

 

 





