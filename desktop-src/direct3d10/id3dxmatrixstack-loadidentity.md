---
description: Lädt die Identität in der aktuellen Matrix.
ms.assetid: 324b49c2-3aca-4bbb-90f3-62f3ffb2fa45
title: 'ID3DXMATRIXStack:: loadidentity-Methode (d3dx10. h)'
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
ms.openlocfilehash: 85a58529be3bfcb4d52ba096bb6134fe08994d77
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373548"
---
# <a name="id3dxmatrixstackloadidentity-method-d3dx10h"></a>ID3DXMATRIXStack:: loadidentity-Methode (d3dx10. h)

Lädt die Identität in der aktuellen Matrix.

## <a name="syntax"></a>Syntax


```C++
HRESULT LoadIdentity();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.

## <a name="remarks"></a>Bemerkungen

Die Identitätsmatrix ist eine Matrix, in der alle Koeffizienten 0,0 sind, mit Ausnahme der \[ 1, 1 \] \[ 2, 2 \] \[ 3, 3 \] \[ 4, 4 Koeffizienten \] , die auf 1,0 festgelegt sind. Die Identitätsmatrix ist ein besonderes, da Sie bei der Anwendung auf Vertices nicht geändert wird. Die Identitätsmatrix dient als Ausgangspunkt für Matrizen, die Scheitelpunkt Werte ändern, um Drehungen, Übersetzungen und andere Transformationen zu erstellen, die durch eine 4 x 4-Matrix dargestellt werden können.

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

 

 




