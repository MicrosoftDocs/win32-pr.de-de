---
title: D3DX11CreateAsyncMemoryLoader-Funktion (D3DX11async.h)
description: Hinweis Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt. Siehe Hinweise. Erstellen Sie ein asynchrones Speicherladeprogramm.
ms.assetid: 0bf1e6a2-a968-4644-a7b4-e847ed4f7450
keywords:
- D3DX11CreateAsyncMemoryLoader-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncMemoryLoader
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c65f1f094337aed5fee6b026896bba98c151576077c4d89ad750486e0fa48cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124875"
---
# <a name="d3dx11createasyncmemoryloader-function"></a>D3DX11CreateAsyncMemoryLoader-Funktion

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store Apps nicht unterstützt. Siehe Hinweise.

 

Erstellen Sie ein asynchrones Speicherladeprogramm.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX11CreateAsyncMemoryLoader(
  _In_  LPCVOID           pData,
  _In_  SIZE_T            cbData,
  _Out_ ID3DX11DataLoader **ppDataLoader
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pData* \[ In\]
</dt> <dd>

Typ: **[ **LPCVOID**](/windows/desktop/WinProg/windows-data-types)**

Zeiger auf die Daten.

</dd> <dt>

*cbData* \[ In\]
</dt> <dd>

Typ: **[ **SIZE \_ T**](/windows/desktop/WinProg/windows-data-types)**

Größe der Daten.

</dd> <dt>

*ppDataLoader* \[ out\]
</dt> <dd>

Typ: **[ **ID3DX11DataLoader**](id3dx11dataloader.md)\*\***

Die Adresse eines Zeigers auf das asynchrone Datenladeprogramm (siehe [**ID3DX11DataLoader-Schnittstelle).**](id3dx11dataloader.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der In [Direct3D 11-Rückgabecodes aufgeführten](d3d11-graphics-reference-returnvalues.md)Werte.

## <a name="remarks"></a>Hinweise

Es gibt keine Implementierung des asynchronen Ladevorgangs außerhalb von D3DX 10 und D3DX 11.

Für Windows Store-Apps enthalten die DirectX-Beispiele (z. B. das [Direct3D-Tutorialbeispiel)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)das **BasicLoader-Modul,** das das asynchrone Programmiermodell Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))) verwendet.

Für Win32-Desktop-Apps können Sie die [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) verwenden, um etwas ähnliches wie das asynchrone Programmiermodell Windows Runtime zu implementieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX11async.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX11.lib</dt> </dl>    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Funktionen](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

