---
title: IWMPStringCollection2 getiteminfo-Methode
description: Die getiteminfo-Methode gibt die Zeichenfolge zurück, die dem angegebenen Index und Namen des Zeichen folgen Auflistungs Elements entspricht.
ms.assetid: 4a107e85-9eb7-42be-b1f9-8e9e92e6e509
keywords:
- getiteminfo-Methode, Windows Media Player
- getiteminfo-Methode, Windows Media Player, IWMPStringCollection2-Schnittstelle
- IWMPStringCollection2 Interface, Windows Media Player, getiteminfo-Methode
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4741c4a3ba74b03038974d8b66bc42c23830ebb3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372682"
---
# <a name="iwmpstringcollection2getiteminfo-method"></a><span data-ttu-id="495cf-106">IWMPStringCollection2:: getiteminfo-Methode</span><span class="sxs-lookup"><span data-stu-id="495cf-106">IWMPStringCollection2::getItemInfo method</span></span>

<span data-ttu-id="495cf-107">Die **getiteminfo** -Methode gibt die Zeichenfolge zurück, die dem angegebenen Index und Namen des Zeichen folgen Auflistungs Elements entspricht.</span><span class="sxs-lookup"><span data-stu-id="495cf-107">The **getItemInfo** method returns the string corresponding to the specified string collection item index and name.</span></span>

## <a name="syntax"></a><span data-ttu-id="495cf-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="495cf-108">Syntax</span></span>


```CSharp
public System.String getItemInfo(
  System.Int32 lCollectionIndex,
  System.String bstrItemName
);
```


```VB

Public Function getItemInfo( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrItemName As System.String _
) As System.String
Implements IWMPStringCollection2.getItemInfo
```





## <a name="parameters"></a><span data-ttu-id="495cf-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="495cf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="495cf-110">*lcollectionindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="495cf-110">*lCollectionIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="495cf-111">Der **System. Int32** -Wert, der den NULL basierten Index des Zeichen folgen-Sammel Elements angibt, aus dem das Attribut abgeleitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="495cf-111">The **System.Int32** specifying the zero-based index of the string collection item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="495cf-112">*bstritemname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="495cf-112">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="495cf-113">Der **System. String** -Wert, der der Attribut Name ist.</span><span class="sxs-lookup"><span data-stu-id="495cf-113">The **System.String** that is the attribute name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="495cf-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="495cf-114">Return value</span></span>

<span data-ttu-id="495cf-115">Der **System. String** -Wert, der der Name des Zeichen folgen-Sammel Elements ist.</span><span class="sxs-lookup"><span data-stu-id="495cf-115">The **System.String** that is the name of the string collection item.</span></span> <span data-ttu-id="495cf-116">Bei Attributen, deren zugrunde liegender Wert **System. Boolean** ist, wird die Zeichenfolge "true" oder "false" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="495cf-116">For attributes whose underlying value is **System.Boolean**, it returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="495cf-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="495cf-117">Remarks</span></span>

<span data-ttu-id="495cf-118">Um Attribute mit mehreren Werten und Attributen mit komplexen Werten abzurufen, verwenden Sie die **getItemInfoByType** -Methode.</span><span class="sxs-lookup"><span data-stu-id="495cf-118">To retrieve attributes with multiple values and attributes with complex values, use the **getItemInfoByType** method.</span></span>

<span data-ttu-id="495cf-119">Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="495cf-119">To use this method, read access to the library is required.</span></span> <span data-ttu-id="495cf-120">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="495cf-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="495cf-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="495cf-121">Requirements</span></span>



| <span data-ttu-id="495cf-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="495cf-122">Requirement</span></span> | <span data-ttu-id="495cf-123">Wert</span><span class="sxs-lookup"><span data-stu-id="495cf-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="495cf-124">Version</span><span class="sxs-lookup"><span data-stu-id="495cf-124">Version</span></span><br/>   | <span data-ttu-id="495cf-125">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="495cf-125">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="495cf-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="495cf-126">Namespace</span></span><br/> | <span data-ttu-id="495cf-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="495cf-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="495cf-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="495cf-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="495cf-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="495cf-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="495cf-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="495cf-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="495cf-131">**IWMPStringCollection2-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="495cf-131">**IWMPStringCollection2 Interface**</span></span>](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="495cf-132">**IWMPStringCollection2. getItemInfoByType (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="495cf-132">**IWMPStringCollection2.getItemInfoByType (VB and C#)**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





