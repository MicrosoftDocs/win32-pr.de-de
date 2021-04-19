---
description: Extrahiert die Cluster-IDs pro Beispiel aus einem komprimierten ID3DXPRTCompBuffer-Datenpuffer.
ms.assetid: d78d82ab-58bc-4b73-9ca0-8b7f06867618
title: 'ID3DXPRTCompBuffer:: extractclusterids-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractClusterIDs
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ef68a972109e89e318adb83ab388c653c6a3deed
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364011"
---
# <a name="id3dxprtcompbufferextractclusterids-method"></a>ID3DXPRTCompBuffer:: extractclusterids-Methode

Extrahiert die Cluster-IDs pro Beispiel aus einem komprimierten [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) -Datenpuffer.

## <a name="syntax"></a>Syntax


```C++
HRESULT ExtractClusterIDs(
  [in, out] UINT *pClusterIDs
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pclusterids* \[ in, out\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)\***

Zeiger auf den Speicherort im Arbeitsspeicher, an dem IDs geschrieben werden. Die erforderliche Arbeitsspeicher Länge ist der von [**ID3DXPRTCompBuffer:: getnumsamples**](id3dxprtcompbuffer--getnumsamples.md)zurückgegebene Wert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTCompBuffer](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
