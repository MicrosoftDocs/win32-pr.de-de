---
description: Erstellen Sie einen Datenprozessor, der eine Ressource lädt, und erstellen Sie dann eine Shader-Ressourcen Ansicht dafür. Datenprozessoren sind eine Komponente der Funktion zum asynchronen Laden von Daten in d3dx10, die Thread-Pumpen verwendet.
ms.assetid: 6e5a6138-c218-4200-a24e-d906d34933b8
title: D3DX10CreateAsyncShaderResourceViewProcessor-Funktion (D3DX10Async. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncShaderResourceViewProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: bd55e4191382c5abde52ce05d0a16b5533d79eac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353755"
---
# <a name="d3dx10createasyncshaderresourceviewprocessor-function"></a>D3DX10CreateAsyncShaderResourceViewProcessor-Funktion

Erstellen Sie einen Datenprozessor, der eine Ressource lädt, und erstellen Sie dann eine Shader-Ressourcen Ansicht dafür. Datenprozessoren sind eine Komponente der Funktion zum asynchronen Laden von Daten in d3dx10, die [**Thread-Pumpen**](id3dx10threadpump.md)verwendet.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10CreateAsyncShaderResourceViewProcessor(
  _In_  ID3D10Device           *pDevice,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX10DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdevice* \[ in\]
</dt> <dd>

Typ: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Zeiger auf das Direct3D-Gerät (siehe [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)), das verwendet wird, um eine Ressource und eine Shader-Ressourcen Ansicht für diese Ressource zu erstellen.

</dd> <dt>

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

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Async. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Universell Funktionen](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 




