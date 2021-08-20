---
description: 'ID3DXMATRIXStack::LoadIdentity-Methode (D3DX10.h): Lädt die Identität in die aktuelle Matrix.'
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
ms.openlocfilehash: 26d52ca8bd8ebccf04a3f2e4f36e35a1ac4e5b2b74d8c0e0a79bd9b85568cfc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736059"
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

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="remarks"></a>Hinweise

Die Identitätsmatrix ist eine Matrix, in der alle Koeffizienten 0,0 sind, mit Ausnahme der \[ Koeffizienten 1,1 \] \[ 2,2 \] \[ 3,3 \] \[ 4,4, \] die auf 1,0 festgelegt sind. Die Identitätsmatrix ist besonders, da sie unverändert bleibt, wenn sie auf Scheitelpunkte angewendet wird. Die Identitätsmatrix wird als Ausgangspunkt für Matrizen verwendet, die Scheitelpunktwerte ändern, um Drehungen, Übersetzungen und andere Transformationen zu erstellen, die durch eine 4x4-Matrix dargestellt werden können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXMatrixStack](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




