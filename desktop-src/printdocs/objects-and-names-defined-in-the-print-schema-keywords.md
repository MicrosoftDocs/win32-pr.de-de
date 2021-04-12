---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 5a07ec21-dc7c-46d5-b1c2-de06f53fe6bf
title: In den Schlüsselwörtern des Druck Schemas definierte Objekte und Namen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2347c73dd647f90a88821658cdcf9e2ed846e83
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104219053"
---
# <a name="objects-and-names-defined-in-the-print-schema-keywords"></a><span data-ttu-id="92f2b-104">In den Schlüsselwörtern des Druck Schemas definierte Objekte und Namen</span><span class="sxs-lookup"><span data-stu-id="92f2b-104">Objects and Names Defined in the Print Schema Keywords</span></span>

<span data-ttu-id="92f2b-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="92f2b-105">This topic is not current.</span></span> <span data-ttu-id="92f2b-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="92f2b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="92f2b-107">Das Print Schema-Framework definiert einen Namespace, der die in den Schlüsselwörtern des Druck Schemas definierten Elemente und XML-Attribute enthält.</span><span class="sxs-lookup"><span data-stu-id="92f2b-107">The Print Schema Framework defines a namespace that includes the elements and XML attributes defined in the Print Schema Keywords.</span></span> <span data-ttu-id="92f2b-108">Dies schließt Elemente wie "Feature", "Option" und "ScoredProperty;" ein. Attributnamen wie "Name" und "propagieren" und Werte für XML-Attribute wie z. b. eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="92f2b-108">This includes elements such as Feature, Option, and ScoredProperty; attribute names such as name and propagate; and values for XML attributes such as constrained.</span></span> <span data-ttu-id="92f2b-109">Anders ausgedrückt: jede Verwendung eines Namens, der in den Schlüsselwörtern des Druck Schemas definiert ist, muss explizit mit diesem Namespace qualifiziert werden oder implizit mit diesem Namespace verknüpft werden, indem ein xmlns-Standard Attribut verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="92f2b-109">In other words, every use of a name that is defined in the Print Schema Keywords should be explicitly qualified with this namespace, or should be implicitly associated with this namespace by the use of a default xmlns attribute.</span></span> <span data-ttu-id="92f2b-110">Das Dokument mit dem Schlüsselwort "Print Schema" definiert die öffentlichen Element Instanzen, die möglicherweise in einem beliebigen Kontext oder Speicherort vorkommen.</span><span class="sxs-lookup"><span data-stu-id="92f2b-110">The Print Schema Keywords document defines the public element instances that may appear in any given context or location.</span></span> <span data-ttu-id="92f2b-111">Element Instanzen dürfen nur innerhalb des Kontexts oder des Speicher Orts angezeigt werden, der im Druck Schema Framework festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="92f2b-111">Element instances must appear only within the context or location designated in the Print Schema Framework.</span></span> <span data-ttu-id="92f2b-112">Beispielsweise muss die <PSF: Option Name = "PSK: Letter" > Instanz, die in den Schlüsselwörtern des Druck Schemas definiert ist, innerhalb der <PSF: Feature Name = "PSK: PageMediaSize" >-Instanz (auch in den Schlüsselwörtern des Druck Schemas definiert) angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="92f2b-112">For example, the <psf:Option name= "psk:Letter"> instance that is defined in the Print Schema Keywords must appear within the <psf:Feature name = "psk:PageMediaSize"> instance (also defined in the Print Schema Keywords).</span></span> <span data-ttu-id="92f2b-113">Sie haben keine Möglichkeit, eine angegebene Options Instanz außerhalb des angegebenen Kontexts zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="92f2b-113">You do not have the freedom to use a given Option instance outside of its specified context.</span></span>

<span data-ttu-id="92f2b-114">Privat definierte Element Instanzen können beliebig angezeigt werden, solange der Elementtyp in einem Kontext angezeigt wird, der vom Druck Schema Framework zugelassen wird.</span><span class="sxs-lookup"><span data-stu-id="92f2b-114">Privately-defined element instances may appear anywhere as long as the element type appears in a context allowed by the Print Schema Framework.</span></span>

## <a name="related-topics"></a><span data-ttu-id="92f2b-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="92f2b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92f2b-116">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="92f2b-116">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



