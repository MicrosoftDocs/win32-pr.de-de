---
description: Erfahren Sie mehr über das Hinzufügen von Eigenschafteninstanzen. Mit dem Druckschema können Eigenschaftsinstanzen in einer Option-Instanz vorhanden sein.
ms.assetid: dac287a9-77ca-44d8-8019-b05e4c61dc52
title: Hinzufügen von Eigenschafteninstanzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8085fa10f824f32dc76aef0f1e5f78ca05b22b93
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409693"
---
# <a name="adding-property-instances"></a><span data-ttu-id="299f8-104">Hinzufügen von Eigenschafteninstanzen</span><span class="sxs-lookup"><span data-stu-id="299f8-104">Adding Property Instances</span></span>

<span data-ttu-id="299f8-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="299f8-105">This topic is not current.</span></span> <span data-ttu-id="299f8-106">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="299f8-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="299f8-107">Mit dem Druckschema können Eigenschaftsinstanzen in einer Option-Instanz vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="299f8-107">The Print Schema allows Property instances to be present in an Option instance.</span></span> <span data-ttu-id="299f8-108">Die im PrintCapabilities-Dokument definierten Eigenschafteninstanzen werden nicht an die Option-Instanzen weitergegeben, die im PrintTicket gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="299f8-108">The Property instances defined in the PrintCapabilities document are not propagated to the Option instances saved in the PrintTicket.</span></span> <span data-ttu-id="299f8-109">Eigenschaftselemente wirken sich nicht auf das Ergebnis des Bewertungsprozesses aus, wenn zwei Optionsinstanzen verglichen werden, aber ScoredProperty-Instanzen wirken sich auf diesen Prozess aus.</span><span class="sxs-lookup"><span data-stu-id="299f8-109">Property elements do not affect the result of the scoring process when two Option instances are compared, but ScoredProperty instances do affect this process.</span></span> <span data-ttu-id="299f8-110">Alle Gerätetreiber, die einen Bewertungsalgorithmus implementieren, sollten diese Konvention einhalten.</span><span class="sxs-lookup"><span data-stu-id="299f8-110">All device drivers that implement a scoring algorithm should observe this convention.</span></span> <span data-ttu-id="299f8-111">PrintCapabilities-Anbieter dürfen Einer Option Eigenschafteninstanzen hinzufügen, wenn diese Instanzen spezifisch für diese bestimmte Option und keine anderen sind oder wenn der Anbieter beabsichtigt, dass der Wert dieser Eigenschaft für jede Option in der Funktion angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="299f8-111">PrintCapabilities providers are permitted to add Property instances to an Option if these instances are specific to that particular Option and no others, or if the provider intends for the value of this Property to appear for every Option in the Feature.</span></span> <span data-ttu-id="299f8-112">Angenommen, die PrintRate-Eigenschaft hängt von der Option ab, die für das PageResolution-Feature ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="299f8-112">For example, suppose that the PrintRate Property is dependent on the Option selected for the PageResolution Feature.</span></span> <span data-ttu-id="299f8-113">Wenn die PrintRate-Eigenschaft auf der Stammebene des PrintCapabilities-Dokuments platziert würde, wäre sie einwertig und würde nur die Druckrate für die aktuell ausgewählte Auflösung widerspiegeln.</span><span class="sxs-lookup"><span data-stu-id="299f8-113">If the PrintRate Property were placed at the root level of the PrintCapabilities document, it would be single-valued and would reflect only the print rate for the currently selected resolution.</span></span> <span data-ttu-id="299f8-114">Wenn die PrintRate-Eigenschaft jedoch innerhalb jeder PageResolution-Option platziert wird, kann jede Instanz der PrintRate-Eigenschaft die Druckrate für die PageResolution-Option widerspiegeln, die sie enthielt.</span><span class="sxs-lookup"><span data-stu-id="299f8-114">However, if the PrintRate Property were placed within each PageResolution Option, each instance of the PrintRate Property could reflect the print rate for the PageResolution Option that contained it.</span></span> <span data-ttu-id="299f8-115">Das PrintCapabilities-Dokument würde mehrere Definitionen für PrintRate enthalten, eine für jede PageResolution-Option.</span><span class="sxs-lookup"><span data-stu-id="299f8-115">The PrintCapabilities document would contain multiple definitions for PrintRate, one corresponding to each PageResolution Option.</span></span> <span data-ttu-id="299f8-116">Mithilfe einer Kurzformdarstellung würden die PrintCapabilities Folgendes enthalten:</span><span class="sxs-lookup"><span data-stu-id="299f8-116">Using a shorthand representation, the PrintCapabilities would contain:</span></span>

