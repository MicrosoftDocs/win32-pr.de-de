---
title: " pragma-Direktive"
description: Präprozessordirektive, die computerspezifische oder betriebssystemspezifische Features bereitstellt und gleichzeitig die Allgemeine Kompatibilität mit den Sprachen C und C++ beibehält.
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
ms.openlocfilehash: a16101eac6f303dbba03819c8d9f460c06c2613c748ef8ce4c74ae3fe30bb0f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024610"
---
# <a name="pragma-directive"></a>\#pragma-Direktive

Präprozessordirektive, die computerspezifische oder betriebssystemspezifische Features bereitstellt und gleichzeitig die Allgemeine Kompatibilität mit den Sprachen C und C++ beibehält.



| \#pragma *token-string* |
|-------------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                                                    | BESCHREIBUNG                                                                                                                              |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="token-string"></span><span id="TOKEN-STRING"></span>*Tokenzeichenfolge*<br/> | Eine Reihe von Zeichen, die eine bestimmte Compileranweisung und Argumente liefern. Dieser Parameter unterliegt der Makroerweiterung. <br/> |



 

## <a name="remarks"></a>Hinweise

Wenn der Compiler ein Pragma findet, das nicht erkannt wird, gibt er eine Warnung aus, aber die Kompilierung wird fortgesetzt.

Der HLSL-Compiler erkennt die folgenden Pragmas:

-   [Def](dx-graphics-hlsl-appendix-pre-pragma-def.md)
-   [Nachricht](message-pragma-directive--directx-hlsl-.md)
-   [\_Packmatrix](dx-graphics-hlsl-appendix-pre-pragma-pack-matrix.md)
-   [warning](dx-graphics-hlsl-appendix-pre-pragma-warning.md)

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Präprozessordirektiven (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





