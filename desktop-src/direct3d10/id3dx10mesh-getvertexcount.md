---
description: Abrufen der Anzahl von Scheitelpunkten im Gitternetz.
ms.assetid: fea8a3b5-ca10-4066-b2ca-6579829d31b6
title: ID3DX10Mesh::GetVertexCount-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetVertexCount
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 00fd0cd84aedb32e2da567a92ffc421f41394a991872f9216b06a4f28f895183
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119566890"
---
# <a name="id3dx10meshgetvertexcount-method"></a>ID3DX10Mesh::GetVertexCount-Methode

Abrufen der Anzahl von Scheitelpunkten im Gitternetz. Ein Gitternetz kann mehrere Scheitelpunktpuffer enthalten (d. h. ein Scheitelpunktpuffer kann alle Positionsdaten enthalten, ein anderer kann alle Texturkoordinatendaten enthalten usw.), aber jeder Scheitelpunktpuffer enthält die gleiche Anzahl von Elementen.

## <a name="syntax"></a>Syntax


```C++
UINT GetVertexCount();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Die Anzahl der Scheitelpunkte im Netz.

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

 

 