``` syntax
<psf:Feature name="psk:PageResolution">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:ResolutionX">
      <psf:Value xsi:type="xs:string">800dpi</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:ResolutionY">
      <psf:Value xsi:type="xs:string">600dpi</psf:Value>
    </psf:ScoredProperty>
    <!-- Note: The following Property is not part of the Print Schema Framework -->
    <!-- It is included for illustration purposes. -->
    <!-- It is shown as a privately defined implementation-->
    <Property name="FabrikamES500:PrintRate">
      <Value xsi:type="string">20ppm</Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

<span data-ttu-id="299f8-117">In einigen Situationen ist das Platzieren einer Eigenschaft für die Druckrate innerhalb jeder Auflösungsoption für den Client praktischer, da der Client auf einen Blick den Effekt jeder Auflösungsoption auf die Druckrate bestimmen kann, ohne dass für jede Auflösungseinstellung ein neues PrintCapabilities-Dokument erhalten werden muss.</span><span class="sxs-lookup"><span data-stu-id="299f8-117">In some situations, placing a print rate Property within each resolution Option is more convenient for the client, because the client can determine at a glance the effect that each resolution Option has on the print rate, without the need for obtaining a new PrintCapabilities document for each resolution setting.</span></span>

<span data-ttu-id="299f8-118">Beachten Sie auch, dass Eigenschafteninstanzen auch als untergeordnete Elemente von Feature-Elementen hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="299f8-118">Note also that Property instances can also be added as child elements of Feature elements.</span></span> <span data-ttu-id="299f8-119">Dies ist nützlich, wenn Eigenschafteninstanzen oder Werte von Eigenschafteninstanzen vorhanden sind, die für jedes Feature spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="299f8-119">This is useful if there are Property instances or values of Property instances that are specific to each Feature.</span></span> <span data-ttu-id="299f8-120">Beispielsweise kann eine Eigenschaft vorhanden sein, die angibt, ob nur eine Option gleichzeitig für ein Feature ausgewählt werden darf oder ob mehrere Optionen ausgewählt werden können.</span><span class="sxs-lookup"><span data-stu-id="299f8-120">For example, there might be a Property that specifies whether only one Option is permitted to be selected at one time for a Feature, or whether multiple Options may be selected.</span></span> <span data-ttu-id="299f8-121">Dies ist die \_ PICK ONE- und PICK \_ MANY-Eigenschaft, die in PPD- und GPD-Dateien verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="299f8-121">This is the PICK\_ONE, PICK\_MANY property used in PPD and GPD files.</span></span> <span data-ttu-id="299f8-122">Da einige Featureinstanzen als PICK ONE identifiziert werden \_ können, während andere als PICK MANY identifiziert werden \_ können, muss diese Eigenschaft für jedes Feature definiert werden.</span><span class="sxs-lookup"><span data-stu-id="299f8-122">Because some Feature instances might be identified as PICK\_ONE, while others might be identified as PICK\_MANY, this Property must be defined for each Feature.</span></span> <span data-ttu-id="299f8-123">Das Suchen der Eigenschaft als untergeordnetes Element des Features erzeugt die Zuordnung zwischen der Eigenschaft und dem Feature.</span><span class="sxs-lookup"><span data-stu-id="299f8-123">Locating the Property as a child element of the Feature produces the association between the Property and the Feature.</span></span>

## <a name="related-topics"></a><span data-ttu-id="299f8-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="299f8-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="299f8-125">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="299f8-125">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



