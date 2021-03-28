---
title: " undef-Direktive"
description: Eine Präprozessordirektive, mit der die aktuelle Definition einer Konstante oder eines Makros entfernt wird, die zuvor mit der \ define-Direktive definiert wurde.
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
ms.openlocfilehash: 7358dc60d002e784394f64773934a18f7413e493
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312552"
---
# <a name="undef-directive"></a>\#undef-Direktive

Eine Präprozessordirektive, die die aktuelle Definition einer Konstante oder eines Makros entfernt, die zuvor mit der [ \# define](dx-graphics-hlsl-appendix-pre-define.md) -Direktive definiert wurde.



| \#undef- *Bezeichner* |
|----------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                                              | BESCHREIBUNG                                                                                                                                                      |
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="identifier"></span><span id="IDENTIFIER"></span>*Figur*<br/> | Der Bezeichner der Konstante oder des Makros, dessen Definition entfernt werden soll. Wenn Sie ein Makro definieren, geben Sie nur den Bezeichner und nicht die Parameterliste an. <br/> |



 

## <a name="remarks"></a>Bemerkungen

Sie können die \# undef-Direktive auf einen Bezeichner anwenden, der keine vorherige Definition hat. Dadurch wird sichergestellt, dass der Bezeichner nicht definiert ist. Makro Ersetzung wird nicht innerhalb von \# undef-Anweisungen ausgeführt.

Die \# undef-Direktive wird in der Regel mit einer [ \# define](dx-graphics-hlsl-appendix-pre-define.md) -Direktive gekoppelt, um einen Bereich in einem Quell Programm zu erstellen, in dem ein Bezeichner eine besondere Bedeutung hat. Beispielsweise kann eine bestimmte Funktion des Quellprogramms Manifestkonstanten verwenden, um umgebungsspezifische Werte zu definieren, die sich nicht auf das übrige Programm auswirken. Die \# undef-Direktive funktioniert auch mit der [)-Direktive, um die bedingte Kompilierung des Quell Programms zu steuern.

Konstanten und Makros können mithilfe der/U-Option in der Befehlszeile nicht definiert werden, gefolgt von den bezeichlern, die nicht definiert werden sollen. Dies entspricht dem Hinzufügen einer Sequenz von \# undef-Direktiven am Anfang der Quelldatei.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie die \# undef-Direktive verwendet wird, um Definitionen einer symbolischen Konstante und eines Makros zu entfernen.


```
#define WIDTH           80
#define ADD( X, Y )     (X) + (Y)

#undef WIDTH
#undef ADD
```



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Präprozessordirektiven (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#define-Direktive (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[\#Wenn,)](dx-graphics-hlsl-appendix-pre-if.md)
</dt> </dl>

 

 





