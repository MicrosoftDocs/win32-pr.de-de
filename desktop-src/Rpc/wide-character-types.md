---
title: Wide-Character Typen
description: Microsoft RPC unterstützt den breit Zeichentyp WCHAR \_ t.
ms.assetid: 1a601461-df34-456d-93e8-4cf0b655cf2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 821d69999a0ec7e175409120f223721defd6cd10
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102030"
---
# <a name="wide-character-types"></a><span data-ttu-id="70fb4-103">Wide-Character Typen</span><span class="sxs-lookup"><span data-stu-id="70fb4-103">Wide-Character Types</span></span>

<span data-ttu-id="70fb4-104">Microsoft RPC unterstützt den breit Zeichentyp [**WCHAR \_ t**](/windows/desktop/Midl/wchar-t).</span><span class="sxs-lookup"><span data-stu-id="70fb4-104">Microsoft RPC supports the wide-character type [**wchar\_t**](/windows/desktop/Midl/wchar-t).</span></span> <span data-ttu-id="70fb4-105">Der breit Zeichentyp verwendet für jedes Zeichen 2 Bytes.</span><span class="sxs-lookup"><span data-stu-id="70fb4-105">The wide-character type uses 2 bytes for each character.</span></span> <span data-ttu-id="70fb4-106">Mit der ANSI C-Language-Definition können Sie lange und lange Zeichen folgen wie folgt initialisieren:</span><span class="sxs-lookup"><span data-stu-id="70fb4-106">The ANSI C-language definition allows you to initialize long characters and long strings as:</span></span>

``` syntax
wchar_t wcInitial = L'a';
wchar_t * pwszString = L"Hello, world";
```

 

 