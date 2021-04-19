---
description: Ändern der zu ändernden Scheitel Punkte
ms.assetid: b0d71f3e-9a2d-469d-808b-2fa768cf14b0
title: 'ID3DX10SkinInfo:: remapvertices-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.RemapVertices
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cc51c912794135b456542bb9a8a779601681f393
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355190"
---
# <a name="id3dx10skininforemapvertices-method"></a>ID3DX10SkinInfo:: remapvertices-Methode

Ändern der zu ändernden Scheitel Punkte

## <a name="syntax"></a>Syntax


```C++
HRESULT RemapVertices(
  [in] UINT NewVertexCount,
  [in] UINT *pVertexRemap
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Newvertexcount* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die neue Anzahl von Vertices.

</dd> <dt>

*pvertexremap* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)\***

Ein Zeiger auf ein Array von Scheitelpunkt Indizes, die die Neuzuordnung beschreiben. Beispiel: "skininfo" enthält einige Scheitel Punkte, z. b. "bone0", "v0", "bone1 to v1" und "bone2" zu "V2" und "Array mit 2, 1, 0" für "pboneremap". Dies bewirkt, dass bone0 v2, bone1 zu v1 und bone2 zu v0 zugeordnet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert lauten: e \_ outo-Memory oder e \_ invalidArg.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx10. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
