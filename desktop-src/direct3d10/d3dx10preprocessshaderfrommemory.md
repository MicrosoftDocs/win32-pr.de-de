---
description: Hinweis Anstelle dieser Legacyfunktion wird empfohlen, die D3DPreprocess-API zu verwenden. Erstellen Sie einen Shader aus dem Arbeitsspeicher, ohne ihn zu kompilieren.
ms.assetid: 099bc010-1269-4833-8a96-a7c78ed48206
title: D3DX10PreprocessShaderFromMemory-Funktion (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10PreprocessShaderFromMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a15bc79c593cbb527d440636d41c88d6d03ce5708e19a6bc961b491853d99116
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989130"
---
# <a name="d3dx10preprocessshaderfrommemory-function"></a>D3DX10PreprocessShaderFromMemory-Funktion

> [!Note]  
> Anstatt diese Legacyfunktion zu verwenden, wird empfohlen, die [**D3DPreprocess-API zu**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) verwenden.

 

Erstellen Sie einen Shader aus dem Arbeitsspeicher, ohne ihn zu kompilieren.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10PreprocessShaderFromMemory(
  _In_        LPCSTR             pSrcData,
  _In_        SIZE_T             SrcDataSize,
  _In_        LPCSTR             pFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSrcData* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Zeiger auf den Speicher, der den Shader enthält.

</dd> <dt>

*SrcDataSize* \[ In\]
</dt> <dd>

Typ: **[ **SIZE \_ T**](../winprog/windows-data-types.md)**

Größe des Shaders.

</dd> <dt>

*pFileName* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Name des Shaders.

</dd> <dt>

*pDefdefine* \[ In\]
</dt> <dd>

Typ: **const [**D3D \_ SHADER \_ MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***

Ein auf NULL terminiertes Array von Shadermakros (siehe [**D3D-SHADER-MAKRO). \_ \_**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)Legen Sie diesen Wert auf **NULL** fest, um keine Makros anzugeben.

</dd> <dt>

*pInclude* \[ In\]
</dt> <dd>

Typ: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

Ein Zeiger auf eine Includeschnittstelle (siehe [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); Legen Sie diesen Wert **auf NULL** fest, um anzugeben, dass keine Includedatei enthalten ist.

</dd> <dt>

*pPump* \[ In\]
</dt> <dd>

Typ: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

Ein Zeiger auf eine Threadpumpschnittstelle (siehe [**ID3DX10ThreadPump-Schnittstelle**](id3dx10threadpump.md)). Verwenden **Sie NULL,** um anzugeben, dass diese Funktion erst zurückgegeben werden soll, wenn sie abgeschlossen ist.

</dd> <dt>

*ppShaderText* \[ out\]
</dt> <dd>

Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Ein Zeiger auf den Arbeitsspeicher (siehe [**ID3D10Blob-Schnittstelle),**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)der den nicht kompilierten Shader enthält.

</dd> <dt>

*ppErrorMsgs* \[ out\]
</dt> <dd>

Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Die Adresse eines Zeigers auf den Arbeitsspeicher (siehe [**ID3D10Blob-Schnittstelle**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)), der Fehler bei der Erstellung von Effekten enthält, sofern ein Fehler aufgetreten ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Unter [Direct3D 10-Rückgabecodes aufgeführten Werte.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Universell Functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
