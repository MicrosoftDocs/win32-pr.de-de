---
title: '\#define-Direktive (Makro)'
description: Präprozessordi directive that creates a function-like macro.
ms.assetid: 73c19cf8-fbc5-444b-a51f-dc9f881f397b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d0c54c0c433c91522c8a72c5955a419eb72f9eee
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387516"
---
# <a name="define-directive-macro"></a>\#define-Direktive (Makro)

Präprozessordi directive that creates a function-like macro.



| \#define *identifier*( *argument0*, ... , *argumentN-1* ) *token-string* |
|--------------------------------------------------------------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                                                                                                                                                                                                                          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="identifier"></span><span id="IDENTIFIER"></span>*Bezeichner*<br/>                                                                                                                                                                             | Bezeichner des Makros. <br/> Eine zweite [ \# Definition für](dx-graphics-hlsl-appendix-pre-define.md) ein Makro mit einem Bezeichner, der bereits im aktuellen Kontext vorhanden ist, generiert einen Fehler, es sei denn, die zweite Tokensequenz ist mit der ersten identisch. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="___________argument0___...___argumentN-1_________"></span><span id="___________argument0___...___argumentn-1_________"></span><span id="___________ARGUMENT0___...___ARGUMENTN-1_________"></span> ( *argument0*, ... , *argumentN-1* ) <br/> | Liste der Argumente für das Makro. Die Argumentliste ist durch Kommas getrennt, kann eine beliebige Länge haben und muss in Klammern eingeschlossen werden. Jeder Argumentname in der Liste muss eindeutig sein. Der Bezeichnerparameter und die öffnende *Klammer* können nicht durch Leerzeichen getrennt werden. <br/> Verwenden Sie die Zeilenkonkettierung, um einen zurücken Schrägstrich ( ) direkt vor dem Zeilenumbruchzeichen zu platzieren, um lange Anweisungen auf mehrere \\ Quellzeilen zu teilen. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="token-string__optional________"></span><span id="TOKEN-STRING__OPTIONAL________"></span>*token-string* \[ Optional\] <br/>                                                                                                                     | Der Wert des Makros. Dieser Parameter besteht aus einer Reihe von Token, z. B. Schlüsselwörtern, Konstanten oder vollständigen Anweisungen. Mindestens ein Leerzeichen muss diesen Parameter vom *Bezeichnerparameter* trennen. dieses Leerzeichen wird weder als Teil des ersetzten Texts noch als Leerzeichen nach dem letzten Token des Texts betrachtet. Verwenden Sie Klammern, um sicherzustellen, dass komplizierte Argumente richtig interpretiert werden. <br/> Wenn der Wert  des Bezeichnerparameters im Tokenzeichenfolgenparameter auftritt (auch als Ergebnis einer anderen Makroerweiterung), wird er nicht erweitert.  <br/> Wenn Sie diesen Parameter ausschließen,  werden alle Instanzen des Bezeichnerparameters aus der Quelldatei entfernt. Der Bezeichner bleibt definiert und kann mithilfe der [ \# if-definierten](dx-graphics-hlsl-appendix-pre-ifdef.md)Anweisungen , \# ifdef und \# ifndef getestet werden. <br/> |



 

## <a name="remarks"></a>Hinweise

Alle Instanzen des  Bezeichnerparameters, die nach der [ \# define-Direktive](dx-graphics-hlsl-appendix-pre-define.md) in der Quelldatei auftreten, bilden einen Makroaufruf, und der Bezeichner wird durch eine Version des *Tokenzeichenfolgenparameters* ersetzt, der tatsächliche Argumente durch formale Parameter ersetzt. Die Anzahl der Parameter im Aufruf muss mit der Anzahl der Parameter in der Makrodefinition übereinstimmen. Der Bezeichner wird nur ersetzt, wenn er ein Token bildet. Beispielsweise wird der Bezeichner nicht ersetzt, wenn er in einem Kommentar, innerhalb einer Zeichenfolge oder als Teil eines längeren Bezeichners angezeigt wird.

Die [ \# Undef-Direktive](dx-graphics-hlsl-appendix-pre-undef.md) weist den Präprozessor an, die Definition eines Bezeichners zu vergessen. Weitere Informationen finden Sie unter \# undef Directive (DirectX HLSL).

Das Definieren von Konstanten mit der Compileroption /D hat die gleiche Wirkung wie die Verwendung der [ \# define-Direktive](dx-graphics-hlsl-appendix-pre-define.md) am Anfang der Datei. Mit der Option /D können bis zu 30 Makros definiert werden.

Die tatsächlichen Argumente im Makroaufruf werden mit den entsprechenden formalen Argumenten in der Makrodefinition übereinstimmen. Jedes formale Argument in der Tokenzeichenfolge wird durch das entsprechende tatsächliche Argument ersetzt, es sei denn, dem Argument ist ein Zeichenfolgenoperator ( ), ein Zeichenoperator ( @) oder ein Operator gefolgt von einem -Operator \# \# \# \# \# \# vorangegangen. Alle Makros im tatsächlichen Argument werden erweitert, bevor die Anweisung den formalen Parameter ersetzt.

Das Einfing von Token im HLSL-Compiler ist etwas anders als das Einfing von Token im C-Compiler, da die einzugebenden Token selbst gültige Token sein müssen. Betrachten Sie beispielsweise die folgende Makrodefinition:


```
#define MERGE(a, b) a##b
MERGE(float, 4x4) test;
```



Im C-Compiler führt dies zu Folgendem:


```
float4x4 test
```



Im HLSL-Compiler führt dies jedoch zu Folgendem:


```
float4 x4 test
```



Sie können dieses Verhalten mithilfe der folgenden Makrodefinition vermeiden.


```
MERGE(MERGE(float, 4), x4) test;
```



## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein Makro verwendet, um Cursorzeilen zu definieren.


```
#define CURSOR(top, bottom) (((top) << 8) | (bottom))
```



Im folgenden Beispiel wird ein Makro definiert, das eine pseudozufällige ganze Zahl im angegebenen Bereich abruft.


```
#define getrandom(min, max) \
((rand()%(int)(((max) + 1)-(min)))+ (min))
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Präprozessordirektiven (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#Definieren von Überladungen](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[\#undef-Direktive (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-undef.md)
</dt> </dl>

 

 





