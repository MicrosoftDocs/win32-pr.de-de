---
description: Extrahiert den Mittelwert und die Hauptkomponentenanalyse (PCA) für einen bestimmten Cluster aus einem ID3DXPRTCompBuffer-komprimierten Datenpuffer.
ms.assetid: dcb1372f-2c8f-4d18-9840-5982b2ed0d6e
title: 'ID3DXPRTCompBuffer:: extractbasis-Methode (D3DX9Mesh. h)'
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
ms.openlocfilehash: ebedef91c9f3d1e277a099ffd295903e9ba77ba8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357251"
---
# <a name="id3dxprtcompbufferextractbasis-method"></a>ID3DXPRTCompBuffer:: extractbasis-Methode

Extrahiert den Mittelwert und die Hauptkomponentenanalyse (PCA) für einen bestimmten Cluster aus einem [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) -komprimierten Datenpuffer.

## <a name="syntax"></a>Syntax


```C++
HRESULT ExtractBasis(
  [in]      UINT  Cluster,
  [in, out] FLOAT *pClusterBasis
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Cluster* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Cluster, für den die Basis extrahiert wird.

</dd> <dt>

*pclusterbasis* \[ in, out\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)\***

Zeiger auf ein Array von Basis Vektordaten für Cluster. Die Größe der gespeicherten float-Daten beträgt: (1 + Anzahl der PCA-Vektoren pro Cluster) \* (Anzahl der Koeffizienten) \* (Anzahl der farbchannels)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTCompBuffer](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
