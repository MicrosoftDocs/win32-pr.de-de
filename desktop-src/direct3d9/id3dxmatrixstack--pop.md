---
description: Entfernt die aktuelle Matrix vom oberen Rand des Stapels.
ms.assetid: 4c542012-058a-4818-8ec4-27e7d3357ca3
title: ID3DXMATRIXStack::P op-Methode (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Pop
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 229892ab9b6a1ec75396b24cd9313e27667d0acf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050840"
---
# <a name="id3dxmatrixstackpop-method-d3dx9mathh"></a>ID3DXMATRIXStack::P op-Methode (D3dx9math. h)

Entfernt die aktuelle Matrix vom oberen Rand des Stapels.

## <a name="syntax"></a>Syntax


```C++
HRESULT Pop();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.

## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass diese Methode die Anzahl der Elemente im Stapel um 1 verringert, wodurch die aktuelle Matrix aus dem Stapel Rand entfernt und eine Matrix an den Anfang des Stapels herauf gestuft wird. Wenn die aktuelle Anzahl der Elemente auf dem Stapel 0 ist, wird diese Methode zurückgegeben, ohne eine Aktion auszuführen. Wenn die aktuelle Anzahl der Elemente auf dem Stapel 1 ist, wird der Stapel von dieser Methode geleert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack:: GetTop**](id3dxmatrixstack--gettop.md)
</dt> <dt>

[**ID3DXMATRIXStack::P USH**](id3dxmatrixstack--push.md)
</dt> </dl>

 

 




