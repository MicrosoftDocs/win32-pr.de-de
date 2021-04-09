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
# <a name="wide-character-types"></a>Wide-Character Typen

Microsoft RPC unterstützt den breit Zeichentyp [**WCHAR \_ t**](/windows/desktop/Midl/wchar-t). Der breit Zeichentyp verwendet für jedes Zeichen 2 Bytes. Mit der ANSI C-Language-Definition können Sie lange und lange Zeichen folgen wie folgt initialisieren:

``` syntax
wchar_t wcInitial = L'a';
wchar_t * pwszString = L"Hello, world";
```

 

 