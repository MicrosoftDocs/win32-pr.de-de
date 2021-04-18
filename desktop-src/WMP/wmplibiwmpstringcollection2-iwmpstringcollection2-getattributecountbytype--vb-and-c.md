---
title: IWMPStringCollection2 getattributezähltbytype-Methode
description: Die getattributezähltbytype-Methode gibt die Anzahl der Attribute zurück, die dem angegebenen Zeichen folgen-Sammlungs Index, dem angegebenen Attributnamen und der angegebenen Sprache zugeordnet sind.
ms.assetid: 30312039-3676-4322-b6f6-fb86098bf578
keywords:
- getattributezähltbytype-Methode, Windows Media Player
- getattributezähltbytype-Methode, Windows Media Player, IWMPStringCollection2-Schnittstelle
- IWMPStringCollection2 Interface Windows Media Player, getattributezähltbytype-Methode
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getAttributeCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9bb60fdd843fb3f45b6e4e3aff444a8a915fa0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365748"
---
# <a name="iwmpstringcollection2getattributecountbytype-method"></a><span data-ttu-id="e1bfe-106">IWMPStringCollection2:: getattributezähltbytype-Methode</span><span class="sxs-lookup"><span data-stu-id="e1bfe-106">IWMPStringCollection2::getAttributeCountByType method</span></span>

<span data-ttu-id="e1bfe-107">Die **getattributezähltbytype** -Methode gibt die Anzahl der Attribute zurück, die dem angegebenen Zeichen folgen-Sammlungs Index, dem angegebenen Attributnamen und der angegebenen Sprache zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e1bfe-107">The **getAttributeCountByType** method returns the number of attributes associated with the specified string collection index, attribute name, and language.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1bfe-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1bfe-108">Syntax</span></span>


```CSharp
public System.Int32 getAttributeCountByType(
  System.Int32 lCollectionIndex,
  System.String bstrType,
  System.String bstrLanguage
);
```


```VB

Public Function getAttributeCountByType( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String _
) As System.Int32
Implements IWMPStringCollection2.getAttributeCountByType
```





## <a name="parameters"></a><span data-ttu-id="e1bfe-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1bfe-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1bfe-110">*lcollectionindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e1bfe-110">*lCollectionIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1bfe-111">Der **System. Int32** -Wert, der den NULL basierten Index des Zeichen folgen-Sammel Elements angibt, aus dem das Attribut abgeleitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e1bfe-111">The **System.Int32** specifying the zero-based index of the string collection item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="e1bfe-112">*bstrintype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e1bfe-112">*bstrType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1bfe-113">Die **System. String** -Eigenschaft, die den Namen des Attributs ist.</span><span class="sxs-lookup"><span data-stu-id="e1bfe-113">The **System.String** that is the name of the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="e1bfe-114">*bstraulanguage* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e1bfe-114">*bstrLanguage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1bfe-115">Die **System. String** , die den Namen der Sprache hat.</span><span class="sxs-lookup"><span data-stu-id="e1bfe-115">The **System.String** that is the name of the language.</span></span> <span data-ttu-id="e1bfe-116">Wenn der Wert auf NULL oder auf eine Zeichenfolge der Länge 0 (null) festgelegt ist, wird die aktuelle Gebiets Schema Zeichenfolge verwendet.</span><span class="sxs-lookup"><span data-stu-id="e1bfe-116">If the value is set to null or to a zero-length string (""), the current locale string is used.</span></span> <span data-ttu-id="e1bfe-117">Andernfalls muss der Wert eine gültige RFC 1766-sprach Zeichenfolge sein, z. b. "en-US".</span><span class="sxs-lookup"><span data-stu-id="e1bfe-117">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1bfe-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e1bfe-118">Return value</span></span>

<span data-ttu-id="e1bfe-119">Der **System. Int32** -Wert, der die Anzahl ist.</span><span class="sxs-lookup"><span data-stu-id="e1bfe-119">The **System.Int32** that is the count.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1bfe-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e1bfe-120">Remarks</span></span>

<span data-ttu-id="e1bfe-121">Diese Methode wird verwendet, um die Anzahl von Attributen zu ermitteln, die einem bestimmten Attributnamen für ein bestimmtes **StringCollection** -Element entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e1bfe-121">This method is used to discover the number of attributes corresponding to a particular attribute name for a given **StringCollection** item.</span></span> <span data-ttu-id="e1bfe-122">Index Nummern können dann an den vierten Parameter der **getItemInfoByType** -Methode übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="e1bfe-122">Index numbers can then be passed to the fourth parameter of the **getItemInfoByType** method.</span></span>

<span data-ttu-id="e1bfe-123">Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e1bfe-123">To use this method, read access to the library is required.</span></span> <span data-ttu-id="e1bfe-124">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="e1bfe-124">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e1bfe-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e1bfe-125">Requirements</span></span>



| <span data-ttu-id="e1bfe-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e1bfe-126">Requirement</span></span> | <span data-ttu-id="e1bfe-127">Wert</span><span class="sxs-lookup"><span data-stu-id="e1bfe-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1bfe-128">Version</span><span class="sxs-lookup"><span data-stu-id="e1bfe-128">Version</span></span><br/>   | <span data-ttu-id="e1bfe-129">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="e1bfe-129">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="e1bfe-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="e1bfe-130">Namespace</span></span><br/> | <span data-ttu-id="e1bfe-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="e1bfe-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="e1bfe-132">Assembly</span><span class="sxs-lookup"><span data-stu-id="e1bfe-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e1bfe-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e1bfe-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1bfe-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e1bfe-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1bfe-135">**IWMPStringCollection2-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e1bfe-135">**IWMPStringCollection2 Interface (VB and C#)**</span></span>](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e1bfe-136">**IWMPStringCollection2. getItemInfoByType (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e1bfe-136">**IWMPStringCollection2.getItemInfoByType (VB and C#)**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





