---
description: Skaliert alle Stichproben, die einem bestimmten Untermesh zugeordnet sind. Die -Methode ist nützlich für das Berechnen von Unteroberflächen-Punktdiagrammen.
ms.assetid: abb9ca6a-5fc2-4986-8a38-29998fe5e537
title: ID3DXPRTEngine::ScaleMeshChunk-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ScaleMeshChunk
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a42046678ef0b44f011c8440cd3456dc9ff236ec0f7a280b4650b49aa53c10d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729584"
---
# <a name="id3dxprtenginescalemeshchunk-method"></a>ID3DXPRTEngine::ScaleMeshChunk-Methode

Skaliert alle Stichproben, die einem bestimmten Untermesh zugeordnet sind. Die -Methode ist nützlich für das Berechnen von Unteroberflächen-Punktdiagrammen.

## <a name="syntax"></a>Syntax


```C++
HRESULT ScaleMeshChunk(
  [in]      UINT            uMeshChunk,
  [in]      FLOAT           fScale,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*uMeshChunk* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Position im Gitternetz, an der mit der Skalierung von Beispielen gestartet werden soll.

</dd> <dt>

*fScale* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Der Wert, mit dem jeder Vektor im Untermesh multipliziert werden soll.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf ein [**ID3DXPRTBuffer-Objekt,**](id3dxprtbuffer.md) um neu skalierte Beispiele im Untermesh zu empfangen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
