---
title: Column. ColumnID
description: Das ColumnID-Attribut gibt eine Spalten-ID im Wiedergabelisten-Steuerelement an oder ruft diese ab.
ms.assetid: c7b51f0b-e347-46be-a26d-aaa0bce83e0c
keywords:
- Column. ColumnID-Fenster Media Player
topic_type:
- apiref
api_name:
- COLUMN.columnID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4bc9aa6485443ae17486616b030b903a911a8e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352021"
---
# <a name="columncolumnid"></a><span data-ttu-id="b6ef5-104">Column. ColumnID</span><span class="sxs-lookup"><span data-stu-id="b6ef5-104">COLUMN.columnID</span></span>

<span data-ttu-id="b6ef5-105">Das **ColumnID** -Attribut gibt eine Spalten-ID im **Wiedergabe** Listen-Steuerelement an oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="b6ef5-105">The **columnID** attribute specifies or retrieves a column ID in the **PLAYLIST** control.</span></span>

``` syntax
        elementID.columnID
```

## <a name="possible-values"></a><span data-ttu-id="b6ef5-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="b6ef5-106">Possible Values</span></span>

<span data-ttu-id="b6ef5-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="b6ef5-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6ef5-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b6ef5-108">Remarks</span></span>

<span data-ttu-id="b6ef5-109">Bei den **ColumnID** -Werten handelt es sich um dieselben Werte, die mit der **getiteminfo** -Methode für ein **Medien** Objekt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b6ef5-109">The **columnID** values are the same values used with the **getItemInfo** method on a **Media** object.</span></span> <span data-ttu-id="b6ef5-110">Eine Liste kann mithilfe der *Medien* abgerufen werden. **AttributeCount** -Eigenschaft, um die Anzahl der für ein bestimmtes **Medien** Objekt verfügbaren Attribute zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="b6ef5-110">A list can be obtained by using the *Media*.**attributeCount** property to determine the number of attributes available for a given **Media** object.</span></span> <span data-ttu-id="b6ef5-111">Index Nummern können dann mit den *Medien* verwendet werden. die **GetAttributeName** -Methode, um die Namen der Attribute zu bestimmen, die wiederum an *Medien* übermittelt werden können. **getiteminfo**.</span><span class="sxs-lookup"><span data-stu-id="b6ef5-111">Index numbers can then be used with the *Media*.**getAttributeName** method to determine the names of the attributes, which can in turn be passed to *Media*.**getItemInfo**.</span></span> <span data-ttu-id="b6ef5-112">Die **ColumnID** -Eigenschaft kann nur auf diese Werte festgelegt werden, mit Ausnahme einiger Werte, die möglicherweise nicht von *Medien* zurückgegeben werden. **GetAttributeName**.</span><span class="sxs-lookup"><span data-stu-id="b6ef5-112">The **columnID** property can only be set to these values, with the exception of some values that may not be returned by *Media*.**getAttributeName**.</span></span> <span data-ttu-id="b6ef5-113">Diese Werte sind unten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="b6ef5-113">These values are listed below.</span></span>



| <span data-ttu-id="b6ef5-114">Wert</span><span class="sxs-lookup"><span data-stu-id="b6ef5-114">Value</span></span>     | <span data-ttu-id="b6ef5-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b6ef5-115">Description</span></span>                                                                        |
|-----------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b6ef5-116">name</span><span class="sxs-lookup"><span data-stu-id="b6ef5-116">name</span></span>      | <span data-ttu-id="b6ef5-117">Zeigt den Namen des **Medien** Objekts an.</span><span class="sxs-lookup"><span data-stu-id="b6ef5-117">Displays the name of the **Media** object.</span></span>                                         |
| <span data-ttu-id="b6ef5-118">duration</span><span class="sxs-lookup"><span data-stu-id="b6ef5-118">duration</span></span>  | <span data-ttu-id="b6ef5-119">Zeigt die Dauer des **Medien** Objekts an.</span><span class="sxs-lookup"><span data-stu-id="b6ef5-119">Displays the duration of the **Media** object.</span></span>                                     |
| <span data-ttu-id="b6ef5-120">SourceURL</span><span class="sxs-lookup"><span data-stu-id="b6ef5-120">sourceURL</span></span> | <span data-ttu-id="b6ef5-121">Zeigt die URL des **Medien** Objekts an.</span><span class="sxs-lookup"><span data-stu-id="b6ef5-121">Displays the URL of the **Media** object.</span></span>                                          |
| <span data-ttu-id="b6ef5-122">status</span><span class="sxs-lookup"><span data-stu-id="b6ef5-122">status</span></span>    | <span data-ttu-id="b6ef5-123">Zeigt den Status zum Kopieren von Dateien an.</span><span class="sxs-lookup"><span data-stu-id="b6ef5-123">Displays the status of copying files.</span></span>                                              |
| <span data-ttu-id="b6ef5-124">Größe</span><span class="sxs-lookup"><span data-stu-id="b6ef5-124">size</span></span>      | <span data-ttu-id="b6ef5-125">Zeigt die Größe der Datei an, die das **Medien** Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="b6ef5-125">Displays the size of the file that the **Media** object represents.</span></span>                |
| <span data-ttu-id="b6ef5-126">Erweiterung</span><span class="sxs-lookup"><span data-stu-id="b6ef5-126">extension</span></span> | <span data-ttu-id="b6ef5-127">Zeigt die Dateinamenerweiterung der Datei an, die das **Medien** Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="b6ef5-127">Displays the file name extension of the file that the **Media** object represents.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="b6ef5-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b6ef5-128">Requirements</span></span>



| <span data-ttu-id="b6ef5-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b6ef5-129">Requirement</span></span> | <span data-ttu-id="b6ef5-130">Wert</span><span class="sxs-lookup"><span data-stu-id="b6ef5-130">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="b6ef5-131">Version</span><span class="sxs-lookup"><span data-stu-id="b6ef5-131">Version</span></span><br/> | <span data-ttu-id="b6ef5-132">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="b6ef5-132">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b6ef5-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6ef5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6ef5-134">**Column-Element**</span><span class="sxs-lookup"><span data-stu-id="b6ef5-134">**COLUMN Element**</span></span>](column-element.md)
</dt> <dt>

[<span data-ttu-id="b6ef5-135">**Medienobjekt**</span><span class="sxs-lookup"><span data-stu-id="b6ef5-135">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="b6ef5-136">**Media. AttributeCount**</span><span class="sxs-lookup"><span data-stu-id="b6ef5-136">**Media.attributeCount**</span></span>](media-attributecount.md)
</dt> <dt>

[<span data-ttu-id="b6ef5-137">**Media. GetAttributeName**</span><span class="sxs-lookup"><span data-stu-id="b6ef5-137">**Media.getAttributeName**</span></span>](media-getattributename.md)
</dt> <dt>

[<span data-ttu-id="b6ef5-138">**Media. getiteminfo**</span><span class="sxs-lookup"><span data-stu-id="b6ef5-138">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> </dl>

 

 





