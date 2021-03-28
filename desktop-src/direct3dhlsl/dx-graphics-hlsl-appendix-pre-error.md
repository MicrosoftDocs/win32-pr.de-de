---
title: " Error-Direktive"
description: Eine Präprozessordirektive, die compilerzeitfehlermeldungen erzeugt.
ms.assetid: e32bcd6f-f2c1-43f7-a0bb-2c384b056492
keywords:
- Fehler-Direktive HLSL
topic_type:
- apiref
api_name:
- error Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 362150e494398abbc708416e6bfca6aa83756c52
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389153"
---
# <a name="error-directive"></a>\#Error-Direktive

Eine Präprozessordirektive, die compilerzeitfehlermeldungen erzeugt.



| \#Fehler *Token-Zeichenfolge* |
|------------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                                                    | BESCHREIBUNG                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="token-string"></span><span id="TOKEN-STRING"></span>*Tokenzeichenfolge*<br/> | Fehlermeldung. Dieser Parameter besteht aus einer Reihe von Token, wie z. b. Schlüsselwörtern, Konstanten oder Complete-Anweisungen. Die Tokenzeichenfolge unterliegt der Makro Erweiterung. <br/> |



 

## <a name="remarks"></a>Bemerkungen

\#Fehler Anweisungen sind besonders nützlich, wenn Sie Programmierer-Inkonsistenzen erkennen und Einschränkungen während der Vorverarbeitung verletzen. Wenn eine \# Fehler Anweisung auftritt, wird die Kompilierung beendet.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Fehler Verarbeitung während der Vorverarbeitung veranschaulicht.


```
#if !defined(__cplusplus)
  #error C++ compiler required.
#endif
```



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Präprozessordirektiven (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





