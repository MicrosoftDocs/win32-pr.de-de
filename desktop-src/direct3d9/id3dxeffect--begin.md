---
description: Startet ein aktives Verfahren.
ms.assetid: 6598d77b-8b53-4f2d-aa43-adf358ad486d
title: 'ID3DXEffect:: Begin-Methode (D3DX9Effect. h)'
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
ms.openlocfilehash: 1912698fbb6d6ac13f119161c4d05926f05d245b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219547"
---
# <a name="id3dxeffectbegin-method"></a>ID3DXEffect:: Begin-Methode

Startet ein aktives Verfahren.

## <a name="syntax"></a>Syntax


```C++
HRESULT Begin(
  [out] UINT  *pPasses,
  [in]  DWORD Flags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppasses* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)\***

Ein Zeiger auf einen zurückgegebenen Wert, der die Anzahl der zum renderingder aktuellen Technik benötigten Pass-ins angibt.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

DWORD, das bestimmt, ob der durch einen Effekt geänderte Zustand gespeichert und wieder hergestellt wird. Der Standardwert 0 gibt an, dass **ID3DXEffect:: begin** und [**ID3DXEffect:: End**](id3dxeffect--end.md) alle durch den Effekt geänderten Status (einschließlich Pixel-und Vertexshader-Konstanten) speichern und wiederherstellen. Gültige Flags können als [Speicher-und Wiederherstellungs Flags des Effekts](d3dxfx.md)erkannt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.

## <a name="remarks"></a>Bemerkungen

Eine Anwendung legt eine aktive Technik im Effektsystem fest, indem **ID3DXEffect:: begin** aufgerufen wird. Das Effektsystem antwortet, indem er den gesamten Pipeline Status erfasst, der durch die Technik in einem Zustands Block geändert werden kann. Eine Anwendung signalisiert das Ende einer Technik durch Aufrufen von [**ID3DXEffect:: End**](id3dxeffect--end.md), bei der der State-Block verwendet wird, um den ursprünglichen Zustand wiederherzustellen. Folglich übernimmt das Effektsystem das Speichern des Zustands, wenn eine Technik aktiv wird und der Zustand wieder hergestellt wird, wenn eine Technik endet. Wenn Sie diese Speicher-und Wiederherstellungs Funktion deaktivieren möchten, finden Sie weitere Informationen unter [D3DXFX \_ donotsavesamplerstate](d3dxfx.md).

Innerhalb des **ID3DXEffect:: begin** -und [**ID3DXEffect:: End**](id3dxeffect--end.md) -Paars verwendet eine Anwendung [**ID3DXEffect:: beginpass**](id3dxeffect--beginpass.md) , um den aktiven Durchlauf festzulegen, [**ID3DXEffect:: CommitChanges**](id3dxeffect--commitchanges.md) , wenn nach dem Aktivieren des Pass Zustandsänderungen aufgetreten sind, und [**ID3DXEffect:: endpass**](id3dxeffect--endpass.md) , um den aktiven Durchlauf zu beenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 
