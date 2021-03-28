---
title: " line-Direktive"
description: Eine Präprozessordirektive, die die intern gespeicherte Zeilennummer und den Dateinamen des Compilers auf die angegebenen Werte festlegt.
ms.assetid: 307410af-bd78-4b3d-b515-adf58298f35f
keywords:
- line-Direktive HLSL
topic_type:
- apiref
api_name:
- line Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0932138ce5aec85ad3d3e7058db0c2a93e131181
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389151"
---
# <a name="line-directive"></a>\#line-Direktive

Eine Präprozessordirektive, die die intern gespeicherte Zeilennummer und den Dateinamen des Compilers auf die angegebenen Werte festlegt.



| \#Zeile *LineNumber* "*Dateiname*" |
|----------------------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                                                                                              | BESCHREIBUNG                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="lineNumber"></span><span id="linenumber"></span><span id="LINENUMBER"></span>*LineNumber*<br/>                    | Die festzulegende Zeilennummer. Dies kann eine beliebige ganzzahlige Konstante sein. Die Makro Ersetzung kann für die Vorverarbeitungs Token ausgeführt werden, solange das Ergebnis die richtige Syntax ergibt. <br/>                     |
| <span id="filename__optional__________"></span><span id="FILENAME__OPTIONAL__________"></span>*Dateiname* \[ optionale\] <br/> | Der festzulegende Datei Name. Der Dateiname kann eine beliebige Kombination von Zeichen sein und muss in doppelte Anführungszeichen ("") eingeschlossen werden. Wenn dieser Parameter ausgelassen wird, bleibt der vorherige Dateiname unverändert. <br/> |



 

## <a name="remarks"></a>Bemerkungen

Der Compiler verwendet die Zeilennummer und den Dateinamen, um auf Fehler zu verweisen, die während der Kompilierung gefunden werden. Die Zeilennummer verweist normalerweise auf die aktuelle Eingabezeile, und der Dateiname verweist auf die aktuelle Eingabedatei. Nach der Verarbeitung jeder Zeile wird die Zeilennummer erhöht. Wenn Sie die Zeilennummer und den Dateinamen ändern, ignoriert der Compiler die vorherigen Werte und setzt die Verarbeitung mit den neuen Werten fort. Die \# line-Direktive wird in der Regel von Programm-Generatoren verwendet, damit Fehlermeldungen auf die ursprüngliche Quelldatei und nicht auf das generierte Programm verweisen.

Der Konvertierer verwendet die Zeilennummer und den Dateinamen, um die Werte der vordefinierten \_ \_ Datei \_ \_ und \_ \_ Zeile \_ \_ der Makros zu bestimmen. Sie können diese Makros verwenden, um selbsterklärende Fehlermeldungen in den Programmtext einzufügen. Das \_ \_ Datei \_ \_ Makro wird zu einer Zeichenfolge erweitert, deren Inhalt der Dateiname ist, umgeben von doppelten Anführungszeichen ("").

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Zeilennummer auf 151 und der Dateiname auf "Copy. c" festgelegt.


```
#line 151 "copy.c"
```



Im folgenden Beispiel verwendet das Makro Assert die vordefinierte Makros \_ \_ -Zeile \_ \_ und- \_ \_ Datei \_ \_ , um eine Fehlermeldung zur Quelldatei auszugeben, wenn die angegebene Behauptung nicht true ist.


```
#define ASSERT(cond)

if( !(cond) )\
{printf( "assertion error line %d, file(%s)\n", \
__LINE__, __FILE__ );}
```



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Präprozessordirektiven (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





