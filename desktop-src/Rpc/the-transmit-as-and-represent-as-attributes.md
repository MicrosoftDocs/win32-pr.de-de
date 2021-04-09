---
title: Die Transmit_as-und represent_as Attribute
description: In diesem Abschnitt wird die Implementierung der Konvertierung von programmierdatentypen mithilfe der Attribute "", "übertragen" \_ als \ und \ \_ als \ Attribute erläutert.
ms.assetid: 2e1af786-f507-453f-bb10-74805ef6b1a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16760091479a306b9dc9c815c7f3a41b25012ca2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858309"
---
# <a name="the-transmit_as-and-represent_as-attributes"></a><span data-ttu-id="6342f-103">Die Übertragung \_ als und stellt \_ als Attribute dar.</span><span class="sxs-lookup"><span data-stu-id="6342f-103">The transmit\_as and represent\_as Attributes</span></span>

<span data-ttu-id="6342f-104">In diesem Abschnitt wird die Implementierung der Konvertierung von programmierdatentypen mithilfe der Mittelwert **\[** [**Übertragung \_ als**](/windows/desktop/Midl/transmit-as) **\]** und **\[** [**Darstellung \_ als**](/windows/desktop/Midl/represent-as) **\]** Attribute erläutert.</span><span class="sxs-lookup"><span data-stu-id="6342f-104">This section discusses the implementation of programmer data type conversion using the MIDL **\[**[**transmit\_as**](/windows/desktop/Midl/transmit-as)**\]** and **\[**[**represent\_as**](/windows/desktop/Midl/represent-as)**\]** attributes.</span></span> <span data-ttu-id="6342f-105">Die Erörterung finden Sie in den folgenden Abschnitten:</span><span class="sxs-lookup"><span data-stu-id="6342f-105">The discussion is presented in the following sections:</span></span>

-   [<span data-ttu-id="6342f-106">Das Attribut "über **tragen \_ als** "</span><span class="sxs-lookup"><span data-stu-id="6342f-106">The **transmit\_as** Attribute</span></span>](the-transmit-as-attribute.md)
-   [<span data-ttu-id="6342f-107">Der **Typ \_ der \_ xmit** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="6342f-107">The **type\_to\_xmit** Function</span></span>](the-type-to-xmit-function.md)
-   [<span data-ttu-id="6342f-108">Der **Typ \_ aus der \_ xmit** -Funktion</span><span class="sxs-lookup"><span data-stu-id="6342f-108">The **type\_from\_xmit** Function</span></span>](the-type-from-xmit-function.md)
-   [<span data-ttu-id="6342f-109">Die **Type \_ Free \_ xmit** -Funktion</span><span class="sxs-lookup"><span data-stu-id="6342f-109">The **type\_free\_xmit** Function</span></span>](the-type-free-xmit-function.md)
-   [<span data-ttu-id="6342f-110">Die **\_ typfreie \_ inst** -Funktion</span><span class="sxs-lookup"><span data-stu-id="6342f-110">The **type\_free\_inst** Function</span></span>](the-type-free-inst-function.md)
-   [<span data-ttu-id="6342f-111">Das **\_ As** -Attribut.</span><span class="sxs-lookup"><span data-stu-id="6342f-111">The **represent\_as** Attribute</span></span>](the-represent-as-attribute.md)
-   [<span data-ttu-id="6342f-112">Der **benannte \_ Typ \_ aus der \_ lokalen** Funktion.</span><span class="sxs-lookup"><span data-stu-id="6342f-112">The **named\_type\_from\_local** Function</span></span>](the-named-type-from-local-function.md)
-   [<span data-ttu-id="6342f-113">Der **benannte \_ Typ \_ der \_ lokalen** Funktion.</span><span class="sxs-lookup"><span data-stu-id="6342f-113">The **named\_type\_to\_local** Function</span></span>](the-named-type-to-local-function.md)
-   [<span data-ttu-id="6342f-114">Die **benannte \_ \_ typfreie \_ lokale** Funktion</span><span class="sxs-lookup"><span data-stu-id="6342f-114">The **named\_type\_free\_local** Function</span></span>](the-named-type-free-local-function.md)
-   [<span data-ttu-id="6342f-115">Die **benannte \_ \_ typfreie \_ inst** -Funktion</span><span class="sxs-lookup"><span data-stu-id="6342f-115">The **named\_type\_free\_inst** Function</span></span>](the-named-type-free-inst-function.md)

 

 