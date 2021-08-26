---
title: " error-Direktive"
description: Präprozessordirektive, die Fehlermeldungen zur Compilerzeit erzeugt.
ms.assetid: e32bcd6f-f2c1-43f7-a0bb-2c384b056492
keywords:
- error Directive HLSL
topic_type:
- apiref
api_name:
- error Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5fa1af02a693b5168a2d96e653726fd0a468587bf2b8c1825afbf8e73057f61f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068330"
---
# <a name="error-directive"></a>\#error-Direktive

Präprozessordirektive, die Fehlermeldungen zur Compilerzeit erzeugt.



| \#*Fehlertokenzeichenfolge* |
|------------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                                                    | BESCHREIBUNG                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="token-string"></span><span id="TOKEN-STRING"></span>*Tokenzeichenfolge*<br/> | Fehlermeldung. Dieser Parameter besteht aus einer Reihe von Token, z. B. Schlüsselwörtern, Konstanten oder vollständigen Anweisungen. Die Tokenzeichenfolge unterliegt der Makroerweiterung. <br/> |



 

## <a name="remarks"></a>Hinweise

\#Fehlerdirektiven sind besonders nützlich, um Inkonsistenzen von Programmierern und Verstöße gegen Einschränkungen während der Vorverarbeitung zu erkennen. Wenn eine \# Fehlerdirektive gefunden wird, wird die Kompilierung beendet.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Fehlerverarbeitung während der Vorverarbeitung veranschaulicht.


```
#if !defined(__cplusplus)
  #error C++ compiler required.
#endif
```



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Präprozessordirektiven (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





