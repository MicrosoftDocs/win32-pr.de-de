---
description: 'ID3DXMATRIXStack::LoadIdentity-Methode (D3dx9math.h): Lädt die Identität in der aktuellen Matrix.'
ms.assetid: e314a51f-4016-4819-a95d-d91864a54b2e
title: ID3DXMATRIXStack::LoadIdentity-Methode (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 046267b11f1a2aa977eda7f5fe461e5c44a2cf59e1f50ae291cf714f063088c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847740"
---
# <a name="id3dxmatrixstackloadidentity-method-d3dx9mathh"></a>ID3DXMATRIXStack::LoadIdentity-Methode (D3dx9math.h)

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

## <a name="remarks"></a>Hinweise

Die Identitätsmatrix ist eine Matrix, in der alle Koeffizienten 0,0 sind, mit Ausnahme der \[ 1,1 \] \[ 2,2 \] \[ 3,3 \] \[ 4,4 Koeffizienten, die auf \] 1,0 festgelegt sind. Die Identitätsmatrix ist besonders, da sie unverändert bleibt, wenn sie auf Scheitelzeichen angewendet wird. Die Identitätsmatrix wird als Ausgangspunkt für Matrizen verwendet, die Scheitelpunktwerte ändern, um Drehungen, Übersetzungen und alle anderen Transformationen zu erstellen, die durch eine 4x4-Matrix dargestellt werden können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack::LoadMatrix**](id3dxmatrixstack--loadmatrix.md)
</dt> </dl>

 

 




