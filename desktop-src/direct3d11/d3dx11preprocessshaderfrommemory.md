---
title: D3DX11PreprocessShaderFromMemory-Funktion (D3DX11async.h)
description: Hinweis Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store Apps nicht unterstützt. Hinweis Anstatt diese Funktion zu verwenden, wird empfohlen, die D3DPreprocess-API zu verwenden. Erstellen Sie einen Shader aus dem Arbeitsspeicher, ohne ihn zu kompilieren.
ms.assetid: 3c646914-9334-44fe-a8a0-b84d0dc1a16e
keywords:
- D3DX11PreprocessShaderFromMemory-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11PreprocessShaderFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fb626bb01f36ebc93a69c551f038ba82f07a0bd0c07f71093588f6de3cf31f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118535985"
---
# <a name="d3dx11preprocessshaderfrommemory-function"></a>D3DX11PreprocessShaderFromMemory-Funktion

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store Apps nicht unterstützt.

 

> [!Note]  
> Anstatt diese Funktion zu verwenden, wird empfohlen, die [**D3DPreprocess-API**](/windows/desktop/direct3dhlsl/d3dpreprocess) zu verwenden.

 

Erstellen Sie einen Shader aus dem Arbeitsspeicher, ohne ihn zu kompilieren.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX11PreprocessShaderFromMemory(
  _In_        LPCSTR             pSrcData,
  _In_        SIZE_T             SrcDataSize,
  _In_        LPCSTR             pFileName,
  _In_  const D3D11_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX11ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSrcData* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Zeiger auf den Arbeitsspeicher, der den Shader enthält.

</dd> <dt>

*SrcDataSize* \[ In\]
</dt> <dd>

Typ: **[ **SIZE \_ T**](/windows/desktop/WinProg/windows-data-types)**

Größe des Shaders.

</dd> <dt>

*pFileName* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Name des Shaders.

</dd> <dt>

*pDefine* \[ In\]
</dt> <dd>

Typ: **const D3D11 \_ SHADER \_ MACRO \***

Ein NULL-endendes Array von Shadermakros; Legen Sie diesen Wert auf **NULL** fest, um keine Makros anzugeben.

</dd> <dt>

*pInclude* \[ In\]
</dt> <dd>

Typ: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

Ein Zeiger auf eine Includeschnittstelle; Legen Sie diesen Wert auf **NULL** fest, um anzugeben, dass keine Includedatei vorhanden ist.

</dd> <dt>

*pPump* \[ In\]
</dt> <dd>

Typ: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***

Ein Zeiger auf eine Threadpumpschnittstelle (siehe [**ID3DX11ThreadPump-Schnittstelle).**](id3dx11threadpump.md) Geben Sie mit **NULL** an, dass diese Funktion erst zurückgegeben werden soll, wenn sie abgeschlossen ist.

</dd> <dt>

*ppShaderText* \[ out\]
</dt> <dd>

Typ: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Ein Zeiger auf den Arbeitsspeicher, der den nicht kompilierten Shader enthält.

</dd> <dt>

*ppErrorMsgs* \[ out\]
</dt> <dd>

Typ: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Die Adresse eines Zeigers auf den Arbeitsspeicher, der Ggf. Fehler bei der Effekterstellung enthält.

</dd> <dt>

*pHResult* \[ out\]
</dt> <dd>

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Ein Zeiger auf den Rückgabewert. Kann **NULL** sein. Wenn *pPump* nicht **NULL** ist, muss *pHResult* ein gültiger Speicherort sein, bis die asynchrone Ausführung abgeschlossen ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der In [Direct3D 11-Rückgabecodes aufgeführten](d3d11-graphics-reference-returnvalues.md)Werte.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX11async.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX11.lib</dt> </dl>    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Funktionen](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

