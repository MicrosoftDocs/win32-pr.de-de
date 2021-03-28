---
title: ID3DX11EffectScalarVariable-Schnittstelle (D3dx11effect. h)
description: Eine Effect-Skalarvariable-Schnittstelle greift auf skalare Werte zu.
ms.assetid: 52e3b856-aa1b-4ed2-b140-7ae96ec1c94b
keywords:
- ID3DX11EffectScalarVariable-Schnittstelle Direct3D 11
- ID3DX11EffectScalarVariable Interface Direct3D 11, beschrieben
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
ms.openlocfilehash: 3d07f0d14ce37f9c84c20564189e1b8475e69887
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219446"
---
# <a name="id3dx11effectscalarvariable-interface"></a>ID3DX11EffectScalarVariable-Schnittstelle

Eine Effect-Skalarvariable-Schnittstelle greift auf skalare Werte zu.

## <a name="members"></a>Member

Die **ID3DX11EffectScalarVariable** -Schnittstelle erbt von [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectScalarVariable** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX11EffectScalarVariable** -Schnittstelle verfügt über diese Methoden.



| Methode                                                             | BESCHREIBUNG                                          |
|:-------------------------------------------------------------------|:-----------------------------------------------------|
| [**GetBool**](id3dx11effectscalarvariable-getbool.md)             | Eine boolesche Variable erhalten.<br/>                   |
| [**Getboolarray**](id3dx11effectscalarvariable-getboolarray.md)   | Ein Array von booleschen Variablen erhalten.<br/>        |
| [**GetFloat**](id3dx11effectscalarvariable-getfloat.md)           | Eine Gleit Komma Variable erhalten.<br/>            |
| [**Getfloatarray**](id3dx11effectscalarvariable-getfloatarray.md) | Ein Array von Gleit Komma Variablen erhalten.<br/> |
| [**GetInt**](id3dx11effectscalarvariable-getint.md)               | Eine ganzzahlige Variable erhalten.<br/>                  |
| [**Getintarray**](id3dx11effectscalarvariable-getintarray.md)     | Ein Array von ganzzahligen Variablen erhalten.<br/>        |
| [**SetBool**](id3dx11effectscalarvariable-setbool.md)             | Legen Sie eine boolesche Variable fest.<br/>                   |
| [**Setboolarray**](id3dx11effectscalarvariable-setboolarray.md)   | Legen Sie ein Array von booleschen Variablen fest.<br/>        |
| [**SetFloat**](id3dx11effectscalarvariable-setfloat.md)           | Legen Sie eine Gleit Komma Variable fest.<br/>            |
| [**Setfloatarray**](id3dx11effectscalarvariable-setfloatarray.md) | Legen Sie ein Array von Gleit Komma Variablen fest.<br/> |
| [**SetInt**](id3dx11effectscalarvariable-setint.md)               | Legen Sie eine Integer-Variable fest.<br/>                  |
| [**"Tartintarray"**](id3dx11effectscalarvariable-setintarray.md)     | Legen Sie ein Array von ganzzahligen Variablen fest.<br/>        |



 

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen. Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Effekte 11-Schnittstellen](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





