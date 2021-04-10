---
description: Optimiert das patchemesh für effizientes Mosaik.
ms.assetid: 0049e649-5fe5-45b4-9b09-14b7f99b4988
title: 'ID3DXPatchMesh:: optimiert-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.Optimize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6fa66aadd0ef1f9f9f65747694fc311f80172449
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961766"
---
# <a name="id3dxpatchmeshoptimize-method"></a>ID3DXPatchMesh:: optimiert-Methode

Optimiert das patchemesh für effizientes Mosaik.

## <a name="syntax"></a>Syntax


```C++
HRESULT Optimize(
  [in] DWORD Flags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Derzeit nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ cannotattrsort.

## <a name="remarks"></a>Bemerkungen

Nachdem eine Anwendung Informationen zu einem Mesh generiert hat, können die Mesh-Daten optimiert (neu angeordnet) werden, um die Leistung zu verbessern. Diese Methode bestimmt, welche Patches nebeneinander liegen (innerhalb der bereitgestellten Toleranz).

Informationen zur Informations Optimierung werden auch verwendet, um den Mosaik Prozess zu optimieren. Generieren Sie Informationen zu den Informationen einmal, und wiederholen Sie den Prozess durch Aufrufen von [**ID3DXPatchMesh::**](id3dxpatchmesh--tessellate.md)Mosaik. Die ausgeführte Optimierung ist unabhängig von der tatsächlich verwendeten Mosaik Ebene. Wenn die Gitter Scheitel Punkte geändert werden, müssen Sie jedoch die Informationen zur Informationsquellen Generierung erneut generieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> <dt>

[**ID3DXPatchMesh:: generateency**](id3dxpatchmesh--generateadjacency.md)
</dt> </dl>

 

 
