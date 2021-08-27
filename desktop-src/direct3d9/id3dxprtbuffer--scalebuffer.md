---
description: Multipliziert jeden Wert im Puffer mit einem konstanten Wert.
ms.assetid: 3d7ef530-b83a-4123-a2ed-fff2b21378ee
title: ID3DXPRTBuffer::ScaleBuffer-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ScaleBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e5cba39f6816e301f2d36e21e6f81c7bb1f6bb4792fe4ea8017de5d452faf357
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118801488"
---
# <a name="id3dxprtbufferscalebuffer-method"></a>ID3DXPRTBuffer::ScaleBuffer-Methode

Multipliziert jeden Wert im Puffer mit einem konstanten Wert.

## <a name="syntax"></a>Syntax


```C++
HRESULT ScaleBuffer(
  [in] FLOAT Scale
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Skalieren* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Konstanter Wert, der zum Skalieren des Puffers verwendet wird. Jeder Wert im Puffer wird durch das Produkt dieses Werts und den ursprünglichen Pufferwert ersetzt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn bei der Methode ein Fehler auftritt, wird der folgende Wert zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 
