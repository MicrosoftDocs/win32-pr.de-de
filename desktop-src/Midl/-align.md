---
title: /align-Schalter
description: Der/Align-Schalter ist funktional identisch mit der Option "Mittel l/ZP" und wird vom Mittelwert des compl-Compilers nur aus Gründen der Abwärtskompatibilität mit MkTypLib erkannt.
ms.assetid: 7f303c49-a6b5-4e3c-95e5-5c49e338c766
keywords:
- /align-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /align
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 019a06be10a4937127d98d508275b57dfe508399
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104516335"
---
# <a name="align-switch"></a>/align-Schalter

Der **/align** -Schalter ist funktional identisch mit der Option "Mittel l [**/ZP**](-zp.md) " und wird vom Mittelwert des compl-Compilers nur aus Gründen der Abwärtskompatibilität mit MkTypLib erkannt.

> [!Note]  
> Das Mktyplib.exe Tool ist veraltet. Verwenden Sie stattdessen den Mittel l-Compiler.

 

``` syntax
midl /align:alignment
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

*Richt* 
</dt> <dd>

Gibt die Ausrichtung für Typen in der Bibliothek an. Der *Ausrichtungs* Wert kann 1, 2, 4 oder 8 sein. Der Wert 1 gibt die natürliche Ausrichtung an. *n* gibt die Ausrichtung auf Byte *n* an. Wenn Sie den **/align** -Schalter nicht angeben, ist der Standardwert 8.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie ein neues Makefile-Skript erstellen, verwenden Sie den [**/ZP**](-zp.md) -Schalter.

Der Ausrichtungs Wert entspricht dem [**/ZP**](-zp.md) -Optionswert, der vom Microsoft C/C++-Compiler verwendet wird. Achten Sie darauf, dass Sie die gleiche Ausrichtung angeben, wenn Sie den C-Compiler aufrufen, als wenn Sie den Mittelwert Compiler aufrufen.

Weitere Informationen finden Sie in der Microsoft C/C++-Programmier Dokumentation. Eine Erläuterung der möglichen Gefahren bei der Verwendung nicht standardmäßiger Verpackungs Stufen finden Sie im [**/ZP**](-zp.md) -Hilfethema.

## <a name="examples"></a>Beispiele

**Mittel l/align: 4 filename. idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> <dt>

[**/ZP**](-zp.md)
</dt> </dl>

 

 




