---
title: " undef-Direktive"
description: Präprozessordirektive, die die aktuelle Definition einer Konstante oder eines Makros entfernt, die zuvor mithilfe der \define-Direktive definiert wurde.
ms.assetid: ba6bbe6b-ecfa-40cb-887f-e42b6e22c7bd
keywords:
- undef-Direktive HLSL
topic_type:
- apiref
api_name:
- undef Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f70ecdf2aca8386e730a06a982ab108cf7292c5d41af46f1b0e9ec8c9735ff97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118091122"
---
# <a name="undef-directive"></a>\#undef-Direktive

Präprozessordirektive, die die aktuelle Definition einer Konstante oder eines Makros entfernt, die zuvor mithilfe der [ \# define-Direktive](dx-graphics-hlsl-appendix-pre-define.md) definiert wurde.



| \#*Undef-Bezeichner* |
|----------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                                              | Beschreibung                                                                                                                                                      |
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="identifier"></span><span id="IDENTIFIER"></span>*Bezeichner*<br/> | Bezeichner der Konstante oder des Makros, von dem die Definition entfernt werden soll. Wenn Sie ein Makro nicht definieren, geben Sie nur den Bezeichner und nicht die Parameterliste an. <br/> |



 

## <a name="remarks"></a>Hinweise

Sie können die \# Undef-Direktive auf einen Bezeichner anwenden, der über keine vorherige Definition verfügt. Dadurch wird sichergestellt, dass der Bezeichner nicht definiert ist. Die Makroersetzung erfolgt nicht innerhalb von \# undef-Anweisungen.

Die \# Undef-Direktive wird in der Regel mit einer [ \# define-Direktive](dx-graphics-hlsl-appendix-pre-define.md) gekoppelt, um einen Bereich in einem Quellprogramm zu erstellen, in dem ein Bezeichner eine besondere Bedeutung hat. Beispielsweise kann eine bestimmte Funktion des Quellprogramms Manifestkonstanten verwenden, um umgebungsspezifische Werte zu definieren, die sich nicht auf das übrige Programm auswirken. Die \# undef-Direktive funktioniert auch mit der [)-Direktive, um die bedingte Kompilierung des Quellprogramms zu steuern.

Konstanten und Makros können mithilfe der Option /U über die Befehlszeile undefiniert werden, gefolgt von den nicht definierten Bezeichnern. Dies entspricht dem Hinzufügen einer Sequenz von \# Undef-Direktiven am Anfang der Quelldatei.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie die \# Undef-Direktive verwendet wird, um Definitionen einer symbolischen Konstante und eines Makros zu entfernen.


```
#define WIDTH           80
#define ADD( X, Y )     (X) + (Y)

#undef WIDTH
#undef ADD
```



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Präprozessordirektiven (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#define-Direktive (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[\#if, )](dx-graphics-hlsl-appendix-pre-if.md)
</dt> </dl>

 

 





