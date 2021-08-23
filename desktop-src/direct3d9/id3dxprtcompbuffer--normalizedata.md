---
description: Normalisiert alle Gewichtungen der Hauptkomponentenanalyse (Principal Component Analysis, PCA), sodass sie zwischen -1 und 1 liegen. Basisvektoren werden geändert, um diese Normalisierung widerzuspiegeln.
ms.assetid: f1c87049-a1ec-452e-b556-a2dc95324d5d
title: ID3DXPRTCompBuffer::NormalizeData-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.NormalizeData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 64c704fd22fc3d2b87a792dd5cf12a82f14713fe17dbf7c7086ef0e5b01ac502
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629080"
---
# <a name="id3dxprtcompbuffernormalizedata-method"></a>ID3DXPRTCompBuffer::NormalizeData-Methode

Normalisiert alle Gewichtungen der Hauptkomponentenanalyse (Principal Component Analysis, PCA), sodass sie zwischen -1 und 1 liegen. Basisvektoren werden geändert, um diese Normalisierung widerzuspiegeln.

## <a name="syntax"></a>Syntax


```C++
HRESULT NormalizeData();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTCompBuffer](id3dxprtcompbuffer.md)
</dt> </dl>

 

 




