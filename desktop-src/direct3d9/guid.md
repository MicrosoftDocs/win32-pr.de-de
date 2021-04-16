---
description: Definiert eine GUID, die in anderen Vorlagen verwendet werden kann.
ms.assetid: dbfdd307-310f-4c80-b4aa-f16a81a9a372
title: GUID (DirectX 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e83e45d6e993153cf293a2ad55080c74f2e6049d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521432"
---
# <a name="guid-directx-9"></a>GUID (DirectX 9)

Definiert eine GUID, die in anderen Vorlagen verwendet werden kann.

``` syntax
template Guid
{
    < a42790e0-7810-11cf-8f52-0040333594a3 >
    DWORD data1;
    WORD data2;
    WORD data3;
    array UCHAR data4[8];
} 
```

Dabei bilden die Parameter zusammen das binäre Speicherformat für eine GUID:

-   data1-32-Bit-Ganzzahl ohne Vorzeichen
-   data2-16-Bit-Ganzzahl ohne Vorzeichen
-   data3-16-Bit-Ganzzahl ohne Vorzeichen
-   data4-ein Array nicht signierter Zeichen

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



