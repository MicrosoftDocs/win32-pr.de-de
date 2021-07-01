---
description: Grundlegendes zu Parametern im PrintCapabilities-Dokument. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: d317d052-c207-412a-896e-09cb57b0dd5f
title: Parameter im PrintCapabilities-Dokument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6b2ba61f1985fdcd02f40e8e08100725968a8e
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118625"
---
# <a name="parameters-in-the-printcapabilities-document"></a><span data-ttu-id="4fed3-105">Parameter im PrintCapabilities-Dokument</span><span class="sxs-lookup"><span data-stu-id="4fed3-105">Parameters in the PrintCapabilities Document</span></span>

<span data-ttu-id="4fed3-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="4fed3-106">This topic is not current.</span></span> <span data-ttu-id="4fed3-107">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="4fed3-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4fed3-108">Wie unter [Parameterverweiselemente](parameter-reference-elements.md)erläutert, kann auf ParameterInit-Elemente innerhalb von Option-Instanzen verwiesen werden, aber das Parameterkonstrukt verfügt auch über eine Verwendung, die von diesem Elementtyp unabhängig ist.</span><span class="sxs-lookup"><span data-stu-id="4fed3-108">As discussed in [Parameter Reference Elements](parameter-reference-elements.md), ParameterInit elements may be referenced from within Option instances, but the parameter construct also has a use that is independent of this type of element.</span></span>

<span data-ttu-id="4fed3-109">Ein Beispiel für ein Gerätekonfigurationsattribut, das sich gut für die Parameterdarstellung eignet, ist CopyCount.</span><span class="sxs-lookup"><span data-stu-id="4fed3-109">An example of a device configuration attribute that is well suited for parameter representation is CopyCount.</span></span> <span data-ttu-id="4fed3-110">Die zulässigen Werte für dieses Gerätekonfigurationsattribut können einfach und präzise definiert werden, ohne dass sie explizit aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="4fed3-110">The allowed values for this device configuration attribute can be easily and concisely defined without listing each of them explicitly.</span></span> <span data-ttu-id="4fed3-111">Obwohl es zwar mühsam wäre, jeden CopyCount-Wert in einer eigenen Option aufzulisten, können einige Gerätekonfigurationsattribute einfach nicht mit einem Feature-/Optionskonstrukt dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="4fed3-111">Although it would be possible, though tedious, to list each CopyCount value in its own Option, some device configuration attributes simply cannot be represented using a Feature/Option construct.</span></span> <span data-ttu-id="4fed3-112">Betrachten Sie beispielsweise ein Gerät, das eine Textzeichenfolge akzeptiert, die dann verwendet wird, um auf jeder Ausgabeseite ein virtuelles Wasserzeichen zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="4fed3-112">As an example, consider a device that accepts a text string that is then used to produce a virtual watermark on each output page.</span></span> <span data-ttu-id="4fed3-113">Der Satz aller möglichen Textzeichenfolgen kann nicht einfach explizit aufzählen, aber die Textzeichenfolge kann leicht mithilfe eines ParameterDef-Elements beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="4fed3-113">The set of all possible text strings cannot easily be explicitly enumerated, but the text string can easily be described using a ParameterDef element.</span></span>

<span data-ttu-id="4fed3-114">Das Dokument Print Schema Keywords (Schlüsselwörter für Druckschemas) definiert eine Reihe häufig verwendeter Parameterkonstrukte, aber PrintCapabilities-Anbieter können zusätzliche eigene Parameterkonstrukte definieren.</span><span class="sxs-lookup"><span data-stu-id="4fed3-114">The Print Schema Keywords document defines a number of commonly used parameter constructs, but PrintCapabilities providers are free to define additional ones of their own.</span></span> <span data-ttu-id="4fed3-115">Diese privat definierten Parameterkonstrukte sind jedoch nicht auf andere Geräte übertragbar, da ein von einer anderen Partei bereitgestelltes PrintCapabilities-Dokument ein solches Parameterkonstrukt nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="4fed3-115">However, these privately-defined parameter constructs are not portable to other devices, due to the fact that a PrintCapabilities document provided by another party does not define such a parameter construct.</span></span> <span data-ttu-id="4fed3-116">Unabhängig davon, ob schemadefiniert oder privat definiert, muss die ParameterDef-Instanz im PrintCapabilities-Dokument vorhanden sein, bevor der Parameter erkannt und von Clients verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4fed3-116">Whether schema-defined or privately-defined, the ParameterDef instance must be present in the PrintCapabilities document before the parameter is recognized and used by clients.</span></span> <span data-ttu-id="4fed3-117">Diese Parameter werden als *festgelegte Parameter* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="4fed3-117">These parameters are referred to as *designated parameters*.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4fed3-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4fed3-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4fed3-119">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="4fed3-119">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



