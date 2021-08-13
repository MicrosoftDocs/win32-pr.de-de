---
title: D3DX11CreateThreadPump-Funktion (D3DX11core.h)
description: Hinweis Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt. Siehe Hinweise. Erstellen Sie eine Threadpumpe.
ms.assetid: 8983a2e2-185f-43c0-baf0-a4c883d91220
keywords:
- D3DX11CreateThreadPump-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateThreadPump
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a3a19c338b330604caae9ce5a1e7f7222664b0521f9874c3eff07ff1fc8a4f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118536101"
---
# <a name="d3dx11createthreadpump-function"></a>D3DX11CreateThreadPump-Funktion

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt. Siehe Hinweise.

 

Erstellen Sie eine Threadpumpe.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX11CreateThreadPump(
  _In_  UINT              cIoThreads,
  _In_  UINT              cProcThreads,
  _Out_ ID3DX11ThreadPump **ppThreadPump
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*cIoThreads* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Die Anzahl der zu erstellenden E/A-Threads. Wenn 0 angegeben ist, versucht Direct3D, die optimale Anzahl von Threads basierend auf der Hardwarekonfiguration zu berechnen.

</dd> <dt>

*cProcThreads* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Die Anzahl der zu erstellenden Prozessthreads. Wenn 0 angegeben ist, versucht Direct3D, die optimale Anzahl von Threads basierend auf der Hardwarekonfiguration zu berechnen.

</dd> <dt>

*ppThreadPump* \[ out\]
</dt> <dd>

Typ: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\*\***

Die erstellte Threadpumpe. Siehe [**ID3DX11ThreadPump-Schnittstelle.**](id3dx11threadpump.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der In [Direct3D 11-Rückgabecodes aufgeführten](d3d11-graphics-reference-returnvalues.md)Werte.

## <a name="remarks"></a>Hinweise

Eine Threadpumpe ist ein sehr ressourcenintensives Objekt. Pro Anwendung sollte nur eine Threadpumpe erstellt werden.

Es gibt keine Implementierung des asynchronen Ladevorgangs außerhalb von D3DX 10 und D3DX 11.

Für Windows Store-Apps enthalten die DirectX-Beispiele (z. B. das [Direct3D-Tutorialbeispiel)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)das **BasicLoader-Modul,** das das asynchrone Programmiermodell Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))) verwendet.

Für Win32-Desktop-Apps können Sie die [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) verwenden, um etwas ähnliches wie das asynchrone Programmiermodell Windows Runtime zu implementieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX11core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX11.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[D3DX-Funktionen](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

