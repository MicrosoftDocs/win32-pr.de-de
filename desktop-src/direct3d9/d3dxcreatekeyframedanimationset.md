---
description: Erstellt eine ID3DXKeyframedAnimationSet-Schnittstelle für keyframed animation set.
ms.assetid: 7b4fffdc-696c-400c-a0cc-fc755fd25b75
title: D3DXCreateKeyframedAnimationSet-Funktion (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateKeyframedAnimationSet
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c4fbfb31b712e1521930fa468bae315a443105f3a6bc0863fe3267f9586f874a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118804566"
---
# <a name="d3dxcreatekeyframedanimationset-function"></a>D3DXCreateKeyframedAnimationSet-Funktion

Erstellt eine [**ID3DXKeyframedAnimationSet-Schnittstelle**](id3dxkeyframedanimationset.md) für keyframed animation set.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateKeyframedAnimationSet(
  _In_        LPCSTR                      pName,
  _In_        DOUBLE                      TicksPerSecond,
  _In_        D3DXPLAYBACK_TYPE           Playback,
  _In_        UINT                        NumAnimations,
  _In_        UINT                        NumCallbackKeys,
  _In_  const LPD3DXKEY_CALLBACK          *pCallKeys,
  _Out_       LPD3DXKEYFRAMEDANIMATIONSET *ppAnimationSet
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

*NumAnimations* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl von Skalierungs-, Dreh- und Übersetzungsanimationsätzen (SRT).

</dd> <dt>

*NumCallbackKeys* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl von Rückrufschlüsseln.

</dd> <dt>

*pCallKeys* \[ In\]
</dt> <dd>

Typ: **const [**LPD3DXKEY \_ CALLBACK**](d3dxkey-callback.md) \***

Zeiger auf eine [**D3DXKEY \_ CALLBACK-Struktur,**](d3dxkey-callback.md) die Benutzerrückrufdaten speichert.

</dd> <dt>

*ppAnimationSet* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXKEYFRAMEDANIMATIONSET**](id3dxkeyframedanimationset.md)\***

Adresse eines Zeigers auf die [**Schnittstelle id3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) key framed animation set.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Animationsfunktionen](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
