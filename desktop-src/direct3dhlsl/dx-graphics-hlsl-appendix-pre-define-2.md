---
title: '\#define-Direktive (Makro)'
description: Eine Präprozessordirektive, die ein Funktions ähnliches Makro erstellt.
ms.assetid: 73c19cf8-fbc5-444b-a51f-dc9f881f397b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a8de5a47fc92c02e9f565c80f600359e8e5b32f9
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "104993278"
---
# <a name="define-directive-macro"></a>\#define-Direktive (Makro)

Eine Präprozessordirektive, die ein Funktions ähnliches Makro erstellt.



| \#*Bezeichner* definieren ( *argument0*,..., *argumentn-1* ) *Tokenzeichenfolge* |
|--------------------------------------------------------------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                                                                                                                                                                                                                          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="identifier"></span><span id="IDENTIFIER"></span>*Figur*<br/>                                                                                                                                                                             | Der Bezeichner des Makros. <br/> Eine zweite [ \# Definition](dx-graphics-hlsl-appendix-pre-define.md) für ein Makro mit einem Bezeichner, der bereits im aktuellen Kontext vorhanden ist, generiert einen Fehler, es sei denn, die zweite tokensequenz ist mit der ersten identisch. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="___________argument0___...___argumentN-1_________"></span><span id="___________argument0___...___argumentn-1_________"></span><span id="___________ARGUMENT0___...___ARGUMENTN-1_________"></span> ( *argument0*,..., *argumentn-1* ) <br/> | Liste der Argumente für das Makro. Die Argumentliste ist durch Kommas getrennt, kann eine beliebige Länge aufweisen und muss in Klammern eingeschlossen werden. Jeder Argument Name in der Liste muss eindeutig sein. Der *bezeichnerparameter* und die öffnende Klammer können nicht durch Leerzeichen getrennt werden. <br/> Zeilen Verkettung platzieren platzieren Sie einen umgekehrten Schrägstrich ( \) unmittelbar vor dem Zeilen Umleitungs Zeichen, um lange Direktiven in mehrere Quellzeilen aufzuteilen. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="token-string__optional________"></span><span id="TOKEN-STRING__OPTIONAL________"></span>*Tokenzeichenfolge* \[ optionale\] <br/>                                                                                                                     | Der Wert des Makros. Dieser Parameter besteht aus einer Reihe von Token, wie z. b. Schlüsselwörtern, Konstanten oder Complete-Anweisungen. Dieser Parameter muss von einem oder mehreren Leerzeichen vom *bezeichnerparameter* getrennt werden. Dieser Leerraum wird nicht als Teil des ersetzten Texts betrachtet, und es ist kein Leerraum nach dem letzten Token des Texts enthalten. Nehmen Sie eine liberale Verwendung von Klammern vor, um sicherzustellen, dass komplizierte Argumente ordnungsgemäß interpretiert werden. <br/> Wenn der Wert des *bezeichnerparameters* innerhalb des *Tokenzeichenfolgen-* Parameters auftritt (auch als Ergebnis einer anderen Makro Erweiterung), wird er nicht erweitert. <br/> Wenn Sie diesen Parameter ausschließen, werden alle Instanzen des *bezeichnerparameters* aus der Quelldatei entfernt. Der Bezeichner bleibt definiert und kann mithilfe der Direktiven [ \# if defined](dx-graphics-hlsl-appendix-pre-ifdef.md), \# ifdef und \# ifndef getestet werden. <br/> |



 

## <a name="remarks"></a>Bemerkungen

Alle Instanzen des *bezeichnerparameters* , die nach der [ \# define](dx-graphics-hlsl-appendix-pre-define.md) -Direktive in der Quelldatei auftreten, bilden einen Makro-Aufrufwert, und der Bezeichner wird durch eine Version des *Tokenzeichenfolgen-* Parameters ersetzt, der tatsächliche Argumente für formale Parameter ersetzt. Die Anzahl der Parameter im-Aufrufwert muss mit der Anzahl von Parametern in der Makro Definition identisch sein. Der Bezeichner wird nur ersetzt, wenn er ein Token bildet. Beispielsweise wird der Bezeichner nicht ersetzt, wenn er in einem Kommentar, innerhalb einer Zeichenfolge oder als Teil eines längeren Bezeichners angezeigt wird.

Die [ \# undef](dx-graphics-hlsl-appendix-pre-undef.md) -Direktive weist den Präprozessor an, die Definition eines Bezeichners zu vergessen. Weitere Informationen finden Sie unter \# undef-Direktive (DirectX HLSL).

Das Definieren von Konstanten mit der/D-Compileroption hat dieselbe Auswirkung wie die Verwendung der [ \# define](dx-graphics-hlsl-appendix-pre-define.md) -Direktive am Anfang der Datei. Bis zu 30 Makros können mit der/D-Option definiert werden.

Die tatsächlichen Argumente im Makro-Befehl werden mit den entsprechenden formalen Argumenten in der Makro Definition abgeglichen. Jedes formale Argument in der Tokenzeichenfolge wird durch das entsprechende tatsächliche Argument ersetzt, es sei denn, dem Argument ist ein \# Zeichen folgen Operator (), ein \# Zeichen (@) oder ein tokeneinfügeoperator ( \# \# ) oder ein \# \# Operator gefolgt. Alle Makros im tatsächlichen Argument werden erweitert, bevor die Anweisung den formalen Parameter ersetzt.

Das Einfügen von Token im HLSL-Compiler unterscheidet sich geringfügig von der tokeneinfügefunktion im C-Compiler, da die eingefügten Token selbst gültige Token sein müssen. Beachten Sie beispielsweise die folgende Makro Definition:


```
#define MERGE(a, b) a##b
MERGE(float, 4x4) test;
```



Im C-Compiler führt dies zu folgendem:


```
float4x4 test
```



Im HLSL-Compiler führt dies jedoch zu folgendem:


```
float4 x4 test
```



Sie können dieses Verhalten umgehen, indem Sie stattdessen die folgende Makro Definition verwenden.


```
MERGE(MERGE(float, 4), x4) test;
```



## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein-Makro zum Definieren von Cursor Linien verwendet.


```
#define CURSOR(top, bottom) (((top) << 8) | (bottom))
```



Im folgenden Beispiel wird ein Makro definiert, das eine Pseudo Zufalls-Ganzzahl im angegebenen Bereich abruft.


```
#define getrandom(min, max) \
((rand()%(int)(((max) + 1)-(min)))+ (min))
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Präprozessordirektiven (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#Definieren von über Ladungen](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[\#undef-Direktive (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-undef.md)
</dt> </dl>

 

 





