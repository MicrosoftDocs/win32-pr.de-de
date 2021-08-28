---
title: /Zp-Schalter
description: Der Schalter /Zp ist mit der Option /pack identisch.
ms.assetid: ccdae6a5-e53c-4ddc-9f5f-2b2118709fdb
keywords:
- /Zp switch MIDL
topic_type:
- apiref
api_name:
- /Zp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1795068aae1a5a8c3e793b828d5a80dbab369e16f9c5383af367b66d0febc738
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067440"
---
# <a name="zp-switch"></a>/Zp-Schalter

Der **Schalter /Zp** ist mit der Option [**/pack**](-pack.md) identisch.

``` syntax
midl /Zp packing_level
```

## <a name="switch-options"></a>Switch-Optionen

<dl> <dt>

*\_Packebene* 
</dt> <dd>

Gibt die Packebene von Strukturen im Zielsystem an. Der Füllebenenwert kann auf 1, 2, 4 oder 8 festgelegt werden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der **Schalter /Zp** bestimmt die Packebene von Strukturen im Zielsystem. Der Wert der Packebene entspricht dem **/Zp-Optionswert,** der vom Microsoft C/C++-Compiler verwendet wird. Weitere Informationen finden Sie in der Dokumentation zur C/C++-Programmierung von Microsoft.

Geben Sie die gleiche Packebene an, wenn Sie den MIDL-Compiler und den C-Compiler aufrufen.

Die Standardpackungsebene, die verwendet wird, wenn weder **der Schalter /Zp** noch [**/pack**](-pack.md) angegeben wird, ist in allen Buildumgebungen 8.

> [!Note]  
> Verwenden Sie **/Zp1 oder** **/Zp2** nicht auf MIPS- oder Alphaplattformen und **nicht /Zp4** oder **/Zp8** auf 16-Bit-Plattformen. Je nach Datentyp und Speicherort, der vom C-Compiler zur Laufzeit zugewiesen wird, kann dies zu einer Datenfehlausnahme auf MIPS- und Alphaplattformen führen. Auf MS-DOS-Plattformen stellt der C-Compiler die Ausrichtung bei 4 oder 8 nicht sicher, sodass die Anwendung beendet werden kann.

 

## <a name="examples"></a>Beispiele

**midl /Zp4 filename.idl**

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> <dt>

[**/pack**](-pack.md)
</dt> </dl>

 

 




