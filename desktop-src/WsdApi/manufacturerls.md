---
description: Gibt eine lokalisierte Version des Herstellernamens an.
ms.assetid: e87de50f-60ec-4c18-b21c-81f7b6928752
title: manufacturerLS-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d24950355c5439d9a99c4ef451f1330772f3459
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993677"
---
# <a name="manufacturerls-element"></a><span data-ttu-id="65a39-103">manufacturerLS-Element</span><span class="sxs-lookup"><span data-stu-id="65a39-103">manufacturerLS element</span></span>

<span data-ttu-id="65a39-104">Gibt eine lokalisierte Version des Herstellernamens an.</span><span class="sxs-lookup"><span data-stu-id="65a39-104">Specifies a localized version of the manufacturer name.</span></span>

## <a name="usage"></a><span data-ttu-id="65a39-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="65a39-105">Usage</span></span>

``` syntax
<manufacturerLS
  Language = "language identifier string"
  Data = "localized manufacturer name string"/>
```

## <a name="attributes"></a><span data-ttu-id="65a39-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="65a39-106">Attributes</span></span>



| <span data-ttu-id="65a39-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="65a39-107">Attribute</span></span>               | <span data-ttu-id="65a39-108">type</span><span class="sxs-lookup"><span data-stu-id="65a39-108">Type</span></span>                                          | <span data-ttu-id="65a39-109">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="65a39-109">Required</span></span>       | <span data-ttu-id="65a39-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="65a39-110">Description</span></span>                                                             |
|-------------------------|-----------------------------------------------|----------------|-------------------------------------------------------------------------|
| <span data-ttu-id="65a39-111">**Data**</span><span class="sxs-lookup"><span data-stu-id="65a39-111">**Data**</span></span><br/>     | <span data-ttu-id="65a39-112">Lokalisierte Name-Zeichenfolge des Herstellers</span><span class="sxs-lookup"><span data-stu-id="65a39-112">localized manufacturer name string</span></span><br/> | <span data-ttu-id="65a39-113">Ja</span><span class="sxs-lookup"><span data-stu-id="65a39-113">Yes</span></span><br/> | <span data-ttu-id="65a39-114">Der lokalisierte Herstellername.</span><span class="sxs-lookup"><span data-stu-id="65a39-114">The localized manufacturer name.</span></span><br/> <br/>                 |
| <span data-ttu-id="65a39-115">**Sprache**</span><span class="sxs-lookup"><span data-stu-id="65a39-115">**Language**</span></span><br/> | <span data-ttu-id="65a39-116">Sprachbezeichnerzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="65a39-116">language identifier string</span></span><br/>         | <span data-ttu-id="65a39-117">Ja</span><span class="sxs-lookup"><span data-stu-id="65a39-117">Yes</span></span><br/> | <span data-ttu-id="65a39-118">Die Sprache des lokalisierten Herstellernamens.</span><span class="sxs-lookup"><span data-stu-id="65a39-118">The language of the localized manufacturer name.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="65a39-119">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="65a39-119">Child elements</span></span>

<span data-ttu-id="65a39-120">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="65a39-120">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="65a39-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="65a39-121">Parent elements</span></span>



| <span data-ttu-id="65a39-122">Element</span><span class="sxs-lookup"><span data-stu-id="65a39-122">Element</span></span>                                                   | <span data-ttu-id="65a39-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="65a39-123">Description</span></span>                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="65a39-124">**thisModelMetadata**</span><span class="sxs-lookup"><span data-stu-id="65a39-124">**thisModelMetadata**</span></span>](thismodelmetadata.md)<br/> | <span data-ttu-id="65a39-125">Definiert die Hersteller- und Modellmetadaten für das zu implementierte Gerät.</span><span class="sxs-lookup"><span data-stu-id="65a39-125">Defines the manufacturer and model metadata for the device to be implemented.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="65a39-126">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="65a39-126">Element information</span></span>



| <span data-ttu-id="65a39-127">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="65a39-127">Label</span></span> | <span data-ttu-id="65a39-128">Wert</span><span class="sxs-lookup"><span data-stu-id="65a39-128">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="65a39-129">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="65a39-129">Minimum supported system</span></span><br/> | <span data-ttu-id="65a39-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="65a39-130">Windows Vista</span></span> |
| <span data-ttu-id="65a39-131">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="65a39-131">Can be empty</span></span>                        | <span data-ttu-id="65a39-132">Ja</span><span class="sxs-lookup"><span data-stu-id="65a39-132">Yes</span></span>           |



 

 




