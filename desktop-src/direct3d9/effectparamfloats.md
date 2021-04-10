---
description: Definiert die Auswirkungen von Gleit Komma Zahlen. Diese Vorlage ersetzt die effectfloat-Vorlage.
ms.assetid: 7b41d0dc-209f-4ade-a7ed-aa54f421e520
title: Effectparamfloat
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0954ce7679691920c2e104277d12a48f7a34ddf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104041185"
---
# <a name="effectparamfloats"></a>Effectparamfloat

Definiert die Auswirkungen von Gleit Komma Zahlen. Diese Vorlage ersetzt die [**effectfloat**](effectfloats.md) -Vorlage.

``` syntax
template EffectParamFloats
{
    < 3014B9A0-62F5-478c-9B86-E4AC9F4E418B >
    STRING ParamName;
    DWORD nFloats;
    array float Floats[nFloats];
} 
```

Hierbei gilt:

-   ParamName: der Name des Arrays von Gleit Komma Zahlen.
-   nfloat: Anzahl von Gleit Komma Werten im Array.
-   Schwebt ein \[ nfloat \] -Array von Gleit Komma Werten.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



