---
title: IWMPStringCollection2 getItemInfoByType-Methode
description: Die getItemInfoByType-Methode gibt den Wert zurück, der dem angegebenen Index, dem Namen, der Sprache und dem Attribut Index für Zeichen folgen Auflistungs Elemente entspricht.
ms.assetid: 51035fed-51ce-4cd2-a936-4c99802128f2
keywords:
- getItemInfoByType-Methode, Windows Media Player
- getItemInfoByType-Methode, Windows Media Player, IWMPStringCollection2-Schnittstelle
- IWMPStringCollection2 Interface, Windows Media Player, getItemInfoByType-Methode
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getItemInfobyType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e227d6471ecf41c8f48420ded61c6f4e7eaac8cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366851"
---
# <a name="iwmpstringcollection2getiteminfobytype-method"></a><span data-ttu-id="2655b-106">IWMPStringCollection2:: getItemInfoByType-Methode</span><span class="sxs-lookup"><span data-stu-id="2655b-106">IWMPStringCollection2::getItemInfobyType method</span></span>

<span data-ttu-id="2655b-107">Die **getItemInfoByType** -Methode gibt den Wert zurück, der dem angegebenen Index, dem Namen, der Sprache und dem Attribut Index für Zeichen folgen Auflistungs Elemente entspricht.</span><span class="sxs-lookup"><span data-stu-id="2655b-107">The **getItemInfoByType** method returns the value corresponding to the specified string collection item index, name, language, and attribute index.</span></span>

## <a name="syntax"></a><span data-ttu-id="2655b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2655b-108">Syntax</span></span>


```CSharp
public System.Object getItemInfobyType(
  System.Int32 lCollectionIndex,
  System.String bstrType,
  System.String bstrLanguage,
  System.Int32 lAttributeIndex
);
```


```VB

Public Function getItemInfobyType( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String, _
  ByVal lAttributeIndex As System.Int32 _
) As System.Object
Implements IWMPStringCollection2.getItemInfobyType
```





## <a name="parameters"></a><span data-ttu-id="2655b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2655b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2655b-110">*lcollectionindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2655b-110">*lCollectionIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2655b-111">Der **System. Int32** -Wert, der der null basierte Index des Zeichen folgen-Sammel Elements ist, aus dem das Attribut abgeleitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2655b-111">The **System.Int32** that is the zero-based index of the string collection item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="2655b-112">*bstrintype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2655b-112">*bstrType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2655b-113">Der **System. String** -Wert, der der Attribut Name ist.</span><span class="sxs-lookup"><span data-stu-id="2655b-113">The **System.String** that is the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="2655b-114">*bstraulanguage* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2655b-114">*bstrLanguage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2655b-115">Die **System. String** -Wert, der die Sprache angibt.</span><span class="sxs-lookup"><span data-stu-id="2655b-115">The **System.String** that indicates the language.</span></span> <span data-ttu-id="2655b-116">Wenn der Wert auf NULL oder auf eine Zeichenfolge der Länge 0 (null) festgelegt ist, wird die aktuelle Gebiets Schema Zeichenfolge verwendet.</span><span class="sxs-lookup"><span data-stu-id="2655b-116">If the value is set to null or to a zero-length string (""), the current locale string is used.</span></span> <span data-ttu-id="2655b-117">Andernfalls muss der Wert eine gültige RFC 1766-sprach Zeichenfolge sein, z. b. "en-US".</span><span class="sxs-lookup"><span data-stu-id="2655b-117">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> <dt>

<span data-ttu-id="2655b-118">*lattributeindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2655b-118">*lAttributeIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2655b-119">Ein **System. Int32** -Wert, der der null basierte Index des Attributs ist.</span><span class="sxs-lookup"><span data-stu-id="2655b-119">A **System.Int32** that is the zero-based index of the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2655b-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2655b-120">Return value</span></span>

<span data-ttu-id="2655b-121">Ein **System. Object** , das das Zeichen folgen Auflistungs Element ist.</span><span class="sxs-lookup"><span data-stu-id="2655b-121">A **System.Object** that is the string collection item.</span></span>

## <a name="remarks"></a><span data-ttu-id="2655b-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2655b-122">Remarks</span></span>

<span data-ttu-id="2655b-123">Diese Methode unterstützt Attribute mit mehreren Werten und Attributen mit komplexen Werten.</span><span class="sxs-lookup"><span data-stu-id="2655b-123">This method supports attributes with multiple values and attributes with complex values.</span></span> <span data-ttu-id="2655b-124">Die **getiteminfo** -Methode unterstützt keine Attribute mit mehreren Werten oder Attributen mit komplexen Werten.</span><span class="sxs-lookup"><span data-stu-id="2655b-124">The **getItemInfo** method does not support attributes with multiple values or attributes with complex values.</span></span>

