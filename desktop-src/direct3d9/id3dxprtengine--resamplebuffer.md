---
description: Gibt einen ID3DXPRTBuffer-Puffer für die Eingabe erneut aus und speichert ihn in einem Ausgabepuffer. Diese Methode kann verwendet werden, um einen Vertex-Puffer in einen Textur Puffer zu konvertieren und umgekehrt. Sie kann auch verwendet werden, um Puffer mit einem Kanal in 3-Kanal-Puffer zu konvertieren und umgekehrt.
ms.assetid: 78015044-38a9-4c08-a690-28f6427dae8c
title: 'ID3DXPRTEngine:: resamplebuffer-Methode (D3DX9Mesh. h)'
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
ms.openlocfilehash: c8517d04be1d63159a2548935f3e09c12e646775
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762291"
---
# <a name="id3dxprtengineresamplebuffer-method"></a>ID3DXPRTEngine:: resamplebuffer-Methode

Gibt einen [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Puffer für die Eingabe erneut aus und speichert ihn in einem Ausgabepuffer. Diese Methode kann verwendet werden, um einen Vertex-Puffer in einen Textur Puffer zu konvertieren und umgekehrt. Sie kann auch verwendet werden, um Puffer mit einem Kanal in 3-Kanal-Puffer zu konvertieren und umgekehrt.

## <a name="syntax"></a>Syntax


```C++
HRESULT ResampleBuffer(
  [in]      LPD3DXPRTBUFFER pBufferIn,
  [in, out] LPD3DXPRTBUFFER pBufferOut
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbufferin* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf den [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Eingabepuffer.

</dd> <dt>

*pbufferout* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf den [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Ausgabepuffer.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 




