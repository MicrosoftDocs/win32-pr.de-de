---
title: Registrieren
description: Registrieren
ms.assetid: 45149f8c-8b76-4247-98d7-d141d7268da3
keywords:
- REGISTRIEREN VON HLSL
topic_type:
- apiref
api_name:
- register
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0102716529471b3e867e17b0e9b635274cdfc28ec603f239d66c76ffb0fdaa19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983210"
---
# <a name="register"></a>Registrieren

Optionales Schlüsselwort zum Zuweisen einer Shadervariable zu einem bestimmten Register, das die folgende Syntax verwendet:



| : register ( *\[ shader \_ profile \]*, *Type \# \[ subcomponent \]* ) |
|----------------------------------------------------------------|



 

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="register"></span><span id="REGISTER"></span>Registrieren
</dt> <dd>

Erforderliches Schlüsselwort.

</dd> <dt>

<span id="_shader_profile_"></span><span id="_SHADER_PROFILE_"></span>*\[\_Shaderprofil\]*
</dt> <dd>

Optionales [Shaderprofil,](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax)bei dem es sich um ein Shaderziel oder einfach **ps** oder **im Vergleich zu** sein kann.

</dd> <dt>

<span id="Type__subcomponent_"></span><span id="type__subcomponent_"></span><span id="TYPE__SUBCOMPONENT_"></span>*\# \[ Typunterkomponente\]*
</dt> <dd>

Registertyp, Zahl und Unterkomponentendeklaration.

-   Der Typ ist einer der folgenden:

    

    | type | Registerbeschreibung       |
    |------|----------------------------|
    | b    | Konstantenpuffer            |
    | t    | Textur- und Texturpuffer |
    | c    | Pufferoffset              |
    | s    | Sampler                    |
    | u    | Ungeordnete Zugriffsansicht      |

    

     

-   *\#* ist die Registernummer, bei der es sich um eine ganzzahlige Zahl handelt.
-   Die *Unterkomponente* ist eine optionale ganzzahlige Zahl.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Sie können derselben Variablendeklaration eine oder mehrere Registerzuweisungen hinzufügen, die durch Leerzeichen getrennt sind.

Für Direct3D 10-Variablen im globalen Gültigkeitsbereich verhält sich das **Schlüsselwort register** genauso wie das [Schlüsselwort packoffset (DirectX HLSL).](dx-graphics-hlsl-variable-packoffset.md)

## <a name="examples"></a>Beispiele

Hier sind einige Beispiele:


```
sampler myVar : register( ps_5_0, s ); 
```




```
sampler myVar : register( vs, s[8] );
```




```
sampler myVar : register( ps, s[2] ) 
              : register( ps_5_0, s[0] ) 
              : register( vs, s[8] );
```



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Variablensyntax](dx-graphics-hlsl-variable-syntax.md)
</dt> <dt>

[Variablen (DirectX HLSL)](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 