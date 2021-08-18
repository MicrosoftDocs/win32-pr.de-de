---
description: Erstellen Sie eine Shader-Ressourcenansicht aus einer Ressource.
ms.assetid: 207cda5f-5b7e-420a-988f-135cd2a04eb0
title: D3DX10CreateShaderResourceViewFromResource-Funktion (D3DX10Tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateShaderResourceViewFromResource
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f948e31c1218b095bda98c68a92abbb01d381d62c4acfed027be8b81701367e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634620"
---
# <a name="d3dx10createshaderresourceviewfromresource-function"></a>D3DX10CreateShaderResourceViewFromResource-Funktion

Erstellen Sie eine Shader-Ressourcenansicht aus einer Ressource.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10CreateShaderResourceViewFromResource(
  _In_  ID3D10Device             *pDevice,
  _In_  HMODULE                  hSrcModule,
  _In_  LPCTSTR                  pSrcResource,
  _In_  D3DX10_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX10ThreadPump        *pPump,
  _Out_ ID3D10ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDevice* \[ In\]
</dt> <dd>

Typ: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Ein Zeiger auf das Gerät (siehe [**ID3D10Device-Schnittstelle),**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)das die Ressource verwendet.

</dd> <dt>

*hSrcModule* \[ In\]
</dt> <dd>

Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**

Behandeln Sie das Ressourcenmodul, das die Ansicht shader-resource enthält. HMODULE kann mit der [GetModuleHandle-Funktion](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea)abgerufen werden.

</dd> <dt>

*pSrcResource* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Name der Shaderressourcenansicht in hSrcModule. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst. Andernfalls wird der Datentyp in LPCSTR aufgelöst.

</dd> <dt>

*pLoadInfo* \[ In\]
</dt> <dd>

Typ: **[ **D3DX10 \_ IMAGE \_ LOAD \_ INFO**](d3dx10-image-load-info.md)\***

Optional. Identifiziert die Merkmale einer Textur (siehe [**D3DX10 \_ IMAGE \_ LOAD \_ INFO),**](d3dx10-image-load-info.md)wenn der Datenprozessor erstellt wird. Legen Sie diese Eigenschaft auf **NULL** fest, um die Merkmale einer Textur zu lesen, wenn die Textur geladen wird.

</dd> <dt>

*pPump* \[ In\]
</dt> <dd>

Typ: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

Ein Zeiger auf eine Threadpumpschnittstelle (siehe [**ID3DX10ThreadPump-Schnittstelle).**](id3dx10threadpump.md) Wenn **NULL** angegeben wird, verhält sich diese Funktion synchron und wird erst zurückgegeben, wenn sie abgeschlossen ist.

</dd> <dt>

*ppShaderResourceView* \[ out\]
</dt> <dd>

Typ: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***

Adresse eines Zeigers auf die Shader-Ressourcenansicht (siehe [**ID3D10ShaderResourceView-Schnittstelle).**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)

</dd> <dt>

*pHResult* \[ out\]
</dt> <dd>

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Ein Zeiger auf den Rückgabewert. Kann **NULL** sein. Wenn *pPump* nicht **NULL** ist, muss *pHResult* ein gültiger Speicherort sein, bis die asynchrone Ausführung abgeschlossen ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der In [Direct3D 10-Rückgabecodes aufgeführten](d3d10-graphics-reference-returnvalues.md)Werte.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Texturfunktionen in D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[Universell Functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
