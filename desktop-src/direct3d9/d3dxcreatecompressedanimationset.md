---
description: Erstellt eine ID3DXCompressedAnimationSet-Schnittstelle für keyframed-Animationssets, die Keyframedaten in einem komprimierten Format speichert.
ms.assetid: c3f97d35-5654-4d85-a337-d77819ce3874
title: D3DXCreateCompressedAnimationSet-Funktion (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCompressedAnimationSet
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2acca9d1b697bb9b06b47aa75948ca74ec00cc7ecb919334c01cf874293cb495
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118299285"
---
# <a name="d3dxcreatecompressedanimationset-function"></a>D3DXCreateCompressedAnimationSet-Funktion

Erstellt eine [**ID3DXCompressedAnimationSet-Keyframed-Animationssatzschnittstelle,**](id3dxcompressedanimationset.md) die Keyframedaten in einem komprimierten Format speichert.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateCompressedAnimationSet(
  _In_        LPCSTR                       pName,
  _In_        DOUBLE                       TicksPerSecond,
  _In_        D3DXPLAYBACK_TYPE            Playback,
  _In_        LPD3DXBUFFER                 pCompressedData,
  _In_        UINT                         NumCallbackKeys,
  _In_  const LPD3DXKEY_CALLBACK           *pCallKeys,
  _Out_       LPD3DXCOMPRESSEDANIMATIONSET *ppAnimationSet
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Zeiger auf den Namen des Animationssets.

</dd> <dt>

*TicksPerSecond* \[ In\]
</dt> <dd>

Typ: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Anzahl der Keyframe-Ticks, die pro Sekunde verstreichen.

</dd> <dt>

*Wiedergabe* \[ In\]
</dt> <dd>

Typ: **[ **D3DXPLAYBACK-TYP \_**](./d3dxplayback-type.md)**

Typ der Wiedergabeschleife des Animationssets. Siehe [**D3DXPLAYBACK \_ TYPE**](./d3dxplayback-type.md).

</dd> <dt>

*pCompressedData* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)**

Zeiger auf den [**ID3DXBuffer-Puffer,**](id3dxbuffer.md) der den Animationssatz als komprimierte Daten speichert.

</dd> <dt>

*NumCallbackKeys* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl von Rückrufschlüsseln.

</dd> <dt>

*pCallKeys* \[ In\]
</dt> <dd>

Typ: **const [**LPD3DXKEY \_ CALLBACK**](d3dxkey-callback.md) \***

Zeiger auf eine [**D3DXKEY \_ CALLBACK-Struktur,**](d3dxkey-callback.md) in der Benutzerrückrufdaten gespeichert werden.

</dd> <dt>

*ppAnimationSet* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXCOMJSDANIMATIONSET**](id3dxcompressedanimationset.md)\***

Adresse eines Zeigers auf die [**ID3DXCompressedAnimationSet-Schnittstelle,**](id3dxcompressedanimationset.md) die Schlüsselframed-Animationssatzdaten in einem komprimierten Format speichert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Animationsfunktionen](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
