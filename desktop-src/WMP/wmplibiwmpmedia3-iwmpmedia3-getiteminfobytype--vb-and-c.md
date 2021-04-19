---
title: IWMPMedia3 getItemInfoByType-Methode
description: Die getItemInfoByType-Methode gibt den Wert des Attributs zurück, das dem angegebenen Attributtyp und Index entspricht.
ms.assetid: e4cf14b4-3c59-485f-a573-734a0076647b
keywords:
- getItemInfoByType-Methode, Windows Media Player
- getItemInfoByType-Methode, Windows Media Player, IWMPMedia3-Schnittstelle
- IWMPMedia3 Interface, Windows Media Player, getItemInfoByType-Methode
topic_type:
- apiref
api_name:
- IWMPMedia3.getItemInfoByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f37992201d5d19397724071f8c2a4b8e851aac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352819"
---
# <a name="iwmpmedia3getiteminfobytype-method"></a><span data-ttu-id="25b3a-106">IWMPMedia3:: getItemInfoByType-Methode</span><span class="sxs-lookup"><span data-stu-id="25b3a-106">IWMPMedia3::getItemInfoByType method</span></span>

<span data-ttu-id="25b3a-107">Die **getItemInfoByType** -Methode gibt den Wert des Attributs zurück, das dem angegebenen Attributtyp und Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="25b3a-107">The **getItemInfoByType** method returns the value of the attribute corresponding to the specified attribute type and index.</span></span>

## <a name="syntax"></a><span data-ttu-id="25b3a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="25b3a-108">Syntax</span></span>


```CSharp
public System.Object getItemInfoByType(
  System.String bstrType,
  System.String bstrLanguage,
  System.Int32 lIndex
);
```


```VB

Public Function getItemInfoByType( _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String, _
  ByVal lIndex As System.Int32 _
) As System.Object
Implements IWMPMedia3.getItemInfoByType
```





## <a name="parameters"></a><span data-ttu-id="25b3a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="25b3a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25b3a-110">*bstrintype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25b3a-110">*bstrType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25b3a-111">Ein **System. String** -Wert, der der Attributtyp ist.</span><span class="sxs-lookup"><span data-stu-id="25b3a-111">A **System.String** that is the attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="25b3a-112">*bstraulanguage* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25b3a-112">*bstrLanguage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25b3a-113">Ein **System. String** -Wert, der die Sprache ist.</span><span class="sxs-lookup"><span data-stu-id="25b3a-113">A **System.String** that is the language.</span></span> <span data-ttu-id="25b3a-114">Wenn der Wert auf NULL oder eine Zeichenfolge der Länge 0 (null) ("") festgelegt ist, wird die aktuelle Gebiets Schema Zeichenfolge verwendet.</span><span class="sxs-lookup"><span data-stu-id="25b3a-114">If the value is set to null or a zero-length string (""), the current locale string is used.</span></span> <span data-ttu-id="25b3a-115">Andernfalls muss der Wert eine gültige RFC 1766-sprach Zeichenfolge sein, z. b. "en-US".</span><span class="sxs-lookup"><span data-stu-id="25b3a-115">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> <dt>

<span data-ttu-id="25b3a-116">*Lindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25b3a-116">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25b3a-117">Ein **System. Int32** -Wert, der der Attribut Index ist.</span><span class="sxs-lookup"><span data-stu-id="25b3a-117">A **System.Int32** that is the attribute index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25b3a-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="25b3a-118">Return value</span></span>

<span data-ttu-id="25b3a-119">Ein **System. Object** , das den Wert des Attributs ist.</span><span class="sxs-lookup"><span data-stu-id="25b3a-119">A **System.Object** that is the value of the attribute.</span></span> <span data-ttu-id="25b3a-120">Der Typ, in den dieses Objekt umgewandelt werden soll, hängt vom Typ des Attributs ab.</span><span class="sxs-lookup"><span data-stu-id="25b3a-120">The type to cast this object to depends on the type of the attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="25b3a-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="25b3a-121">Remarks</span></span>

<span data-ttu-id="25b3a-122">Diese Methode gibt die Metadaten für ein einzelnes digitales Medien Element oder ein Medien Element zurück, das Teil einer Wiedergabeliste ist.</span><span class="sxs-lookup"><span data-stu-id="25b3a-122">This method returns the metadata for an individual digital media item or a media item that is part of a playlist.</span></span>

<span data-ttu-id="25b3a-123">Diese Methode unterstützt Attribute mit mehreren Werten und Attributen mit komplexen Werten.</span><span class="sxs-lookup"><span data-stu-id="25b3a-123">This method supports attributes with multiple values and attributes with complex values.</span></span> <span data-ttu-id="25b3a-124">Die **getiteminfo** -Methode unterstützt keine Attribute mit mehreren Werten und Attributen mit komplexen Werten.</span><span class="sxs-lookup"><span data-stu-id="25b3a-124">The **getItemInfo** method does not support attributes with multiple values and attributes with complex values.</span></span>

