---
description: Die publishfeatures-Aktion schreibt den Status jeder Funktion in die Systemregistrierung.
ms.assetid: 8205e865-e625-43b9-8ce9-cff8026b2717
title: Publishfeatures-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f5356ef89aa2651c470917a9b8d81b79ee83d01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351666"
---
# <a name="publishfeatures-action"></a><span data-ttu-id="dee2b-103">Publishfeatures-Aktion</span><span class="sxs-lookup"><span data-stu-id="dee2b-103">PublishFeatures Action</span></span>

<span data-ttu-id="dee2b-104">Die publishfeatures-Aktion schreibt den Status jeder Funktion in die Systemregistrierung.</span><span class="sxs-lookup"><span data-stu-id="dee2b-104">The PublishFeatures action writes each feature's state into the system registry.</span></span> <span data-ttu-id="dee2b-105">Der Funktionsstatus kann entweder nicht vorhanden, angekündigt oder installiert sein.</span><span class="sxs-lookup"><span data-stu-id="dee2b-105">The feature state may be either absent, advertised, or installed.</span></span> <span data-ttu-id="dee2b-106">Die publishfeatures-Aktion schreibt auch die featurekomponentenzuordnung für jede installierte Funktion in die Systemregistrierung.</span><span class="sxs-lookup"><span data-stu-id="dee2b-106">The PublishFeatures action also writes the feature-component mapping into the system registry for each installed feature.</span></span>

<span data-ttu-id="dee2b-107">Mit der publishfeatures-Aktion werden die [FeatureComponents-Tabelle](featurecomponents-table.md),- [Funktions Tabelle](feature-table.md)und- [Komponenten Tabelle](component-table.md)abgefragt.</span><span class="sxs-lookup"><span data-stu-id="dee2b-107">The PublishFeatures action queries the [FeatureComponents table](featurecomponents-table.md), [Feature table](feature-table.md), and [Component table](component-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="dee2b-108">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="dee2b-108">Sequence Restrictions</span></span>

<span data-ttu-id="dee2b-109">Die publishfeatures-Aktion muss vor [publishproduct](publishproduct-action.md)erfolgen.</span><span class="sxs-lookup"><span data-stu-id="dee2b-109">The PublishFeatures action must come before [PublishProduct](publishproduct-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="dee2b-110">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="dee2b-110">ActionData Messages</span></span>



| <span data-ttu-id="dee2b-111">Feld</span><span class="sxs-lookup"><span data-stu-id="dee2b-111">Field</span></span> | <span data-ttu-id="dee2b-112">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="dee2b-112">Description of action data</span></span>        |
|-------|-----------------------------------|
| <span data-ttu-id="dee2b-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="dee2b-113">\[1\]</span></span> | <span data-ttu-id="dee2b-114">Bezeichner der angekündigten Funktion.</span><span class="sxs-lookup"><span data-stu-id="dee2b-114">Identifier of advertised feature.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="dee2b-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dee2b-115">Remarks</span></span>

<span data-ttu-id="dee2b-116">Die publishfeatures-Aktion veröffentlicht die Komposition aller Features, die für die Ankündigung oder Installation ausgewählt wurden.</span><span class="sxs-lookup"><span data-stu-id="dee2b-116">The PublishFeatures action publishes the composition of all features that are selected to be advertised or installed.</span></span>

 

 



