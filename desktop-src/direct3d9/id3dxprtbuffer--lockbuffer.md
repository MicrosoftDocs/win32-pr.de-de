---
description: Sperrt einen Bereich von Vertex-oder Texel-Beispiel Daten und erhält einen Zeiger auf die Position im Pufferspeicher.
ms.assetid: 8de2725f-507e-41ee-828d-2fb19cc2252c
title: 'ID3DXPRTBuffer:: LockBuffer-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.LockBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a2da8cb5a6a2e036fb7b495a129a5ef29d9ff749
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350700"
---
# <a name="id3dxprtbufferlockbuffer-method"></a>ID3DXPRTBuffer:: LockBuffer-Methode

Sperrt einen Bereich von Vertex-oder Texel-Beispiel Daten und erhält einen Zeiger auf die Position im Pufferspeicher.

## <a name="syntax"></a>Syntax


```C++
HRESULT LockBuffer(
  [in]  UINT  Start,
  [in]  UINT  NumSamples,
  [out] FLOAT **ppData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Starten* \[ Sie in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Index der Stichprobenentnahme von Vertex-oder textex.

</dd> <dt>

*NumSamples* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl der abtasteten Scheitel Punkte (oder Texels).

</dd> <dt>

*ppData* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)\*\***

Zeiger auf den Speicherort im Arbeitsspeicher, an dem das Start Beispiel beginnt. Das Speicher Layout der Puffer Daten lautet:


```
float fData[NumberSamples][NumberChannels][NumberCoefficients]      
```



</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben:

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> <dt>

[**ID3DXPRTBuffer:: getnumchannels**](id3dxprtbuffer--getnumchannels.md)
</dt> <dt>

[**ID3DXPRTBuffer:: getnumcoeffs**](id3dxprtbuffer--getnumcoeffs.md)
</dt> <dt>

[**ID3DXPRTBuffer:: getnumsamples**](id3dxprtbuffer--getnumsamples.md)
</dt> </dl>

 

 
