---
description: Skaliert alle einem angegebenen submesh zugeordneten Beispiele. Die-Methode ist nützlich für das Berechnen der unter Surface-Struktur.
ms.assetid: abb9ca6a-5fc2-4986-8a38-29998fe5e537
title: 'ID3DXPRTEngine:: scalemeschchunk-Methode (D3DX9Mesh. h)'
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
ms.openlocfilehash: f688a5175e7b50c33dd93d06a4f988a14c062c86
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367480"
---
# <a name="id3dxprtenginescalemeshchunk-method"></a>ID3DXPRTEngine:: scalemeschchunk-Methode

Skaliert alle einem angegebenen submesh zugeordneten Beispiele. Die-Methode ist nützlich für das Berechnen der unter Surface-Struktur.

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

*Umschlag* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Speicherort im Mesh, an dem mit dem Skalieren von Beispielen begonnen wird.

</dd> <dt>

*f-Skala* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Der Wert, um den die einzelnen Vektor im submesh multipliziert werden sollen.

</dd> <dt>

*pdataout* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf ein [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt, um die im submesh übernommenen Beispiele zu erhalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
