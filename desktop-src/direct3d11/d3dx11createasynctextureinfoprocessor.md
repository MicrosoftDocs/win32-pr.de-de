---
title: D3DX11CreateAsyncTextureInfoProcessor-Funktion (D3DX11tex.h)
description: Hinweis Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt. Siehe Hinweise. Erstellen Sie einen Datenprozessor, der mit einer Threadpumpe verwendet werden soll. | D3DX11CreateAsyncTextureInfoProcessor-Funktion (D3DX11tex.h)
ms.assetid: 87de73a5-21f7-4abd-b83a-65c6761681c3
keywords:
- D3DX11CreateAsyncTextureInfoProcessor-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncTextureInfoProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da992c258fe79bd1ed81274495e884339f40aed337fcf11665ec27110afaf422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118536259"
---
# <a name="d3dx11createasynctextureinfoprocessor-function"></a>D3DX11CreateAsyncTextureInfoProcessor-Funktion

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store Apps nicht unterstützt. Siehe Hinweise.

 

Erstellen Sie einen Datenprozessor, der mit einer [**Threadpumpe**](id3dx11threadpump.md)verwendet werden soll.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX11CreateAsyncTextureInfoProcessor(
  _In_  D3DX11_IMAGE_INFO    *pImageInfo,
  _Out_ ID3DX11DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pImageInfo* \[ In\]
</dt> <dd>

Typ: **[ **D3DX11 \_ IMAGE \_ INFO**](d3dx11-image-info.md)\***

Optional. Identifiziert die Merkmale einer Textur (siehe [**D3DX11 \_ IMAGE \_ INFO),**](d3dx11-image-info.md)wenn der Datenprozessor erstellt wird. Legen Sie diese Eigenschaft auf **NULL** fest, um die Merkmale einer Textur zu lesen, wenn die Textur geladen wird.

</dd> <dt>

*ppDataProcessor* \[ out\]
</dt> <dd>

Typ: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***

Adresse eines Zeigers auf einen Puffer, der den erstellten Datenprozessor enthält (siehe [**ID3DX11DataProcessor-Schnittstelle).**](id3dx11dataprocessor.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der In [Direct3D 11-Rückgabecodes aufgeführten](d3d11-graphics-reference-returnvalues.md)Werte.

## <a name="remarks"></a>Hinweise

Diese API erstellt eine Datenprozessorschnittstelle. [**D3DX11CreateAsyncTextureProcessor**](d3dx11createasynctextureprocessor.md) erstellt die Datenprozessorschnittstelle und lädt die Textur.

Es gibt keine Implementierung des asynchronen Ladevorgangs außerhalb von D3DX 10 und D3DX 11.

Für Windows Store-Apps enthalten die DirectX-Beispiele (z. B. das [Direct3D-Tutorialbeispiel)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)das **BasicLoader-Modul,** das das asynchrone Programmiermodell Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))) verwendet.

Für Win32-Desktop-Apps können Sie die [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) verwenden, um etwas ähnliches wie das asynchrone Programmiermodell Windows Runtime zu implementieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX11tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX11.lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Funktionen](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

