---
title: Einfache Typen
description: Alle einfachen Typen werden durch ein einzelnes Formatzeichen dargestellt, das den Typ anhand seines Namens angibt.
ms.assetid: 77c293a1-70c4-4825-bb2e-de36e01d3abb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e265c24d1eaf4b85ab67c7f8997c656257522bfc8290e73596a8628bdd4215c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925160"
---
# <a name="simple-types"></a>Einfache Typen

Alle einfachen Typen werden durch ein einzelnes Formatzeichen dargestellt, das den Typ anhand seines Namens angibt. Dies schließt alle numerischen Typen und einige andere spezielle IDL-Typen ein. Die Liste sieht wie folgt aus:

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

Die Typen SMALL, WCHAR, HYPER, ERROR \_ STATUS \_ T und \_ \_ INT3264 sind intrinsische MIDL-Funktionen mit speziellen RPC-Interpretationen. Die Typen INT und \_ \_ INT32 werden FC \_ LONG zugeordnet, unsigned INT und \_ \_ unsigned INT32 werden FC \_ ULONG, \_ \_ INT64 und \_ \_ unsigned INT64 FC HYPER \_ zugeordnet.

Die \_ \_ Typen INT128, FLOAT128 und FLOAT80 werden nicht unterstützt.

 

 




