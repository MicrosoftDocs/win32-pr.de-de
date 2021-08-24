---
description: Startet eine aktive Technik.
ms.assetid: 6598d77b-8b53-4f2d-aa43-adf358ad486d
title: ID3DXEffect::Begin-Methode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.Begin
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 4f4e41830b0bb4507e3969c327c84a85c5336e5f07389fa12e05f3a92f4089a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675460"
---
# <a name="id3dxeffectbegin-method"></a>ID3DXEffect::Begin-Methode

Startet eine aktive Technik.

## <a name="syntax"></a>Syntax


```C++
HRESULT Begin(
  [out] UINT  *pPasses,
  [in]  DWORD Flags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pPasses* \[ out\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Zeiger auf einen zurückgegebenen Wert, der die Anzahl von Durchläufen angibt, die zum Rendern der aktuellen Technik erforderlich sind.

</dd> <dt>

*Flags* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

DWORD, das bestimmt, ob der durch einen Effekt geänderte Zustand gespeichert und wiederhergestellt wird. Der Standardwert 0 gibt an, dass **ID3DXEffect::Begin** und [**ID3DXEffect::End**](id3dxeffect--end.md) alle durch den Effekt geänderten Status (einschließlich Pixel- und Vertex-Shaderkonstten) speichern und wiederherstellen. Gültige Flags finden Sie unter [Effect State Save and Restore Flags](d3dxfx.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert einer der folgenden Sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Hinweise

Eine Anwendung legt eine aktive Technik im Effektsystem fest, indem sie **ID3DXEffect::Begin aufruft.** Das Effektsystem reagiert, indem es den sämtlichen Pipelinezustand erfasst, der durch die Technik in einem Zustandsblock geändert werden kann. Eine Anwendung signalisiert das Ende einer Technik, indem sie [**ID3DXEffect::End**](id3dxeffect--end.md)aufruft, die den Zustandsblock verwendet, um den ursprünglichen Zustand wiederherzustellen. Das Effektsystem kümmert sich daher um das Speichern des Zustands, wenn eine Technik aktiv wird, und stellt den Zustand wieder auf, wenn eine Technik beendet wird. Wenn Sie diese Funktion zum Speichern und Wiederherstellen deaktivieren möchten, lesen Sie [D3DXFX \_ DONOTSAVESAMPLERSTATE](d3dxfx.md).

Innerhalb des Paars **ID3DXEffect::Begin** und [**ID3DXEffect::End**](id3dxeffect--end.md) verwendet eine Anwendung [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) zum Festlegen des aktiven Durchgangs, [**ID3DXEffect::CommitChanges, wenn zustandsänderungen**](id3dxeffect--commitchanges.md) nach der Aktivierung des Durchgangs aufgetreten sind, und [**ID3DXEffect::EndPass,**](id3dxeffect--endpass.md) um den aktiven Pass zu beenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 
