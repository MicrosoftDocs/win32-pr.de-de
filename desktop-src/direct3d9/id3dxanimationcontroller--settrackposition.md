---
description: Legt den Track auf die angegebene lokale Animations Zeit fest.
ms.assetid: 2ce87b06-1196-415f-958c-7bd407d6c69c
title: 'ID3DXAnimationController:: settrackposition-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackPosition
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 95c408a43df3047a52d93da0cca3d9b17053d320
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355042"
---
# <a name="id3dxanimationcontrollersettrackposition-method"></a>ID3DXAnimationController:: settrackposition-Methode

Legt den Track auf die angegebene lokale Animations Zeit fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetTrackPosition(
  [in] UINT   Track,
  [in] DOUBLE Position
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Nach *verfolgen* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Bezeichner nachverfolgen.

</dd> <dt>

*Position* \[ in\]
</dt> <dd>

Typ: **[ **Double**](../winprog/windows-data-types.md)**

Der Wert der lokalen Animations Zeit, der der Spur zugewiesen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
