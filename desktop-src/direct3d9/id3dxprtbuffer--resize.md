---
description: Ändert die Anzahl der im Puffer enthaltenen Stichproben.
ms.assetid: c3cceba8-0bbc-46e5-95d9-cdf58d8a2510
title: ID3DXPRTBuffer::Resize-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.Resize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5c6da4c5de4b38f5fe86b36622b7032e10ffe1be794ee8990ba19362cfd77d98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117730073"
---
# <a name="id3dxprtbufferresize-method"></a>ID3DXPRTBuffer::Resize-Methode

Ändert die Anzahl der im Puffer enthaltenen Stichproben.

## <a name="syntax"></a>Syntax


```C++
HRESULT Resize(
  [in] UINT NewSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NewSize* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl von Stichproben, die im Puffer enthalten sein sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: E \_ OUTOFMEMORY.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 
