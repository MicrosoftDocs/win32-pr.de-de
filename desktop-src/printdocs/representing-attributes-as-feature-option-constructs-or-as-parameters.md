---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 055e502d-631f-49d2-8577-65396373d478
title: Darstellen von Attributen als Feature/Options-Konstrukte oder als Parameter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2c24843a175337f40a84dcdacc41e1a2ab1e15e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104050730"
---
# <a name="representing-attributes-as-featureoption-constructs-or-as-parameters"></a><span data-ttu-id="9380b-104">Darstellen von Attributen als Feature/Options-Konstrukte oder als Parameter</span><span class="sxs-lookup"><span data-stu-id="9380b-104">Representing Attributes as Feature/Option Constructs or as Parameters</span></span>

<span data-ttu-id="9380b-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="9380b-105">This topic is not current.</span></span> <span data-ttu-id="9380b-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9380b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9380b-107">Der Autor eines printfunktionalitäten-Dokuments definiert Geräte Attribute, die die Konfiguration bilden.</span><span class="sxs-lookup"><span data-stu-id="9380b-107">The author of a PrintCapabilities document defines device attributes that make up the configuration.</span></span> <span data-ttu-id="9380b-108">Im printfunktionalitäten-Dokument kann der Autor ein Geräte Attribut entweder als Funktions-/optionskonstrukt oder als Parameter Konstrukt darstellen.</span><span class="sxs-lookup"><span data-stu-id="9380b-108">In the PrintCapabilities document, the author can choose to represent a device attribute either as a Feature/Option construct or as a parameter construct.</span></span>

<span data-ttu-id="9380b-109">Wenn ein Geräte Attribut über eine relativ kleine Anzahl möglicher Zustände verfügt, die nicht in irgendeiner Art von offensichtlichem Muster vorkommen, ist ein Funktions-/optionskonstrukt normalerweise die bessere Wahl.</span><span class="sxs-lookup"><span data-stu-id="9380b-109">If a device attribute has a relatively small number of possible states that do not fall into any sort of obvious pattern, a Feature/Option construct is usually the better choice.</span></span> <span data-ttu-id="9380b-110">Wenn z. b. die zulässigen Werte für das PageMediaSize-Geräte Attribut die Werte Letter, Legal, A4ISO, Boulevard und Envelope10 sind, wäre ein Funktions-/optionskonstrukt die bessere Wahl für die Darstellung.</span><span class="sxs-lookup"><span data-stu-id="9380b-110">For example, if the allowed values for the PageMediaSize device attribute are the values Letter, Legal, A4ISO, Tabloid, and Envelope10, a Feature/Option construct would be the better choice for representation.</span></span> <span data-ttu-id="9380b-111">Aufgrund der Schwierigkeit und Mehrdeutigkeit im Zusammenhang mit dem Ausdrücken der zulässigen Werte ohne explizite Enumeration ist das Parameter Konstrukt für das PageMediaSize-Attribut nicht geeignet.</span><span class="sxs-lookup"><span data-stu-id="9380b-111">Because of the difficulty and ambiguity associated with expressing the allowable values without explicit enumeration, the parameter construct is not appropriate for the PageMediaSize attribute.</span></span>

<span data-ttu-id="9380b-112">Wenn ein Geräte Attribut durch einen Bereich von ganzen Zahlen dargestellt werden kann, ist die Parameter Darstellung normalerweise die bessere Wahl, insbesondere für Bereiche, die viele Werte enthalten.</span><span class="sxs-lookup"><span data-stu-id="9380b-112">If a device attribute can be represented by a range of integers, parameter representation is usually the better choice, especially for ranges that include many values.</span></span> <span data-ttu-id="9380b-113">Wenn das CopyCount-Geräte Attribut für ein bestimmtes Drucker Modell z. b. zwischen 1 und 99.999 liegen kann, sollte dieses Attribut als Parameter kategorisiert werden, indem eine ParameterDef-Instanz definiert wird.</span><span class="sxs-lookup"><span data-stu-id="9380b-113">For example, if the CopyCount device attribute for a particular model of printer can range from 1 through 99,999, then this attribute should be categorized as a parameter, by defining a ParameterDef instance.</span></span> <span data-ttu-id="9380b-114">Weisen Sie den MinValue-und MaxValue-Standard Eigenschafts Instanzen des ParameterDef-Elements Werte zu, um den Wertebereich für das jobcopycount-Attribut zu definieren.</span><span class="sxs-lookup"><span data-stu-id="9380b-114">Assign values to the MinValue and MaxValue standard Property instances of the ParameterDef element to define the range of values for the JobCopyCount attribute.</span></span> <span data-ttu-id="9380b-115">Aufgrund der großen Anzahl von Werten, die explizit als Options Elemente aufgeführt werden müssen, eignet sich die Funktions-/Options-Darstellung nicht für das jobcopycount-Geräte Attribut.</span><span class="sxs-lookup"><span data-stu-id="9380b-115">Because of the large number of values that must be explicitly listed as Option elements, Feature/Option representation is not appropriate for the JobCopyCount device attribute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9380b-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9380b-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9380b-117">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="9380b-117">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



