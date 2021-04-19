---
title: StringCollection. Item-Methode
description: Die Item-Methode ruft die Zeichenfolge am angegebenen Index ab.
ms.assetid: 5f6afff2-3ecc-4b28-8c67-f859f5440d4f
keywords:
- Element-Methoden Fenster Media Player
- Element-Methode, Windows Media Player, StringCollection-Klasse
- StringCollection-Klasse, Windows Media Player, Element-Methode
topic_type:
- apiref
api_name:
- StringCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4244ad194ff3426dab81baddc0b7188214e0360
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359213"
---
# <a name="stringcollectionitem-method"></a><span data-ttu-id="024c3-106">StringCollection. Item-Methode</span><span class="sxs-lookup"><span data-stu-id="024c3-106">StringCollection.item method</span></span>

<span data-ttu-id="024c3-107">Die **Item** -Methode ruft die Zeichenfolge am angegebenen Index ab.</span><span class="sxs-lookup"><span data-stu-id="024c3-107">The **item** method retrieves the string at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="024c3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="024c3-108">Syntax</span></span>


```JScript
strRetVal = StringCollection.item(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="024c3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="024c3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="024c3-110">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="024c3-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="024c3-111">Die **Zahl** (**Long**), die den Index enthält.</span><span class="sxs-lookup"><span data-stu-id="024c3-111">**Number** (**long**) containing the index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="024c3-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="024c3-112">Return value</span></span>

<span data-ttu-id="024c3-113">Diese Methode gibt eine **Zeichenfolge** zurück.</span><span class="sxs-lookup"><span data-stu-id="024c3-113">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="024c3-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="024c3-114">Remarks</span></span>

<span data-ttu-id="024c3-115">Das **StringCollection** -Objekt wird verwendet, um den Satz von Werten abzurufen, die für ein Attribut verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="024c3-115">The **StringCollection** object is used to retrieve the set of values available for an attribute.</span></span> <span data-ttu-id="024c3-116">Beispielsweise *mediacollection*. die **getAttributeStringCollection** -Methode kann verwendet werden, um ein **StringCollection** -Objekt abzurufen, das alle Werte für das Genre-Attribut im audiomedientyp darstellt.</span><span class="sxs-lookup"><span data-stu-id="024c3-116">For example, the *MediaCollection*.**getAttributeStringCollection** method can be used to retrieve a **StringCollection** object representing all the values for the Genre attribute within the Audio media type.</span></span> <span data-ttu-id="024c3-117">Die **Item** -Eigenschaft kann dann zum Durchlaufen aller möglichen Werte für das Genre-Attribut verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="024c3-117">The **item** property can then be used to iterate through all of the possible values for the Genre attribute.</span></span>

<span data-ttu-id="024c3-118">Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="024c3-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="024c3-119">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="024c3-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="024c3-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="024c3-120">Requirements</span></span>



| <span data-ttu-id="024c3-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="024c3-121">Requirement</span></span> | <span data-ttu-id="024c3-122">Wert</span><span class="sxs-lookup"><span data-stu-id="024c3-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="024c3-123">Version</span><span class="sxs-lookup"><span data-stu-id="024c3-123">Version</span></span><br/> | <span data-ttu-id="024c3-124">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="024c3-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="024c3-125">DLL</span><span class="sxs-lookup"><span data-stu-id="024c3-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="024c3-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="024c3-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="024c3-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="024c3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="024c3-128">**Mediacollection. getAttributeStringCollection**</span><span class="sxs-lookup"><span data-stu-id="024c3-128">**MediaCollection.getAttributeStringCollection**</span></span>](mediacollection-getattributestringcollection.md)
</dt> <dt>

[<span data-ttu-id="024c3-129">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="024c3-129">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="024c3-130">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="024c3-130">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="024c3-131">**StringCollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="024c3-131">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





