---
description: Sie erhalten Informationen zu einem bereits in den Arbeitsspeicher geladenen Image.
ms.assetid: 6750116a-ad4f-4102-aba9-6ef32c367be4
title: D3DX10GetImageInfoFromMemory-Funktion (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetImageInfoFromMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 677ce6a2ac8e4e165ca0a2bbb64b6254870e4ed8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370429"
---
# <a name="d3dx10getimageinfofrommemory-function"></a>D3DX10GetImageInfoFromMemory-Funktion

Sie erhalten Informationen zu einem bereits in den Arbeitsspeicher geladenen Image.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10GetImageInfoFromMemory(
  _In_  LPCVOID           pSrcData,
  _In_  SIZE_T            SrcDataSize,
  _In_  ID3DX10ThreadPump *pPump,
  _In_  D3DX10_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSrcData* \[ in\]
</dt> <dd>

Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**

Zeiger auf das Bild im Arbeitsspeicher.

</dd> <dt>

*Srcdatasize* \[ in\]
</dt> <dd>

Typ: **[ **Größe \_ T**](../winprog/windows-data-types.md)**

Größe des Bilds im Arbeitsspeicher in Bytes.

</dd> <dt>

*ppump* \[ in\]
</dt> <dd>

Typ: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

Optionales threadpump, das verwendet werden kann, um die Informationen asynchron zu laden. Kann **null** sein. Siehe [**ID3DX10ThreadPump**](id3dx10threadpump.md).

</dd> <dt>

*psrcinfo* \[ in\]
</dt> <dd>

Type: **[ **d3dx10 \_ Image \_ Info**](d3dx10-image-info.md)\***

Informationen zum Image im Arbeitsspeicher.

</dd> <dt>

*phresult* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Ein Zeiger auf den Rückgabewert. Kann **null** sein. Wenn *ppump* nicht **null** ist, muss *phresult* eine gültige Speicheradresse sein, bis die asynchrone Ausführung abgeschlossen ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Tex. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Textur Funktionen in D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
