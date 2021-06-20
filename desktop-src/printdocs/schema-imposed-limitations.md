---
description: Erfahren Sie mehr über die Einschränkungen des PrintCapabilities-Schemas. Der PrintCapabilities-Anbieter muss ungültige Konfigurationen erkennen und auflösen.
ms.assetid: 420c5c84-abb8-495a-9b74-dc19a16034fb
title: Schema-Imposed Einschränkungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ee2911d4b90ebc194aa245f398f71575496c877
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404923"
---
# <a name="schema-imposed-limitations"></a><span data-ttu-id="5db44-104">Schema-Imposed Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="5db44-104">Schema-Imposed Limitations</span></span>

<span data-ttu-id="5db44-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="5db44-105">This topic is not current.</span></span> <span data-ttu-id="5db44-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="5db44-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5db44-107">Das PrintCapabilities-Schema bietet PrintCapabilities-Autoren ein erhebliches Maß an Flexibilität und Ausdrucksstärke, das in Gerätebeschreibungen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5db44-107">The PrintCapabilities Schema provides PrintCapabilities authors with a substantial amount of flexibility and expressiveness that can be utilized in device descriptions.</span></span> <span data-ttu-id="5db44-108">Konfigurationsabhängigkeiten schränken diese Flexibilität und Ausdrucksstärke jedoch ein.</span><span class="sxs-lookup"><span data-stu-id="5db44-108">However, configuration dependencies impose a limitation on this flexibility and expressiveness.</span></span> <span data-ttu-id="5db44-109">ParameterDef-Instanzen, die Liste der Feature-Elemente, die Liste der Optionsinstanzen innerhalb der einzelnen Features und die ScoredProperty-Instanzen innerhalb jeder Option dürfen keine Konfigurationsabhängigkeiten enthalten.</span><span class="sxs-lookup"><span data-stu-id="5db44-109">ParameterDef instances, the list of Feature elements, the list of Option instances within each Feature, and the ScoredProperty instances within each Option must not contain configuration dependencies.</span></span> <span data-ttu-id="5db44-110">Der PrintCapabilities-Dokumentanbieter muss ungültige Kombinationen von Konfigurationen erkennen und auflösen.</span><span class="sxs-lookup"><span data-stu-id="5db44-110">The PrintCapabilities document provider must detect invalid combinations of configurations and must resolve them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5db44-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5db44-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5db44-112">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="5db44-112">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



