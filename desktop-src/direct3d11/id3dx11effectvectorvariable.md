---
title: ID3DX11EffectVectorVariable-Schnittstelle (D3dx11effect.h)
description: Eine Vektorvariablenschnittstelle greifen auf einen Vektor mit vier Komponenten zu.
ms.assetid: 191d373b-0562-4d7b-ac3f-cd24abf259bc
keywords:
- ID3DX11EffectVectorVariable-Schnittstelle Direct3D 11
- ID3DX11EffectVectorVariable-Schnittstelle Direct3D 11 , beschrieben
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9343659ac249153805e3dfc4c97595957dfbe52bf7be5c498d81f357c66db8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119851540"
---
# <a name="id3dx11effectvectorvariable-interface"></a>ID3DX11EffectVectorVariable-Schnittstelle

Eine Vektorvariablenschnittstelle greifen auf einen Vektor mit vier Komponenten zu.

## <a name="members"></a>Member

Die **ID3DX11EffectVectorVariable-Schnittstelle** erbt von [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectVectorVariable** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX11EffectVectorVariable-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                         | BESCHREIBUNG                                                                         |
|:-------------------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**GetBoolVector**](id3dx11effectvectorvariable-getboolvector.md)             | Sie erhalten einen Vektor mit vier Komponenten, der boolesche Daten enthält.<br/>                  |
| [**GetBoolVectorArray**](id3dx11effectvectorvariable-getboolvectorarray.md)   | Get an array of four-component vectors that contain boolean data. (Ein Array von Vektoren mit vier Komponenten, die boolesche Daten enthalten.)<br/>        |
| [**GetFloatVector**](id3dx11effectvectorvariable-getfloatvector.md)           | Sie erhalten einen Vektor mit vier Komponenten, der Gleitkommadaten enthält.<br/>           |
| [**GetFloatVectorArray**](id3dx11effectvectorvariable-getfloatvectorarray.md) | Sie erhalten ein Array von Vektoren mit vier Komponenten, die Gleitkommadaten enthalten.<br/> |
| [**GetIntVector**](id3dx11effectvectorvariable-getintvector.md)               | Sie erhalten einen Vektor mit vier Komponenten, der ganzzahlige Daten enthält.<br/>                  |
| [**GetIntVectorArray**](id3dx11effectvectorvariable-getintvectorarray.md)     | Sie erhalten ein Array von Vektoren mit vier Komponenten, die ganzzahlige Daten enthalten.<br/>        |
| [**SetBoolVector**](id3dx11effectvectorvariable-setboolvector.md)             | Legen Sie einen Vektor mit vier Komponenten fest, der boolesche Daten enthält.<br/>                  |
| [**SetBoolVectorArray**](id3dx11effectvectorvariable-setboolvectorarray.md)   | Legen Sie ein Array von Vektoren mit vier Komponenten fest, die boolesche Daten enthalten.<br/>        |
| [**SetFloatVector**](id3dx11effectvectorvariable-setfloatvector.md)           | Legen Sie einen Vektor mit vier Komponenten fest, der Gleitkommadaten enthält.<br/>           |
| [**SetFloatVectorArray**](id3dx11effectvectorvariable-setfloatvectorarray.md) | Legen Sie ein Array von Vektoren mit vier Komponenten fest, die Gleitkommadaten enthalten.<br/> |
| [**SetIntVector**](id3dx11effectvectorvariable-setintvector.md)               | Legen Sie einen Vektor mit vier Komponenten fest, der ganzzahlige Daten enthält.<br/>                  |
| [**SetIntVectorArray**](id3dx11effectvectorvariable-setintvectorarray.md)     | Legen Sie ein Array von Vektoren mit vier Komponenten fest, die ganzzahlige Daten enthalten.<br/>        |



 

## <a name="remarks"></a>Hinweise

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Quelle Effects 11 verwenden, um Ihre Effekttypanwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>Nicht verfügbar (eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Effekte 11 Schnittstellen](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