<span data-ttu-id="25b3a-125">Die **AttributeCount** -Eigenschaft ruft die Anzahl der für ein bestimmtes Medien Element verfügbaren Attributnamen ab.</span><span class="sxs-lookup"><span data-stu-id="25b3a-125">The **attributeCount** property gets the number of attribute names available for a given media item.</span></span> <span data-ttu-id="25b3a-126">Index Nummern können dann mit der **GetAttributeName** -Methode verwendet werden, um den Namen der einzelnen verfügbaren Attribute zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="25b3a-126">Index numbers can then be used with the **getAttributeName** method to determine the name of each available attribute.</span></span> <span data-ttu-id="25b3a-127">Einzelne Attributnamen können an den *Name* -Parameter von **getItemInfoByType** übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="25b3a-127">Individual attribute names can be passed to the *name* parameter of **getItemInfoByType**.</span></span>

<span data-ttu-id="25b3a-128">Die **getattributezähltbytype** -Methode gibt die Anzahl von Attributen zurück, die einem bestimmten Attributnamen für ein bestimmtes Medien Element entsprechen.</span><span class="sxs-lookup"><span data-stu-id="25b3a-128">The **getAttributeCountByType** method returns the number of attributes that correspond to a particular attribute name for a given media item.</span></span> <span data-ttu-id="25b3a-129">Indexnummern können dann an den *Index* -Parameter von **getItemInfoByType** übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="25b3a-129">Index numbers can then be passed to the *index* parameter of **getItemInfoByType**.</span></span> <span data-ttu-id="25b3a-130">Dies ist hilfreich, wenn ein Medien Element z. b. unter mehreren Genres kategorisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="25b3a-130">This is useful when a media item has been categorized under multiple genres, for example.</span></span>

<span data-ttu-id="25b3a-131">Wenn das Medien Element aus einer Bibliothek stammt, die durch den Aufruf von [iwmplibrary. mediacollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)abgerufen wurde, unterscheidet sich der Satz verfügbarer Attribute von denjenigen, die von der lokalen Bibliothek abgerufen werden können, die durch Aufrufen von [AxWindowsMediaPlayer. mediacollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="25b3a-131">If the media item came from a library that was retrieved by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), the set of available attributes will differ from those which can be queried from the local library retrieved by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md).</span></span> <span data-ttu-id="25b3a-132">Beispielsweise sind die Attribute, die in der lokalen Bibliothek verfügbar sind, die mithilfe von **iwmplibrary** abgerufen werden, eine Teilmenge der Attribute, die in der lokalen Bibliothek verfügbar sind, die mithilfe von **AxWindowsMediaPlayer** abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="25b3a-132">For example, the attributes available from the local library retrieved by using **IWMPLibrary** will be a subset of the attributes available from the local library retrieved by using **AxWindowsMediaPlayer**.</span></span> <span data-ttu-id="25b3a-133">Der Satz von Attributen, der aus anderen Quellen (Remote Bibliotheken, portable Geräte oder CDs) verfügbar ist, wird von den anderen Quellen definiert.</span><span class="sxs-lookup"><span data-stu-id="25b3a-133">The set of attributes available from other sources (remote libraries, portable devices, or CDs is defined by the other sources.</span></span>

<span data-ttu-id="25b3a-134">Vor dem Aufrufen dieser Methode müssen Sie über Lesezugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="25b3a-134">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="25b3a-135">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="25b3a-135">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="25b3a-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25b3a-136">Requirements</span></span>



| <span data-ttu-id="25b3a-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="25b3a-137">Requirement</span></span> | <span data-ttu-id="25b3a-138">Wert</span><span class="sxs-lookup"><span data-stu-id="25b3a-138">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25b3a-139">Version</span><span class="sxs-lookup"><span data-stu-id="25b3a-139">Version</span></span><br/>   | <span data-ttu-id="25b3a-140">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="25b3a-140">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="25b3a-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="25b3a-141">Namespace</span></span><br/> | <span data-ttu-id="25b3a-142">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="25b3a-142">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="25b3a-143">Assembly</span><span class="sxs-lookup"><span data-stu-id="25b3a-143">Assembly</span></span><br/>  | <dl> <span data-ttu-id="25b3a-144"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="25b3a-144"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25b3a-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25b3a-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25b3a-146">**IWMPMedia3-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="25b3a-146">**IWMPMedia3 Interface (VB and C#)**</span></span>](iwmpmedia3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="25b3a-147">**Iwmpmedia. AttributeCount (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="25b3a-147">**IWMPMedia.attributeCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="25b3a-148">**Iwmpmedia. GetAttributeName (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="25b3a-148">**IWMPMedia.getAttributeName (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="25b3a-149">**Iwmpmedia. getiteminfo (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="25b3a-149">**IWMPMedia.getItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="25b3a-150">**IWMPMedia3. getattributezähltbytype (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="25b3a-150">**IWMPMedia3.getAttributeCountByType (VB and C#)**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getattributecountbytype--vb-and-c.md)
</dt> </dl>

 

 





