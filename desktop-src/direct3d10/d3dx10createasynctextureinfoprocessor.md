---
description: Erstellen Sie einen Datenprozessor, der mit einem threadpump verwendet werden soll.
ms.assetid: e97b6aca-1839-48ea-8dab-b96a52ec2a68
title: D3DX10CreateAsyncTextureInfoProcessor-Funktion (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncTextureInfoProcessor
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fe56fc217af6ebae9255b4f72d3c3af2f279fa29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353754"
---
# <a name="d3dx10createasynctextureinfoprocessor-function"></a>D3DX10CreateAsyncTextureInfoProcessor-Funktion

Erstellen Sie einen Datenprozessor, der mit einem [**threadpump**](id3dx10threadpump.md)verwendet werden soll.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10CreateAsyncTextureInfoProcessor(
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX10DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ploadinfo* \[ in\]
</dt> <dd>

Type: **[ **d3dx10 \_ Image \_ Load \_ Info**](d3dx10-image-load-info.md)\***

Dies ist optional. Gibt die Merkmale einer Textur an (siehe [**d3dx10 \_ Image \_ Load \_ Info**](d3dx10-image-load-info.md)), wenn der Datenprozessor erstellt wird. Legen Sie diese Einstellung auf **null** fest, um die Merkmale einer Textur beim Laden der Textur zu lesen.

</dd> <dt>

*ppdataprocessor* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***

Adresse eines Zeigers auf einen Puffer, der den erstellten Datenprozessor enthält (siehe [**ID3DX10DataProcessor-Schnittstelle**](id3dx10dataprocessor.md)).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.

## <a name="remarks"></a>Bemerkungen

Diese API erstellt eine Datenprozessor Schnittstelle. [**D3DX10CreateAsyncTextureProcessor**](d3dx10createasynctextureprocessor.md) erstellt die Datenprozessor Schnittstelle und lädt die Textur.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Tex. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Textur Funktionen in D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 




