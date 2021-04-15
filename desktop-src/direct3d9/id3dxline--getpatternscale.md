---
description: Ruft den Skalierungs Wert Stippel-Pattern ab.
ms.assetid: cf80ae8c-493d-4f35-b4f9-5981e64cc842
title: 'ID3DXLine:: getpatternscale-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.GetPatternScale
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 14a9919ede81eb64b844e1882725e37359ad6738
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394262"
---
# <a name="id3dxlinegetpatternscale-method"></a>ID3DXLine:: getpatternscale-Methode

Ruft den Skalierungs Wert Stippel-Pattern ab.

## <a name="syntax"></a>Syntax


```C++
FLOAT GetPatternScale();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **float**](../winprog/windows-data-types.md)**

Gibt den Wert zurück, mit dem das Stippel Muster skaliert wird. 1.0 f ist der Standardwert und stellt keine Skalierung dar. Ein Wert kleiner als 1,0 f verkleinert das Muster, und ein Wert größer als 1,0 dehnt das Muster aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> <dt>

[**ID3DXLine:: setpatternscale**](id3dxline--setpatternscale.md)
</dt> </dl>

 

 
