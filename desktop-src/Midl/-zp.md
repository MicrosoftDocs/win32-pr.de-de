---
title: /ZP-Schalter
description: Der/ZP-Schalter ist mit der Option/Pack identisch.
ms.assetid: ccdae6a5-e53c-4ddc-9f5f-2b2118709fdb
keywords:
- /ZP-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /Zp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 553d99dee7dd08218680fc0b43e6e12237c4f8fa
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718161"
---
# <a name="zp-switch"></a>/ZP-Schalter

Der **/ZP** -Schalter ist mit der Option [**/Pack**](-pack.md) identisch.

``` syntax
midl /Zp packing_level
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

*Packungs \_ Stufe* 
</dt> <dd>

Gibt die Verpackungs Ebene von Strukturen im Zielsystem an. Der Wert auf der Verpackungs Ebene kann auf 1, 2, 4 oder 8 festgelegt werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der **/ZP** -Schalter legt die Verpackungs Ebene von Strukturen im Zielsystem fest. Der Wert auf der Packungs Ebene entspricht dem Wert der **/ZP** -Option, der vom Microsoft C/C++-Compiler verwendet wird. Weitere Informationen finden Sie in der Microsoft C/C++-Programmier Dokumentation.

Geben Sie die gleiche Packungs Ebene an, wenn Sie den Mittelwert Compiler und den C-Compiler aufrufen.

Der standardmäßige Verpackungs Grad, der verwendet wird, wenn weder der Schalter **/ZP** noch [**/Pack**](-pack.md) in allen Buildumgebungen 8 angegeben wird.

> [!Note]  
> Verwenden Sie nicht **/Zp1** oder **/Zp2** auf MIPS-oder Alpha-Plattformen, und verwenden Sie **/zp4** oder **/Zp8** nicht auf 16-Bit-Plattformen. Abhängig vom Datentyp und dem Speicherort, die der C-Compiler zur Laufzeit zugewiesen hat, kann dies zu einer Ausnahme bei der Daten Ausrichtungs Änderung auf MIPS-und Alpha-Plattformen führen. Auf MS-DOS-Plattformen stellt der C-Compiler die Ausrichtung bei 4 oder 8 nicht sicher, sodass die Anwendung beendet werden kann.

 

## <a name="examples"></a>Beispiele

**Mittel l/zp4 Dateiname. idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Pack**](-pack.md)
</dt> </dl>

 

 




