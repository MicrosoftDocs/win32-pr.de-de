---
title: def pragma-Direktive
description: Pragma-Direktive, die manuell ein Gleitkomma-Shaderregister zugibt.
ms.assetid: 45db94c4-f6f6-4c88-9bf2-4eaa9abf7844
keywords:
- def pragma Directive HLSL
topic_type:
- apiref
api_name:
- def pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe6961f5fd8c05f291af3634c07de6befada0efa54586796ca881bffe893bf5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726440"
---
# <a name="def-pragma-directive"></a>def pragma-Direktive

Pragma-Direktive, die manuell ein Gleitkomma-Shaderregister zugibt.



| \#pragma def( *target*, *register*, *val1*, *val2*,*val3*, *val4* ) |
|---------------------------------------------------------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                                        | Beschreibung                                                                 |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="target"></span><span id="TARGET"></span>*Ziel*<br/>       | Ziel, das das zu zuordnende Register enthält. <br/>                  |
| <span id="register"></span><span id="REGISTER"></span>*Registrieren*<br/> | Zu zuordnendes Gleitkomma-Shaderregister. <br/>                     |
| <span id="val0"></span><span id="VAL0"></span>*val0*<br/>             | Erstes Byte des Werts, der dem angegebenen Register zuteilen ist. <br/>  |
| <span id="val1"></span><span id="VAL1"></span>*val1*<br/>             | Zweites Byte des Werts, der dem angegebenen Register zuteilen ist. <br/> |
| <span id="val2"></span><span id="VAL2"></span>*val2*<br/>             | Drittes Byte des Werts, der dem angegebenen Register zuteilen ist. <br/>  |
| <span id="val3"></span><span id="VAL3"></span>*val3*<br/>             | Viertes Byte des Werts, der dem angegebenen Register zuteilen ist. <br/> |



 

## <a name="remarks"></a>Hinweise

Mit dem Def-Pragma kann ein Entwickler ein Gleitkomma-Shaderregister mit dem angegebenen Wert vorab ausfüllen. Dieses Pragma wird selten verwendet.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Präprozessordirektiven (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#pragma-Direktive (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





