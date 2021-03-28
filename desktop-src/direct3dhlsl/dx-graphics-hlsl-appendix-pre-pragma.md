---
title: " pragma-Direktive"
description: Eine Präprozessordirektive, die Computer spezifische oder betriebssystemspezifische Features bereitstellt und gleichzeitig die Gesamt Kompatibilität mit den Programmiersprachen C und C++ beibehält.
ms.assetid: 806ddb9b-ae4b-4dd3-a2c4-39c9cb7f3820
keywords:
- pragma-Direktive HLSL
topic_type:
- apiref
api_name:
- pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f843a218e39daf616fa6c59ca27f73a5511f17b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104037986"
---
# <a name="pragma-directive"></a>\#pragma-Direktive

Eine Präprozessordirektive, die Computer spezifische oder betriebssystemspezifische Features bereitstellt und gleichzeitig die Gesamt Kompatibilität mit den Programmiersprachen C und C++ beibehält.



| \#Pragma *-Token-Zeichenfolge* |
|-------------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                                                    | BESCHREIBUNG                                                                                                                              |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="token-string"></span><span id="TOKEN-STRING"></span>*Tokenzeichenfolge*<br/> | Eine Reihe von Zeichen, die eine bestimmte Compileranweisung und Argumente enthält. Dieser Parameter unterliegt der Makro Erweiterung. <br/> |



 

## <a name="remarks"></a>Bemerkungen

Wenn der Compiler ein Pragma findet, das er nicht erkennt, gibt er eine Warnung aus, die Kompilierung wird jedoch fortgesetzt.

Der HLSL-Compiler erkennt die folgenden Pragmas:

-   [auflösenden](dx-graphics-hlsl-appendix-pre-pragma-def.md)
-   [Nachricht](message-pragma-directive--directx-hlsl-.md)
-   [Paket \_ Matrix](dx-graphics-hlsl-appendix-pre-pragma-pack-matrix.md)
-   [warning](dx-graphics-hlsl-appendix-pre-pragma-warning.md)

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Präprozessordirektiven (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





