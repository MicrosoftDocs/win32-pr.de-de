---
description: ICE74 überprüft, ob die FASTOEM-Eigenschaft in der Eigenschaften Tabelle nicht erstellt wurde.
ms.assetid: 2af132f0-0ffa-405f-9d05-7cb5d5f826b8
title: ICE74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fe2762710e061f2c88f55893294a40fbac8700f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348455"
---
# <a name="ice74"></a><span data-ttu-id="6338f-103">ICE74</span><span class="sxs-lookup"><span data-stu-id="6338f-103">ICE74</span></span>

<span data-ttu-id="6338f-104">ICE74 überprüft, ob die [**FASTOEM**](fastoem.md) -Eigenschaft in der [Eigenschaften Tabelle](property-table.md)nicht erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="6338f-104">ICE74 verifies that the [**FASTOEM**](fastoem.md) property has not been authored into the [Property table](property-table.md).</span></span>

<span data-ttu-id="6338f-105">Mit der [**FASTOEM**](fastoem.md) -Eigenschaft können OEMs den Zeitaufwand für die erstmalige Installation Windows Installer Anwendungen verkürzen.</span><span class="sxs-lookup"><span data-stu-id="6338f-105">The [**FASTOEM**](fastoem.md) property enables OEMs to reduce the time required to install Windows Installer applications for the first time.</span></span> <span data-ttu-id="6338f-106">Sie kann nach der ersten Installation nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6338f-106">It cannot be used after the first install.</span></span> <span data-ttu-id="6338f-107">Die **FASTOEM** -Eigenschaft darf nicht in der Eigenschaften Tabelle erstellt werden, da dies zu den nachfolgenden Installationen für die Wartung, Entfernung oder Reparatur der Anwendung beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="6338f-107">The **FASTOEM** property must not be authored in the Property table because this interferes with subsequent installations for the maintenance, removal, or repair of the application.</span></span>

<span data-ttu-id="6338f-108">ICE74 überprüft auch, ob die [**UpgradeCode**](upgradecode.md) -Eigenschaft in der [Eigenschaften Tabelle](property-table.md)erstellt wurde und ob der Wert keine NULL-GUID ist {00000000-0000-0000-0000-000000000000} .</span><span class="sxs-lookup"><span data-stu-id="6338f-108">ICE74 also verifies that the [**UpgradeCode**](upgradecode.md) property is authored into the [Property table](property-table.md), and that its value is not a null GUID, {00000000-0000-0000-0000-000000000000}.</span></span>

## <a name="result"></a><span data-ttu-id="6338f-109">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="6338f-109">Result</span></span>

<span data-ttu-id="6338f-110">ICE74 kann die folgenden Fehler veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="6338f-110">ICE74 can post the following errors.</span></span>



| <span data-ttu-id="6338f-111">ICE74-Fehler</span><span class="sxs-lookup"><span data-stu-id="6338f-111">ICE74 error</span></span>                                                                       | <span data-ttu-id="6338f-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6338f-112">Description</span></span>                                                                                             |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6338f-113">Die [**FASTOEM**](fastoem.md) -Eigenschaft kann in der Eigenschaften Tabelle nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6338f-113">The [**FASTOEM**](fastoem.md) property cannot be authored in the Property table.</span></span> | <span data-ttu-id="6338f-114">Die [**FASTOEM**](fastoem.md) -Eigenschaft wurde in der Eigenschaften Tabelle festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6338f-114">The [**FASTOEM**](fastoem.md) property has been set in the Property table.</span></span>                             |
| <span data-ttu-id="6338f-115">" \[ 2 \] " ist kein gültiger [**UpgradeCode**](upgradecode.md).</span><span class="sxs-lookup"><span data-stu-id="6338f-115">'\[2\]' is not a valid [**UpgradeCode**](upgradecode.md).</span></span>                        | <span data-ttu-id="6338f-116">Eine NULL-GUID wurde für die [**UpgradeCode**](upgradecode.md) -Eigenschaft in der Eigenschaften Tabelle eingegeben.</span><span class="sxs-lookup"><span data-stu-id="6338f-116">A null GUID has been entered for the [**UpgradeCode**](upgradecode.md) property in the Property table.</span></span> |



 

<span data-ttu-id="6338f-117">ICE74 kann folgende Warnung veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="6338f-117">ICE74 can post the following warning.</span></span>



| <span data-ttu-id="6338f-118">ICE74-Warnung</span><span class="sxs-lookup"><span data-stu-id="6338f-118">ICE74 warning</span></span>                                                                                                                                                                                             | <span data-ttu-id="6338f-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6338f-119">Description</span></span>                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6338f-120">Die [**UpgradeCode**](upgradecode.md) -Eigenschaft ist in der Eigenschaften Tabelle nicht erstellt.</span><span class="sxs-lookup"><span data-stu-id="6338f-120">The [**UpgradeCode**](upgradecode.md) property is not authored in the Property table.</span></span> <span data-ttu-id="6338f-121">Es wird dringend empfohlen, dass Autoren von Installationspaketen einen **UpgradeCode** für Ihre Anwendung angeben.</span><span class="sxs-lookup"><span data-stu-id="6338f-121">It is strongly recommended that authors of installation packages specify an **UpgradeCode** for their application.</span></span> | <span data-ttu-id="6338f-122">Die [**UpgradeCode**](upgradecode.md) -Eigenschaft ist in der Eigenschaften Tabelle nicht erstellt.</span><span class="sxs-lookup"><span data-stu-id="6338f-122">The [**UpgradeCode**](upgradecode.md) property is not authored in the Property table.</span></span> |



 

## <a name="example"></a><span data-ttu-id="6338f-123">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6338f-123">Example</span></span>

<span data-ttu-id="6338f-124">ICE74 meldet den folgenden Fehler, wenn die [**FASTOEM**](fastoem.md) -Eigenschaft festgelegt ist: FASTOEM</span><span class="sxs-lookup"><span data-stu-id="6338f-124">ICE74 reports the following error if the [**FASTOEM**](fastoem.md) property is set: The FASTOEM</span></span>

``` syntax
 property cannot be authored in the Property table.
```

<span data-ttu-id="6338f-125">[Eigenschaften Tabelle](property-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="6338f-125">[Property Table](property-table.md) (partial)</span></span>



| <span data-ttu-id="6338f-126">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6338f-126">Property</span></span>                   | <span data-ttu-id="6338f-127">Wert</span><span class="sxs-lookup"><span data-stu-id="6338f-127">Value</span></span> |
|----------------------------|-------|
| [<span data-ttu-id="6338f-128">**FASTOEM**</span><span class="sxs-lookup"><span data-stu-id="6338f-128">**FASTOEM**</span></span>](fastoem.md) | <span data-ttu-id="6338f-129">1</span><span class="sxs-lookup"><span data-stu-id="6338f-129">1</span></span>     |



 

<span data-ttu-id="6338f-130">Entfernen Sie die [**FASTOEM**](fastoem.md) -Eigenschaft aus der Eigenschaften Tabelle, um diesen Fehler zu beheben.</span><span class="sxs-lookup"><span data-stu-id="6338f-130">To fix this error remove the [**FASTOEM**](fastoem.md) property from the Property Table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6338f-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6338f-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6338f-132">**FASTOEM-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="6338f-132">**FASTOEM property**</span></span>](fastoem.md)
</dt> <dt>

[<span data-ttu-id="6338f-133">Eigenschaften Tabelle</span><span class="sxs-lookup"><span data-stu-id="6338f-133">Property table</span></span>](property-table.md)
</dt> <dt>

[<span data-ttu-id="6338f-134">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="6338f-134">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



