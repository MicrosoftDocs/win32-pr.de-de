---
title: ID3DX11EffectScalarVariable-Schnittstelle (D3dx11effect.h)
description: Eine Effect-Scalar-Variable-Schnittstelle greifen auf Skalarwerte zu.
ms.assetid: 52e3b856-aa1b-4ed2-b140-7ae96ec1c94b
keywords:
- ID3DX11EffectScalarVariable-Schnittstelle Direct3D 11
- ID3DX11EffectScalarVariable-Schnittstelle Direct3D 11 , beschrieben
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a33445045d463591659902a4d599deddb3b33f092ef646df736d72db501fde
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119408150"
---
# <a name="id3dx11effectscalarvariable-interface"></a>ID3DX11EffectScalarVariable-Schnittstelle

Eine Effect-Scalar-Variable-Schnittstelle greifen auf Skalarwerte zu.

## <a name="members"></a>Member

Die **ID3DX11EffectScalarVariable-Schnittstelle** erbt von [**ID3DX11EffectVariable.**](id3dx11effectvariable.md) **ID3DX11EffectScalarVariable** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX11EffectScalarVariable-Schnittstelle** verfügt über diese Methoden.



| Methode                                                             | BESCHREIBUNG                                          |
|:-------------------------------------------------------------------|:-----------------------------------------------------|
| [**GetBool**](id3dx11effectscalarvariable-getbool.md)             | Hier erhalten Sie eine boolesche Variable.<br/>                   |
| [**GetBoolArray**](id3dx11effectscalarvariable-getboolarray.md)   | Hier erhalten Sie ein Array boolescher Variablen.<br/>        |
| [**Getfloat**](id3dx11effectscalarvariable-getfloat.md)           | Hier erhalten Sie eine Gleitkommavariable.<br/>            |
| [**GetFloatArray**](id3dx11effectscalarvariable-getfloatarray.md) | Hier erhalten Sie ein Array von Gleitkommavariablen.<br/> |
| [**GetInt**](id3dx11effectscalarvariable-getint.md)               | Hier erhalten Sie eine ganzzahlige Variable.<br/>                  |
| [**GetIntArray**](id3dx11effectscalarvariable-getintarray.md)     | Hier erhalten Sie ein Array von ganzzahligen Variablen.<br/>        |
| [**SetBool**](id3dx11effectscalarvariable-setbool.md)             | Legen Sie eine boolesche Variable fest.<br/>                   |
| [**SetBoolArray**](id3dx11effectscalarvariable-setboolarray.md)   | Legen Sie ein Array von booleschen Variablen fest.<br/>        |
| [**SetFloat**](id3dx11effectscalarvariable-setfloat.md)           | Legen Sie eine Gleitkommavariable fest.<br/>            |
| [**SetFloatArray**](id3dx11effectscalarvariable-setfloatarray.md) | Legen Sie ein Array von Gleitkommavariablen fest.<br/> |
| [**SetInt**](id3dx11effectscalarvariable-setint.md)               | Legen Sie eine ganzzahlige Variable fest.<br/>                  |
| [**SetIntArray**](id3dx11effectscalarvariable-setintarray.md)     | Legen Sie ein Array von ganzzahligen Variablen fest.<br/>        |



 

## <a name="remarks"></a>Hinweise

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Quelle Effects 11 verwenden, um Ihre Effekttypanwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>Nicht verfügbar (eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Effekte 11 Schnittstellen](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





