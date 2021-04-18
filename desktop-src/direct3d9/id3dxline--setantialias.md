---
description: Schaltet das Zeilen-Antialiasing um.
ms.assetid: 9c212823-2dc6-40dd-b1aa-9fc4a2c540f4
title: 'ID3DXLine:: setantialias-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetAntialias
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 893e2061beedb6d45dc86e87903613984e3d1785
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365138"
---
# <a name="id3dxlinesetantialias-method"></a>ID3DXLine:: setantialias-Methode

Schaltet das Zeilen-Antialiasing um.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetAntialias(
  [in] BOOL bAntiAlias
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bantialias* \[ in\]
</dt> <dd>

Typ: **[ **bool**](../winprog/windows-data-types.md)**

Schaltet das Antialiasing ein und aus. **True** schaltet das Antialiasing ein, und **false** deaktiviert das Antialiasing.

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
</dt> <dt>

[**ID3DXLine:: getAntialias**](id3dxline--getantialias.md)
</dt> </dl>

 

 
