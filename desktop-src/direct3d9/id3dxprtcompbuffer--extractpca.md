---
description: Extrahiert die Pro-Sample-Projektionskoeffizienten für die Prinzipalkomponentenanalyse (Principal Component Analysis, PCA) aus einem komprimierten ID3DXPRTCompBuffer-Datenpuffer.
ms.assetid: 149098c2-35ca-46e9-a13a-94906c95cfd9
title: ID3DXPRTCompBuffer::ExtractPCA-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractPCA
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6b172682883c5e5272ece103879aefbbdfb79193b0576e9be04432b5d48b1bb6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856140"
---
# <a name="id3dxprtcompbufferextractpca-method"></a>ID3DXPRTCompBuffer::ExtractPCA-Methode

Extrahiert die Pro-Sample-Projektionskoeffizienten für die Prinzipalkomponentenanalyse (Principal Component Analysis, PCA) aus einem komprimierten [**ID3DXPRTCompBuffer-Datenpuffer.**](id3dxprtcompbuffer.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT ExtractPCA(
  [in] UINT  StartPCA,
  [in] UINT  NumExtract,
  [in] FLOAT *pPCACoefficients
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*StartPCA* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Startindex für PCA-Projektionskoeffizienten, die aus dem Puffer extrahiert werden sollen.

</dd> <dt>

*NumExtract* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der PCA-Projektionskoeffizienten, die aus dem Puffer extrahiert werden sollen.

</dd> <dt>

*pPCACoefficients* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Zeiger auf den Speicherort, an dem CPCA-Koeffizienten (Cluster Principal Component Analysis) geschrieben werden. Die Größe der geschriebenen Daten ist (Anzahl der Stichproben) \* (Anzahl der PCA-Koeffizienten).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXPRTCompBuffer](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
