---
description: Hinweis Anstelle dieser Legacyfunktion wird empfohlen, die D3DPreprocess-API zu verwenden. Erstellen Sie einen Shader aus einer Ressource, ohne ihn zu kompilieren.
ms.assetid: ca93e208-7627-4bf5-ab83-d4e906e149eb
title: D3DX10PreprocessShaderFromResource-Funktion (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10PreprocessShaderFromResource
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 63546fbf7424189c5b9d398b4c6ddce076d7e02db5900031c15b579048da1965
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753160"
---
# <a name="d3dx10preprocessshaderfromresource-function"></a>D3DX10PreprocessShaderFromResource-Funktion

> [!Note]  
> Anstatt diese Legacyfunktion zu verwenden, wird empfohlen, die [**D3DPreprocess-API zu**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) verwenden.

 

Erstellen Sie einen Shader aus einer Ressource, ohne ihn zu kompilieren.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10PreprocessShaderFromResource(
  _In_        HMODULE            hModule,
  _In_        LPCTSTR            pResourceName,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hModule* \[ In\]
</dt> <dd>

Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**

Handle für das Ressourcenmodul, das den Shader enthält. HMODULE kann mit der [GetModuleHandle-Funktion erhalten werden.](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea)

</dd> <dt>

*pResourceName* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Der Name der Ressource in side hModule, die den Shader enthält. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR auflösen. Andernfalls wird der Datentyp in LPCSTR auflösen.

</dd> <dt>

*pSrcFileName* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Optional. Name der Effect-Datei, die nur für Fehlermeldungen verwendet wird. Kann NULL **sein.**

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

 

 
