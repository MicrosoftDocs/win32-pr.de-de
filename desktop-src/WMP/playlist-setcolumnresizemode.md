---
title: Wiedergabeliste. setcolumnresizemode
description: Die setcolumnresizemode-Methode gibt die Größe der indizierten Spalten an.
ms.assetid: 84ca0e60-ca24-4058-ae08-5b9cf3d7c38f
keywords:
- Wiedergabeliste. setcolumnresizemode (Windows Media Player)
topic_type:
- apiref
api_name:
- PLAYLIST.setColumnResizeMode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a1b83020f4400f4f1095c84e281fe498f2b67da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372770"
---
# <a name="playlistsetcolumnresizemode"></a><span data-ttu-id="27752-104">Wiedergabeliste. setcolumnresizemode</span><span class="sxs-lookup"><span data-stu-id="27752-104">PLAYLIST.setColumnResizeMode</span></span>

<span data-ttu-id="27752-105">Die **setcolumnresizemode** -Methode gibt die Größe der indizierten Spalten an.</span><span class="sxs-lookup"><span data-stu-id="27752-105">The **setColumnResizeMode** method specifies how the indexed column sizes itself.</span></span>

``` syntax
        elementID.setColumnResizeMode(column, mode)
```

## <a name="parameters"></a><span data-ttu-id="27752-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="27752-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27752-107"><span id="column"></span><span id="COLUMN"></span>*Kolumne*</span><span class="sxs-lookup"><span data-stu-id="27752-107"><span id="column"></span><span id="COLUMN"></span>*column*</span></span>
</dt> <dd>

<span data-ttu-id="27752-108">**Zahl** (**Long**), die den Index der zu ändernden Spalte angibt.</span><span class="sxs-lookup"><span data-stu-id="27752-108">**Number** (**long**) indicating the index of the column to be changed.</span></span>

</dd> <dt>

<span data-ttu-id="27752-109"><span id="mode"></span><span id="MODE"></span>*Spar*</span><span class="sxs-lookup"><span data-stu-id="27752-109"><span id="mode"></span><span id="MODE"></span>*mode*</span></span>
</dt> <dd>

<span data-ttu-id="27752-110">**Zeichenfolge** , die den Größen Anpassungsmodus angibt.</span><span class="sxs-lookup"><span data-stu-id="27752-110">**String** indicating the sizing mode.</span></span> <span data-ttu-id="27752-111">Enthält einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="27752-111">Contains one of the following values.</span></span>



| <span data-ttu-id="27752-112">Wert</span><span class="sxs-lookup"><span data-stu-id="27752-112">Value</span></span>          | <span data-ttu-id="27752-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="27752-113">Description</span></span>                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27752-114">Autosizeheader</span><span class="sxs-lookup"><span data-stu-id="27752-114">AutosizeHeader</span></span> | <span data-ttu-id="27752-115">Die Größe der Spaltengröße wird an alle Daten in der Spalte und in der Kopfzeile angepasst.</span><span class="sxs-lookup"><span data-stu-id="27752-115">The column resizes to accommodate all data in both the column and the header.</span></span>                                  |
| <span data-ttu-id="27752-116">Autosizedata</span><span class="sxs-lookup"><span data-stu-id="27752-116">AutosizeData</span></span>   | <span data-ttu-id="27752-117">Die Spaltengröße ändert sich, um nur alle Daten in der Spalte zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="27752-117">The column resizes to accommodate all data in the column only.</span></span>                                                 |
| <span data-ttu-id="27752-118">Fest</span><span class="sxs-lookup"><span data-stu-id="27752-118">Fixed</span></span>          | <span data-ttu-id="27752-119">Die Spalte hat eine Größe mit fester Größe.</span><span class="sxs-lookup"><span data-stu-id="27752-119">The column is a fixed size.</span></span>                                                                                    |
| <span data-ttu-id="27752-120">Dehn</span><span class="sxs-lookup"><span data-stu-id="27752-120">Stretches</span></span>      | <span data-ttu-id="27752-121">Die Größe der Spalte ändert sich, um den verbleibenden Platz im **Wiedergabe** Listenelement zu verwenden, nachdem alle anderen Spalten geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="27752-121">The column resizes to use the remaining space in the **PLAYLIST** element after all other columns are resized.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27752-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="27752-122">Return Value</span></span>

<span data-ttu-id="27752-123">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="27752-123">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="27752-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27752-124">Requirements</span></span>



| <span data-ttu-id="27752-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="27752-125">Requirement</span></span> | <span data-ttu-id="27752-126">Wert</span><span class="sxs-lookup"><span data-stu-id="27752-126">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="27752-127">Version</span><span class="sxs-lookup"><span data-stu-id="27752-127">Version</span></span><br/> | <span data-ttu-id="27752-128">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="27752-128">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="27752-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27752-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27752-130">**Wiedergabelisten Element**</span><span class="sxs-lookup"><span data-stu-id="27752-130">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





