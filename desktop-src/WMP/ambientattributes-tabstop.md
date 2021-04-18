---
title: Ambientattribute. Tabstopps
description: Mit dem Tabstopps-Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob sich das Steuerelement in der Tabstopps-Reihenfolge befindet Sie legen die Reihenfolge der Tabstopps fest, indem Sie das-Steuerelement im gesamten Skript vor oder nach anderen Steuerelement Tags platzieren.
ms.assetid: 3d4b7fe4-1032-44e1-bae5-f253d00881bf
keywords:
- Ambientattribute. tabstoppwindows-Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.tabStop
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4005fc26a2bc5f928cde0f5ed67ec2098cf3e6bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365769"
---
# <a name="ambientattributestabstop"></a><span data-ttu-id="5a159-105">Ambientattribute. Tabstopps</span><span class="sxs-lookup"><span data-stu-id="5a159-105">AmbientAttributes.tabStop</span></span>

<span data-ttu-id="5a159-106">Mit dem Tabstopps-Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob sich das Steuerelement in der **Tabstopps** -Reihenfolge befindet</span><span class="sxs-lookup"><span data-stu-id="5a159-106">The **tabStop** attribute specifies or retrieves a value indicating whether the control is in the tabbing order.</span></span> <span data-ttu-id="5a159-107">Sie legen die Reihenfolge der Tabstopps fest, indem Sie das-Steuerelement im gesamten Skript vor oder nach anderen Steuerelement Tags platzieren.</span><span class="sxs-lookup"><span data-stu-id="5a159-107">You set the tabbing order by placing the control in the overall script before or after other control tags.</span></span>

``` syntax
        elementID.tabStop
```

## <a name="possible-values"></a><span data-ttu-id="5a159-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="5a159-108">Possible Values</span></span>

<span data-ttu-id="5a159-109">Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="5a159-109">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="5a159-110">Wert</span><span class="sxs-lookup"><span data-stu-id="5a159-110">Value</span></span> | <span data-ttu-id="5a159-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5a159-111">Description</span></span>                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a159-112">true</span><span class="sxs-lookup"><span data-stu-id="5a159-112">true</span></span>  | <span data-ttu-id="5a159-113">Das Steuerelement befindet sich in der Tabulator Reihenfolge (das Steuerelement verfügt über eine Tabstopp Anforderung).</span><span class="sxs-lookup"><span data-stu-id="5a159-113">Control is in the tabbing order (control will have a tab stop: accessibility requirement).</span></span> |
| <span data-ttu-id="5a159-114">false</span><span class="sxs-lookup"><span data-stu-id="5a159-114">false</span></span> | <span data-ttu-id="5a159-115">Das Steuerelement befindet sich nicht in der Reihenfolge der Registerkarten.</span><span class="sxs-lookup"><span data-stu-id="5a159-115">Control is not in the tabbing order.</span></span>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="5a159-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5a159-116">Remarks</span></span>

<span data-ttu-id="5a159-117">Das **Tabstopps** -Attribut ist für das **Effects** -Element nicht anwendbar.</span><span class="sxs-lookup"><span data-stu-id="5a159-117">The **tabStop** attribute is not applicable to the **EFFECTS** element.</span></span>

<span data-ttu-id="5a159-118">Der Standardwert für dieses Attribut ist true für alle Elemente außer **automenu** und **Text**, die den Standardwert false aufweisen.</span><span class="sxs-lookup"><span data-stu-id="5a159-118">The default value for this attribute is true for all elements except **AUTOMENU** and **TEXT**, which have a default value of false.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a159-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5a159-119">Requirements</span></span>



| <span data-ttu-id="5a159-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5a159-120">Requirement</span></span> | <span data-ttu-id="5a159-121">Wert</span><span class="sxs-lookup"><span data-stu-id="5a159-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="5a159-122">Version</span><span class="sxs-lookup"><span data-stu-id="5a159-122">Version</span></span><br/> | <span data-ttu-id="5a159-123">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="5a159-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5a159-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a159-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a159-125">**Ambient-Attribute**</span><span class="sxs-lookup"><span data-stu-id="5a159-125">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





