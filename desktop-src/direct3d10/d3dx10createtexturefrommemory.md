---
description: Erstellen Sie eine Texturressource aus einer Datei im Systemspeicher.
ms.assetid: 63eac44b-0540-457f-96c0-d151fbd44df0
title: D3DX10CreateTextureFromMemory-Funktion (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateTextureFromMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7b64c3c429ef356fa4ab8c206682c3b1711a14fe29ee6b2024b92b8113951062
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753350"
---
# <a name="d3dx10createtexturefrommemory-function"></a>D3DX10CreateTextureFromMemory-Funktion

Erstellen Sie eine Texturressource aus einer Datei im Systemspeicher.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10CreateTextureFromMemory(
  _In_  ID3D10Device           *pDevice,
  _In_  LPCVOID                pSrcData,
  _In_  SIZE_T                 SrcDataSize,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX10ThreadPump      *pPump,
  _Out_ ID3D10Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDevice* \[ In\]
</dt> <dd>

Typ: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Ein Zeiger auf das Gerät (siehe [**ID3D10Device Interface),**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)das die Ressource verwendet.

</dd> <dt>

*pSrcData* \[ In\]
</dt> <dd>

Typ: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Zeiger auf die Ressource im Systemspeicher.

</dd> <dt>

*SrcDataSize* \[ In\]
</dt> <dd>

Typ: **[ **SIZE \_ T**](../winprog/windows-data-types.md)**

Größe der Ressource im Systemspeicher.

</dd> <dt>

*pLoadInfo* \[ In\]
</dt> <dd>

Typ: **[ **D3DX10 \_ IMAGE \_ LOAD \_ INFO**](d3dx10-image-load-info.md)\***

Optional. Identifiziert die Merkmale einer Textur (siehe [**D3DX10 \_ IMAGE \_ LOAD \_ INFO),**](d3dx10-image-load-info.md)wenn der Datenprozessor erstellt wird. Legen Sie diese auf **NULL** fest, um die Merkmale einer Textur zu lesen, wenn die Textur geladen wird.

</dd> <dt>

*pPump* \[ In\]
</dt> <dd>

Typ: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

Ein Zeiger auf eine Threadpumpschnittstelle (siehe [**ID3DX10ThreadPump-Schnittstelle**](id3dx10threadpump.md)). Wenn **NULL** angegeben wird, verhält sich diese Funktion synchron und gibt erst dann zurück, wenn sie abgeschlossen ist.

</dd> <dt>

*ppTexture* \[ out\]
</dt> <dd>

Typ: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***

Adresse eines Zeigers auf die erstellte Ressource. Siehe [**ID3D10Resource-Schnittstelle**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).

</dd> <dt>

*pHResult* \[ out\]
</dt> <dd>

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Ein Zeiger auf den Rückgabewert. Kann NULL **sein.** Wenn *pPump* nicht **NULL ist,** muss *pHResult* ein gültiger Speicherort sein, bis die asynchrone Ausführung abgeschlossen ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Unter [Direct3D 10-Rückgabecodes aufgeführten Werte.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Hinweise

Eine Liste der unterstützten Bildformate finden Sie [**unter D3DX10 \_ IMAGE FILE \_ \_ FORMAT**](d3dx10-image-file-format.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Texturfunktionen in D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[Universell Functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
