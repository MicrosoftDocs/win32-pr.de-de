---
description: Dehnt das Stippel Muster entlang der Zeilen Richtung aus.
ms.assetid: 411464db-d721-4252-bff3-bec57252273e
title: 'ID3DXLine:: setpatternscale-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetPatternScale
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 44c040a2e8899784bcea9b93bf0781afb39c2464
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219711"
---
# <a name="id3dxlinesetpatternscale-method"></a>ID3DXLine:: setpatternscale-Methode

Dehnt das Stippel Muster entlang der Zeilen Richtung aus.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetPatternScale(
  [in] FLOAT fPatternScale
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

" *bpatternscale* \[ " in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Skalierungs Wert von Stippel Mustern. 1.0 f ist der Standardwert und stellt keine Skalierung dar. Ein Wert kleiner als 1,0 f verkleinert das Muster, und ein Wert größer als 1,0 dehnt das Muster aus.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> </dl>

 

 
