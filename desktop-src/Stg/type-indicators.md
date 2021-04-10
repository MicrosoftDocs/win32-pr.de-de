---
title: Typindikatoren
description: Die tatsächlichen Eigenschaften Folgen der Tabelle der Eigenschaftswerte für Eigenschaften Bezeichner/Offset Paare. Jede Eigenschaft wird als DWORD gespeichert, gefolgt vom Wert des-Datentyps.
ms.assetid: 8523458b-8b1b-4e9f-8f96-d7601e57675c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8383a860f07e908b72a7b25091f3cc2e280e4407
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039351"
---
# <a name="type-indicators"></a><span data-ttu-id="43ffc-104">Typindikatoren</span><span class="sxs-lookup"><span data-stu-id="43ffc-104">Type Indicators</span></span>

<span data-ttu-id="43ffc-105">Die tatsächlichen Eigenschaften Folgen der Tabelle der Eigenschaftswerte für Eigenschaften Bezeichner/Offset Paare.</span><span class="sxs-lookup"><span data-stu-id="43ffc-105">The actual properties follow the table of Property Identifiers/Offset Pairs property set values.</span></span> <span data-ttu-id="43ffc-106">Jede Eigenschaft wird als **DWORD** gespeichert, gefolgt vom Wert des-Datentyps.</span><span class="sxs-lookup"><span data-stu-id="43ffc-106">Each property is stored as a **DWORD**, followed by the data type value.</span></span>

<span data-ttu-id="43ffc-107">Typindikatoren und die zugehörigen Werte werden in der [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Struktur beschrieben.</span><span class="sxs-lookup"><span data-stu-id="43ffc-107">Type indicators and their associated values are described in the [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structure.</span></span>

<span data-ttu-id="43ffc-108">Alle Typ/Wert-Paare müssen mit einer 32-Bit-Grenze beginnen.</span><span class="sxs-lookup"><span data-stu-id="43ffc-108">All Type/Value pairs must begin on a 32-bit boundary.</span></span> <span data-ttu-id="43ffc-109">Folglich können Werte mit NULL Bytes gefolgt werden, um das nachfolgende Paar an einer 32-Bit-Grenze auszurichten.</span><span class="sxs-lookup"><span data-stu-id="43ffc-109">Thus, values may be followed with null bytes to align the subsequent pair on a 32-bit boundary.</span></span>

<span data-ttu-id="43ffc-110">Im folgenden Beispielcode wird berechnet, wie viele Bytes an einer 32-Bit-Grenze ausgerichtet werden müssen, wenn die Anzahl von Bytes angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="43ffc-110">The following example code calculates how many bytes are required to align on a 32-bit boundary, given a count of bytes.</span></span>


```C++
cbAdd = (((cbCurrent + 3) >> 2) << 2) - cbCurrent ;
```



<span data-ttu-id="43ffc-111">Innerhalb eines Vektor von Werten muss jede Wiederholung eines einfachen skalarwerts, der kleiner als 32 Bits ist, an der natürlichen Ausrichtung und nicht an der 32-Bit-Ausrichtung ausgerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="43ffc-111">Within a vector of values, each repetition of a simple scalar value smaller than 32 bits must align with its natural alignment rather than with a 32-bit alignment.</span></span> <span data-ttu-id="43ffc-112">In der Praxis ist dies nur für die Typen **VT \_ UI1**, **VT \_ UI2**, **VT \_ I2** und **VT \_ bool** (die eine natürliche Ausrichtung mit einem oder zwei Bytes aufweisen) wichtig.</span><span class="sxs-lookup"><span data-stu-id="43ffc-112">In practice, this is only significant for types **VT\_UI1**, **VT\_UI2**, **VT\_I2**, and **VT\_BOOL** (which have one-byte or two-byte natural alignment).</span></span> <span data-ttu-id="43ffc-113">Alle anderen Typen haben eine natürliche Ausrichtung von vier Bytes.</span><span class="sxs-lookup"><span data-stu-id="43ffc-113">All other types have four-byte natural alignment.</span></span> <span data-ttu-id="43ffc-114">Einige Typen, z. b. **VT \_ R8**, verfügen tatsächlich über eine natürliche 8-Byte-Ausrichtung, werden jedoch so gespeichert, als hätten Sie eine 4-Byte-Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="43ffc-114">Some types, for example, **VT\_R8**, actually have 8-byte natural alignment, but are stored as if they have four-byte alignment.</span></span>

<span data-ttu-id="43ffc-115">Ein Eigenschafts Wert mit dem Typ Indicator **VT \_ I2** - \| **\_ Vektor** würde Folgendes umfassen:</span><span class="sxs-lookup"><span data-stu-id="43ffc-115">A property value with type indicator **VT\_I2** \| **VT\_VECTOR** would include:</span></span>

-   <span data-ttu-id="43ffc-116">Eine **DWORD** -Element Anzahl.</span><span class="sxs-lookup"><span data-stu-id="43ffc-116">A **DWORD** element count.</span></span>
-   <span data-ttu-id="43ffc-117">Eine Sequenz von gefüllten 2-Byte-Ganzzahlen ohne NULL-Leerraum zwischen diesen.</span><span class="sxs-lookup"><span data-stu-id="43ffc-117">A sequence of packed two-byte integers with no null padding between them.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="43ffc-118">Alle 32-Bit-Zähler oder-Eigenschafts Typen, die als Teil eines Vector Property-Elements gespeichert werden, müssen ebenfalls 32-Bit-ausgerichtet sein.</span><span class="sxs-lookup"><span data-stu-id="43ffc-118">Any 32-bit counts or property types that are stored as a part of a vector property element must also be 32-bit aligned.</span></span>

 

<span data-ttu-id="43ffc-119">Ein Eigenschafts Wert des Typbezeichners **VT \_ LPSTR** \| **VT- \_ Vektor** würde Folgendes umfassen:</span><span class="sxs-lookup"><span data-stu-id="43ffc-119">A property value of type identifier **VT\_LPSTR** \| **VT\_VECTOR** would include:</span></span>

-   <span data-ttu-id="43ffc-120">Eine **DWORD** -Element Anzahl (**DWORD**- *celems*).</span><span class="sxs-lookup"><span data-stu-id="43ffc-120">A **DWORD** element count (**DWORD** *cElems*).</span></span>
-   <span data-ttu-id="43ffc-121">Eine Sequenz von Zeichen folgen (**char** *rgch \[ \]*), denen jeweils ein **DWORD** -Längen Zähler und möglicherweise ein NULL-Abstand vorangestellt ist, um auf eine 32-Bit-Grenze zu runden.</span><span class="sxs-lookup"><span data-stu-id="43ffc-121">A sequence of strings (**char** *rgch\[\]*), each preceded by a length-count **DWORD** and possibly followed by null padding to round to a 32-bit boundary.</span></span>

 

 