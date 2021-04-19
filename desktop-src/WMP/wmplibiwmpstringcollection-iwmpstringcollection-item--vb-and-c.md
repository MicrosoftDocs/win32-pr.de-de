---
title: Iwmpstringcollection-Element Methode
description: Die Item-Methode gibt die Zeichenfolge am angegebenen Index zurück.
ms.assetid: 77546cb2-eda5-4bb8-97b9-55270461815f
keywords:
- Element-Methoden Fenster Media Player
- Element-Methode, Windows Media Player, iwmpstringcollection-Schnittstelle
- Iwmpstringcollection-Schnittstelle, Windows Media Player, Element-Methode
topic_type:
- apiref
api_name:
- IWMPStringCollection.Item
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f69bdc63448699a595238b9907f4b1253209ad06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359328"
---
# <a name="iwmpstringcollectionitem-method"></a><span data-ttu-id="da394-106">Iwmpstringcollection:: Item-Methode</span><span class="sxs-lookup"><span data-stu-id="da394-106">IWMPStringCollection::Item method</span></span>

<span data-ttu-id="da394-107">Die **Item** -Methode gibt die Zeichenfolge am angegebenen Index zurück.</span><span class="sxs-lookup"><span data-stu-id="da394-107">The **Item** method returns the string at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="da394-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="da394-108">Syntax</span></span>


```CSharp
public System.String Item(
  System.Int32 lIndex
);
```


```VB

Public Function Item( _
  ByVal lIndex As System.Int32 _
) As System.String
Implements IWMPStringCollection.Item
```





## <a name="parameters"></a><span data-ttu-id="da394-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="da394-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da394-110">*Lindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da394-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da394-111">Ein **System. Int32** -Wert, der der Index ist.</span><span class="sxs-lookup"><span data-stu-id="da394-111">A **System.Int32** that is the index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da394-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="da394-112">Return value</span></span>

<span data-ttu-id="da394-113">Eine **System. String** , bei der es sich um die Zeichenfolge am angegebenen Index handelt.</span><span class="sxs-lookup"><span data-stu-id="da394-113">A **System.String** that is the string at the specified index.</span></span>

## <a name="remarks"></a><span data-ttu-id="da394-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="da394-114">Remarks</span></span>

<span data-ttu-id="da394-115">Die **iwmpstringcollection** -Schnittstelle wird verwendet, um den Satz von Werten abzurufen, die für ein Attribut verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="da394-115">The **IWMPStringCollection** interface is used to retrieve the set of values available for an attribute.</span></span> <span data-ttu-id="da394-116">Beispielsweise kann die **iwmpmediacollection. getAttributeStringCollection** -Methode zum Abrufen einer **iwmpstringcollection** -Schnittstelle verwendet werden, die alle Werte für das Genre-Attribut innerhalb des audiomedientyps darstellt.</span><span class="sxs-lookup"><span data-stu-id="da394-116">For example, the **IWMPMediaCollection.getAttributeStringCollection** method can be used to retrieve an **IWMPStringCollection** interface representing all the values for the Genre attribute within the Audio media type.</span></span> <span data-ttu-id="da394-117">Die **Item** -Methode kann dann zum Durchlaufen aller möglichen Werte für das Genre-Attribut verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="da394-117">The **Item** method can then be used to iterate through all of the possible values for the Genre attribute.</span></span>

<span data-ttu-id="da394-118">Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="da394-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="da394-119">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="da394-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="da394-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da394-120">Requirements</span></span>



| <span data-ttu-id="da394-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da394-121">Requirement</span></span> | <span data-ttu-id="da394-122">Wert</span><span class="sxs-lookup"><span data-stu-id="da394-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da394-123">Version</span><span class="sxs-lookup"><span data-stu-id="da394-123">Version</span></span><br/>   | <span data-ttu-id="da394-124">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="da394-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="da394-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="da394-125">Namespace</span></span><br/> | <span data-ttu-id="da394-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="da394-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="da394-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="da394-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="da394-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="da394-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da394-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da394-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da394-130">**Iwmpmediacollection. getAttributeStringCollection (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="da394-130">**IWMPMediaCollection.getAttributeStringCollection (VB and C#)**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getattributestringcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="da394-131">**IWMPSettings2. mediaaccessrights (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="da394-131">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="da394-132">**IWMPSettings2. requestmediaaccessrights (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="da394-132">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="da394-133">**Iwmpstringcollection-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="da394-133">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





