---
description: 'ID3DXMATRIXStack::P op-Methode (D3dx9math.h): Entfernt die aktuelle Matrix vom anfang des Stapels.'
ms.assetid: 4c542012-058a-4818-8ec4-27e7d3357ca3
title: ID3DXMATRIXStack::P op-Methode (D3dx9math.h)
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
ms.openlocfilehash: c8d9185d10b9ef98a1fc3499f49c2ccc9c17a366
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093502"
---
# <a name="id3dxmatrixstackpop-method-d3dx9mathh"></a>ID3DXMATRIXStack::P op-Methode (D3dx9math.h)

Entfernt die aktuelle Matrix vom anfang des Stapels.

## <a name="syntax"></a>Syntax


```C++
HRESULT Pop();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK.

## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass diese Methode die Anzahl der Elemente im Stapel um 1 dekrementiert, indem die aktuelle Matrix effektiv von der obersten Seite des Stapels entfernt und eine Matrix an den Anfang des Stapels hoch gerechnet wird. Wenn die aktuelle Anzahl von Elementen im Stapel 0 beträgt, gibt diese Methode zurück, ohne eine Aktion ausführen zu müssen. Wenn die aktuelle Anzahl von Elementen im Stapel 1 beträgt, leert diese Methode den Stapel.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack::GetTop**](id3dxmatrixstack--gettop.md)
</dt> <dt>

[**ID3DXMATRIXStack::P ush**](id3dxmatrixstack--push.md)
</dt> </dl>

 

 




