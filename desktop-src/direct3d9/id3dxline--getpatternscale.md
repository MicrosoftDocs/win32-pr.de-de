---
description: Ruft den Skalierungswert des Stipplemusters ab.
ms.assetid: cf80ae8c-493d-4f35-b4f9-5981e64cc842
title: ID3DXLine::GetPatternScale-Methode (D3dx9core.h)
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
ms.openlocfilehash: 3799901d071da08ee1bb0de4994ed330fabe2d8fedf3b59ce556105f0a280e3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675142"
---
# <a name="id3dxlinegetpatternscale-method"></a>ID3DXLine::GetPatternScale-Methode

Ruft den Skalierungswert des Stipplemusters ab.

## <a name="syntax"></a>Syntax


```C++
FLOAT GetPatternScale();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Gibt den Wert zurück, der zum Skalieren des Stipple-Pattern verwendet wird. 1.0f ist der Standardwert und stellt keine Skalierung dar. Ein Wert kleiner als 1,0f verkleinert das Muster, und ein Wert größer als 1,0 streckt das Muster.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> <dt>

[**ID3DXLine::SetPatternScale**](id3dxline--setpatternscale.md)
</dt> </dl>

 

 
