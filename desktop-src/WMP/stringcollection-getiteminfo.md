---
title: StringCollection. getiteminfo-Methode
description: Die getiteminfo-Methode ruft die Zeichenfolge ab, die dem angegebenen Index und Namen des StringCollection-Elements entspricht.
ms.assetid: a031b91e-9d3b-47ac-bc5b-c111d5e3bc12
keywords:
- getiteminfo-Methode, Windows Media Player
- getiteminfo-Methode, Windows Media Player, StringCollection-Klasse
- StringCollection-Klasse, Windows Media Player, getiteminfo-Methode
topic_type:
- apiref
api_name:
- StringCollection.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c9552dcebbc7d565ebc797c62ac3bc00ee109fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358122"
---
# <a name="stringcollectiongetiteminfo-method"></a><span data-ttu-id="9664d-106">StringCollection. getiteminfo-Methode</span><span class="sxs-lookup"><span data-stu-id="9664d-106">StringCollection.getItemInfo method</span></span>

<span data-ttu-id="9664d-107">Die **getiteminfo** -Methode ruft die Zeichenfolge ab, die dem angegebenen Index und Namen des **StringCollection** -Elements entspricht.</span><span class="sxs-lookup"><span data-stu-id="9664d-107">The **getItemInfo** method retrieves the string corresponding to the specified **StringCollection** item index and name.</span></span>

## <a name="syntax"></a><span data-ttu-id="9664d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9664d-108">Syntax</span></span>


```JScript
strRetVal = StringCollection.getItemInfo(
  index,
  name
)
```



## <a name="parameters"></a><span data-ttu-id="9664d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9664d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9664d-110">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9664d-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9664d-111">**Number** (**Long**) gibt den NULL basierten Index des **StringCollection** -Elements an, aus dem das Attribut bezogen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9664d-111">**Number** (**long**) specifying the zero-based index of the **StringCollection** item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="9664d-112">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9664d-112">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9664d-113">**Zeichenfolge** , die den Attributnamen enthält.</span><span class="sxs-lookup"><span data-stu-id="9664d-113">**String** containing the attribute name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9664d-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9664d-114">Return value</span></span>

<span data-ttu-id="9664d-115">Diese Methode gibt eine **Zeichenfolge** zurück, die den Wert des angegebenen Attributs darstellt.</span><span class="sxs-lookup"><span data-stu-id="9664d-115">This method returns a **String** representing the value of the specified attribute.</span></span> <span data-ttu-id="9664d-116">Bei Attributen, deren zugrunde liegender Wert **boolescher** Wert ist, wird die Zeichenfolge "true" oder "false" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9664d-116">For attributes whose underlying value is **Boolean**, it returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="9664d-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9664d-117">Remarks</span></span>

<span data-ttu-id="9664d-118">Um Attribute mit mehreren Werten und Attributen mit komplexen Werten abzurufen, verwenden Sie die **getItemInfoByType** -Methode.</span><span class="sxs-lookup"><span data-stu-id="9664d-118">To retrieve attributes with multiple values and attributes with complex values, use the **getItemInfoByType** method.</span></span>

<span data-ttu-id="9664d-119">Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9664d-119">To use this method, read access to the library is required.</span></span> <span data-ttu-id="9664d-120">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="9664d-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9664d-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9664d-121">Requirements</span></span>



| <span data-ttu-id="9664d-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9664d-122">Requirement</span></span> | <span data-ttu-id="9664d-123">Wert</span><span class="sxs-lookup"><span data-stu-id="9664d-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9664d-124">Version</span><span class="sxs-lookup"><span data-stu-id="9664d-124">Version</span></span><br/> | <span data-ttu-id="9664d-125">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="9664d-125">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="9664d-126">DLL</span><span class="sxs-lookup"><span data-stu-id="9664d-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="9664d-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9664d-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9664d-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9664d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9664d-129">**StringCollection. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="9664d-129">**StringCollection.getItemInfoByType**</span></span>](stringcollection-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="9664d-130">**StringCollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="9664d-130">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





