---
title: DEF-pragma-Direktive
description: Pragma-Direktive, die manuell ein Gleit Komma-Shader-Register zugeordnet.
ms.assetid: 45db94c4-f6f6-4c88-9bf2-4eaa9abf7844
keywords:
- DEF-pragma-Direktive HLSL
topic_type:
- apiref
api_name:
- def pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2a921e17f8ddee4aaabfe50e75f42ce44812863d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104992911"
---
# <a name="def-pragma-directive"></a>DEF-pragma-Direktive

Pragma-Direktive, die manuell ein Gleit Komma-Shader-Register zugeordnet.



| \#pragma DEF ( *target*, *Register*, *Wert1*, *Wert2*,*val3*, *val4* ) |
|---------------------------------------------------------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                                        | BESCHREIBUNG                                                                 |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="target"></span><span id="TARGET"></span>*Spar*<br/>       | Das Ziel, das das zuzuordnende Register enthält. <br/>                  |
| <span id="register"></span><span id="REGISTER"></span>*sich*<br/> | Die zuzuordnende Gleit Komma-Shader-Registrierung. <br/>                     |
| <span id="val0"></span><span id="VAL0"></span>*val0*<br/>             | Das erste Byte des Werts, der dem angegebenen Register zuzuordnen ist. <br/>  |
| <span id="val1"></span><span id="VAL1"></span>*Wert1*<br/>             | Zweites Byte des Werts, der dem angegebenen Register zuzuordnen ist. <br/> |
| <span id="val2"></span><span id="VAL2"></span>*Wert2*<br/>             | Drittes Byte des Werts, der dem angegebenen Register zuzuordnen ist. <br/>  |
| <span id="val3"></span><span id="VAL3"></span>*val3*<br/>             | Viertes Byte des Werts, der dem angegebenen Register zuzuordnen ist. <br/> |



 

## <a name="remarks"></a>Bemerkungen

Mithilfe des DEF-Pragmas kann ein Entwickler ein Gleit Komma-Shader-Register mit dem angegebenen Wert vorab ausfüllen. Dieses Pragma wird nur selten verwendet.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Präprozessordirektiven (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#pragma-Direktive (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





