---
description: Das Druckschemaframework definiert einen Namespace, der die in den Druckschemaschlüsselwörtern definierten Elemente und XML-Attribute enthält.
ms.assetid: 5a07ec21-dc7c-46d5-b1c2-de06f53fe6bf
title: In den Druckschemaschlüsselwörtern definierte Objekte und Namen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73aabdac90de6743388ca1f4d44e1ad52c020dbd
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408553"
---
# <a name="objects-and-names-defined-in-the-print-schema-keywords"></a><span data-ttu-id="27503-103">In den Druckschemaschlüsselwörtern definierte Objekte und Namen</span><span class="sxs-lookup"><span data-stu-id="27503-103">Objects and Names Defined in the Print Schema Keywords</span></span>

<span data-ttu-id="27503-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="27503-104">This topic is not current.</span></span> <span data-ttu-id="27503-105">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="27503-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="27503-106">Das Druckschemaframework definiert einen Namespace, der die in den Druckschemaschlüsselwörtern definierten Elemente und XML-Attribute enthält.</span><span class="sxs-lookup"><span data-stu-id="27503-106">The Print Schema Framework defines a namespace that includes the elements and XML attributes defined in the Print Schema Keywords.</span></span> <span data-ttu-id="27503-107">Dies schließt Elemente wie Feature, Option und ScoredProperty ein. Attributnamen wie name und propagate; - und -Werte für XML-Attribute, z. B. eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="27503-107">This includes elements such as Feature, Option, and ScoredProperty; attribute names such as name and propagate; and values for XML attributes such as constrained.</span></span> <span data-ttu-id="27503-108">Anders ausgedrückt: Jede Verwendung eines Namens, der in den Schlüsselwörtern des Druckschemas definiert ist, sollte explizit mit diesem Namespace qualifiziert werden oder diesem Namespace implizit durch die Verwendung eines xmlns-Standardattributs zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="27503-108">In other words, every use of a name that is defined in the Print Schema Keywords should be explicitly qualified with this namespace, or should be implicitly associated with this namespace by the use of a default xmlns attribute.</span></span> <span data-ttu-id="27503-109">Das Dokument Print Schema Keywords definiert die öffentlichen Elementinstanzen, die in einem kontext- oder orts angegebenen Kontext angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="27503-109">The Print Schema Keywords document defines the public element instances that may appear in any given context or location.</span></span> <span data-ttu-id="27503-110">Elementinstanzen dürfen nur innerhalb des Kontexts oder der Position angezeigt werden, der bzw. der im Druckschemaframework festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="27503-110">Element instances must appear only within the context or location designated in the Print Schema Framework.</span></span> <span data-ttu-id="27503-111">Beispielsweise muss die <psf:Option name= "psk:Letter">-Instanz, die in den Schlüsselwörtern des Druckschemas definiert ist, in der <psf:Featurename = "psk:PageMediaSize">-Instanz (auch in den Schlüsselwörtern für Druckschemas definiert) angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="27503-111">For example, the <psf:Option name= "psk:Letter"> instance that is defined in the Print Schema Keywords must appear within the <psf:Feature name = "psk:PageMediaSize"> instance (also defined in the Print Schema Keywords).</span></span> <span data-ttu-id="27503-112">Sie haben nicht die Möglichkeit, eine bestimmte Option-Instanz außerhalb des angegebenen Kontexts zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="27503-112">You do not have the freedom to use a given Option instance outside of its specified context.</span></span>

<span data-ttu-id="27503-113">Privat definierte Elementinstanzen können an beliebiger Stelle angezeigt werden, solange der Elementtyp in einem vom Druckschemaframework zugelassenen Kontext angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="27503-113">Privately-defined element instances may appear anywhere as long as the element type appears in a context allowed by the Print Schema Framework.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27503-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="27503-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27503-115">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="27503-115">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



