---
title: Iwmpmedia getiteminfobyatom-Methode
description: Die getiteminfobyatom-Methode gibt den Wert des Attributs mit der angegebenen Indexnummer zurück.
ms.assetid: d9a4b737-add1-4bbd-8e03-e58f45d65a62
keywords:
- getiteminfobyatom-Methode, Windows Media Player
- getiteminfobyatom-Methode, Windows Media Player, iwmpmedia-Schnittstelle
- Iwmpmedia Interface, Windows Media Player, getiteminfobyatom-Methode
topic_type:
- apiref
api_name:
- IWMPMedia.getItemInfoByAtom
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb37243960360120fbfe508a39db31e37728ac39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371519"
---
# <a name="iwmpmediagetiteminfobyatom-method"></a><span data-ttu-id="c7e52-106">Iwmpmedia:: getiteminfobyatom-Methode</span><span class="sxs-lookup"><span data-stu-id="c7e52-106">IWMPMedia::getItemInfoByAtom method</span></span>

<span data-ttu-id="c7e52-107">Die **getiteminfobyatom** -Methode gibt den Wert des Attributs mit der angegebenen Indexnummer zurück.</span><span class="sxs-lookup"><span data-stu-id="c7e52-107">The **getItemInfoByAtom** method returns the value of the attribute with the specified index number.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7e52-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7e52-108">Syntax</span></span>


```CSharp
public System.String getItemInfoByAtom(
  System.Int32 lAtom
);
```


```VB

Public Function getItemInfoByAtom( _
  ByVal lAtom As System.Int32 _
) As System.String
Implements IWMPMedia.getItemInfoByAtom
```





## <a name="parameters"></a><span data-ttu-id="c7e52-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7e52-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7e52-110">*latom* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7e52-110">*lAtom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7e52-111">Ein **System. Int32** -Wert, der den Index angibt, an dem das angeforderte Attribut innerhalb des Satzes verfügbarer Attribute liegt.</span><span class="sxs-lookup"><span data-stu-id="c7e52-111">A **System.Int32** that specifies the index at which the requested attribute resides within the set of available attributes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7e52-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c7e52-112">Return value</span></span>

<span data-ttu-id="c7e52-113">Ein **System. String** -Wert, der dem Wert des-Attributs entspricht.</span><span class="sxs-lookup"><span data-stu-id="c7e52-113">A **System.String** that is the value of the attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7e52-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7e52-114">Remarks</span></span>

<span data-ttu-id="c7e52-115">Diese Methode kann verwendet werden, um Metadaten für ein bestimmtes Medien Element mithilfe einer Attribut Indexnummer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c7e52-115">This method can be used to retrieve metadata for a specific media item by using an attribute index number.</span></span> <span data-ttu-id="c7e52-116">Die **AttributeCount** -Eigenschaft kann verwendet werden, um die Anzahl der für das Medien Element verfügbaren Attribute zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="c7e52-116">The **attributeCount** property can be used to determine the number of attributes available for the media item.</span></span>

<span data-ttu-id="c7e52-117">Die **getmediaatom** -Methode der **iwmpmediacollection** -Schnittstelle kann auch verwendet werden, um den Index eines bestimmten Attributs abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c7e52-117">The **getMediaAtom** method of the **IWMPMediaCollection** interface can also be used to retrieve the index of a particular attribute.</span></span> <span data-ttu-id="c7e52-118">Diese Technik ist im Allgemeinen effizienter als die **getiteminfo** -Methode oder die **getItemInfoByType** -Methode bei der Arbeit mit großen Wiedergabelisten.</span><span class="sxs-lookup"><span data-stu-id="c7e52-118">This technique is generally more efficient than the **getItemInfo** or **getItemInfoByType** methods when working with large playlists.</span></span>

<span data-ttu-id="c7e52-119">Vor dem Aufrufen dieser Methode müssen Sie über Lesezugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="c7e52-119">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="c7e52-120">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="c7e52-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c7e52-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c7e52-121">Requirements</span></span>



| <span data-ttu-id="c7e52-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c7e52-122">Requirement</span></span> | <span data-ttu-id="c7e52-123">Wert</span><span class="sxs-lookup"><span data-stu-id="c7e52-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7e52-124">Version</span><span class="sxs-lookup"><span data-stu-id="c7e52-124">Version</span></span><br/>   | <span data-ttu-id="c7e52-125">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="c7e52-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="c7e52-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="c7e52-126">Namespace</span></span><br/> | <span data-ttu-id="c7e52-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="c7e52-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c7e52-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="c7e52-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c7e52-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c7e52-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7e52-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7e52-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7e52-131">**Iwmpmedia-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="c7e52-131">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c7e52-132">**Iwmpmedia. AttributeCount (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="c7e52-132">**IWMPMedia.attributeCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c7e52-133">**Iwmpmedia. getiteminfo (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="c7e52-133">**IWMPMedia.getItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c7e52-134">**Iwmpmedia. Einstellungs Verzeichnis (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="c7e52-134">**IWMPMedia.setItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c7e52-135">**IWMPMedia3. getItemInfoByType (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="c7e52-135">**IWMPMedia3.getItemInfoByType (VB and C#)**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c7e52-136">**Iwmpmediacollection. getmediaatom (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="c7e52-136">**IWMPMediaCollection.getMediaAtom (VB and C#)**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getmediaatom--vb-and-c.md)
</dt> </dl>

 

 





