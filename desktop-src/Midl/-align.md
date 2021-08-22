---
title: /align-Schalter
description: Der Schalter /align ist funktionell identisch mit der MIDL/Zp-Option und wird vom MIDL-Compiler ausschließlich aus Gründen der Abwärtskompatibilität mit MkTypLib erkannt.
ms.assetid: 7f303c49-a6b5-4e3c-95e5-5c49e338c766
keywords:
- /align switch MIDL
topic_type:
- apiref
api_name:
- /align
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 187607b783678d3045224daec021eabf436fa8ba1884128789f44b06ac4365ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067650"
---
# <a name="align-switch"></a>/align-Schalter

Der Schalter **/align** ist funktionell identisch mit der [**MIDL/Zp-Option**](-zp.md) und wird vom MIDL-Compiler ausschließlich aus Gründen der Abwärtskompatibilität mit MkTypLib erkannt.

> [!Note]  
> Das Mktyplib.exe Tool ist veraltet. Verwenden Sie stattdessen den MIDL-Compiler.

 

``` syntax
midl /align:alignment
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

*Ausrichtung* 
</dt> <dd>

Gibt die Ausrichtung für Typen in der Bibliothek an. Der *Ausrichtungswert* kann 1, 2, 4 oder 8 sein. Der Wert 1 gibt eine natürliche Ausrichtung an. *n* gibt die Ausrichtung an Byte *n* an. Wenn Sie den Schalter **/align** nicht angeben, ist der Standardwert 8.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn Sie ein neues Makefile generieren, verwenden Sie den Schalter [**/Zp.**](-zp.md)

Der Ausrichtungswert entspricht dem [**/Zp-Optionswert,**](-zp.md) der vom Microsoft C/C++-Compiler verwendet wird. Achten Sie darauf, dass Sie beim Aufrufen des C-Compilers dieselbe Ausrichtung wie beim Aufrufen des MIDL-Compilers angeben.

Weitere Informationen finden Sie in der C/C++-Programmierdokumentation von Microsoft. Eine Erläuterung der potenziellen Gefährdungen bei der Verwendung von nicht standardmäßigen Komprimierungsstufen finden Sie im [**Hilfethema /Zp.**](-zp.md)

## <a name="examples"></a>Beispiele

**midl /align:4 filename.idl**

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Zp**](-zp.md)
</dt> </dl>

 

 




