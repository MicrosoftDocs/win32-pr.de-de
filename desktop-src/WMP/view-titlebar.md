---
title: View. TitleBar
description: Mit dem TitleBar-Attribut wird ein Wert abgerufen, der angibt, ob die Fenstertitelleiste angezeigt wird.
ms.assetid: 996aa2e0-0313-4a48-adcb-b82f76f38b6a
keywords:
- View. TitleBar-Fenster Media Player
topic_type:
- apiref
api_name:
- VIEW.titleBar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea225103913e3906cf6cd3b129943fbf9b9f165
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367638"
---
# <a name="viewtitlebar"></a><span data-ttu-id="9fbc7-104">View. TitleBar</span><span class="sxs-lookup"><span data-stu-id="9fbc7-104">VIEW.titleBar</span></span>

<span data-ttu-id="9fbc7-105">Mit dem **TitleBar** -Attribut wird ein Wert abgerufen, der angibt, ob die Fenstertitelleiste angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9fbc7-105">The **titleBar** attribute retrieves a value indicating whether the window title bar is shown.</span></span>

``` syntax
        elementID.titleBar
```

## <a name="possible-values"></a><span data-ttu-id="9fbc7-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="9fbc7-106">Possible Values</span></span>

<span data-ttu-id="9fbc7-107">Dieses Attribut ist ein Schreib geschützter **boolescher** Wert.</span><span class="sxs-lookup"><span data-stu-id="9fbc7-107">This attribute is a read-only **Boolean**.</span></span>



| <span data-ttu-id="9fbc7-108">Wert</span><span class="sxs-lookup"><span data-stu-id="9fbc7-108">Value</span></span> | <span data-ttu-id="9fbc7-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9fbc7-109">Description</span></span>                             |
|-------|-----------------------------------------|
| <span data-ttu-id="9fbc7-110">true</span><span class="sxs-lookup"><span data-stu-id="9fbc7-110">true</span></span>  | <span data-ttu-id="9fbc7-111">Standard.</span><span class="sxs-lookup"><span data-stu-id="9fbc7-111">Default.</span></span> <span data-ttu-id="9fbc7-112">Die Fenstertitelleiste wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9fbc7-112">The window title bar is shown.</span></span> |
| <span data-ttu-id="9fbc7-113">false</span><span class="sxs-lookup"><span data-stu-id="9fbc7-113">false</span></span> | <span data-ttu-id="9fbc7-114">Die Fenstertitelleiste wird nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9fbc7-114">The window title bar is not shown.</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="9fbc7-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9fbc7-115">Remarks</span></span>

<span data-ttu-id="9fbc7-116">Wenn die Titelleiste angezeigt wird, werden die Schaltflächen "Kontrollkästchen", "minimieren" und "Schließen" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9fbc7-116">If the title bar is shown, the control box, minimize, and close buttons will be shown.</span></span> <span data-ttu-id="9fbc7-117">Der Titel des Fensters ist der Titel des **Ansichts** Elements.</span><span class="sxs-lookup"><span data-stu-id="9fbc7-117">The title of the window will be the title of the **VIEW** element.</span></span>

<span data-ttu-id="9fbc7-118">Wenn **TitleBar** auf true festgelegt ist und der Benutzer versucht, den Wert von " **Video. Zoom**" zu ändern, wird die Änderung nicht durchgeführt, es sei denn, die Skin überwacht den **Zoom** und führt die entsprechende Aktion aus, um die Größe zu ändern.</span><span class="sxs-lookup"><span data-stu-id="9fbc7-118">If **titleBar** is set to true and the user attempts to change the value of **Video.zoom**, the change will not take place unless the skin monitors **zoom** and takes appropriate action to resize itself.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fbc7-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9fbc7-119">Requirements</span></span>



| <span data-ttu-id="9fbc7-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9fbc7-120">Requirement</span></span> | <span data-ttu-id="9fbc7-121">Wert</span><span class="sxs-lookup"><span data-stu-id="9fbc7-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="9fbc7-122">Version</span><span class="sxs-lookup"><span data-stu-id="9fbc7-122">Version</span></span><br/> | <span data-ttu-id="9fbc7-123">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="9fbc7-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9fbc7-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9fbc7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fbc7-125">**View-Element**</span><span class="sxs-lookup"><span data-stu-id="9fbc7-125">**VIEW Element**</span></span>](view-element.md)
</dt> <dt>

[<span data-ttu-id="9fbc7-126">**View. Title**</span><span class="sxs-lookup"><span data-stu-id="9fbc7-126">**VIEW.title**</span></span>](view-title.md)
</dt> <dt>

[<span data-ttu-id="9fbc7-127">**Video. Zoom**</span><span class="sxs-lookup"><span data-stu-id="9fbc7-127">**VIDEO.zoom**</span></span>](video-zoom.md)
</dt> </dl>

 

 





