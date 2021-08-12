---
description: Extrahiert die PcA-Basisvektoren (Mean and Principal Component Analysis) für einen bestimmten Cluster aus einem komprimierten ID3DXPRTCompBuffer-Datenpuffer.
ms.assetid: dcb1372f-2c8f-4d18-9840-5982b2ed0d6e
title: ID3DXPRTCompBuffer::ExtractBasis-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractBasis
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 288a96a5f56bc04b245eaaf032bbcd946ed227c5b4fcad9e5d5d200dfa9903bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118294033"
---
# <a name="id3dxprtcompbufferextractbasis-method"></a>ID3DXPRTCompBuffer::ExtractBasis-Methode

Extrahiert die PcA-Basisvektoren (Mean and Principal Component Analysis) für einen bestimmten Cluster aus einem komprimierten [**ID3DXPRTCompBuffer-Datenpuffer.**](id3dxprtcompbuffer.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT ExtractBasis(
  [in]      UINT  Cluster,
  [in, out] FLOAT *pClusterBasis
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Cluster* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Cluster, für den die Basis extrahiert wird.

</dd> <dt>

*pClusterBasis* \[ in, out\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Zeiger auf ein Array von Basisvektordaten für Cluster. Die Größe der gespeicherten FLOAT-Daten beträgt: (1 + Anzahl von PCA-Vektoren pro Cluster) (Anzahl der Koeffizienten) \* \* (Anzahl der Farbkanäle)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn bei der Methode ein Fehler auftritt, wird der folgende Wert zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTCompBuffer](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
