---
title: Bestimmen eines Attribut Typs
description: Das systemFlags-Attribut eines attributeSchema-Objekts enthält einen Satz von Flags, die verschiedene Qualitäten des Attribut Objekts angeben, z. b. ob das Attribut erstellt oder nicht repliziert wird.
ms.assetid: 58f44ea4-ecbd-4650-b366-37b05a975c68
ms.tgt_platform: multiple
keywords:
- Bestimmen eines Attribut Typs "AD"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b64b4d8b0ae5d6cbac38c9c44ed8e4a7aa5d5f57
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038768"
---
# <a name="determining-an-attribute-type"></a><span data-ttu-id="6983d-104">Bestimmen eines Attribut Typs</span><span class="sxs-lookup"><span data-stu-id="6983d-104">Determining an Attribute Type</span></span>

<span data-ttu-id="6983d-105">Das [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) -Attribut eines [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) -Objekts enthält einen Satz von Flags, die verschiedene Qualitäten des Attribut Objekts angeben, z. b. ob das Attribut erstellt oder nicht repliziert wird.</span><span class="sxs-lookup"><span data-stu-id="6983d-105">The [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) attribute of an [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) object contains a set of flags that indicate various qualities of the attribute object, such as whether the attribute is constructed or non-replicated.</span></span> <span data-ttu-id="6983d-106">In der folgenden Tabelle werden die Flags des **systemFlags** -Attributs aufgelistet, die sich auf den Speichertyp des Attributs auswirken.</span><span class="sxs-lookup"><span data-stu-id="6983d-106">The following table lists the flags of the **systemFlags** attribute that affect the storage type of the attribute.</span></span> 

| <span data-ttu-id="6983d-107">Flagwert</span><span class="sxs-lookup"><span data-stu-id="6983d-107">Flag value</span></span> | <span data-ttu-id="6983d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6983d-108">Description</span></span>                                                                                                          |
|------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6983d-109">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6983d-109">0x00000001</span></span> | <span data-ttu-id="6983d-110">Wenn dieses Flag im [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) -Attribut vorhanden ist, wird das Attribut nicht repliziert.</span><span class="sxs-lookup"><span data-stu-id="6983d-110">If this flag is present in the [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) attribute, the attribute is not replicated.</span></span> |
| <span data-ttu-id="6983d-111">0x00000004</span><span class="sxs-lookup"><span data-stu-id="6983d-111">0x00000004</span></span> | <span data-ttu-id="6983d-112">Wenn dieses Flag im [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) -Attribut vorhanden ist, wird das-Attribut erstellt.</span><span class="sxs-lookup"><span data-stu-id="6983d-112">If this flag is present in the [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) attribute, the attribute is constructed.</span></span>    |



 

<span data-ttu-id="6983d-113">Es ist möglich, eine Abfrage Zeichenfolge zu erstellen, die zum Abfragen von konstruierten oder nicht replizierten Attributen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="6983d-113">It is possible to construct a query string that can be used to query for constructed or non-replicated attributes.</span></span> <span data-ttu-id="6983d-114">Die folgende Abfrage Zeichenfolge findet beispielsweise alle nicht replizierten [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) -Objekte.</span><span class="sxs-lookup"><span data-stu-id="6983d-114">For example, the following query string finds all non-replicated [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) objects.</span></span> <span data-ttu-id="6983d-115">Beachten Sie, dass die Abfrage Zeichenfolge die Dezimal Entsprechung des-Werts erfordert, nicht die hexadezimale Entsprechung des-Werts.</span><span class="sxs-lookup"><span data-stu-id="6983d-115">Be aware that the query string requires the decimal equivalent of the value, not the hexadecimal equivalent of the value.</span></span> <span data-ttu-id="6983d-116">Weitere Informationen zur abgleichsregel-OID, die von dieser Abfrage Zeichenfolge verwendet wird, finden [Sie unter Angeben von Vergleichswerten](how-to-specify-comparison-values.md).</span><span class="sxs-lookup"><span data-stu-id="6983d-116">For more information about the matching rule OID used by this query string, see [How to Specify Comparison Values](how-to-specify-comparison-values.md).</span></span>


```C++
(&(objectCategory=attributeSchema)(systemFlags:1.2.840.113556.1.4.804:=1))
```



<span data-ttu-id="6983d-117">Das [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) -Attribut des [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) -Objekts jedes Attributs definiert, ob ein Attribut indiziert ist. ein indiziertes Attribut hat den Wert 1, ein nicht indiziertes Attribut hat den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="6983d-117">The [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) attribute of each attribute's [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) object defines whether an attribute is indexed; an indexed attribute has a value of 1, a non-indexed attribute has a value of 0.</span></span> <span data-ttu-id="6983d-118">Die folgende Abfrage Zeichenfolge findet z. b. die **attributeSchema** -Objekte, die indizierte Attribute darstellen.</span><span class="sxs-lookup"><span data-stu-id="6983d-118">For example, the following query string finds the **attributeSchema** objects representing indexed attributes.</span></span>


```C++
(&(objectCategory=attributeSchema)(searchFlags=1))
```



<span data-ttu-id="6983d-119">Das [**ismembership ofpartialattributeset**](/windows/desktop/ADSchema/a-ismemberofpartialattributeset) -Attribut des [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) -Objekts jedes Attributs definiert, ob ein Attribut in den globalen Katalog repliziert wird.</span><span class="sxs-lookup"><span data-stu-id="6983d-119">The [**isMemberOfPartialAttributeSet**](/windows/desktop/ADSchema/a-ismemberofpartialattributeset) attribute of each attribute's [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) object defines whether an attribute is replicated to the global catalog.</span></span> <span data-ttu-id="6983d-120">Dieses Attribut hat den Wert **true** , wenn das Attribut ein Member des globalen Katalogs ist, oder **false** , wenn sich die Attribute nicht im globalen Katalog befinden.</span><span class="sxs-lookup"><span data-stu-id="6983d-120">This attribute has a value of **TRUE** if the attribute is a member of the global catalog or **FALSE** if the attributes is not in the global catalog.</span></span> <span data-ttu-id="6983d-121">Beispielsweise durchsucht die folgende Abfrage Zeichenfolge die **attributeSchema** -Objekte, die repliziert werden, in den globalen Katalog.</span><span class="sxs-lookup"><span data-stu-id="6983d-121">For example, the following query string searches the **attributeSchema** objects that are replicated to the global catalog.</span></span>


```C++
(&(objectCategory=attributeSchema)(isMemberOfPartialAttributeSet=TRUE))
```



 

 