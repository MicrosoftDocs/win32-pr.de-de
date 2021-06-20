---
description: Diese Artikel enthalten ausführlichere Informationen zur Bedeutung und Verwendung der Print Schema-Elementtypen.
ms.assetid: 05c7fd07-1c32-409d-8ca5-820038af3440
title: Druckschemaframework
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 570701df700954ad85fb724b9528b7e7912f3174
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407163"
---
# <a name="print-schema-framework"></a><span data-ttu-id="860da-103">Druckschemaframework</span><span class="sxs-lookup"><span data-stu-id="860da-103">Print Schema Framework</span></span>

<span data-ttu-id="860da-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="860da-104">This topic is not current.</span></span> <span data-ttu-id="860da-105">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="860da-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="860da-106">Dieser Abschnitt enthält ausführlichere Informationen zur Bedeutung und Verwendung der Print Schema-Elementtypen.</span><span class="sxs-lookup"><span data-stu-id="860da-106">This section provides more detailed information on the meaning and usage of the Print Schema element types.</span></span> <span data-ttu-id="860da-107">Der Schwerpunkt der anfänglichen Version des Druckschemaframeworks liegt auf der Darstellung von Konfigurationen und Funktionen von Geräteattributen.</span><span class="sxs-lookup"><span data-stu-id="860da-107">The main focus of the initial version of the Print Schema Framework is to represent configurations and capabilities of device attributes.</span></span> <span data-ttu-id="860da-108">Auf hoher Ebene bietet dieses Framework zwei verschiedene Stile zur Beschreibung eines Geräteattributs: als Feature-/Optionskonstrukt oder als Parameterkonstrukt.</span><span class="sxs-lookup"><span data-stu-id="860da-108">At a high level, this framework offers two different styles of describing a device attribute: as a Feature/Option construct, or as a parameter construct.</span></span> <span data-ttu-id="860da-109">Wenn ein Geräteattribut über eine kleine Anzahl verfügbarer Werte oder Zustände verfügt, sollte das Attribut als Feature mit den zulässigen Werten oder Zuständen gekennzeichnet werden, die als Option-Elemente bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="860da-109">If a device attribute has a small number of available values or states, then the attribute should be characterized as a Feature with the allowed values or states referred to as Option elements.</span></span> <span data-ttu-id="860da-110">Wenn dagegen ein Geräteattribut über eine große Anzahl verfügbarer Werte oder Zustände verfügt und der Satz aller möglichen Werte leicht definiert werden kann, ohne auf eine explizite Enumeration zurückzugreifen, sollte das Geräteattribut als Parameter gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="860da-110">Conversely, if a device attribute has a large number of available values or states and the set of all possible values is easily defined without resorting to explicit enumeration, the device attribute should be characterized as a parameter.</span></span> <span data-ttu-id="860da-111">(Ein Parameter wird mithilfe eines ParameterDef-Elements definiert, und eine Parameterinstanz wird mithilfe eines ParameterInit-Elements initialisiert.) Eigenschaftselemente werden in Feature-/Options- und Parameterkonstrukten verwendet, um eine differenziertere Unterscheidung zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="860da-111">(A parameter is defined by means of a ParameterDef element, and a parameter instance is initialized by means of a ParameterInit element.) Property elements are used within Feature/Option and parameter constructs to provide a finer level of differentiation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="860da-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="860da-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="860da-113">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="860da-113">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



