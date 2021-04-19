---
title: StringCollection. getattributezähltbytype-Methode
description: Die getattributezähltbytype-Methode ruft die Anzahl der Attribute ab, die dem angegebenen StringCollection-Element Index, dem angegebenen Attributnamen und der angegebenen Sprache zugeordnet sind.
ms.assetid: 3671b7b7-d6d4-4049-8710-d0f34c740b1e
keywords:
- getattributezähltbytype-Methode, Windows Media Player
- getattributecountrytbytype-Methode, Windows Media Player, StringCollection-Klasse
- StringCollection-Klasse, Windows Media Player, getattributezähltbytype-Methode
topic_type:
- apiref
api_name:
- StringCollection.getAttributeCountByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2acf2d7a1f8849f9bd0e83ead3880ca90d2d6149
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361944"
---
# <a name="stringcollectiongetattributecountbytype-method"></a><span data-ttu-id="055b5-106">StringCollection. getattributezähltbytype-Methode</span><span class="sxs-lookup"><span data-stu-id="055b5-106">StringCollection.getAttributeCountByType method</span></span>

<span data-ttu-id="055b5-107">Die **getattributezähltbytype** -Methode ruft die Anzahl der Attribute ab, die dem angegebenen **StringCollection** -Element Index, dem angegebenen Attributnamen und der angegebenen Sprache zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="055b5-107">The **getAttributeCountByType** method retrieves the number of attributes associated with the specified **StringCollection** item index, attribute name, and language.</span></span>

## <a name="syntax"></a><span data-ttu-id="055b5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="055b5-108">Syntax</span></span>


```JScript
retVal = StringCollection.getAttributeCountByType(
  index,
  name,
  language
)
```



## <a name="parameters"></a><span data-ttu-id="055b5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="055b5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="055b5-110">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="055b5-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="055b5-111">**Number** (**Long**) gibt den NULL basierten Index des **StringCollection** -Elements an, aus dem das Attribut bezogen werden soll.</span><span class="sxs-lookup"><span data-stu-id="055b5-111">**Number** (**long**) specifying the zero-based index of the **StringCollection** item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="055b5-112">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="055b5-112">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="055b5-113">**Zeichenfolge** , die den Namen des Attributs enthält.</span><span class="sxs-lookup"><span data-stu-id="055b5-113">**String** containing the name of the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="055b5-114">*Sprache* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="055b5-114">*language* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="055b5-115">**Zeichenfolge** , die die Sprache enthält.</span><span class="sxs-lookup"><span data-stu-id="055b5-115">**String** containing the language.</span></span> <span data-ttu-id="055b5-116">Wenn der Wert auf NULL oder eine leere Zeichenfolge ("") festgelegt ist, wird die aktuelle Gebiets Schema Zeichenfolge verwendet.</span><span class="sxs-lookup"><span data-stu-id="055b5-116">If the value is set to null or the empty string (""), the current locale string is used.</span></span> <span data-ttu-id="055b5-117">Andernfalls muss der Wert eine gültige RFC 1766-sprach Zeichenfolge sein, z. b. "en-US".</span><span class="sxs-lookup"><span data-stu-id="055b5-117">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="055b5-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="055b5-118">Return value</span></span>

<span data-ttu-id="055b5-119">Diese Methode gibt eine **Zahl** (**Long**) zurück.</span><span class="sxs-lookup"><span data-stu-id="055b5-119">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="055b5-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="055b5-120">Remarks</span></span>

<span data-ttu-id="055b5-121">Diese Methode wird verwendet, um die Anzahl der Attribute zu bestimmen, die einem bestimmten Attributnamen für ein bestimmtes **StringCollection** -Element entsprechen.</span><span class="sxs-lookup"><span data-stu-id="055b5-121">This method is used to determine the number of attributes corresponding to a particular attribute name for a particular **StringCollection** item.</span></span> <span data-ttu-id="055b5-122">Index Nummern können dann an den vierten Parameter der **StringCollection. getItemInfoByType** -Methode übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="055b5-122">Index numbers can then be passed to the fourth parameter of the **StringCollection.getItemInfoByType** method.</span></span>

<span data-ttu-id="055b5-123">Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="055b5-123">To use this method, read access to the library is required.</span></span> <span data-ttu-id="055b5-124">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="055b5-124">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="055b5-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="055b5-125">Requirements</span></span>



| <span data-ttu-id="055b5-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="055b5-126">Requirement</span></span> | <span data-ttu-id="055b5-127">Wert</span><span class="sxs-lookup"><span data-stu-id="055b5-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="055b5-128">Version</span><span class="sxs-lookup"><span data-stu-id="055b5-128">Version</span></span><br/> | <span data-ttu-id="055b5-129">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="055b5-129">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="055b5-130">DLL</span><span class="sxs-lookup"><span data-stu-id="055b5-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="055b5-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="055b5-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="055b5-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="055b5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="055b5-133">**StringCollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="055b5-133">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





