---
title: /pack-Schalter
description: Der Schalter /pack entspricht der Option /Zp.
ms.assetid: 381e3099-adb4-4219-bbb4-89c9e1dd3928
keywords:
- /pack switch MIDL
topic_type:
- apiref
api_name:
- /pack
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad9282cd5ab56d2e037ba585676a83c5cd558ecb26354ab191899ad341506f5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117991942"
---
# <a name="pack-switch"></a>/pack-Schalter

Der Schalter **/pack** entspricht der Option [**/Zp.**](-zp.md)

``` syntax
midl /pack packing_level
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

*\_Komprimierungsebene* 
</dt> <dd>

Gibt die Komprimierungsebene von Strukturen im Zielsystem an. Der Komprimierungsebenenwert kann auf 1, 2, 4 oder 8 festgelegt werden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Schalter **/pack** bestimmt die Komprimierungsebene von Strukturen im Zielsystem. Der Wert auf Komprimierungsebene entspricht dem [**/Zp-Optionswert,**](-zp.md) der vom Microsoft C/C++-Compiler der Version 7.0 verwendet wird. Weitere Informationen finden Sie in der C/C++-Programmierdokumentation von Microsoft.

Geben Sie die gleiche Komprimierungsebene an, wenn Sie den MIDL-Compiler und den C-Compiler aufrufen. Die Standard-Komprimierungsstufe, die verwendet wird, wenn weder der Schalter [**"/Zp"**](-zp.md) noch **"/pack"** angegeben ist, ist in beiden Buildumgebungen 8.

Eine Erläuterung der potenziellen Gefährdungen bei der Verwendung von nicht standardmäßigen Komprimierungsstufen finden Sie im [**Hilfethema /Zp.**](-zp.md)

## <a name="examples"></a>Beispiele

**midl /pack 2 filename.idl**

**midl /pack 8 bar.idl**

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> <dt>

[**/env**](-env.md)
</dt> <dt>

[**/Zp**](-zp.md)
</dt> </dl>

 

 




