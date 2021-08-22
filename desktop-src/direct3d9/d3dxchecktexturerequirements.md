---
description: Überprüft Texturerstellungsparameter.
ms.assetid: f8e788f3-02a9-4ee7-b74d-9e781a2fb39f
title: D3DXCheckTextureRequirements-Funktion (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckTextureRequirements
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4c7166f981c0351054a2a6c359127a4ce1959b45a6e71c44db9e2546825bc5f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119496100"
---
# <a name="d3dxchecktexturerequirements-function"></a>D3DXCheckTextureRequirements-Funktion

Überprüft Texturerstellungsparameter.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCheckTextureRequirements(
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Inout_ UINT              *pWidth,
  _Inout_ UINT              *pHeight,
  _Inout_ UINT              *pNumMipLevels,
  _In_    DWORD             Usage,
  _Inout_ D3DFORMAT         *pFormat,
  _In_    D3DPOOL           Pool
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDevice* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) die das Gerät darstellt, das der Textur zugeordnet werden soll.

</dd> <dt>

*pWidth* \[ in, out\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Zeiger auf die angeforderte Breite in Pixel oder **NULL.** Gibt die korrigierte Größe zurück.

</dd> <dt>

*pHeight* \[ in, out\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Zeiger auf die angeforderte Höhe in Pixel oder **NULL.** Gibt die korrigierte Größe zurück.

</dd> <dt>

*pNumMipLevels* \[ in, out\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Zeiger auf die Anzahl der angeforderten Mipmapebenen oder **NULL.** Gibt die korrigierte Anzahl von Mipmapebenen zurück.

</dd> <dt>

*Verwendung* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

0 oder [**D3DUSAGE \_ RENDERTARGET**](d3dusage.md). Das Festlegen dieses Flags auf D3DUSAGE RENDERTARGET gibt an, dass die Oberfläche \_ als Renderziel verwendet werden soll. Die Ressource kann dann an den pNewRenderTarget-Parameter der [**SetRenderTarget-Methode übergeben**](/windows/desktop/api) werden. Wenn **D3DUSAGE \_ RENDERTARGET** angegeben ist, sollte die Anwendung überprüfen, ob das Gerät diesen Vorgang unterstützt, indem [**CheckDeviceFormat aufruft.**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)

</dd> <dt>

*pFormat* \[ in, out\]
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)\***

Zeiger auf einen Member des [aufzählten D3DFORMAT-Typs.](d3dformat.md) Gibt das gewünschte Pixelformat oder **NULL an.** Gibt das korrigierte Format zurück.

</dd> <dt>

*Pool* \[ In\]
</dt> <dd>

Typ: **[ **D3DPOOL**](./d3dpool.md)**

Member des [**aufzählten D3DPOOL-Typs,**](./d3dpool.md) der die Speicherklasse beschreibt, in der die Textur platziert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE.

## <a name="remarks"></a>Hinweise

Wenn Parameter für diese Funktion ungültig sind, gibt diese Funktion korrigierte Parameter zurück.

Diese Funktion verwendet die folgende Heuristik, wenn die angeforderten Anforderungen mit verfügbaren Formaten verglichen werden:

-   Wählen Sie kein Format mit weniger Kanälen aus.
-   Vermeiden [Sie FOURCC-](d3dformat.md) und 24-Bit-Formate, sofern dies nicht explizit angefordert wird.
-   Versuchen Sie nicht, neue Kanäle hinzuzufügen.
-   Versuchen Sie nicht, die Anzahl der Bits pro Kanal zu ändern.
-   Vermeiden Sie die Konvertierung zwischen Formattypen. Vermeiden Sie beispielsweise die Konvertierung eines ARGB-Formats in ein Tiefenformat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Texturfunktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
