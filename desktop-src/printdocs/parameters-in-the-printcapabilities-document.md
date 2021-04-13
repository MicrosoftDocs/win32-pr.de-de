---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: d317d052-c207-412a-896e-09cb57b0dd5f
title: Parameter im printfunktionalitäten-Dokument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ecfcfee581014bdb57ff70adebaf5f4c8b6fedc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351829"
---
# <a name="parameters-in-the-printcapabilities-document"></a><span data-ttu-id="1dabf-104">Parameter im printfunktionalitäten-Dokument</span><span class="sxs-lookup"><span data-stu-id="1dabf-104">Parameters in the PrintCapabilities Document</span></span>

<span data-ttu-id="1dabf-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="1dabf-105">This topic is not current.</span></span> <span data-ttu-id="1dabf-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1dabf-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1dabf-107">Wie in [Parameter Verweis Elementen](parameter-reference-elements.md)erläutert, kann auf parameterinit-Elemente in Options Instanzen verwiesen werden, aber das Parameter Konstrukt verfügt auch über eine Verwendung, die von diesem Elementtyp unabhängig ist.</span><span class="sxs-lookup"><span data-stu-id="1dabf-107">As discussed in [Parameter Reference Elements](parameter-reference-elements.md), ParameterInit elements may be referenced from within Option instances, but the parameter construct also has a use that is independent of this type of element.</span></span>

<span data-ttu-id="1dabf-108">Ein Beispiel für ein Geräte Konfigurations Attribut, das sich gut für die Parameter Darstellung eignet, ist CopyCount.</span><span class="sxs-lookup"><span data-stu-id="1dabf-108">An example of a device configuration attribute that is well suited for parameter representation is CopyCount.</span></span> <span data-ttu-id="1dabf-109">Die zulässigen Werte für dieses Geräte Konfigurations Attribut können problemlos und kurz definiert werden, ohne dass Sie explizit aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="1dabf-109">The allowed values for this device configuration attribute can be easily and concisely defined without listing each of them explicitly.</span></span> <span data-ttu-id="1dabf-110">Obwohl es möglich wäre, aber mühsam jeden CopyCount-Wert in einer eigenen Option aufzulisten, können einige Geräte Konfigurations Attribute einfach nicht mithilfe eines Funktions-/optionskonstrukts dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1dabf-110">Although it would be possible, though tedious, to list each CopyCount value in its own Option, some device configuration attributes simply cannot be represented using a Feature/Option construct.</span></span> <span data-ttu-id="1dabf-111">Angenommen, ein Gerät akzeptiert eine Text Zeichenfolge, mit der dann auf jeder Ausgabe Seite ein virtueller Wasserzeichen erzeugt wird.</span><span class="sxs-lookup"><span data-stu-id="1dabf-111">As an example, consider a device that accepts a text string that is then used to produce a virtual watermark on each output page.</span></span> <span data-ttu-id="1dabf-112">Der Satz aller möglichen Text Zeichenfolgen kann nicht leicht explizit aufgelistet werden, aber die Text Zeichenfolge kann problemlos mithilfe eines ParameterDef-Elements beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="1dabf-112">The set of all possible text strings cannot easily be explicitly enumerated, but the text string can easily be described using a ParameterDef element.</span></span>

<span data-ttu-id="1dabf-113">Das Dokument mit den Schlüsselwörtern für den Druck Schema definiert eine Reihe häufig verwendeter Parameterkonstrukte, aber printfunktionalitäten-Anbieter können zusätzliche eigene Parameter definieren.</span><span class="sxs-lookup"><span data-stu-id="1dabf-113">The Print Schema Keywords document defines a number of commonly used parameter constructs, but PrintCapabilities providers are free to define additional ones of their own.</span></span> <span data-ttu-id="1dabf-114">Diese privat definierten Parameterkonstrukte können jedoch nicht auf andere Geräte portiert werden, da ein von einer anderen Partei bereitgestelltes Printworks-Dokument kein solches Parameter Konstrukt definiert.</span><span class="sxs-lookup"><span data-stu-id="1dabf-114">However, these privately-defined parameter constructs are not portable to other devices, due to the fact that a PrintCapabilities document provided by another party does not define such a parameter construct.</span></span> <span data-ttu-id="1dabf-115">Unabhängig davon, ob das Schema definiert oder privat definiert ist, muss die ParameterDef-Instanz im printfunktionalitäten-Dokument vorhanden sein, bevor der Parameter erkannt und von Clients verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1dabf-115">Whether schema-defined or privately-defined, the ParameterDef instance must be present in the PrintCapabilities document before the parameter is recognized and used by clients.</span></span> <span data-ttu-id="1dabf-116">Diese Parameter werden als fest *gelegte Parameter* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="1dabf-116">These parameters are referred to as *designated parameters*.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1dabf-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1dabf-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1dabf-118">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="1dabf-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



