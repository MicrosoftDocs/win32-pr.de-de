---
description: Legt einen Albedo-Wert für jeden Gitter Scheitelpunkt fest, wobei vorherige Albedo-Werte überschrieben werden.
ms.assetid: 5220dfe3-8d41-480c-a850-b9aad3d2bb2f
title: 'ID3DXPRTEngine:: setpervertexalbedo-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetPerVertexAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: da7a33a79cc50963e87d0eff15baf22ee8d79ce3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361218"
---
# <a name="id3dxprtenginesetpervertexalbedo-method"></a>ID3DXPRTEngine:: setpervertexalbedo-Methode

Legt einen Albedo-Wert für jeden Gitter Scheitelpunkt fest, wobei vorherige Albedo-Werte überschrieben werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetPerVertexAlbedo(
  [in] const VOID *pDataIn,
  [in]       UINT NumChannels,
  [in]       UINT Stride
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdatain* \[ in\]
</dt> <dd>

Typ: Konstante **void \***

Zeiger auf float Albedo-Daten des ersten Beispiels.

</dd> <dt>

*Numchannels* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl der festzulegenden Farbkanäle. Legen Sie auf 1 fest, um graue Materialien (R = G = B) oder 3 anzugeben, um Farb Blutungen zu aktivieren.

</dd> <dt>

*Stride* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Der Schritt in Bytes, der benötigt wird, um den Albedo-Wert des nächsten Beispiels zu erhalten. Siehe [Breite und Tonhöhe (Direct3D 9)](width-vs--pitch.md).

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

 

 
