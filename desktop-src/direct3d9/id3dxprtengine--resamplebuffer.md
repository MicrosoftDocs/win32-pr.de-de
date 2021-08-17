---
description: Verwendet einen ID3DXPRTBuffer-Eingabepuffer neu und speichert ihn in einem Ausgabepuffer. Diese Methode kann verwendet werden, um einen Scheitelpunktpuffer in einen Texturpuffer zu konvertieren und umgekehrt. Sie kann auch verwendet werden, um Einkanalpuffer in 3-Kanal-Puffer und umgekehrt zu konvertieren.
ms.assetid: 78015044-38a9-4c08-a690-28f6427dae8c
title: ID3DXPRTEngine::ResampleBuffer-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ResampleBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: aa945be7b01c928a5dc8f5e44a6a31e8cb6d879be102145d25e03e7bef73f3b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729614"
---
# <a name="id3dxprtengineresamplebuffer-method"></a>ID3DXPRTEngine::ResampleBuffer-Methode

Verwendet einen [**ID3DXPRTBuffer-Eingabepuffer neu**](id3dxprtbuffer.md) und speichert ihn in einem Ausgabepuffer. Diese Methode kann verwendet werden, um einen Scheitelpunktpuffer in einen Texturpuffer zu konvertieren und umgekehrt. Sie kann auch verwendet werden, um Einkanalpuffer in 3-Kanal-Puffer und umgekehrt zu konvertieren.

## <a name="syntax"></a>Syntax


```C++
HRESULT ResampleBuffer(
  [in]      LPD3DXPRTBUFFER pBufferIn,
  [in, out] LPD3DXPRTBUFFER pBufferOut
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pBufferIn* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf den Eingabepuffer [**ID3DXPRTBuffer.**](id3dxprtbuffer.md)

</dd> <dt>

*pBufferOut* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf den Ausgabepuffer [**ID3DXPRTBuffer.**](id3dxprtbuffer.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 




