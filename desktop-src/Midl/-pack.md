---
title: /Pack-Schalter
description: Der/Pack-Schalter ist mit der Option/ZP identisch.
ms.assetid: 381e3099-adb4-4219-bbb4-89c9e1dd3928
keywords:
- /Pack-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /pack
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c807846148d81e0e59620046d9f24380fe647c11
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104038108"
---
# <a name="pack-switch"></a>/Pack-Schalter

Der **/Pack** -Schalter ist mit der Option [**/ZP**](-zp.md) identisch.

``` syntax
midl /pack packing_level
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

*Packungs \_ Stufe* 
</dt> <dd>

Gibt die Verpackungs Ebene von Strukturen im Zielsystem an. Der Wert auf der Verpackungs Ebene kann auf 1, 2, 4 oder 8 festgelegt werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der **/Pack** -Schalter legt die Verpackungs Ebene von Strukturen im Zielsystem fest. Der Wert auf der Packungs Ebene entspricht dem Wert der [**/ZP**](-zp.md) -Option, der vom Microsoft C/C++-Compiler, Version 7,0, verwendet wird. Weitere Informationen finden Sie in der Microsoft C/C++-Programmier Dokumentation.

Geben Sie die gleiche Packungs Ebene an, wenn Sie den Mittelwert Compiler und den C-Compiler aufrufen. Der standardmäßige Verpackungs Grad, der verwendet wird, wenn weder der [**/ZP**](-zp.md) -noch der **/Pack** -Schalter angegeben ist, in beiden Buildumgebungen 8.

Eine Erläuterung der möglichen Gefahren bei der Verwendung nicht standardmäßiger Verpackungs Stufen finden Sie im [**/ZP**](-zp.md) -Hilfethema.

## <a name="examples"></a>Beispiele

**Mittel l/Pack 2 Dateiname. idl**

**Mittel l/Pack 8. idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> <dt>

[**/ENV**](-env.md)
</dt> <dt>

[**/ZP**](-zp.md)
</dt> </dl>

 

 




