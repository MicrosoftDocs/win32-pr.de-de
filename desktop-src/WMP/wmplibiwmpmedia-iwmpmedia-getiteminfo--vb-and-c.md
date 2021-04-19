---
title: Iwmpmedia getiteminfo-Methode
description: Die getiteminfo-Methode gibt den Wert des angegebenen Attributs für das Medien Element zurück.
ms.assetid: b95fa61d-a600-4f31-a930-d80516204034
keywords:
- getiteminfo-Methode, Windows Media Player
- getiteminfo-Methode, Windows Media Player, iwmpmedia-Schnittstelle
- Iwmpmedia Interface, Windows Media Player, getiteminfo-Methode
topic_type:
- apiref
api_name:
- IWMPMedia.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 523e57e68d13df55395cd4deca6e09904723bbaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356068"
---
# <a name="iwmpmediagetiteminfo-method"></a><span data-ttu-id="95e4b-106">Iwmpmedia:: getiteminfo-Methode</span><span class="sxs-lookup"><span data-stu-id="95e4b-106">IWMPMedia::getItemInfo method</span></span>

<span data-ttu-id="95e4b-107">Die **getiteminfo** -Methode gibt den Wert des angegebenen Attributs für das Medien Element zurück.</span><span class="sxs-lookup"><span data-stu-id="95e4b-107">The **getItemInfo** method returns the value of the specified attribute for the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="95e4b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="95e4b-108">Syntax</span></span>


```CSharp
public System.String getItemInfo(
  System.String bstrItemName
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrItemName As System.String _
) As System.String
Implements IWMPMedia.getItemInfo
```





## <a name="parameters"></a><span data-ttu-id="95e4b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="95e4b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95e4b-110">*bstritemname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95e4b-110">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95e4b-111">Ein **System. String** -Wert, der den Namen des Attributs ist.</span><span class="sxs-lookup"><span data-stu-id="95e4b-111">A **System.String** that is the name of the attribute.</span></span> <span data-ttu-id="95e4b-112">Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Attribut Referenz](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="95e4b-112">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95e4b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="95e4b-113">Return value</span></span>

<span data-ttu-id="95e4b-114">Ein **System. String** -Wert, der den Wert des angegebenen Attributs ist.</span><span class="sxs-lookup"><span data-stu-id="95e4b-114">A **System.String** that is the value of the specified attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="95e4b-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95e4b-115">Remarks</span></span>

<span data-ttu-id="95e4b-116">Diese Methode gibt die Metadaten für ein einzelnes Medien Element oder ein Medien Element zurück, das Teil einer Wiedergabeliste ist.</span><span class="sxs-lookup"><span data-stu-id="95e4b-116">This method returns the metadata for an individual media item or a media item that is part of a playlist.</span></span>

<span data-ttu-id="95e4b-117">Die **AttributeCount** -Eigenschaft ruft die Anzahl der für ein bestimmtes Medien Element verfügbaren Attributnamen ab.</span><span class="sxs-lookup"><span data-stu-id="95e4b-117">The **attributeCount** property gets the number of attribute names available for a given media item.</span></span> <span data-ttu-id="95e4b-118">Index Nummern können dann mit der **GetAttributeName** -Methode verwendet werden, um den Namen der einzelnen verfügbaren Attribute zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="95e4b-118">Index numbers can then be used with the **getAttributeName** method to determine the name of each available attribute.</span></span> <span data-ttu-id="95e4b-119">Einzelne Attributnamen können an **getiteminfo** übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="95e4b-119">Individual attribute names can be passed to **getItemInfo**.</span></span>

<span data-ttu-id="95e4b-120">Um Attribute mit mehreren Werten und Attributen mit komplexen Werten abzurufen, verwenden Sie die **getItemInfoByType** -Methode.</span><span class="sxs-lookup"><span data-stu-id="95e4b-120">To retrieve attributes with multiple values and attributes with complex values, use the **getItemInfoByType** method.</span></span>

<span data-ttu-id="95e4b-121">Wenn das Medien Element aus einer Bibliothek stammt, die durch den Aufruf von [iwmplibrary. mediacollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)abgerufen wurde, unterscheidet sich der Satz verfügbarer Attribute von denjenigen, die von der lokalen Bibliothek abgerufen werden können, die durch Aufrufen von [AxWindowsMediaPlayer. mediacollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="95e4b-121">If the media item came from a library that was retrieved by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), the set of available attributes will differ from those which can be queried from the local library retrieved by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md).</span></span> <span data-ttu-id="95e4b-122">Beispielsweise sind die Attribute, die in der lokalen Bibliothek verfügbar sind, die mithilfe von **iwmplibrary** abgerufen werden, eine Teilmenge der Attribute, die in der lokalen Bibliothek verfügbar sind, die mithilfe von **iwmpcore** abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="95e4b-122">For example, the attributes available from the local library retrieved by using **IWMPLibrary** will be a subset of the attributes available from the local library retrieved by using **IWMPCore**.</span></span> <span data-ttu-id="95e4b-123">Der Satz von Attributen, der aus anderen Quellen (Remote Bibliotheken, portable Geräte oder CDs) verfügbar ist, wird von den anderen Quellen definiert.</span><span class="sxs-lookup"><span data-stu-id="95e4b-123">The set of attributes available from other sources (remote libraries, portable devices, or CDs) is defined by the other sources.</span></span>

<span data-ttu-id="95e4b-124">Vor dem Aufrufen dieser Methode müssen Sie über Lesezugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="95e4b-124">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="95e4b-125">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="95e4b-125">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="95e4b-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95e4b-126">Requirements</span></span>



| <span data-ttu-id="95e4b-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95e4b-127">Requirement</span></span> | <span data-ttu-id="95e4b-128">Wert</span><span class="sxs-lookup"><span data-stu-id="95e4b-128">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95e4b-129">Version</span><span class="sxs-lookup"><span data-stu-id="95e4b-129">Version</span></span><br/>   | <span data-ttu-id="95e4b-130">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="95e4b-130">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="95e4b-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="95e4b-131">Namespace</span></span><br/> | <span data-ttu-id="95e4b-132">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="95e4b-132">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="95e4b-133">Assembly</span><span class="sxs-lookup"><span data-stu-id="95e4b-133">Assembly</span></span><br/>  | <dl> <span data-ttu-id="95e4b-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="95e4b-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95e4b-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95e4b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95e4b-136">**Attribut Verweis**</span><span class="sxs-lookup"><span data-stu-id="95e4b-136">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="95e4b-137">**Iwmpmedia-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="95e4b-137">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="95e4b-138">**Iwmpmedia. AttributeCount (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="95e4b-138">**IWMPMedia.attributeCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="95e4b-139">**Iwmpmedia. GetAttributeName (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="95e4b-139">**IWMPMedia.getAttributeName (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="95e4b-140">**Iwmpmedia. Einstellungs Verzeichnis (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="95e4b-140">**IWMPMedia.setItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="95e4b-141">**IWMPMedia3. getItemInfoByType (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="95e4b-141">**IWMPMedia3.getItemInfoByType (VB and C#)**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





