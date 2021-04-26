---
description: Gibt eine lokalisierte Version des Gerätenamens an.
ms.assetid: 67ebbca0-bdb2-4a6e-98d8-3d8d1029884f
title: modelNameLS-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e47d2f83d1b636efc30e98dff8c46600bcee555d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995497"
---
# <a name="modelnamels-element"></a><span data-ttu-id="c811b-103">modelNameLS-Element</span><span class="sxs-lookup"><span data-stu-id="c811b-103">modelNameLS element</span></span>

<span data-ttu-id="c811b-104">Gibt eine lokalisierte Version des Gerätenamens an.</span><span class="sxs-lookup"><span data-stu-id="c811b-104">Specifies a localized version of the device name.</span></span>

## <a name="usage"></a><span data-ttu-id="c811b-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="c811b-105">Usage</span></span>

``` syntax
<modelNameLS
  Language = "language identifier string"
  Data = "localized model name string"/>
```

## <a name="attributes"></a><span data-ttu-id="c811b-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="c811b-106">Attributes</span></span>



| <span data-ttu-id="c811b-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="c811b-107">Attribute</span></span>               | <span data-ttu-id="c811b-108">type</span><span class="sxs-lookup"><span data-stu-id="c811b-108">Type</span></span>                                   | <span data-ttu-id="c811b-109">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c811b-109">Required</span></span>       | <span data-ttu-id="c811b-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c811b-110">Description</span></span>                                                      |
|-------------------------|----------------------------------------|----------------|------------------------------------------------------------------|
| <span data-ttu-id="c811b-111">**Data**</span><span class="sxs-lookup"><span data-stu-id="c811b-111">**Data**</span></span><br/>     | <span data-ttu-id="c811b-112">Lokalisierte Modellnamenzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c811b-112">localized model name string</span></span><br/> | <span data-ttu-id="c811b-113">Ja</span><span class="sxs-lookup"><span data-stu-id="c811b-113">Yes</span></span><br/> | <span data-ttu-id="c811b-114">Der lokalisierte Modellname.</span><span class="sxs-lookup"><span data-stu-id="c811b-114">The localized model name.</span></span><br/> <br/>                 |
| <span data-ttu-id="c811b-115">**Sprache**</span><span class="sxs-lookup"><span data-stu-id="c811b-115">**Language**</span></span><br/> | <span data-ttu-id="c811b-116">Sprachbezeichnerzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c811b-116">language identifier string</span></span><br/>  | <span data-ttu-id="c811b-117">Ja</span><span class="sxs-lookup"><span data-stu-id="c811b-117">Yes</span></span><br/> | <span data-ttu-id="c811b-118">Die Sprache des lokalisierten Modellnamens.</span><span class="sxs-lookup"><span data-stu-id="c811b-118">The language of the localized model name.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="c811b-119">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c811b-119">Child elements</span></span>

<span data-ttu-id="c811b-120">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="c811b-120">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="c811b-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c811b-121">Parent elements</span></span>



| <span data-ttu-id="c811b-122">Element</span><span class="sxs-lookup"><span data-stu-id="c811b-122">Element</span></span>                                                   | <span data-ttu-id="c811b-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c811b-123">Description</span></span>                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c811b-124">**thisModelMetadata**</span><span class="sxs-lookup"><span data-stu-id="c811b-124">**thisModelMetadata**</span></span>](thismodelmetadata.md)<br/> | <span data-ttu-id="c811b-125">Definiert die Hersteller- und Modellmetadaten für das zu implementierte Gerät.</span><span class="sxs-lookup"><span data-stu-id="c811b-125">Defines the manufacturer and model metadata for the device to be implemented.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="c811b-126">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="c811b-126">Element information</span></span>



| <span data-ttu-id="c811b-127">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="c811b-127">Label</span></span> | <span data-ttu-id="c811b-128">Wert</span><span class="sxs-lookup"><span data-stu-id="c811b-128">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="c811b-129">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="c811b-129">Minimum supported system</span></span><br/> | <span data-ttu-id="c811b-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c811b-130">Windows Vista</span></span> |
| <span data-ttu-id="c811b-131">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="c811b-131">Can be empty</span></span>                        | <span data-ttu-id="c811b-132">Ja</span><span class="sxs-lookup"><span data-stu-id="c811b-132">Yes</span></span>           |



 

 




