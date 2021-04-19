---
title: Ambientattribute. aktiviert
description: Mit dem aktivierten Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob das Steuerelement aktiviert oder deaktiviert ist.
ms.assetid: cf96ab7c-8acd-42b6-b7ca-d084a89c97e2
keywords:
- Ambientattribute. aktivierte Windows-Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.enabled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c34d24e86118a1cca0939d535b6da6e86c2df34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369945"
---
# <a name="ambientattributesenabled"></a><span data-ttu-id="3905f-104">Ambientattribute. aktiviert</span><span class="sxs-lookup"><span data-stu-id="3905f-104">AmbientAttributes.enabled</span></span>

<span data-ttu-id="3905f-105">Mit dem **aktivierten** Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob das Steuerelement aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3905f-105">The **enabled** attribute specifies or retrieves a value indicating whether the control is enabled or disabled.</span></span>

``` syntax
        elementID.enabled
```

## <a name="possible-values"></a><span data-ttu-id="3905f-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="3905f-106">Possible Values</span></span>

<span data-ttu-id="3905f-107">Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="3905f-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="3905f-108">Wert</span><span class="sxs-lookup"><span data-stu-id="3905f-108">Value</span></span> | <span data-ttu-id="3905f-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3905f-109">Description</span></span>               |
|-------|---------------------------|
| <span data-ttu-id="3905f-110">true</span><span class="sxs-lookup"><span data-stu-id="3905f-110">true</span></span>  | <span data-ttu-id="3905f-111">Standard.</span><span class="sxs-lookup"><span data-stu-id="3905f-111">Default.</span></span> <span data-ttu-id="3905f-112">Steuerelement aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3905f-112">Control enabled.</span></span> |
| <span data-ttu-id="3905f-113">false</span><span class="sxs-lookup"><span data-stu-id="3905f-113">false</span></span> | <span data-ttu-id="3905f-114">Steuerelement deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="3905f-114">Control disabled.</span></span>         |



 

## <a name="remarks"></a><span data-ttu-id="3905f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3905f-115">Remarks</span></span>

<span data-ttu-id="3905f-116">Wenn das Steuerelement aktiviert ist, kann es über einen Tabstopp verfügen, und alle Ambient-Ereignisse werden empfangen.</span><span class="sxs-lookup"><span data-stu-id="3905f-116">If the control is enabled, it can have a tab stop, and will receive all ambient events.</span></span> <span data-ttu-id="3905f-117">Wenn diese Option deaktiviert ist, verfügt das Steuerelement nicht über eine Tabstopp Taste und empfängt keine Umgebungs Maus-oder Tastatur Ereignisse, die darauf ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="3905f-117">When disabled, the control does not have a tab stop, and does not receive any ambient mouse or keyboard events fired to it.</span></span> <span data-ttu-id="3905f-118">(Es werden jedoch weiterhin alle anderen Ambient-Ereignisse empfangen, die darauf ausgelöst werden.)</span><span class="sxs-lookup"><span data-stu-id="3905f-118">(However, it will continue to receive all other ambient events fired to it.)</span></span>

<span data-ttu-id="3905f-119">Dieses Attribut wird für das **subview** -Element nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3905f-119">This attribute is not supported for the **SUBVIEW** element.</span></span>

## <a name="requirements"></a><span data-ttu-id="3905f-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3905f-120">Requirements</span></span>



| <span data-ttu-id="3905f-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3905f-121">Requirement</span></span> | <span data-ttu-id="3905f-122">Wert</span><span class="sxs-lookup"><span data-stu-id="3905f-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="3905f-123">Version</span><span class="sxs-lookup"><span data-stu-id="3905f-123">Version</span></span><br/> | <span data-ttu-id="3905f-124">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="3905f-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3905f-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3905f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3905f-126">**Ambient-Attribute**</span><span class="sxs-lookup"><span data-stu-id="3905f-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





