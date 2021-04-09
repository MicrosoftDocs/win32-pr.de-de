---
description: Schaltet den Modus um, um OpenGL-stillinien zu zeichnen.
ms.assetid: 298bf391-9f2b-4352-b9f8-3bc2ab661eee
title: 'ID3DXLine:: setgllines-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetGLLines
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 131c472ef4a2254880ef560edccb9c0cf1c8774b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870204"
---
# <a name="id3dxlinesetgllines-method"></a>ID3DXLine:: setgllines-Methode

Schaltet den Modus um, um OpenGL-stillinien zu zeichnen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetGLLines(
  [in] BOOL bGLLines
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bgllines* \[ in\]
</dt> <dd>

Typ: **[ **bool**](../winprog/windows-data-types.md)**

Schaltet die Zeilen Zeichnung im OpenGL-Stil um. **True** aktiviert die Zeilen im OpenGL-Stil, und **false** aktiviert Direct3D-Linien.

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

 

 
