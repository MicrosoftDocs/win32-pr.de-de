---
description: 'ID3DXMATRIXStack::LoadIdentity-Methode (D3DX10.h): Lädt die Identität in der aktuellen Matrix.'
ms.assetid: 324b49c2-3aca-4bbb-90f3-62f3ffb2fa45
title: ID3DXMATRIXStack::LoadIdentity-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.LoadIdentity
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f056a911b19c0ea18f5f728a6ce8c4403dd14587
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107988"
---
# <a name="id3dxmatrixstackloadidentity-method-d3dx10h"></a>ID3DXMATRIXStack::LoadIdentity-Methode (D3DX10.h)

Lädt die Identität in der aktuellen Matrix.

## <a name="syntax"></a>Syntax


```C++
HRESULT LoadIdentity();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="remarks"></a>Bemerkungen

Die Identitätsmatrix ist eine Matrix, in der alle Koeffizienten 0,0 sind, mit Ausnahme der \[ 1,1 \] \[ 2,2 \] \[ 3,3 \] \[ 4,4-Koeffizienten, die auf \] 1,0 festgelegt sind. Die Identitätsmatrix ist besonders, da sie unverändert bleibt, wenn sie auf Scheitelzeichen angewendet wird. Die Identitätsmatrix wird als Ausgangspunkt für Matrizen verwendet, die Scheitelpunktwerte ändern, um Drehungen, Übersetzungen und alle anderen Transformationen zu erstellen, die durch eine 4x4-Matrix dargestellt werden können.

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

 

 




