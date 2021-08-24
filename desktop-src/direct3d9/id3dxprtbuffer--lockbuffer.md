---
description: Sperrt einen Bereich von Scheitelpunkt- oder Texel-Beispieldaten und ruft einen Zeiger auf die Position im Pufferspeicher ab.
ms.assetid: 8de2725f-507e-41ee-828d-2fb19cc2252c
title: ID3DXPRTBuffer::LockBuffer-Methode (D3DX9Mesh.h)
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
ms.openlocfilehash: 5d8e3b6310951a5784af99b913298c20d5556baa10b012926f3b68e44d402dbb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606890"
---
# <a name="id3dxprtbufferlockbuffer-method"></a>ID3DXPRTBuffer::LockBuffer-Methode

Sperrt einen Bereich von Scheitelpunkt- oder Texel-Beispieldaten und ruft einen Zeiger auf die Position im Pufferspeicher ab.

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

*Starten Sie* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Index der Stichprobe von Scheitelpunkt- oder Texeldaten.

</dd> <dt>

*NumSamples* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der Scheitelpunkte (oder Texel), die als Stichprobe entnommen wurden.

</dd> <dt>

*ppData* \[ out\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\*\***

Zeiger auf die Position im Arbeitsspeicher, an der das Startbeispiel beginnt. Das Speicherlayout der Pufferdaten lautet:


```
float fData[NumberSamples][NumberChannels][NumberCoefficients]      
```



</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben:

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> <dt>

[**ID3DXPRTBuffer::GetNumChannels**](id3dxprtbuffer--getnumchannels.md)
</dt> <dt>

[**ID3DXPRTBuffer::GetNumCoeffs**](id3dxprtbuffer--getnumcoeffs.md)
</dt> <dt>

[**ID3DXPRTBuffer::GetNumSamples**](id3dxprtbuffer--getnumsamples.md)
</dt> </dl>

 

 
