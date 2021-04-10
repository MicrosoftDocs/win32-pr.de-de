---
title: Transmit_as und Represent_as
description: '\_Übertragen als und stellen dar \_ , dass dasselbe Layout mit Ausnahme des führenden Tokens identisch ist. das Token liest FC-über \_ Tragung \_ als oder FC \_ , der als dargestellt wird \_ , aber der zugrunde liegende Code ist allgemein.'
ms.assetid: 70fbb4bf-0892-4c26-9790-9fc21ff8c0dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69267741536314c3e30e2270e7be61edfdb5caff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948782"
---
# <a name="transmit_as-and-represent_as"></a><span data-ttu-id="d2114-103">Übertragen \_ als und Darstellung \_ als</span><span class="sxs-lookup"><span data-stu-id="d2114-103">Transmit\_as and Represent\_as</span></span>

<span data-ttu-id="d2114-104">\_Übertragen als und stellen dar \_ , dass dasselbe Layout mit Ausnahme des führenden Tokens identisch ist. das Token liest FC-über \_ Tragung \_ als oder FC \_ , der als dargestellt wird \_ , aber der zugrunde liegende Code ist allgemein.</span><span class="sxs-lookup"><span data-stu-id="d2114-104">Transmit\_as and represent\_as share the same layout except for the leading token; the token reads FC\_TRANSMIT\_AS or FC\_REPRESENT\_AS, but the underlying code is common.</span></span>

<span data-ttu-id="d2114-105">Die Beschreibung hat folgendes Layout:</span><span class="sxs-lookup"><span data-stu-id="d2114-105">The description has the following layout:</span></span>

``` syntax
FC_TRANSMIT_AS | FC_REPRESENT_AS
flags<1>
quintuple_index<2>
presented_type_memory_size<2>
transmitted_type_buffer_size<2>
transmitted_type_offset<2>
```

<span data-ttu-id="d2114-106">Die Flags<1> Byte bestehen aus dem oberen Flag-Halbbyte und dem unteren Ausrichtungs-Halbbyte.</span><span class="sxs-lookup"><span data-stu-id="d2114-106">The flags<1> byte consists of the upper flag nibble and the lower alignment nibble.</span></span>

<span data-ttu-id="d2114-107">Der Ausrichtungs-Halbbyte behält die Netzwerk Ausrichtung des übertragenen Typs bei.</span><span class="sxs-lookup"><span data-stu-id="d2114-107">The alignment nibble keeps the wire alignment of the transmitted type.</span></span> <span data-ttu-id="d2114-108">Dies ist erforderlich, wenn die Puffergröße und die übertragene Typgröße aus dem Format Code verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d2114-108">This is needed when buffer sizing and using the transmitted type size from the format code.</span></span>

<span data-ttu-id="d2114-109">Das Flag Halbbyte kann die folgenden Flags aufweisen:</span><span class="sxs-lookup"><span data-stu-id="d2114-109">The flag nibble can have the following flags:</span></span>

``` syntax
#define PRESENTED_TYPE_IS_ARRAY     0x10
#define PRESENTED_TYPE_ALIGN_4      0x20
#define PRESENTED_TYPE_ALIGN_8      0x40
```

<span data-ttu-id="d2114-110">Der dargestellte \_ Typ \_ ist \_ ein arrayflag, das als Argument der obersten Ebene übertragen wird, als ein Array von etwas und einem Wert, das ein Array aus einem Wert darstellt.</span><span class="sxs-lookup"><span data-stu-id="d2114-110">The PRESENTED\_TYPE\_IS\_ARRAY flag marks a top-level transmit as (or represent as) argument being an array of something and passed-by value.</span></span> <span data-ttu-id="d2114-111">Der [**– Oi**](/windows/desktop/Midl/-oi) -Interpreter verwendet dieses Flag zum Durchlaufen eines solchen Arguments (bei dem es sich eigentlich um einen Zeiger auf den Stapel handelt, nicht um das Array).</span><span class="sxs-lookup"><span data-stu-id="d2114-111">The [**–Oi**](/windows/desktop/Midl/-oi) interpreter uses this flag to step over such an argument (which is actually a pointer on stack, not the array).</span></span> <span data-ttu-id="d2114-112">Die anderen beiden Flags werden auch nur in vorherigen Interpretern verwendet, um einen ordnungsgemäßen Schritt für einen dargestellten Typ auf dem Stapel durchzusetzen.</span><span class="sxs-lookup"><span data-stu-id="d2114-112">The other two flags are also used only in previous interpreters to step correctly over a presented type on the stack.</span></span>

<span data-ttu-id="d2114-113">Der quintupel- \_ Index<2> ist ein Index der Rückruf Routine-quintupel (Dies ist eigentlich ein Vierfaches) von Funktionen.</span><span class="sxs-lookup"><span data-stu-id="d2114-113">The quintuple\_index<2> is an index of the callback routine quintuple (this is actually a quadruple) of functions.</span></span> <span data-ttu-id="d2114-114">Die-Tabelle wird häufig sowohl als als auch als dargestellt, und es gibt eine offensichtliche Zuordnung für die Position der Routinen, wie der Dienst, den der Dienst übermittelt und als Codes darstellt.</span><span class="sxs-lookup"><span data-stu-id="d2114-114">The table is common to both transmit as and represent as and there is an obvious mapping for the position of the routines, as the same entry points service transmit as and represent as codes.</span></span> <span data-ttu-id="d2114-115">Die Zuordnung erfolgt aus \_ local => to \_ xmit, \_ local => from \_ xmit, Free \_ inst => Free \_ xmit, Free \_ local => Free \_ INST.</span><span class="sxs-lookup"><span data-stu-id="d2114-115">The mapping is from\_local => to\_xmit, to\_local => from\_xmit, free\_inst => free\_xmit, free\_local => free\_inst.</span></span>

<span data-ttu-id="d2114-116">Die dargestellte Größe des Arbeits \_ \_ Speichers \_<2> bietet immer eine Größe für den dargestellten/lokalen Typ, einschließlich unbekannter Darstellung als Typen.</span><span class="sxs-lookup"><span data-stu-id="d2114-116">The presented\_type\_memory\_size<2> always provides a size for the presented/local type, including unknown represent as types.</span></span>

<span data-ttu-id="d2114-117">Die übertragene \_ \_ typpuffer \_ Größe<2> ist entweder 0 (null), wenn die Größe unterschiedlich ist, oder die tatsächliche Größe.</span><span class="sxs-lookup"><span data-stu-id="d2114-117">The transmitted\_type\_buffer\_size<2> is either zero, when the size is varying, or the actual fixed size.</span></span> <span data-ttu-id="d2114-118">Dies ist eine Optimierung, die das Überspringen einiger Rückrufe bei der Größenanpassung des Puffers ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="d2114-118">This is an optimization that enables skipping some callbacks when sizing the buffer.</span></span>

<span data-ttu-id="d2114-119">Der übertragene \_ \_ typoffset<2> ist der übliche relative typoffset der übertragenen typformatzeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="d2114-119">The transmitted\_type\_offset<2> is the usual relative type offset to the transmitted type format string.</span></span>

 

 