<span data-ttu-id="2655b-125">Durch Übergeben des Werts "childlist" im *bstrintype* -Parameter können Sie eine neue Zeichen folgen Auflistung abrufen, die die untergeordneten Elemente eines der Elemente in der übergeordneten Zeichen folgen Auflistung enthält.</span><span class="sxs-lookup"><span data-stu-id="2655b-125">By passing the value "ChildList" in the *bstrType* parameter, you can retrieve a new string collection that contains the children of one of the items in the parent string collection.</span></span> <span data-ttu-id="2655b-126">Wenn die übergeordnete Auflistung z. b. eine Liste von albumids enthält, können Sie mit dieser Methode eine untergeordnete Zeichen folgen Auflistung abrufen, die alle Spuren für eines der Alben enthält.</span><span class="sxs-lookup"><span data-stu-id="2655b-126">For instance, if the parent collection contains a list of AlbumIDs, you can use this method to obtain a child string collection that contains all the tracks for one of the albums.</span></span> <span data-ttu-id="2655b-127">Diese Vorgehensweise ist schneller und effizienter als das doppelte Aufrufen der **IWMPMediaCollection2. getstringcollectionbyquery** -Methode. einmal, um eine Auflistung von albumids zu erhalten, und ein zweites Mal, um eine Sammlung von Spuren für eine bestimmte albumId zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2655b-127">This approach is faster and more efficient than calling the **IWMPMediaCollection2.getStringCollectionByQuery** method twice; once to get a collection of AlbumIDs, and a second time to get a collection of tracks for a particular AlbumID.</span></span> <span data-ttu-id="2655b-128">Um childlist auf die soeben beschriebene Weise zu verwenden, muss die übergeordnete Zeichen folgen Auflistung aus einer Mediensammlung über **iwmplibraryservices** abgerufen werden, und nicht mithilfe der **AxWindowsMediaPlayer. mediacollection** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="2655b-128">To use ChildList in the way just described, the parent string collection must be obtained from a media collection through **IWMPLibraryServices**, and not by using the **AxWindowsMediaPlayer.mediaCollection** property.</span></span>

<span data-ttu-id="2655b-129">Wenn Sie childlist verwenden, übergeben Sie den Wert "childlist" im *bstrintype* -Parameter und den Wert "0" im Parameter " *lattributeindex* ".</span><span class="sxs-lookup"><span data-stu-id="2655b-129">When using ChildList, pass the value "ChildList" in the *bstrType* parameter, and the value 0 in the *lAttributeIndex* parameter.</span></span> <span data-ttu-id="2655b-130">Anschließend können Sie das zurückgegebene-Objekt in eine **IWMPStringCollection2** -Schnittstelle umwandeln, um auf die untergeordnete Liste zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="2655b-130">You can then cast the object that is returned to an **IWMPStringCollection2** interface to access the child list.</span></span>

<span data-ttu-id="2655b-131">Um diese Methode verwenden zu können, müssen Sie über Lesezugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="2655b-131">To use this method, you must have read access to the library.</span></span> <span data-ttu-id="2655b-132">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="2655b-132">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2655b-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2655b-133">Requirements</span></span>



| <span data-ttu-id="2655b-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2655b-134">Requirement</span></span> | <span data-ttu-id="2655b-135">Wert</span><span class="sxs-lookup"><span data-stu-id="2655b-135">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2655b-136">Version</span><span class="sxs-lookup"><span data-stu-id="2655b-136">Version</span></span><br/>   | <span data-ttu-id="2655b-137">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="2655b-137">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="2655b-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="2655b-138">Namespace</span></span><br/> | <span data-ttu-id="2655b-139">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="2655b-139">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="2655b-140">Assembly</span><span class="sxs-lookup"><span data-stu-id="2655b-140">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2655b-141"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2655b-141"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2655b-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2655b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2655b-143">**AlbumId-Attribut**</span><span class="sxs-lookup"><span data-stu-id="2655b-143">**AlbumID Attribute**</span></span>](albumid-attribute.md)
</dt> <dt>

[<span data-ttu-id="2655b-144">**Iwmplibraryservices-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="2655b-144">**IWMPLibraryServices Interface (VB and C#)**</span></span>](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2655b-145">**IWMPMediaCollection2. getstringcollectionbyquery (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="2655b-145">**IWMPMediaCollection2.getStringCollectionByQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2655b-146">**IWMPStringCollection2-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="2655b-146">**IWMPStringCollection2 Interface**</span></span>](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2655b-147">**IWMPStringCollection2. getiteminfo (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="2655b-147">**IWMPStringCollection2.getItemInfo (VB and C#)**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfo--vb-and-c.md)
</dt> </dl>

 

 





