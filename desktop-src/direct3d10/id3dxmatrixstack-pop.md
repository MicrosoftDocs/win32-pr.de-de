---
description: Entfernt die aktuelle Matrix vom oberen Rand des Stapels.
ms.assetid: f4e4ff5d-a7a1-4f87-9b7e-53b9d044ba51
title: ID3DXMATRIXStack::P op-Methode (d3dx10. h)
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
ms.openlocfilehash: a9a7b88cc749ef61c8b04395497fcc00ea9b36ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367402"
---
# <a name="id3dxmatrixstackpop-method-d3dx10h"></a>ID3DXMATRIXStack::P op-Methode (d3dx10. h)

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
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx10. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXMatrixStack](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




