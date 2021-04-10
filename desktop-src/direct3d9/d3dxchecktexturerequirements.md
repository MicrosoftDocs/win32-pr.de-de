---
description: Überprüft die Parameter für die Textur Erstellung.
ms.assetid: f8e788f3-02a9-4ee7-b74d-9e781a2fb39f
title: D3DXCheckTextureRequirements-Funktion (D3dx9tex. h)
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
ms.openlocfilehash: d4fdc0998bfda2144e900c099919bc75c01e8ee3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219558"
---
# <a name="d3dxchecktexturerequirements-function"></a>D3DXCheckTextureRequirements-Funktion

Überprüft die Parameter für die Textur Erstellung.

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

*pdevice* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der Textur zugeordnet werden soll.

</dd> <dt>

*pWidth* \[ in, out\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)\***

Ein Zeiger auf die angeforderte Breite in Pixel oder **null**. Gibt die korrigierte Größe zurück.

</dd> <dt>

*pHeight* \[ in, out\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)\***

Ein Zeiger auf die angeforderte Höhe in Pixel oder **null**. Gibt die korrigierte Größe zurück.

</dd> <dt>

*pnummiplevels* \[ in, out\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)\***

Ein Zeiger auf die Anzahl der angeforderten MipMap-Ebenen oder **null**. Gibt die korrigierte Anzahl von MipMap-Ebenen zurück.

</dd> <dt>

*Verwendung* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

0 oder [**D3DUSAGE \_ renderTarget**](d3dusage.md). Wenn dieses Flag auf D3DUSAGE \_ renderTarget festgelegt wird, wird angegeben, dass die Oberfläche als Renderziel verwendet werden soll. Die Ressource kann dann an den pnewrendertarget-Parameter der Methode "Setup [**target**](/windows/desktop/api) " übergeben werden. Wenn **D3DUSAGE \_ renderTarget** angegeben ist, muss die Anwendung überprüfen, ob das Gerät diesen Vorgang durch Aufrufen von [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)unterstützt.

</dd> <dt>

*pformat* \[ in, out\]
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)\***

Zeiger auf einen Member des [D3DFORMAT](d3dformat.md) -enumerierten Typs. Gibt das gewünschte Pixel Format oder **null** an. Gibt das korrigierte Format zurück.

</dd> <dt>

*Pool* \[ in\]
</dt> <dd>

Typ: **[ **D3DPOOL**](./d3dpool.md)**

Member des [**D3DPOOL**](./d3dpool.md) -Enumerationstyps, der die Speicher Klasse beschreibt, in der die Textur platziert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcallable, D3DERR \_ NotAvailable.

## <a name="remarks"></a>Bemerkungen

Wenn die Parameter dieser Funktion ungültig sind, gibt diese Funktion korrigierte Parameter zurück.

Diese Funktion verwendet die folgende Heuristik, wenn die angeforderten Anforderungen mit den verfügbaren Formaten verglichen werden:

-   Wählen Sie kein Format aus, das über weniger Kanäle verfügt.
-   Vermeiden Sie [FourCC](d3dformat.md) -und 24-Bit-Formate, sofern diese nicht explizit angefordert werden
-   Versuchen Sie nicht, neue Kanäle hinzuzufügen.
-   Versuchen Sie nicht, die Anzahl von Bits pro Kanal zu ändern.
-   Versuchen Sie, die Typformatierung zwischen Typen von Formaten zu vermeiden. Vermeiden Sie beispielsweise die Typumwandlung eines ARGB-Formats in ein tiefen Format.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Textur Funktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
