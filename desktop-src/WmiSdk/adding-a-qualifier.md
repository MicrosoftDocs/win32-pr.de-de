---
description: Ein Qualifizierer ist eine Daten Zeichenfolge, die weitere Informationen über eine Klasse, eine Instanz, eine Eigenschaft, eine Methode oder einen Parameter bereitstellt.
ms.assetid: 6984b575-b365-49dd-aeab-a763430f434c
ms.tgt_platform: multiple
title: Fügen eines Qualifizierers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5a6f18f2b79bcd25b2b4ca75811157c9091e6eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355466"
---
# <a name="adding-a-qualifier"></a><span data-ttu-id="fa826-103">Fügen eines Qualifizierers</span><span class="sxs-lookup"><span data-stu-id="fa826-103">Adding a Qualifier</span></span>

<span data-ttu-id="fa826-104">Ein Qualifizierer ist eine Daten Zeichenfolge, die weitere Informationen über eine Klasse, eine Instanz, eine Eigenschaft, eine Methode oder einen Parameter bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="fa826-104">A qualifier is a data string that provides more information about a class, instance, property, method, or parameter.</span></span>

<span data-ttu-id="fa826-105">Die folgende Klassendefinition ist ein Beispiel für eine abgeleitete Klasse mit Klassen Qualifizierern.</span><span class="sxs-lookup"><span data-stu-id="fa826-105">The following class definition is an example of a derived class that has class qualifiers.</span></span>

``` syntax
[Dynamic, Provider ("ProviderX")] 
class MyDerivedClass : MyClass
{
    [key] string sKey;
    [Implemented] sint32 ValueMethod();
    [Implemented] sint32 MyMethod ([in, Id(0)] sint32 Param);
};
```

<span data-ttu-id="fa826-106">Qualifizierer können in Standard Qualifizierer, CIM-Qualifizierer und eindeutige Qualifizierer unterteilt werden:</span><span class="sxs-lookup"><span data-stu-id="fa826-106">Qualifiers can be divided into standard qualifiers, CIM qualifiers, and unique qualifiers include the following:</span></span>

-   <span data-ttu-id="fa826-107">Standard Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="fa826-107">Standard qualifier</span></span>

    <span data-ttu-id="fa826-108">Ein Standard Qualifizierer ist ein von WMI definierter Qualifizierer, der häufig in MOF-Code verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fa826-108">A standard qualifier is a qualifier defined by WMI and commonly used in MOF code.</span></span> <span data-ttu-id="fa826-109">Beispielsweise sind die Qualifizierer " [**Dynamic**](dynamic-qualifier.md) " und " [**Read**](standard-qualifiers.md) " Standard Qualifizierer.</span><span class="sxs-lookup"><span data-stu-id="fa826-109">For example, the [**Dynamic**](dynamic-qualifier.md) and [**Read**](standard-qualifiers.md) qualifiers are both standard qualifiers.</span></span> <span data-ttu-id="fa826-110">Weitere Informationen finden Sie unter [WMI-Qualifizierer](wmi-qualifiers.md).</span><span class="sxs-lookup"><span data-stu-id="fa826-110">For more information, see [WMI Qualifiers](wmi-qualifiers.md).</span></span>

-   <span data-ttu-id="fa826-111">CIM Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="fa826-111">CIM qualifier</span></span>

    <span data-ttu-id="fa826-112">Ein CIM-Qualifizierer ist ein Qualifizierer in der CIM-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="fa826-112">A CIM qualifier is a qualifier included in the CIM specification.</span></span> <span data-ttu-id="fa826-113">Während Sie CIM-Qualifizierer in MOF-Code verwenden, sind die Standard Qualifizierer speziell auf WMI zugeschnitten.</span><span class="sxs-lookup"><span data-stu-id="fa826-113">While use CIM qualifiers in MOF code, the standard qualifiers are designed specifically with WMI in mind.</span></span> <span data-ttu-id="fa826-114">Weitere Informationen finden Sie in der DMTF [CIM-Spezifikation](https://www.dmtf.org/spec/cims.html/).</span><span class="sxs-lookup"><span data-stu-id="fa826-114">For more information, see the DMTF [CIM Specification](https://www.dmtf.org/spec/cims.html/).</span></span>

-   <span data-ttu-id="fa826-115">Eindeutige Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="fa826-115">Unique qualifier</span></span>

    <span data-ttu-id="fa826-116">Ein eindeutiger Qualifizierer ist ein Qualifizierer, der speziell für eine neue Klasse durch einen Klassen Anbieter definiert ist</span><span class="sxs-lookup"><span data-stu-id="fa826-116">A unique qualifier is a qualifier defined specifically for a new class by a class provider.</span></span> <span data-ttu-id="fa826-117">Der [**Einheiten**](standard-qualifiers.md) Qualifizierer ist beispielsweise ein nicht standardmäßiger Anbieter spezifischer Qualifizierer.</span><span class="sxs-lookup"><span data-stu-id="fa826-117">For example, the [**Units**](standard-qualifiers.md) qualifier is a nonstandard, provider-specific qualifier.</span></span> <span data-ttu-id="fa826-118">Sie können Ihre eigenen Qualifizierer für die Verwendung mit Ihrem Anbieter erstellen.</span><span class="sxs-lookup"><span data-stu-id="fa826-118">You can create your own qualifiers for use with your provider.</span></span> <span data-ttu-id="fa826-119">Weitere Informationen zum Erstellen eines Anbieters finden Sie unter [Entwickeln eines WMI-Anbieters](developing-a-wmi-provider.md).</span><span class="sxs-lookup"><span data-stu-id="fa826-119">For more information about creating a provider, see [Developing a WMI Provider](developing-a-wmi-provider.md).</span></span>

<span data-ttu-id="fa826-120">Was Ihr Qualifizierer tut, der Hauptprozess, den Sie ausführen, ist die Verwendung des Qualifizierers in Ihrem MOF-Code.</span><span class="sxs-lookup"><span data-stu-id="fa826-120">Whatever your qualifier does, the main process you perform is to use the qualifier in your MOF code.</span></span> <span data-ttu-id="fa826-121">Weitere Informationen finden Sie unter [Anwenden eines Qualifizierers](applying-a-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="fa826-121">For more information, see [Applying a Qualifier](applying-a-qualifier.md).</span></span> <span data-ttu-id="fa826-122">Sie können einen Qualifizierer mit einer qualifiziererkonfiguration weiter beschreiben.</span><span class="sxs-lookup"><span data-stu-id="fa826-122">You can further describe a qualifier with a qualifier flavor.</span></span> <span data-ttu-id="fa826-123">Eine qualifiziererkonfiguration enthält weitere Informationen zur Verwendung eines Qualifizierers durch einen Anbieter.</span><span class="sxs-lookup"><span data-stu-id="fa826-123">A qualifier flavor contains more information regarding how a provider should use a qualifier.</span></span> <span data-ttu-id="fa826-124">Weitere Informationen finden Sie unter [beschreiben eines Qualifizierers mit einer qualifiziererkonfiguration](describing-a-qualifier-with-a-qualifier-flavor.md).</span><span class="sxs-lookup"><span data-stu-id="fa826-124">For more information, see [Describing a Qualifier with a Qualifier Flavor](describing-a-qualifier-with-a-qualifier-flavor.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa826-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fa826-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa826-126">Entwerfen von Managed Object Format-Klassen (MOF)</span><span class="sxs-lookup"><span data-stu-id="fa826-126">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



