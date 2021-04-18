---
title: Media. getattributezähltbytype-Methode
description: Die getattributezähltbytype-Methode ruft die Anzahl der Attribute ab, die dem angegebenen Attributnamen und der Sprache zugeordnet sind.
ms.assetid: 5644e823-a9b1-4b02-9dd6-015e524fde64
keywords:
- getattributezähltbytype-Methode, Windows Media Player
- getattributezähltbytype-Methode, Windows Media Player, Medienklasse
- Media Class Windows Media Player, getattributezähltbytype-Methode
topic_type:
- apiref
api_name:
- Media.getAttributeCountByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 613dca43c32322cd5e7de2b2b04605789009cbf6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361025"
---
# <a name="mediagetattributecountbytype-method"></a><span data-ttu-id="bf1c7-106">Media. getattributezähltbytype-Methode</span><span class="sxs-lookup"><span data-stu-id="bf1c7-106">Media.getAttributeCountByType method</span></span>

<span data-ttu-id="bf1c7-107">Die **getattributezähltbytype** -Methode ruft die Anzahl der Attribute ab, die dem angegebenen Attributnamen und der Sprache zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="bf1c7-107">The **getAttributeCountByType** method retrieves the number of attributes associated with the specified attribute name and language.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf1c7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf1c7-108">Syntax</span></span>


```JScript
retVal = Media.getAttributeCountByType(
  name,
  language
)
```



## <a name="parameters"></a><span data-ttu-id="bf1c7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf1c7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf1c7-110">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bf1c7-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf1c7-111">**Zeichenfolge** , die den Namen des Attributs enthält.</span><span class="sxs-lookup"><span data-stu-id="bf1c7-111">**String** containing the name of the attribute.</span></span> <span data-ttu-id="bf1c7-112">Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Referenz](attribute-reference.md)zu Windows Media Player-Attributen.</span><span class="sxs-lookup"><span data-stu-id="bf1c7-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="bf1c7-113">*Sprache* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bf1c7-113">*language* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf1c7-114">**Zeichenfolge** , die die Sprache darstellt.</span><span class="sxs-lookup"><span data-stu-id="bf1c7-114">**String** representing the language.</span></span> <span data-ttu-id="bf1c7-115">Wenn der Wert auf NULL oder "" (leere Zeichenfolge) festgelegt ist, wird die aktuelle Gebiets Schema Zeichenfolge verwendet.</span><span class="sxs-lookup"><span data-stu-id="bf1c7-115">If the value is set to null or "" (empty string), the current locale string is used.</span></span> <span data-ttu-id="bf1c7-116">Andernfalls muss der Wert eine gültige RFC 1766-sprach Zeichenfolge sein, z. b. "en-US".</span><span class="sxs-lookup"><span data-stu-id="bf1c7-116">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf1c7-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bf1c7-117">Return value</span></span>

<span data-ttu-id="bf1c7-118">Diese Methode gibt eine **Zahl** (**Long**) zurück, die die Attribut Anzahl enthält.</span><span class="sxs-lookup"><span data-stu-id="bf1c7-118">This method returns a **Number** (**long**) containing the attribute count.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf1c7-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bf1c7-119">Remarks</span></span>

<span data-ttu-id="bf1c7-120">Diese Methode wird verwendet, um die Anzahl der Attribute zu bestimmen, die einem bestimmten Attributnamen für ein bestimmtes **Medien** Objekt entsprechen.</span><span class="sxs-lookup"><span data-stu-id="bf1c7-120">This method is used to determine the number of attributes corresponding to a particular attribute name for a given **Media** object.</span></span> <span data-ttu-id="bf1c7-121">Index Nummern können dann an die **getItemInfoByType** -Methode weitergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bf1c7-121">Index numbers can then be passed to the **getItemInfoByType** method.</span></span> <span data-ttu-id="bf1c7-122">Dies ist beispielsweise hilfreich, wenn ein Medien Element unter mehreren Genres kategorisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="bf1c7-122">This is useful, for example, when a media item has been categorized under multiple genres.</span></span>

<span data-ttu-id="bf1c7-123">Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bf1c7-123">To use this method, read access to the library is required.</span></span> <span data-ttu-id="bf1c7-124">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="bf1c7-124">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="bf1c7-125">**Windows Media Player 10 Mobile:** Diese Eigenschaft gibt immer 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="bf1c7-125">**Windows Media Player 10 Mobile:** This property always returns 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf1c7-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bf1c7-126">Requirements</span></span>



| <span data-ttu-id="bf1c7-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bf1c7-127">Requirement</span></span> | <span data-ttu-id="bf1c7-128">Wert</span><span class="sxs-lookup"><span data-stu-id="bf1c7-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bf1c7-129">Version</span><span class="sxs-lookup"><span data-stu-id="bf1c7-129">Version</span></span><br/> | <span data-ttu-id="bf1c7-130">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="bf1c7-130">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="bf1c7-131">DLL</span><span class="sxs-lookup"><span data-stu-id="bf1c7-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="bf1c7-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf1c7-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf1c7-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bf1c7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf1c7-134">**Mediaobject**</span><span class="sxs-lookup"><span data-stu-id="bf1c7-134">**MediaObject**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="bf1c7-135">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="bf1c7-135">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="bf1c7-136">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="bf1c7-136">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="bf1c7-137">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="bf1c7-137">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





