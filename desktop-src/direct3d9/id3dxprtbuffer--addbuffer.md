---
description: Fügt der ID3DXPRTBuffer einen weiteren Puffer hinzu und speichert die Ergebnisse in ID3DXPRTBuffer.
ms.assetid: 345412f4-30c5-4c1d-b0ef-6e3e18c4e5ab
title: 'ID3DXPRTBuffer:: addbuffer-Methode (D3DX9Mesh. h)'
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
ms.openlocfilehash: 90b86ad3d5d9fe5aa65db722757bdb34574a1006
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106360244"
---
# <a name="id3dxprtbufferaddbuffer-method"></a>ID3DXPRTBuffer:: addbuffer-Methode

Fügt der [**ID3DXPRTBuffer**](id3dxprtbuffer.md) einen weiteren Puffer hinzu und speichert die Ergebnisse in **ID3DXPRTBuffer**.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddBuffer(
  [in] LPD3DXPRTBUFFER pBuffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbuffer* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Ein Zeiger auf einen Puffer, der Elemente enthält, die den entsprechenden Membern des [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Puffers hinzugefügt werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben.

## <a name="remarks"></a>Bemerkungen

pbuffer und [**ID3DXPRTBuffer**](id3dxprtbuffer.md) müssen über die gleiche Anzahl von Beispielen, Koeffizienten und Farbkanälen verfügen. Andernfalls führt die-Methode zu einem Fehler.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 




