---
title: Ansicht. Größenänderung
description: Das in der Größe änderbare Attribut Ruft einen Wert ab, der angibt, ob die Größe der Sicht geändert werden kann.
ms.assetid: 4f0e4f31-cf16-498f-823f-da43566043b1
keywords:
- Ansicht. Größenänderung in Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.resizable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed4d61973e34891d336ea5729ea40478c6c32808
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365371"
---
# <a name="viewresizable"></a><span data-ttu-id="40613-104">Ansicht. Größenänderung</span><span class="sxs-lookup"><span data-stu-id="40613-104">VIEW.resizable</span></span>

<span data-ttu-id="40613-105">Das in der **Größe** änderbare Attribut Ruft einen Wert ab, der angibt, ob die Größe der **Sicht** geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="40613-105">The **resizable** attribute retrieves a value indicating whether the **VIEW** can be resized.</span></span>

``` syntax
        elementID.resizable
```

## <a name="possible-values"></a><span data-ttu-id="40613-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="40613-106">Possible Values</span></span>

<span data-ttu-id="40613-107">Dieses Attribut ist ein Schreib geschützter **boolescher** Wert mit einem Standardwert, der dem **TitleBar** -Attribut entspricht.</span><span class="sxs-lookup"><span data-stu-id="40613-107">This attribute is a read-only **Boolean** with a default value equal to the **titlebar** attribute.</span></span>



| <span data-ttu-id="40613-108">Werte</span><span class="sxs-lookup"><span data-stu-id="40613-108">Values</span></span> | <span data-ttu-id="40613-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="40613-109">Description</span></span>             |
|--------|-------------------------|
| <span data-ttu-id="40613-110">true</span><span class="sxs-lookup"><span data-stu-id="40613-110">true</span></span>   | <span data-ttu-id="40613-111">Die Größe der Sicht kann geändert werden.</span><span class="sxs-lookup"><span data-stu-id="40613-111">View can be resized.</span></span>    |
| <span data-ttu-id="40613-112">false</span><span class="sxs-lookup"><span data-stu-id="40613-112">false</span></span>  | <span data-ttu-id="40613-113">Die Größe der Sicht kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="40613-113">View cannot be resized.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="40613-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40613-114">Remarks</span></span>

<span data-ttu-id="40613-115">Wenn keine **TitleBar** und somit kein Fenster oder Rahmen vorhanden ist, müssen Sie die size-Methode verwenden, um die **Größe** des **Ansichts** Elements zu ändern.</span><span class="sxs-lookup"><span data-stu-id="40613-115">If there is no **titlebar**, and therefore no window or border, you must use the **size** method to resize the **VIEW** element.</span></span>

## <a name="requirements"></a><span data-ttu-id="40613-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40613-116">Requirements</span></span>



| <span data-ttu-id="40613-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="40613-117">Requirement</span></span> | <span data-ttu-id="40613-118">Wert</span><span class="sxs-lookup"><span data-stu-id="40613-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="40613-119">Version</span><span class="sxs-lookup"><span data-stu-id="40613-119">Version</span></span><br/> | <span data-ttu-id="40613-120">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="40613-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="40613-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40613-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40613-122">**View-Element**</span><span class="sxs-lookup"><span data-stu-id="40613-122">**VIEW Element**</span></span>](view-element.md)
</dt> </dl>

 

 





