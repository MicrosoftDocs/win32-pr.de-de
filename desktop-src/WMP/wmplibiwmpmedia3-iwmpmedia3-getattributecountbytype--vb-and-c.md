---
title: IWMPMedia3 getattributezähltbytype-Methode
description: Die getattributezähltbytype-Methode gibt die Anzahl der Attribute zurück, die dem angegebenen Attributtyp zugeordnet sind.
ms.assetid: d692635f-f9f1-4d8e-a9c5-9d7fa84f41bd
keywords:
- getattributezähltbytype-Methode, Windows Media Player
- getattributezähltbytype-Methode, Windows Media Player, IWMPMedia3-Schnittstelle
- IWMPMedia3 Interface Windows Media Player, getattributezähltbytype-Methode
topic_type:
- apiref
api_name:
- IWMPMedia3.getAttributeCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49505f9e9df8778cc2c17ba062da6700b9b8aec4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357321"
---
# <a name="iwmpmedia3getattributecountbytype-method"></a><span data-ttu-id="9074a-106">IWMPMedia3:: getattributezähltbytype-Methode</span><span class="sxs-lookup"><span data-stu-id="9074a-106">IWMPMedia3::getAttributeCountByType method</span></span>

<span data-ttu-id="9074a-107">Die **getattributezähltbytype** -Methode gibt die Anzahl der Attribute zurück, die dem angegebenen Attributtyp zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="9074a-107">The **getAttributeCountByType** method returns the number of attributes associated with the specified attribute type.</span></span>

## <a name="syntax"></a><span data-ttu-id="9074a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9074a-108">Syntax</span></span>


```CSharp
public System.Int32 getAttributeCountByType(
  System.String bstrType,
  System.String bstrLanguage
);
```


```VB

Public Function getAttributeCountByType( _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String _
) As System.Int32
Implements IWMPMedia3.getAttributeCountByType
```





## <a name="parameters"></a><span data-ttu-id="9074a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9074a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9074a-110">*bstrintype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9074a-110">*bstrType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9074a-111">Ein **System. String** -Wert, der der Attributtyp ist.</span><span class="sxs-lookup"><span data-stu-id="9074a-111">A **System.String** that is the attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="9074a-112">*bstraulanguage* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9074a-112">*bstrLanguage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9074a-113">Ein **System. String** -Wert, der die Sprache ist.</span><span class="sxs-lookup"><span data-stu-id="9074a-113">A **System.String** that is the language.</span></span> <span data-ttu-id="9074a-114">Wenn der Wert auf NULL oder eine Zeichenfolge der Länge 0 (null) ("") festgelegt ist, wird die aktuelle Gebiets Schema Zeichenfolge verwendet.</span><span class="sxs-lookup"><span data-stu-id="9074a-114">If the value is set to null or a zero-length string (""), the current locale string is used.</span></span> <span data-ttu-id="9074a-115">Andernfalls muss der Wert eine gültige RFC 1766-sprach Zeichenfolge sein, z. b. "en-US".</span><span class="sxs-lookup"><span data-stu-id="9074a-115">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9074a-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9074a-116">Return value</span></span>

<span data-ttu-id="9074a-117">Ein **System. Int32** -Wert, der die Anzahl der Attribute ist, die dem Typ zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="9074a-117">A **System.Int32** that is the count of attributes that are associated with the type.</span></span>

## <a name="remarks"></a><span data-ttu-id="9074a-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9074a-118">Remarks</span></span>

<span data-ttu-id="9074a-119">Diese Methode wird verwendet, um die Anzahl von Attributen zu ermitteln, die einem bestimmten Attributnamen für ein bestimmtes Medien Element entsprechen.</span><span class="sxs-lookup"><span data-stu-id="9074a-119">This method is used to discover the number of attributes corresponding to a particular attribute name for a given media item.</span></span> <span data-ttu-id="9074a-120">Index Nummern können dann an die **getItemInfoByType** -Methode weitergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9074a-120">Index numbers can then be passed to the **getItemInfoByType** method.</span></span> <span data-ttu-id="9074a-121">Dies ist beispielsweise hilfreich, wenn ein Medien Element unter mehreren Genres kategorisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="9074a-121">This is useful, for example, when a media item has been categorized under multiple genres.</span></span>

<span data-ttu-id="9074a-122">Vor dem Aufrufen dieser Methode müssen Sie über Lesezugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="9074a-122">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="9074a-123">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="9074a-123">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9074a-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9074a-124">Requirements</span></span>



| <span data-ttu-id="9074a-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9074a-125">Requirement</span></span> | <span data-ttu-id="9074a-126">Wert</span><span class="sxs-lookup"><span data-stu-id="9074a-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9074a-127">Version</span><span class="sxs-lookup"><span data-stu-id="9074a-127">Version</span></span><br/>   | <span data-ttu-id="9074a-128">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="9074a-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="9074a-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="9074a-129">Namespace</span></span><br/> | <span data-ttu-id="9074a-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="9074a-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="9074a-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="9074a-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="9074a-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="9074a-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9074a-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9074a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9074a-134">**IWMPMedia3-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="9074a-134">**IWMPMedia3 Interface (VB and C#)**</span></span>](iwmpmedia3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9074a-135">**IWMPMedia3. getItemInfoByType (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="9074a-135">**IWMPMedia3.getItemInfoByType (VB and C#)**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





