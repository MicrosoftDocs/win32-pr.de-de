---
description: Stellen Sie Attribute als Feature-/Optionskonstrukte oder als Parameter dar. Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 055e502d-631f-49d2-8577-65396373d478
title: Darstellen von Attributen als Feature-/Optionskonstrukte oder als Parameter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c93f4de56709ed310a7f0aa259b1dbfd3377ed42
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120055"
---
# <a name="representing-attributes-as-featureoption-constructs-or-as-parameters"></a><span data-ttu-id="cbc75-105">Darstellen von Attributen als Feature-/Optionskonstrukte oder als Parameter</span><span class="sxs-lookup"><span data-stu-id="cbc75-105">Representing Attributes as Feature/Option Constructs or as Parameters</span></span>

<span data-ttu-id="cbc75-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="cbc75-106">This topic is not current.</span></span> <span data-ttu-id="cbc75-107">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="cbc75-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="cbc75-108">Der Autor eines PrintCapabilities-Dokuments definiert Geräteattribute, aus denen sich die Konfiguration setzt.</span><span class="sxs-lookup"><span data-stu-id="cbc75-108">The author of a PrintCapabilities document defines device attributes that make up the configuration.</span></span> <span data-ttu-id="cbc75-109">Im PrintCapabilities-Dokument kann der Autor ein Geräteattribut entweder als Feature-/Optionskonstrukt oder als Parameterkonstrukt darstellen.</span><span class="sxs-lookup"><span data-stu-id="cbc75-109">In the PrintCapabilities document, the author can choose to represent a device attribute either as a Feature/Option construct or as a parameter construct.</span></span>

<span data-ttu-id="cbc75-110">Wenn ein Geräteattribut über eine relativ kleine Anzahl möglicher Zustände verfügt, die nicht in ein offensichtliches Muster fallen, ist ein Feature/Option-Konstrukt in der Regel die bessere Wahl.</span><span class="sxs-lookup"><span data-stu-id="cbc75-110">If a device attribute has a relatively small number of possible states that do not fall into any sort of obvious pattern, a Feature/Option construct is usually the better choice.</span></span> <span data-ttu-id="cbc75-111">Wenn beispielsweise die zulässigen Werte für das PageMediaSize-Geräteattribut die Werte Letter, Legal, A4ISO,Oid und Envelope10 sind, ist ein Feature/Option-Konstrukt die bessere Wahl für die Darstellung.</span><span class="sxs-lookup"><span data-stu-id="cbc75-111">For example, if the allowed values for the PageMediaSize device attribute are the values Letter, Legal, A4ISO, Tabloid, and Envelope10, a Feature/Option construct would be the better choice for representation.</span></span> <span data-ttu-id="cbc75-112">Aufgrund der Schwierigkeiten und Mehrdeutigkeiten, die mit dem Ausdrücken der zulässigen Werte ohne explizite Enumeration verbunden sind, ist das Parameterkonstrukt für das PageMediaSize-Attribut nicht geeignet.</span><span class="sxs-lookup"><span data-stu-id="cbc75-112">Because of the difficulty and ambiguity associated with expressing the allowable values without explicit enumeration, the parameter construct is not appropriate for the PageMediaSize attribute.</span></span>

<span data-ttu-id="cbc75-113">Wenn ein Geräteattribut durch einen Bereich von ganzen Zahlen dargestellt werden kann, ist die Parameterdarstellung in der Regel die bessere Wahl, insbesondere für Bereiche, die viele Werte enthalten.</span><span class="sxs-lookup"><span data-stu-id="cbc75-113">If a device attribute can be represented by a range of integers, parameter representation is usually the better choice, especially for ranges that include many values.</span></span> <span data-ttu-id="cbc75-114">Wenn das CopyCount-Geräteattribut für ein bestimmtes Druckermodell beispielsweise zwischen 1 und 99.999 liegen kann, sollte dieses Attribut als Parameter kategorisiert werden, indem eine ParameterDef-Instanz definiert wird.</span><span class="sxs-lookup"><span data-stu-id="cbc75-114">For example, if the CopyCount device attribute for a particular model of printer can range from 1 through 99,999, then this attribute should be categorized as a parameter, by defining a ParameterDef instance.</span></span> <span data-ttu-id="cbc75-115">Weisen Sie den Standardeigenschafteninstanzen MinValue und MaxValue Werte des ParametersDef-Elements zu, um den Wertebereich für das JobCopyCount-Attribut zu definieren.</span><span class="sxs-lookup"><span data-stu-id="cbc75-115">Assign values to the MinValue and MaxValue standard Property instances of the ParameterDef element to define the range of values for the JobCopyCount attribute.</span></span> <span data-ttu-id="cbc75-116">Aufgrund der großen Anzahl von Werten, die explizit als Option-Elemente aufgeführt werden müssen, ist die Feature-/Optionsdarstellung für das JobCopyCount-Geräteattribut nicht geeignet.</span><span class="sxs-lookup"><span data-stu-id="cbc75-116">Because of the large number of values that must be explicitly listed as Option elements, Feature/Option representation is not appropriate for the JobCopyCount device attribute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cbc75-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cbc75-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbc75-118">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="cbc75-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



