---
title: D3DX11CreateAsyncFileLoader-Funktion (D3DX11async.h)
description: Hinweis Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt. Siehe Hinweise. Erstellen Sie ein asynchrones Dateilader.
ms.assetid: ee24ac00-3636-4900-9b8a-27778c9a2152
keywords:
- D3DX11CreateAsyncFileLoader-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncFileLoader
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc5997d31765df1de78ed6323a0176be024a5e26bb2eb81a0556f2abedbf2e5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124865"
---
# <a name="d3dx11createasyncfileloader-function"></a>D3DX11CreateAsyncFileLoader-Funktion

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt. Siehe Hinweise.

 

Erstellen Sie ein asynchrones Dateilader.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX11CreateAsyncFileLoader(
  _In_  LPCTSTR           pFileName,
  _Out_ ID3DX11DataLoader **ppDataLoader
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pFileName* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Der Name der zu ladenden Datei. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR auflösen. Andernfalls wird der Datentyp in LPCSTR auflösen.

</dd> <dt>

*ppDataLoader* \[ out\]
</dt> <dd>

Typ: **[ **ID3DX11DataLoader**](id3dx11dataloader.md)\*\***

Adresse eines Zeigers auf das asynchrone Datenlader (siehe [**ID3DX11DataLoader-Schnittstelle**](id3dx11dataloader.md)).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die unter [Direct3D 11-Rückgabecodes aufgeführt sind.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Hinweise

Es gibt keine Implementierung des asynchronen Ladeers außerhalb von D3DX 10 und D3DX 11.

Für Windows Store-Apps enthalten die DirectX-Beispiele (z. B. das [Direct3D-Tutorialbeispiel)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)das **BasicLoader-Modul,** das das asynchrone Windows Runtime-Programmiermodell ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))) verwendet.

Für Win32-Desktop-Apps können [](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) Sie die Concurrency Runtime verwenden, um etwas zu implementieren, das dem asynchronen Windows Runtime-Modell ähnelt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX11async.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX11.lib</dt> </dl>    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Funktionen](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

