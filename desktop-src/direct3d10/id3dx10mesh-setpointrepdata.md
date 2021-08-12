---
description: Legen Sie die Point Rep-Daten für das Gitternetz fest.
ms.assetid: 451a1ff0-68fa-48c4-b3f1-d41d7583cb3f
title: ID3DX10Mesh::SetPointRepData-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetPointRepData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: af7db99222e124e7a137a308863daa6db0413660b06bdc529e12da53b2b90fab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118302585"
---
# <a name="id3dx10meshsetpointrepdata-method"></a>ID3DX10Mesh::SetPointRepData-Methode

Legen Sie die Point Rep-Daten für das Gitternetz fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetPointRepData(
  [in] const UINT *pPointReps
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pPointReps* \[ In\]
</dt> <dd>

Typ: **const [**UINT**](../winprog/windows-data-types.md) \***

Die zu setzenden Punkt-Rep-Daten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Unter [Direct3D 10-Rückgabecodes aufgeführten Werte.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
