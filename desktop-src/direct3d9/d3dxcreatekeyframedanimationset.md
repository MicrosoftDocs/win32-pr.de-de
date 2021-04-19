---
description: Erstellt eine ID3DXKeyframedAnimationSet Key-Animation für Animations Sätze.
ms.assetid: 7b4fffdc-696c-400c-a0cc-fc755fd25b75
title: D3DXCreateKeyframedAnimationSet-Funktion (D3dx9anim. h)
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
ms.openlocfilehash: 3f3eb45e999d25c776014c3df5824e0468d03ffd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363168"
---
# <a name="d3dxcreatekeyframedanimationset-function"></a>D3DXCreateKeyframedAnimationSet-Funktion

Erstellt eine [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) Key-Animation für Animations Sätze.

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

*PName* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Zeiger auf den Namen des Animations Satzes.

</dd> <dt>

*TicksPerSecond* \[ in\]
</dt> <dd>

Typ: **[ **Double**](../winprog/windows-data-types.md)**

Anzahl der Keyframe-Ticks, die pro Sekunde verstrichen sind.

</dd> <dt>

*Wiedergabe* \[ in\]
</dt> <dd>

Type: **[ **D3DXPLAYBACK- \_ Typ**](./d3dxplayback-type.md)**

Der Typ der Wiedergabe Schleife für Animations Sätze. Siehe [**D3DXPLAYBACK \_ Type**](./d3dxplayback-type.md).

</dd> <dt>

*Numanimationen* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl der Skalierungs Gruppen für Skalierung, Drehung und Übersetzung (SRT).

</dd> <dt>

*Numcallbackkeys* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl von Rückruf Schlüsseln.

</dd> <dt>

*pcallkeys* \[ in\]
</dt> <dd>

Typ: **Konstanten [**LPD3DXKEY \_ Rückruf**](d3dxkey-callback.md) \***

Zeiger auf eine [**D3DXKEY- \_ Rückruf**](d3dxkey-callback.md) Struktur, die Benutzer Rückruf Daten speichert.

</dd> <dt>

*ppanimationset* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXKEYFRAMEDANIMATIONSET**](id3dxkeyframedanimationset.md)\***

Adresse eines Zeigers auf die [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) Key Framed Animation Set-Schnittstelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Animations Funktionen](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
