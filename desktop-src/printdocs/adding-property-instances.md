---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: dac287a9-77ca-44d8-8019-b05e4c61dc52
title: Hinzufügen von Eigenschaften Instanzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08e3df1b6c271c37c080968cc775ac11eba2e3ce
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104393874"
---
# <a name="adding-property-instances"></a><span data-ttu-id="46a2e-104">Hinzufügen von Eigenschaften Instanzen</span><span class="sxs-lookup"><span data-stu-id="46a2e-104">Adding Property Instances</span></span>

<span data-ttu-id="46a2e-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="46a2e-105">This topic is not current.</span></span> <span data-ttu-id="46a2e-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="46a2e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="46a2e-107">Mit dem Druck Schema können Eigenschaften Instanzen in einer Options Instanz vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="46a2e-107">The Print Schema allows Property instances to be present in an Option instance.</span></span> <span data-ttu-id="46a2e-108">Die im printfunktionalitäten-Dokument definierten Eigenschaften Instanzen werden nicht an die Options Instanzen weitergegeben, die in PrintTicket gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="46a2e-108">The Property instances defined in the PrintCapabilities document are not propagated to the Option instances saved in the PrintTicket.</span></span> <span data-ttu-id="46a2e-109">Eigenschaften Elemente wirken sich nicht auf das Ergebnis des Bewertungsprozesses aus, wenn zwei Options Instanzen verglichen werden, die ScoredProperty-Instanzen sich jedoch auf diesen Prozess auswirken.</span><span class="sxs-lookup"><span data-stu-id="46a2e-109">Property elements do not affect the result of the scoring process when two Option instances are compared, but ScoredProperty instances do affect this process.</span></span> <span data-ttu-id="46a2e-110">Alle Gerätetreiber, die einen Bewertungs Algorithmus implementieren, sollten diese Konvention beachten.</span><span class="sxs-lookup"><span data-stu-id="46a2e-110">All device drivers that implement a scoring algorithm should observe this convention.</span></span> <span data-ttu-id="46a2e-111">Mithilfe von printfunktionsanbietern können einer Option Eigenschafts Instanzen hinzugefügt werden, wenn diese Instanzen für diese bestimmte Option spezifisch sind, oder wenn der Anbieter beabsichtigt, dass der Wert dieser Eigenschaft für jede Option in der Funktion angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="46a2e-111">PrintCapabilities providers are permitted to add Property instances to an Option if these instances are specific to that particular Option and no others, or if the provider intends for the value of this Property to appear for every Option in the Feature.</span></span> <span data-ttu-id="46a2e-112">Angenommen, die printrate-Eigenschaft ist abhängig von der Option, die für die Funktion PageResolution ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="46a2e-112">For example, suppose that the PrintRate Property is dependent on the Option selected for the PageResolution Feature.</span></span> <span data-ttu-id="46a2e-113">Wenn die printrate-Eigenschaft auf der Stamm Ebene des printfunktionalitäten-Dokuments abgelegt wurde, wäre sie einwertig und würde nur die Druck Rate für die aktuell ausgewählte Auflösung widerspiegeln.</span><span class="sxs-lookup"><span data-stu-id="46a2e-113">If the PrintRate Property were placed at the root level of the PrintCapabilities document, it would be single-valued and would reflect only the print rate for the currently selected resolution.</span></span> <span data-ttu-id="46a2e-114">Wenn jedoch die printrate-Eigenschaft in jeder PageResolution-Option platziert wurde, kann jede Instanz der printrate-Eigenschaft die Druck Rate für die PageResolution-Option widerspiegeln, in der Sie enthalten war.</span><span class="sxs-lookup"><span data-stu-id="46a2e-114">However, if the PrintRate Property were placed within each PageResolution Option, each instance of the PrintRate Property could reflect the print rate for the PageResolution Option that contained it.</span></span> <span data-ttu-id="46a2e-115">Das Dokument printfunktionalitäten enthält mehrere Definitionen für printrate, eines für jede PageResolution-Option.</span><span class="sxs-lookup"><span data-stu-id="46a2e-115">The PrintCapabilities document would contain multiple definitions for PrintRate, one corresponding to each PageResolution Option.</span></span> <span data-ttu-id="46a2e-116">Mit einer kurz Darstellung enthalten die printfunktionen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="46a2e-116">Using a shorthand representation, the PrintCapabilities would contain:</span></span>

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

<span data-ttu-id="46a2e-117">In einigen Situationen ist das Platzieren einer Drucksatz Eigenschaft in jeder Auflösungs Option für den Client bequemer, da der Client auf einen Blick festlegen kann, welche Auswirkung die einzelnen Auflösungsoptionen auf die Druck Rate haben, ohne dass für jede Auflösungseinstellung ein neues printfunktionalitäten-Dokument erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="46a2e-117">In some situations, placing a print rate Property within each resolution Option is more convenient for the client, because the client can determine at a glance the effect that each resolution Option has on the print rate, without the need for obtaining a new PrintCapabilities document for each resolution setting.</span></span>

<span data-ttu-id="46a2e-118">Beachten Sie auch, dass Eigenschaften Instanzen auch als untergeordnete Elemente von Funktions Elementen hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="46a2e-118">Note also that Property instances can also be added as child elements of Feature elements.</span></span> <span data-ttu-id="46a2e-119">Dies ist nützlich, wenn Eigenschafts Instanzen oder-Werte von Eigenschaften Instanzen vorhanden sind, die für die einzelnen Features spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="46a2e-119">This is useful if there are Property instances or values of Property instances that are specific to each Feature.</span></span> <span data-ttu-id="46a2e-120">Es kann z. b. eine Eigenschaft geben, die angibt, ob nur eine Option gleichzeitig für eine Funktion ausgewählt werden darf oder ob mehrere Optionen ausgewählt werden können.</span><span class="sxs-lookup"><span data-stu-id="46a2e-120">For example, there might be a Property that specifies whether only one Option is permitted to be selected at one time for a Feature, or whether multiple Options may be selected.</span></span> <span data-ttu-id="46a2e-121">Dabei handelt es sich um die Auswahl \_ . Wählen Sie \_ viele in PPD-und GPD-Dateien verwendete Eigenschaften aus.</span><span class="sxs-lookup"><span data-stu-id="46a2e-121">This is the PICK\_ONE, PICK\_MANY property used in PPD and GPD files.</span></span> <span data-ttu-id="46a2e-122">Da einige featureinstanzen möglicherweise als Pick \_ 1 identifiziert werden, während andere als "Pick many" bezeichnet werden \_ , muss diese Eigenschaft für jede Funktion definiert werden.</span><span class="sxs-lookup"><span data-stu-id="46a2e-122">Because some Feature instances might be identified as PICK\_ONE, while others might be identified as PICK\_MANY, this Property must be defined for each Feature.</span></span> <span data-ttu-id="46a2e-123">Wenn Sie die-Eigenschaft als untergeordnetes Element der-Funktion suchen, wird die Zuordnung zwischen der-Eigenschaft und der-Funktion erzeugt.</span><span class="sxs-lookup"><span data-stu-id="46a2e-123">Locating the Property as a child element of the Feature produces the association between the Property and the Feature.</span></span>

## <a name="related-topics"></a><span data-ttu-id="46a2e-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="46a2e-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46a2e-125">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="46a2e-125">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



