---
title: Effekte. Zuweisung
description: Mit dem Attribut "attribuwall" wird ein Wert angegeben oder abgerufen, der angibt, ob alle Visualisierungen eingeschlossen werden sollen, die in der Registrierung enthalten sind.
ms.assetid: 8552cc06-05b2-4049-ba7d-f6bd770449e0
keywords:
- Effekte. Zuweisung-Windows-Media Player
topic_type:
- apiref
api_name:
- EFFECTS.allowAll
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56760021fe34522072677e9524fe6636e519e20f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369447"
---
# <a name="effectsallowall"></a><span data-ttu-id="163cf-104">Effekte. Zuweisung</span><span class="sxs-lookup"><span data-stu-id="163cf-104">EFFECTS.allowAll</span></span>

<span data-ttu-id="163cf-105">Mit dem Attribut " **attribuwall** " wird ein Wert angegeben oder abgerufen, der angibt, ob alle Visualisierungen eingeschlossen werden sollen, die in der Registrierung enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="163cf-105">The **allowAll** attribute specifies or retrieves a value indicating whether to include all the visualizations that are in the registry.</span></span>

``` syntax
        elementID.allowAll
```

## <a name="possible-values"></a><span data-ttu-id="163cf-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="163cf-106">Possible Values</span></span>

<span data-ttu-id="163cf-107">Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="163cf-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="163cf-108">Wert</span><span class="sxs-lookup"><span data-stu-id="163cf-108">Value</span></span> | <span data-ttu-id="163cf-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="163cf-109">Description</span></span>                                                         |
|-------|---------------------------------------------------------------------|
| <span data-ttu-id="163cf-110">true</span><span class="sxs-lookup"><span data-stu-id="163cf-110">true</span></span>  | <span data-ttu-id="163cf-111">Standard.</span><span class="sxs-lookup"><span data-stu-id="163cf-111">Default.</span></span> <span data-ttu-id="163cf-112">Ermöglicht das Radfahren aller Visualisierungen auf dem System des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="163cf-112">Allows cycling of all visualizations on the user's system.</span></span> |
| <span data-ttu-id="163cf-113">false</span><span class="sxs-lookup"><span data-stu-id="163cf-113">false</span></span> | <span data-ttu-id="163cf-114">Beschränkt das Radfahren auf Visualisierungen, die in **Effekten** -Tags angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="163cf-114">Limits cycling to visualizations appearing within **EFFECTS** tags.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="163cf-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="163cf-115">Remarks</span></span>

<span data-ttu-id="163cf-116">Wenn dieses Attribut auf false festgelegt ist, können nur die Visualisierungen, die in **Effects** -Tags angezeigt werden, mithilfe von Previous/Next durchlaufen werden.</span><span class="sxs-lookup"><span data-stu-id="163cf-116">If this attribute is set to false, only the visualizations appearing within **EFFECTS** tags can be cycled through using previous/next.</span></span> <span data-ttu-id="163cf-117">Wenn der Wert auf true festgelegt ist, können alle Visualisierungen, die auf dem System des Benutzers registriert sind, durchlaufen werden.</span><span class="sxs-lookup"><span data-stu-id="163cf-117">If it is set to true, then all visualizations that are registered on the user's system can be cycled through.</span></span> <span data-ttu-id="163cf-118">Wenn Sie auf true festgelegt ist und Sie alle Visualisierungen innerhalb von **Effects** -Tags angeben, werden die in diesen Tags angegebenen Attribute auf alle Visualisierungen im System des Benutzers angewendet.</span><span class="sxs-lookup"><span data-stu-id="163cf-118">If it is set to true and you specify any visualizations within **EFFECTS** tags, then the attributes specified in these tags are applied to all visualizations on the user's system.</span></span>

## <a name="requirements"></a><span data-ttu-id="163cf-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="163cf-119">Requirements</span></span>



| <span data-ttu-id="163cf-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="163cf-120">Requirement</span></span> | <span data-ttu-id="163cf-121">Wert</span><span class="sxs-lookup"><span data-stu-id="163cf-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="163cf-122">Version</span><span class="sxs-lookup"><span data-stu-id="163cf-122">Version</span></span><br/> | <span data-ttu-id="163cf-123">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="163cf-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="163cf-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="163cf-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="163cf-125">**Effects-Element**</span><span class="sxs-lookup"><span data-stu-id="163cf-125">**EFFECTS Element**</span></span>](effects-element.md)
</dt> </dl>

 

 





