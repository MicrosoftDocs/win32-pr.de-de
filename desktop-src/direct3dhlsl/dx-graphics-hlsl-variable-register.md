---
title: Registrieren
description: Registrieren
ms.assetid: 45149f8c-8b76-4247-98d7-d141d7268da3
keywords:
- HLSL registrieren
topic_type:
- apiref
api_name:
- register
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b378cd97bc9779951d62873d393009c98d32823
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390347"
---
# <a name="register"></a>Registrieren

Optionales Schlüsselwort zum Zuweisen einer shadervariablen zu einem bestimmten Register, das folgende Syntax verwendet:



| : Register ( *\[ Shader \_ - \] Profil*, *Typ \# \[ unter \] Komponente* ) |
|----------------------------------------------------------------|



 

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="register"></span><span id="REGISTER"></span>sich
</dt> <dd>

Erforderliches Schlüsselwort.

</dd> <dt>

<span id="_shader_profile_"></span><span id="_SHADER_PROFILE_"></span>*\[Shader- \_ Profil\]*
</dt> <dd>

Optionales [Shader-Profil](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax), das ein Shader-Ziel oder einfach **PS** oder **vs** sein kann

</dd> <dt>

<span id="Type__subcomponent_"></span><span id="type__subcomponent_"></span><span id="TYPE__SUBCOMPONENT_"></span>*\# \[ Typsubcomponent\]*
</dt> <dd>

Registrieren Sie den Typ, die Zahl und die unter Komponenten Deklaration.

-   Der Typ ist einer der folgenden:

    

    | type | Register Beschreibung       |
    |------|----------------------------|
    | b    | Konstanter Puffer            |
    | t    | Textur-und Textur Puffer |
    | c    | Puffer Offset              |
    | s    | Sampler                    |
    | u    | Ansicht für ungeordnete Zugriffe      |

    

     

-   *\#* die Registernummer, bei der es sich um eine ganzzahlige Zahl handelt.
-   Die *Unterkomponente* ist eine optionale ganzzahlige Zahl.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Sie können einer Variablen Deklaration eine oder mehrere Registrierungs Zuweisungen hinzufügen, die durch Leerzeichen getrennt sind.

Bei Direct3D 10-Variablen im globalen Gültigkeitsbereich verhält sich das **Register** -Schlüsselwort genauso wie das Schlüsselwort " [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md) ".

## <a name="examples"></a>Beispiele

Hier einige Beispiele:


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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Variablensyntax](dx-graphics-hlsl-variable-syntax.md)
</dt> <dt>

[Variablen (DirectX HLSL)](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 