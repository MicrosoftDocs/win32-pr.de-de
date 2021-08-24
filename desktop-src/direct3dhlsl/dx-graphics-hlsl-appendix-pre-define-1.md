---
title: '\#define-Direktive (Konstante)'
description: Präprozessordi directive that assigns a meaningful name to a constant in your application. (Präprozessordi direktive, die einer Konstante in Ihrer Anwendung einen aussagekräftigen Namen zuordnt.
ms.assetid: cc9b34a3-4c83-4999-99ec-e6261ecb2785
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 06e3992dd81d2ffcc32a672e2d524fa51c1372c02ab90d8b6b8a905100ac9afb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855050"
---
# <a name="define-directive-constant"></a>\#define-Direktive (Konstante)

Präprozessordi directive that assigns a meaningful name to a constant in your application. (Präprozessordi direktive, die einer Konstante in Ihrer Anwendung einen aussagekräftigen Namen zuordnt.



| \#Define *identifiertoken-string* |
|-----------------------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                                                                                       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="identifier"></span><span id="IDENTIFIER"></span>*Bezeichner*<br/>                                          | Bezeichner der Konstante. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="token-string__optional_"></span><span id="TOKEN-STRING__OPTIONAL_"></span>*token-string* \[ Optional\]<br/> | Der Wert der Konstante. Dieser Parameter besteht aus einer Reihe von Token, z. B. Schlüsselwörtern, Konstanten oder vollständigen Anweisungen. Mindestens ein Leerzeichen muss diesen Parameter vom *Bezeichnerparameter* trennen. dieses Leerzeichen wird weder als Teil des ersetzten Texts noch als Leerzeichen nach dem letzten Token des Texts betrachtet. <br/> Wenn Sie diesen Parameter ausschließen,  werden alle Instanzen des Bezeichnerparameters aus der Quelldatei entfernt. Der Bezeichner bleibt definiert und kann mithilfe der [ \# if-definierten](dx-graphics-hlsl-appendix-pre-ifdef.md)Anweisungen , \# ifdef und \# ifndef getestet werden. <br/> |



 

## <a name="remarks"></a>Hinweise

Alle Instanzen des  Bezeichnerparameters, die nach der [ \# define-Direktive](dx-graphics-hlsl-appendix-pre-define.md) in der Quelldatei auftreten, werden durch den Wert des Parameters *token-string* ersetzt. Der Bezeichner wird nur ersetzt, wenn er ein Token bildet. Beispielsweise wird der Bezeichner nicht ersetzt, wenn er in einem Kommentar, innerhalb einer Zeichenfolge oder als Teil eines längeren Bezeichners angezeigt wird.

Die [ \# Undef-Direktive](dx-graphics-hlsl-appendix-pre-undef.md) weist den Präprozessor an, die Definition eines Bezeichners zu vergessen. Weitere Informationen finden Sie unter \# undef Directive (DirectX HLSL).

Das Definieren von Konstanten mit der Compileroption /D hat die gleiche Wirkung wie die Verwendung der [ \# define-Direktive](dx-graphics-hlsl-appendix-pre-define.md) am Anfang der Datei. Mit der Option /D können bis zu 30 Konstanten definiert werden. Ein Beispiel dafür, wie dies verwendet werden kann, finden Sie im Abschnitt Beispiele von [ \# ifdef und ).](dx-graphics-hlsl-appendix-pre-ifdef.md)

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird der Bezeichner WIDTH als ganzzahlige Konstante 80 definiert und dann LENGTH in Bezug auf WIDTH und die ganzzahlige Konstante 10 definiert.


```
#define WIDTH       80
#define LENGTH      ( WIDTH + 10 )
```



Jede nachfolgende Instanz von LENGTH wird durch (WIDTH + 10) ersetzt, und jede nachfolgende Instanz von WIDTH + 10 wird durch den Ausdruck (80 + 10) ersetzt. Die Klammern um WIDTH + 10 sind wichtig, da sie die Interpretation in Anweisungen wie den folgenden steuern.


```
var = LENGTH * 20;
```



Nach der Vorverarbeitungsphase wird die Anweisung wie folgt, die zu 1.800 ausgewertet wird.


```
var = ( 80 + 10 ) * 20;
```



Ohne Klammern würde das Ergebnis wie folgt sein, was zu 280 ausgewertet wird.


```
var = 80 + 10 * 20;
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Präprozessordirektiven (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#Definieren von Überladungen](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[\#undef-Direktive (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-undef.md)
</dt> </dl>

 

 





