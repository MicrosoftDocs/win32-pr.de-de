---
description: 'Beendet die Lebensdauer des ppData-Zeigers, der von ID3DXPRTBuffer:: LockBuffer zurückgegeben wurde.'
ms.assetid: 25464566-8a93-48a4-93fa-17828861f98c
title: 'ID3DXPRTBuffer:: UnlockBuffer-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.UnlockBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9a17d8f186fc1baf62dda3652372c4e73a5de141
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219592"
---
# <a name="id3dxprtbufferunlockbuffer-method"></a>ID3DXPRTBuffer:: UnlockBuffer-Methode

Beendet die Lebensdauer des ppData-Zeigers, der von [**ID3DXPRTBuffer:: LockBuffer**](id3dxprtbuffer--lockbuffer.md)zurückgegeben wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT UnlockBuffer();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 




