---
description: Fügt dem ID3DXPRTBuffer einen weiteren Puffer hinzu und speichert die Ergebnisse in ID3DXPRTBuffer.
ms.assetid: 345412f4-30c5-4c1d-b0ef-6e3e18c4e5ab
title: ID3DXPRTBuffer::AddBuffer-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.AddBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ffbaffbb47d91b18a6fad9bdee98012fa11fb923a7c7586acf7d7b0cd181bcc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118294113"
---
# <a name="id3dxprtbufferaddbuffer-method"></a>ID3DXPRTBuffer::AddBuffer-Methode

Fügt dem [**ID3DXPRTBuffer**](id3dxprtbuffer.md) einen weiteren Puffer hinzu und speichert die Ergebnisse in **ID3DXPRTBuffer.**

## <a name="syntax"></a>Syntax


```C++
HRESULT AddBuffer(
  [in] LPD3DXPRTBUFFER pBuffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pBuffer* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf einen Puffer, der Member enthält, die den entsprechenden Membern des [**ID3DXPRTBuffer-Puffers**](id3dxprtbuffer.md) hinzugefügt werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben.

## <a name="remarks"></a>Hinweise

pBuffer und [**ID3DXPRTBuffer**](id3dxprtbuffer.md) müssen die gleiche Anzahl von Stichproben, Koeffizienten und Farbkanälen aufweisen. andernfalls schlägt die -Methode fehl.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 




