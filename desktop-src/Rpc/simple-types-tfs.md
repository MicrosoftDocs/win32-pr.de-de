---
title: Einfache Typen
description: Alle einfachen Typen werden durch ein einzelnes Formatierungszeichen dargestellt, das den Typ anhand des Namens angibt.
ms.assetid: 77c293a1-70c4-4825-bb2e-de36e01d3abb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afe123ca7c06a0522a139dc0cca8a9e24d1d585d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712744"
---
# <a name="simple-types"></a><span data-ttu-id="58ffc-103">Einfache Typen</span><span class="sxs-lookup"><span data-stu-id="58ffc-103">Simple Types</span></span>

<span data-ttu-id="58ffc-104">Alle einfachen Typen werden durch ein einzelnes Formatierungszeichen dargestellt, das den Typ anhand des Namens angibt.</span><span class="sxs-lookup"><span data-stu-id="58ffc-104">All simple types are represented by a single format character indicating the type by its name.</span></span> <span data-ttu-id="58ffc-105">Dies schließt alle numerischen Typen und einige andere spezielle IDL-Typen ein.</span><span class="sxs-lookup"><span data-stu-id="58ffc-105">This includes all the numerical types and some other special IDL types.</span></span> <span data-ttu-id="58ffc-106">Die Liste lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="58ffc-106">The list is as follows:</span></span>

``` syntax
FC_BYTE,                    // 0x01
FC_CHAR,                    // 0x02
FC_SMALL,                   // 0x03
FC_USMALL,                  // 0x04
FC_WCHAR,                   // 0x05
FC_SHORT,                   // 0x06
FC_USHORT,                  // 0x07
FC_LONG,                    // 0x08
FC_ULONG,                   // 0x09
FC_FLOAT,                   // 0x0a
FC_HYPER,                   // 0x0b
FC_DOUBLE,                  // 0x0c
FC_ENUM16,                  // 0x0d
FC_ENUM32,                  // 0x0e
FC_ERROR_STATUS_T,          // 0x10
FC_INT3264,                 // 0xb8
FC_UINT3264,                // 0xb9
```

<span data-ttu-id="58ffc-107">Die Typen "Small", "WCHAR", "Hyper", "Error \_ Status \_ T" und "INT3264" sind eigen intrinsie systeminterne \_ \_ Funktionen mit speziellen</span><span class="sxs-lookup"><span data-stu-id="58ffc-107">The SMALL, WCHAR, HYPER, ERROR\_STATUS\_T, \_\_INT3264 types are MIDL intrinsics with special RPC interpretations.</span></span> <span data-ttu-id="58ffc-108">Die Typen "int" und " \_ \_ Int32" werden den Typen "Long" \_ , "Ganzzahl ohne Vorzeichen int" und "Ganzzahl ohne Vorzeichen" \_ \_ Int32 Map to FC \_ ulong, \_ \_ Int64 und Ganzzahl ohne Vorzeichen \_ \_ Int64 Map to FC \_ Hyper zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="58ffc-108">The INT and \_\_INT32 types map to FC\_LONG, unsigned INT and unsigned \_\_INT32 map to FC\_ULONG, \_\_INT64 and unsigned \_\_INT64 map to FC\_HYPER.</span></span>

<span data-ttu-id="58ffc-109">Die \_ \_ Typen INT128, FLOAT128 und FLOAT80 werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="58ffc-109">The \_\_INT128, FLOAT128, and FLOAT80 types are not supported.</span></span>

 

 




