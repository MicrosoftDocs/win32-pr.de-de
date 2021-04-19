---
description: Disassemblieren eines Effekts.
ms.assetid: d95d6e97-2e79-4cd2-965e-483aa1a1ddbc
title: D3DXDisassembleEffect-Funktion (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDisassembleEffect
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 945c30319d16264a2b7489d1dc0849a4678cbede
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364365"
---
# <a name="d3dxdisassembleeffect-function"></a>D3DXDisassembleEffect-Funktion

Disassemblieren eines Effekts.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXDisassembleEffect(
  _In_  LPD3DXEFFECT pEffect,
  _In_  BOOL         EnableColorCode,
  _Out_ LPD3DXBUFFER *ppDisassembly
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Peer-ect* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXEFFECT**](id3dxeffect.md)**

Zeiger auf eine [**ID3DXEffect**](id3dxeffect.md) -Schnittstelle, die den Effekt enthält.

</dd> <dt>

*Enablecolorcode* \[ in\]
</dt> <dd>

Typ: **[ **bool**](../winprog/windows-data-types.md)**

Aktivieren Sie die Farbcodierung, um die Disassembly leichter lesbar zu machen.

</dd> <dt>

*ppdisassembly* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Gibt einen Puffer zurück, der den disassemblierten Shader enthält. Siehe [**ID3DXBuffer**](id3dxbuffer.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Effekt Funktionen](dx9-graphics-reference-effects-functions.md)
</dt> </dl>

 

 
