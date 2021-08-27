---
title: ID3DX11EffectMatrixVariable-Schnittstelle (D3dx11effect.h)
description: Eine Matrixvariablenschnittstelle greifen auf eine Matrix zu.
ms.assetid: 44f30d1a-3ec1-49d7-92c0-475cf2fa4d2a
keywords:
- ID3DX11EffectMatrixVariable-Schnittstelle Direct3D 11
- ID3DX11EffectMatrixVariable-Schnittstelle Direct3D 11 , beschrieben
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
ms.openlocfilehash: e9daff97a1980c7f1e5647c0e436d5e774a7a7b575b3100f1164af8b97010dea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118535086"
---
# <a name="id3dx11effectmatrixvariable-interface"></a>ID3DX11EffectMatrixVariable-Schnittstelle

Eine Matrixvariablenschnittstelle greifen auf eine Matrix zu.

## <a name="members"></a>Member

Die **ID3DX11EffectMatrixVariable-Schnittstelle** erbt von [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectMatrixVariable** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX11EffectMatrixVariable-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                 | Beschreibung                                                       |
|:---------------------------------------------------------------------------------------|:------------------------------------------------------------------|
| [**GetMatrix**](id3dx11effectmatrixvariable-getmatrix.md)                             | Hier erhalten Sie eine Matrix.<br/>                                          |
| [**GetMatrixArray**](id3dx11effectmatrixvariable-getmatrixarray.md)                   | Hier erhalten Sie ein Array von Matrizen.<br/>                              |
| [**GetMatrixTranspose**](id3dx11effectmatrixvariable-getmatrixtranspose.md)           | Transponieren und Erhalten einer Gleitkommamatrix.<br/>             |
| [**GetMatrixTransposeArray**](id3dx11effectmatrixvariable-getmatrixtransposearray.md) | Transponieren und Erhalten eines Arrays von Gleitkommamatrizen.<br/> |
| [**SetMatrix**](id3dx11effectmatrixvariable-setmatrix.md)                             | Legen Sie eine Gleitkommamatrix fest.<br/>                           |
| [**SetMatrixArray**](id3dx11effectmatrixvariable-setmatrixarray.md)                   | Legen Sie ein Array von Gleitkommamatrizen fest.<br/>               |
| [**SetMatrixTranspose**](id3dx11effectmatrixvariable-setmatrixtranspose.md)           | Transponieren und Festlegen einer Gleitkommamatrix.<br/>             |
| [**SetMatrixTransposeArray**](id3dx11effectmatrixvariable-setmatrixtransposearray.md) | Transponieren und Festlegen eines Arrays von Gleitkommamatrizen.<br/> |



 

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

 

 





