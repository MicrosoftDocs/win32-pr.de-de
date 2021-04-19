---
description: 'Entfernt Mesh-Daten von dem Gerät, für das ein Commit an das Gerät ausgeführt wurde (mit ID3DX10Mesh:: commitcomdevice).'
ms.assetid: 60eee1f8-f04b-4f33-8f86-0564d0334f97
title: ID3DX10Mesh::D iscard-Methode (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.Discard
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f861de8eefff603954e896a1b6684afc8806764f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367372"
---
# <a name="id3dx10meshdiscard-method"></a>ID3DX10Mesh::D iscard-Methode

Entfernt Mesh-Daten von dem Gerät, für das ein Commit an das Gerät ausgeführt wurde (mit [**ID3DX10Mesh:: commitcomdevice**](id3dx10mesh-committodevice.md)).

## <a name="syntax"></a>Syntax


```C++
HRESULT Discard(
  [in] D3DX10_MESH_DISCARD_FLAGS dwDiscard
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwdiscard* \[ in\]
</dt> <dd>

Type: **[ **d3dx10 \_ Mesh- \_ Verwerfungs \_ Flags**](d3dx10-mesh-discard-flags.md)**

Gibt an, welche Teile von Mesh-Daten vom Gerät verworfen werden sollen. Siehe [**d3dx10 \_ Mesh- \_ Verwerfungs \_ Flags**](d3dx10-mesh-discard-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx10. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




