---
title: Iwmpmediacollection getmediaatom-Methode
description: Die getmediaatom-Methode gibt den Index eines angegebenen Attributs innerhalb des Satzes verfügbarer Attribute zurück.
ms.assetid: 01e3d073-677b-4939-96d3-63ae96eaa25d
keywords:
- getmediaatom-Methode, Windows-Media Player
- getmediaatom-Methode, Windows Media Player, iwmpmediacollection-Schnittstelle
- Iwmpmediacollection Interface, Windows Media Player, getmediaatom-Methode
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getMediaAtom
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08487cf60c351ff4f8e0741209655cb78c30c3f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367196"
---
# <a name="iwmpmediacollectiongetmediaatom-method"></a><span data-ttu-id="896c3-106">Iwmpmediacollection:: getmediaatom-Methode</span><span class="sxs-lookup"><span data-stu-id="896c3-106">IWMPMediaCollection::getMediaAtom method</span></span>

<span data-ttu-id="896c3-107">Die- `getMediaAtom` Methode gibt den Index eines angegebenen Attributs innerhalb des Satzes verfügbarer Attribute zurück.</span><span class="sxs-lookup"><span data-stu-id="896c3-107">The `getMediaAtom` method returns the index of a specified attribute within the set of available attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="896c3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="896c3-108">Syntax</span></span>


```CSharp
public System.Int32 getMediaAtom(
  System.String bstrItemName
);
```


```VB

Public Function getMediaAtom( _
  ByVal bstrItemName As System.String _
) As System.Int32
Implements IWMPMediaCollection.getMediaAtom
```





## <a name="parameters"></a><span data-ttu-id="896c3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="896c3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="896c3-110">*bstritemname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="896c3-110">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="896c3-111">**System. String** der Name des Elements, für das der Index abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="896c3-111">The **System.String** that is the name of the item for which the index should be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="896c3-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="896c3-112">Return value</span></span>

<span data-ttu-id="896c3-113">Der **System. Int32** -Wert, der der Index ist.</span><span class="sxs-lookup"><span data-stu-id="896c3-113">The **System.Int32** that is the index.</span></span>

## <a name="remarks"></a><span data-ttu-id="896c3-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="896c3-114">Remarks</span></span>

<span data-ttu-id="896c3-115">Die mit dieser Methode abgerufene Indexnummer kann an das **iwmpmedia. getiteminfobyatom** -Element übermittelt werden, um auf Attributwerte zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="896c3-115">The index number retrieved with this method can be passed to the **IWMPMedia.getItemInfoByAtom** to access attribute values.</span></span> <span data-ttu-id="896c3-116">Diese Technik ist in der Regel effizienter, wenn Sie mit großen Wiedergabelisten arbeiten als der Zugriff auf einen Attribut Wert über " **iwmpmedia. getiteminfo**".</span><span class="sxs-lookup"><span data-stu-id="896c3-116">This technique is generally more efficient when working with large playlists than accessing an attribute value by name through **IWMPMedia.getItemInfo**.</span></span>

<span data-ttu-id="896c3-117">Vor dem Aufrufen dieser Methode müssen Sie über Lesezugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="896c3-117">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="896c3-118">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="896c3-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="896c3-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="896c3-119">Requirements</span></span>



| <span data-ttu-id="896c3-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="896c3-120">Requirement</span></span> | <span data-ttu-id="896c3-121">Wert</span><span class="sxs-lookup"><span data-stu-id="896c3-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="896c3-122">Version</span><span class="sxs-lookup"><span data-stu-id="896c3-122">Version</span></span><br/>   | <span data-ttu-id="896c3-123">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="896c3-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="896c3-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="896c3-124">Namespace</span></span><br/> | <span data-ttu-id="896c3-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="896c3-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="896c3-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="896c3-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="896c3-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="896c3-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="896c3-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="896c3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="896c3-129">**Iwmpmedia. getiteminfo (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="896c3-129">**IWMPMedia.getItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="896c3-130">**Iwmpmedia. getiteminfobyatom (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="896c3-130">**IWMPMedia.getItemInfoByAtom (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfobyatom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="896c3-131">**Iwmpmediacollection-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="896c3-131">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





