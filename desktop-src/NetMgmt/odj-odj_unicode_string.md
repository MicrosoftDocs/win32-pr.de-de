---
title: ODJ_UNICODE_STRING
description: ODJ_UNICODE_STRING IDL-Definition
ms.assetid: a7999df0-d961-4fd7-ae5e-65ad79a9c17c
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f1134d7b95cca6948932bf9d79fe976d6745448a
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2020
ms.locfileid: "106341973"
---
# <a name="odj_unicode_string-structure"></a><span data-ttu-id="1e648-103">ODJ_UNICODE_STRING Struktur</span><span class="sxs-lookup"><span data-stu-id="1e648-103">ODJ_UNICODE_STRING structure</span></span>

<span data-ttu-id="1e648-104">Enthält eine Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="1e648-104">Contains a Unicode string.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e648-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e648-105">Syntax</span></span>

```C++
typedef struct _ODJ_UNICODE_STRING
{
    USHORT Length;
    USHORT MaximumLength;
    [size_is(MaximumLength/2), length_is(Length/2)] PWSTR Buffer;
} ODJ_UNICODE_STRING, *PODJ_UNICODE_STRING;
```

## <a name="members"></a><span data-ttu-id="1e648-106">Member</span><span class="sxs-lookup"><span data-stu-id="1e648-106">Members</span></span>

### <a name="length"></a><span data-ttu-id="1e648-107">Länge</span><span class="sxs-lookup"><span data-stu-id="1e648-107">Length</span></span>

<span data-ttu-id="1e648-108">Muss auf die Anzahl der Bytes im Puffer mit der Zeichenfolge festgelegt werden, ohne das NULL-Terminator.</span><span class="sxs-lookup"><span data-stu-id="1e648-108">Must be set to the number of bytes in Buffer containing the string, not including the NULL terminator.</span></span>

### <a name="maximumlength"></a><span data-ttu-id="1e648-109">MaximumLength</span><span class="sxs-lookup"><span data-stu-id="1e648-109">MaximumLength</span></span>

<span data-ttu-id="1e648-110">Dies muss auf die Gesamtzahl der Bytes im Puffer festgelegt werden, ohne das NULL-Terminator.</span><span class="sxs-lookup"><span data-stu-id="1e648-110">This MUST be set to the total number of bytes in Buffer, not including the NULL terminator.</span></span>

### <a name="buffer"></a><span data-ttu-id="1e648-111">Buffer</span><span class="sxs-lookup"><span data-stu-id="1e648-111">Buffer</span></span>

<span data-ttu-id="1e648-112">Dabei muss es sich um eine Unicode-Zeichenfolge handeln.</span><span class="sxs-lookup"><span data-stu-id="1e648-112">Must be a Unicode string.</span></span>

## <a name="see-also"></a><span data-ttu-id="1e648-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e648-113">See also</span></span>

[<span data-ttu-id="1e648-114">**IDL-Definitionen im Offline-Domänen Beitritt**</span><span class="sxs-lookup"><span data-stu-id="1e648-114">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)
