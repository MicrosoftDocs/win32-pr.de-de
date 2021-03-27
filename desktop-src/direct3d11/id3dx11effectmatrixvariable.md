---
title: ID3DX11EffectMatrixVariable-Schnittstelle (D3dx11effect. h)
description: Eine Matrix Variable-Schnittstelle greift auf eine Matrix zu.
ms.assetid: 44f30d1a-3ec1-49d7-92c0-475cf2fa4d2a
keywords:
- ID3DX11EffectMatrixVariable-Schnittstelle Direct3D 11
- ID3DX11EffectMatrixVariable Interface Direct3D 11, beschrieben
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5c4c89a231d429fc0a1f8fecbcbb4d06db35cb5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982366"
---
# <a name="id3dx11effectmatrixvariable-interface"></a>ID3DX11EffectMatrixVariable-Schnittstelle

Eine Matrix Variable-Schnittstelle greift auf eine Matrix zu.

## <a name="members"></a>Member

Die **ID3DX11EffectMatrixVariable** -Schnittstelle erbt von [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectMatrixVariable** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX11EffectMatrixVariable** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                 | BESCHREIBUNG                                                       |
|:---------------------------------------------------------------------------------------|:------------------------------------------------------------------|
| [**GetMatrix**](id3dx11effectmatrixvariable-getmatrix.md)                             | Eine Matrix erhalten.<br/>                                          |
| [**Getmatrixarray**](id3dx11effectmatrixvariable-getmatrixarray.md)                   | Ein Array von Matrizen erhalten.<br/>                              |
| [**Getmatrixtransform**](id3dx11effectmatrixvariable-getmatrixtranspose.md)           | Eine Gleit Komma Matrix austauschen und erhalten.<br/>             |
| [**Getmatrixtransposearray**](id3dx11effectmatrixvariable-getmatrixtransposearray.md) | Austauschen und erhalten eines Arrays von Gleit Komma Matrizen.<br/> |
| [**SetMatrix**](id3dx11effectmatrixvariable-setmatrix.md)                             | Legen Sie eine Gleit Komma Matrix fest.<br/>                           |
| [**Setmatrixarray**](id3dx11effectmatrixvariable-setmatrixarray.md)                   | Legen Sie ein Array von Gleit Komma Matrizen fest.<br/>               |
| [**Setmatrixtransform**](id3dx11effectmatrixvariable-setmatrixtranspose.md)           | Sie sollten eine Gleit Komma Matrix austauschen und festlegen.<br/>             |
| [**Setmatrixtransposearray**](id3dx11effectmatrixvariable-setmatrixtransposearray.md) | Ein Array von Gleit Komma Matrizen wird aus-und festgelegt.<br/> |



 

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

 

 





