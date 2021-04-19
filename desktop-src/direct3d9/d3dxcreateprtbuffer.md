---
description: Erstellt einen PRT-Puffer (preberechneten Radiance Transfer), der von einem Simulator komprimiert oder ausgefüllt werden kann. Diese Funktion sollte verwendet werden, um Puffer-oder volumepuffer zu erstellen.
ms.assetid: f79a3691-ab5f-4404-aafd-f9635ff88e71
title: D3DXCreatePRTBuffer-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTBuffer
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8107edfec436d9eda35324f6934b3f70df6a05d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350689"
---
# <a name="d3dxcreateprtbuffer-function"></a>D3DXCreatePRTBuffer-Funktion

Erstellt einen PRT-Puffer (preberechneten Radiance Transfer), der von einem Simulator komprimiert oder ausgefüllt werden kann. Diese Funktion sollte verwendet werden, um Puffer-oder volumepuffer zu erstellen.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreatePRTBuffer(
  _In_    UINT            NumSamples,
  _In_    UINT            NumCoeffs,
  _In_    UINT            NumChannels,
  _Inout_ LPD3DXPRTBUFFER *ppBuffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NumSamples* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl der abtasteten Scheitel Punkte (oder Texels).

</dd> <dt>

*Numkoeffs* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl der Koeffizienten pro Stichproben Speicherort. Bei Verwendung von "sphärischen harmonisch (SH) PRT" sollte die Anzahl der Koeffizienten "Order ²" lauten, wobei "Order" die Reihenfolge der SH-Auswertung ist. Die Reihenfolge muss im Bereich von [D3DXSH \_ minorder](other-d3dx-constants.md) bis D3DXSH \_ maxorder (einschließlich) liegen. Der Bewertungs Grad ist Order-1.

</dd> <dt>

*Numchannels* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl von Farbkanälen, die im Mesh festgelegt werden sollen. Legen Sie auf 1 fest, um graue Materialien (R = G = B) oder 3 anzugeben, um Farb Blutungen zu aktivieren.

</dd> <dt>

*ppbuffer* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***

Adresse eines Zeigers auf das erstellte [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert eines der folgenden Werte sein: D3DERR \_ invalidcall, E \_ oudefmemory.

## <a name="remarks"></a>Bemerkungen

Beim Erstellen des Puffers werden alle Werte mit 0 (null) initialisiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Voraus berechnete Strahlungs Übertragungsfunktionen](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md)
</dt> </dl>

 

 
