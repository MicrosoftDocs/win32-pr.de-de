---
description: Dieser Abschnitt wird von der &\# 0034; IPv6-Adressierungs Architektur&\# 0034; von R kopiert.
ms.assetid: 52faecb9-0d7a-40fa-a021-3cc6816a4db8
title: Text Darstellung von IPv6-Adressen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df97c1c8933f3708fee56e34e05f918d531d2a13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358821"
---
# <a name="text-representation-of-ipv6-addresses"></a><span data-ttu-id="0a177-103">Text Darstellung von IPv6-Adressen</span><span class="sxs-lookup"><span data-stu-id="0a177-103">Text Representation of IPv6 Addresses</span></span>

<span data-ttu-id="0a177-104">Dieser Abschnitt wird von "IPv6-Adressierungs Architektur" von R. Hinder und S. Debug kopiert.</span><span class="sxs-lookup"><span data-stu-id="0a177-104">This section is copied from "IPv6 Addressing Architecture" by R. Hinden and S. Deering.</span></span> <span data-ttu-id="0a177-105">Es gibt drei konventionelle Formen für das darstellen von IPv6-Adressen als Text Zeichenfolgen:</span><span class="sxs-lookup"><span data-stu-id="0a177-105">There are three conventional forms for representing IPv6 addresses as text strings:</span></span>

-   <span data-ttu-id="0a177-106">Das bevorzugte Formular ist "x:x: x:x: x:x: x:x", wobei "x" die hexadezimal Werte der 8 16-Bit-Teile der Adresse sind.</span><span class="sxs-lookup"><span data-stu-id="0a177-106">The preferred form is x:x:x:x:x:x:x:x, where the 'x's are the hexadecimal values of the eight 16-bit pieces of the address.</span></span>

    <span data-ttu-id="0a177-107">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="0a177-107">Examples:</span></span>

    <dl> <span data-ttu-id="0a177-108">FEDC: BA98:7654:3210: FEDC: BA98:7654:3210</span><span class="sxs-lookup"><span data-stu-id="0a177-108">FEDC:BA98:7654:3210:FEDC:BA98:7654:3210</span></span>  
    <span data-ttu-id="0a177-109">1080:0: 0:0: 8:800:200C: 417a</span><span class="sxs-lookup"><span data-stu-id="0a177-109">1080:0:0:0:8:800:200C:417A</span></span>  
    </dl>

> [!Note]  
> <span data-ttu-id="0a177-110">Es ist nicht erforderlich, die führenden Nullen in einem einzelnen Feld zu schreiben, aber es muss mindestens eine Ziffer in jedem Feld vorhanden sein (mit Ausnahme der in der zweiten Form beschriebenen Groß-/Kleinschreibung).</span><span class="sxs-lookup"><span data-stu-id="0a177-110">It is not necessary to write the leading zeros in an individual field, but there must be at least one numeral in every field (except for the case described in the second form).</span></span>

 

-   <span data-ttu-id="0a177-111">Aufgrund der Methode, bestimmte Formatvorlagen von IPv6-Adressen zuzuordnen, ist es üblich, dass Adressen lange Zeichen folgen von Null Bits enthalten.</span><span class="sxs-lookup"><span data-stu-id="0a177-111">Due to the method of allocating certain styles of IPv6 addresses, it is common for addresses to contain long strings of zero bits.</span></span> <span data-ttu-id="0a177-112">Um das Schreiben von Adressen mit 0 Bits zu vereinfachen, ist eine spezielle Syntax zum Komprimieren der Nullen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0a177-112">In order to make writing addresses containing zero bits easier, a special syntax is available to compress the zeros.</span></span> <span data-ttu-id="0a177-113">Die Verwendung doppelter Doppelpunkte ("::") gibt mehrere Gruppen von Nullen mit 16 Bits an.</span><span class="sxs-lookup"><span data-stu-id="0a177-113">The use of double colons ("::") indicates multiple groups of 16-bits of zeros.</span></span>

    <span data-ttu-id="0a177-114">Beispielsweise die Multicast Adresse</span><span class="sxs-lookup"><span data-stu-id="0a177-114">For example, the multicast address</span></span>

    <dl> <span data-ttu-id="0a177-115">FF01:0: 0:0: 0:0: 0:43</span><span class="sxs-lookup"><span data-stu-id="0a177-115">FF01:0:0:0:0:0:0:43</span></span>  
    </dl>

    <span data-ttu-id="0a177-116">kann wie folgt dargestellt werden:</span><span class="sxs-lookup"><span data-stu-id="0a177-116">may be represented as:</span></span>

    <dl> <span data-ttu-id="0a177-117">FF01:: 43</span><span class="sxs-lookup"><span data-stu-id="0a177-117">FF01::43</span></span>  
    </dl>

    <span data-ttu-id="0a177-118">Die doppelten Anführungszeichen ("::") können nur einmal in einer Adresse vorkommen.</span><span class="sxs-lookup"><span data-stu-id="0a177-118">The double quotation marks ("::") can only appear once in an address.</span></span> <span data-ttu-id="0a177-119">Sie können verwendet werden, um führende oder nachfolgende Nullen in einer Adresse zu komprimieren.</span><span class="sxs-lookup"><span data-stu-id="0a177-119">They can be used to compress leading or trailing zeros in an address.</span></span>

-   <span data-ttu-id="0a177-120">Ein alternatives Formular, das beim Umgang mit einer gemischten Umgebung von IPv4-und IPv6-Knoten möglicherweise bequemer ist, ist x:x: x:x: x:x: d. d. d. d, wobei "x" die hexadezimal Werte der sechs groß wertigen 16-Bit-Teile der Adresse sind und die Dezimalwerte der vier 8-Bit-Teile der Adresse (IPv4-Standarddarstellung) sind.</span><span class="sxs-lookup"><span data-stu-id="0a177-120">An alternative form that may be more convenient when dealing with a mixed environment of IPv4 and IPv6 nodes is x:x:x:x:x:x:d.d.d.d, where the 'x's are the hexadecimal values of the six high-order 16-bit pieces of the address, and the 'd's are the decimal values of the four low-order 8-bit pieces of the address (standard IPv4 representation).</span></span>

    <span data-ttu-id="0a177-121">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="0a177-121">Examples:</span></span>

    <dl> <span data-ttu-id="0a177-122">0:0: 0:0: 0:0: 13.1.68.3</span><span class="sxs-lookup"><span data-stu-id="0a177-122">0:0:0:0:0:0:13.1.68.3</span></span>  
    <span data-ttu-id="0a177-123">0:0: 0:0: 0: FFFF: 129.144.52.38</span><span class="sxs-lookup"><span data-stu-id="0a177-123">0:0:0:0:0:FFFF:129.144.52.38</span></span>  
    </dl>

    <span data-ttu-id="0a177-124">oder in komprimierter Form:</span><span class="sxs-lookup"><span data-stu-id="0a177-124">or in compressed form:</span></span>

    <dl> <span data-ttu-id="0a177-125">::13.1.68.3</span><span class="sxs-lookup"><span data-stu-id="0a177-125">::13.1.68.3</span></span>  
    <span data-ttu-id="0a177-126">:: FFFF: 129.144.52.38</span><span class="sxs-lookup"><span data-stu-id="0a177-126">::FFFF:129.144.52.38</span></span>  
    </dl>

 

 



