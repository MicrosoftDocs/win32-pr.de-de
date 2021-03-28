---
title: '\#define-Direktive (Konstante)'
description: Eine Präprozessordirektive, die einer Konstanten in der Anwendung einen aussagekräftigen Namen zuweist.
ms.assetid: cc9b34a3-4c83-4999-99ec-e6261ecb2785
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: deae1ca92c2280cd31cbec2bf3482c61fcf2b88a
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "104038380"
---
# <a name="define-directive-constant"></a>\#define-Direktive (Konstante)

Eine Präprozessordirektive, die einer Konstanten in der Anwendung einen aussagekräftigen Namen zuweist.



| \#" *identifiertoken-String* " definieren |
|-----------------------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                                                                                       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="identifier"></span><span id="IDENTIFIER"></span>*Figur*<br/>                                          | Der Bezeichner der Konstanten. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="token-string__optional_"></span><span id="TOKEN-STRING__OPTIONAL_"></span>*Tokenzeichenfolge* \[ optionale\]<br/> | Der Wert der Konstanten. Dieser Parameter besteht aus einer Reihe von Token, wie z. b. Schlüsselwörtern, Konstanten oder Complete-Anweisungen. Dieser Parameter muss von einem oder mehreren Leerzeichen vom *bezeichnerparameter* getrennt werden. Dieser Leerraum wird nicht als Teil des ersetzten Texts betrachtet, und es ist kein Leerraum nach dem letzten Token des Texts enthalten. <br/> Wenn Sie diesen Parameter ausschließen, werden alle Instanzen des *bezeichnerparameters* aus der Quelldatei entfernt. Der Bezeichner bleibt definiert und kann mithilfe der Direktiven [ \# if defined](dx-graphics-hlsl-appendix-pre-ifdef.md), \# ifdef und \# ifndef getestet werden. <br/> |



 

## <a name="remarks"></a>Bemerkungen

Alle Instanzen des *bezeichnerparameters* , die nach der [ \# define](dx-graphics-hlsl-appendix-pre-define.md) -Direktive in der Quelldatei auftreten, werden durch den Wert des *Tokenzeichenfolgen-* Parameters ersetzt. Der Bezeichner wird nur ersetzt, wenn er ein Token bildet. Beispielsweise wird der Bezeichner nicht ersetzt, wenn er in einem Kommentar, innerhalb einer Zeichenfolge oder als Teil eines längeren Bezeichners angezeigt wird.

Die [ \# undef](dx-graphics-hlsl-appendix-pre-undef.md) -Direktive weist den Präprozessor an, die Definition eines Bezeichners zu vergessen. Weitere Informationen finden Sie unter \# undef-Direktive (DirectX HLSL).

Das Definieren von Konstanten mit der/D-Compileroption hat dieselbe Auswirkung wie die Verwendung der [ \# define](dx-graphics-hlsl-appendix-pre-define.md) -Direktive am Anfang der Datei. Bis zu 30 Konstanten können mit der/D-Option definiert werden. Ein Beispiel für die Verwendung dieser Vorgehensweise finden Sie im Abschnitt "Beispiele" von [ \# ifdef und)](dx-graphics-hlsl-appendix-pre-ifdef.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die bezeichnerbreite als ganzzahlige Konstante 80 definiert, und anschließend wird die Länge in Bezug auf die Breite und die ganzzahlige Konstante 10 definiert.


```
#define WIDTH       80
#define LENGTH      ( WIDTH + 10 )
```



Jede nachfolgende Instanz der Länge wird durch (Width + 10) ersetzt, und jede nachfolgende Instanz der Breite + 10 wird durch den Ausdruck ersetzt (80 + 10). Die Klammern um Breite + 10 sind wichtig, da Sie die Interpretation in Anweisungen wie den folgenden Steuern.


```
var = LENGTH * 20;
```



Nach der Vorverarbeitungs Phase wird die-Anweisung wie folgt ausgewertet und ergibt den Wert 1.800.


```
var = ( 80 + 10 ) * 20;
```



Ohne Klammern wäre das Ergebnis das folgende, das als 280 ausgewertet wird.


```
var = 80 + 10 * 20;
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Präprozessordirektiven (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#Definieren von über Ladungen](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[\#undef-Direktive (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-undef.md)
</dt> </dl>

 

 





