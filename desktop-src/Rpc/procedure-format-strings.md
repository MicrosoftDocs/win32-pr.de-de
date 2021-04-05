---
title: Prozedur Format Zeichenfolgen
description: Im folgenden finden Sie eine ausführliche Beschreibung der Format Zeichenfolge. Es assembliert alle Ebenen, die mit verschiedenen Phasen der interpreterentwicklung verknüpft sind.
ms.assetid: fab603ed-1f68-4e0b-9c8d-b9730b8cd389
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e58a9acf10caad23063bdba117dc402e411638
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948976"
---
# <a name="procedure-format-strings"></a><span data-ttu-id="9119f-104">Prozedur Format Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="9119f-104">Procedure Format Strings</span></span>

<span data-ttu-id="9119f-105">Im folgenden finden Sie eine ausführliche Beschreibung der Format Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="9119f-105">The following is a complete format string description.</span></span> <span data-ttu-id="9119f-106">Es assembliert alle Ebenen, die mit verschiedenen Phasen der interpreterentwicklung verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="9119f-106">It assembles all layers related to different stages of the interpreter evolution.</span></span>

## <a name="procedure-descriptor-overview"></a><span data-ttu-id="9119f-107">Übersicht über den Prozedur Deskriptor</span><span class="sxs-lookup"><span data-stu-id="9119f-107">Procedure Descriptor Overview</span></span>

<span data-ttu-id="9119f-108">Ein Prozedur Deskriptor besteht aus den Header Deskriptoren und den Parameter Deskriptoren.</span><span class="sxs-lookup"><span data-stu-id="9119f-108">A procedure descriptor consists of the header descriptors and the parameter descriptors.</span></span> <span data-ttu-id="9119f-109">Die Beschreibung des [**– Oi**](/windows/desktop/Midl/-oi) -Stils wird in Bezug auf die allgemeine Verwendung in der aktuellen RPC-Programmierung als veraltet eingestuft.</span><span class="sxs-lookup"><span data-stu-id="9119f-109">The [**–Oi**](/windows/desktop/Midl/-oi) style description is considered outdated, in terms of common usage in current RPC programming.</span></span> <span data-ttu-id="9119f-110">**– OIF** gilt als aktueller.</span><span class="sxs-lookup"><span data-stu-id="9119f-110">The **–Oif** is considered more current.</span></span>

## <a name="the-oi-style-description"></a><span data-ttu-id="9119f-111">Die Beschreibung des – Oi-Stils</span><span class="sxs-lookup"><span data-stu-id="9119f-111">The –Oi Style Description</span></span>

<span data-ttu-id="9119f-112">Diese Beschreibung besteht aus den folgenden Elementen:</span><span class="sxs-lookup"><span data-stu-id="9119f-112">This description consists of the following:</span></span>

``` syntax
-Oi_style_header_descriptor<>
{-Oi_style_parameter_descriptor<>}*
```

<span data-ttu-id="9119f-113">Der-Header würde zwischen 6 und 16 Bytes umfassen.</span><span class="sxs-lookup"><span data-stu-id="9119f-113">The header would have from 6 to 16 bytes.</span></span>

<span data-ttu-id="9119f-114">Die gesamte Beschreibung wird generiert, wenn im [**– Oi**](/windows/desktop/Midl/-oi) -Modus kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="9119f-114">The complete description is generated when compiling in [**–Oi**](/windows/desktop/Midl/-oi) mode.</span></span> <span data-ttu-id="9119f-115">Im [**– OS**](/windows/desktop/Midl/-os) -Modus werden nur die Parameter Deskriptoren generiert, die für die Konvertierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9119f-115">In [**–Os**](/windows/desktop/Midl/-os) mode, only the parameter descriptors are generated, which are used for conversion.</span></span> <span data-ttu-id="9119f-116">Der Pick-Interpreter verwendet alte Stil Parameter Deskriptoren.</span><span class="sxs-lookup"><span data-stu-id="9119f-116">The pickling interpreter uses old style parameter descriptors.</span></span>

## <a name="the-oif-style-description"></a><span data-ttu-id="9119f-117">Die Beschreibung des – OIF-Stils</span><span class="sxs-lookup"><span data-stu-id="9119f-117">The –Oif Style Description</span></span>

<span data-ttu-id="9119f-118">Die Beschreibung besteht aus den folgenden Elementen:</span><span class="sxs-lookup"><span data-stu-id="9119f-118">The description consists of the following:</span></span>

``` syntax
-Oif_style_header_descriptor<>
{-Oif_style_parameter_descriptor<6>}*
```

<span data-ttu-id="9119f-119">Der Header Deskriptor des [**– OIF**](/windows/desktop/Midl/-oi) -Stils besteht aus</span><span class="sxs-lookup"><span data-stu-id="9119f-119">The [**–Oif**](/windows/desktop/Midl/-oi) style header descriptor consists of</span></span>

<span data-ttu-id="9119f-120">Die Beschreibung des – OIF-Stils wird generiert, wenn im [**– OIF**](/windows/desktop/Midl/-oi) -oder **– Oicf** -Modus des Compilers kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="9119f-120">The –Oif style description is generated when compiling in [**–Oif**](/windows/desktop/Midl/-oi) or **–Oicf** mode of the compiler.</span></span>

``` syntax
-Oi_style_header_descriptor<>
-Oif_extensions_to_the_old_header<6>
```

<span data-ttu-id="9119f-121">Einige neuere Features wie Pipe, Async und [**/robust**](/windows/desktop/Midl/-robust) erzwingen den [**– Oicf**](/windows/desktop/Midl/-oi) -Modus des Compilers, wenn er verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9119f-121">Some more recent features like pipe, async, and [**/robust**](/windows/desktop/Midl/-robust) force the [**–Oicf**](/windows/desktop/Midl/-oi) mode of the compiler, when used.</span></span>

## <a name="the-extended-oif-description"></a><span data-ttu-id="9119f-122">Die erweiterte –-OIF-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9119f-122">The Extended –Oif Description</span></span>

<span data-ttu-id="9119f-123">Die Beschreibung besteht aus den folgenden Elementen:</span><span class="sxs-lookup"><span data-stu-id="9119f-123">The description consists of the following:</span></span>

``` syntax
-Oif_style_header_descriptor<>
extensions_to_the_-Oif_header<8>
{-Oif style parameter descriptors<6>}*
```

 

 