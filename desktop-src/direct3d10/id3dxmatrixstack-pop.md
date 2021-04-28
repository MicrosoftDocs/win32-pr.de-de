---
description: 'ID3DXMATRIXStack::P op-Methode (D3DX10.h): Entfernt die aktuelle Matrix vom anfang des Stapels.'
ms.assetid: f4e4ff5d-a7a1-4f87-9b7e-53b9d044ba51
title: ID3DXMATRIXStack::P op-Methode (D3DX10.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 19c87cbd5fd81100682225aa16256573c7f95be0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107928"
---
# <a name="id3dxmatrixstackpop-method-d3dx10h"></a>ID3DXMATRIXStack::P op-Methode (D3DX10.h)

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
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXMatrixStack](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




