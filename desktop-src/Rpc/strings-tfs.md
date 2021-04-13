---
title: Zeichen folgen (RPC)
description: Drei Zeichen folgen Typen und Remote Prozedur Aufruf (RPC).
ms.assetid: 186cabeb-ea3f-4213-ba71-53afe91e6e14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 207e20b1c343ded17b5d62db2321bee380463f20
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316059"
---
# <a name="strings-rpc"></a><span data-ttu-id="534c9-103">Zeichen folgen (RPC)</span><span class="sxs-lookup"><span data-stu-id="534c9-103">Strings (RPC)</span></span>

<span data-ttu-id="534c9-104">Es gibt drei Zeichen folgen Typen, die durch die folgenden enden untergeordneten Zeichen folgen im Formatzeichen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="534c9-104">There are three strings types denoted by the following ending sub-strings in the format character.</span></span>



| <span data-ttu-id="534c9-105">type</span><span class="sxs-lookup"><span data-stu-id="534c9-105">Type</span></span>                  | <span data-ttu-id="534c9-106">TEILZEICHENFOLGE</span><span class="sxs-lookup"><span data-stu-id="534c9-106">Substring</span></span> |
|-----------------------|-----------|
| <span data-ttu-id="534c9-107">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="534c9-107">Character string</span></span>      | <span data-ttu-id="534c9-108">CSTRING</span><span class="sxs-lookup"><span data-stu-id="534c9-108">CSTRING</span></span>   |
| <span data-ttu-id="534c9-109">Breit Zeichen-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="534c9-109">Wide character string</span></span> | <span data-ttu-id="534c9-110">WSTRING</span><span class="sxs-lookup"><span data-stu-id="534c9-110">WSTRING</span></span>   |
| <span data-ttu-id="534c9-111">Zeichen folgen fähige Struktur</span><span class="sxs-lookup"><span data-stu-id="534c9-111">String-able structure</span></span> | <span data-ttu-id="534c9-112">SString</span><span class="sxs-lookup"><span data-stu-id="534c9-112">SSTRING</span></span>   |



 

### <a name="nonconformant-strings"></a><span data-ttu-id="534c9-113">Nicht konforme Zeichen folgen</span><span class="sxs-lookup"><span data-stu-id="534c9-113">Nonconformant Strings</span></span>

<span data-ttu-id="534c9-114">Ein Beispiel für eine nicht konforme Zeichenfolge ist eine **\[ Zeichen \]** Folge in einem Array mit fester Größe.</span><span class="sxs-lookup"><span data-stu-id="534c9-114">An example of nonconformant string is a **\[string\]** on a fixed-size array.</span></span>

``` syntax
FC_CSTRING | FC _WSTRING 
FC_PAD 
string_size<2>
```

### <a name="conformant-strings"></a><span data-ttu-id="534c9-115">Konforme Zeichen folgen</span><span class="sxs-lookup"><span data-stu-id="534c9-115">Conformant Strings</span></span>

``` syntax
FC_C_CSTRING | FC_C_WSTRING
FC_PAD 
```

<span data-ttu-id="534c9-116">– oder –</span><span class="sxs-lookup"><span data-stu-id="534c9-116">–or–</span></span>

``` syntax
FC_C_CSTRING | FC_C_WSTRING 
FC_STRING_SIZED 
conformance_description<> 
```

<span data-ttu-id="534c9-117">Das erste Format beschreibt gängige Zeichen folgen, wie z. b. ein **\[ String \]** char- \* Argument.</span><span class="sxs-lookup"><span data-stu-id="534c9-117">The first format describes common strings, like a **\[string\]** char \* argument.</span></span> <span data-ttu-id="534c9-118">Eine konforme Zeichenfolge mit der Größenanpassung hat die letztgenannte Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="534c9-118">A sized conformant string has the latter description.</span></span>

<span data-ttu-id="534c9-119">Die Übereinstimmungs \_ Beschreibung<> ist ein Korrelations Deskriptor, der abhängig davon, ob [**/robust**](/windows/desktop/Midl/-robust) verwendet wird, 4 oder 6 Bytes hat.</span><span class="sxs-lookup"><span data-stu-id="534c9-119">The conformance\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span>

### <a name="structure-strings"></a><span data-ttu-id="534c9-120">Struktur Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="534c9-120">Structure Strings</span></span>

<span data-ttu-id="534c9-121">Im folgenden finden Sie eine nicht konforme Zeichen folgen fähige Struktur:</span><span class="sxs-lookup"><span data-stu-id="534c9-121">The following is a nonconformant string-able structure:</span></span>

``` syntax
FC_SSTRING 
element_size<1> 
number_of_elements<2>
```

<span data-ttu-id="534c9-122">Konforme Zeichen folgen fähige Struktur:</span><span class="sxs-lookup"><span data-stu-id="534c9-122">Conformant string-able structure:</span></span>

``` syntax
FC_C_SSTRING 
element_size<1>
```

<span data-ttu-id="534c9-123">noch</span><span class="sxs-lookup"><span data-stu-id="534c9-123">–or –</span></span>

``` syntax
FC_C_SSTRING 
elements_size<1> 
FC_STRING_SIZED FC_PAD 
conformance_description<>
```

<span data-ttu-id="534c9-124">Die letztgenannte Beschreibung ist für eine Struktur mit einer Größen Zeichenfolge zulässig.</span><span class="sxs-lookup"><span data-stu-id="534c9-124">The latter description is for a sized string-able structure.</span></span>

 

 