---
description: Beachten Sie, dass Sie die D3DDisassemble-API verwenden, anstatt diese Legacy Funktion zu verwenden. Diese Funktion, die einen kompilierten Shader in eine Text Zeichenfolge disassembliert, die Assemblyanweisungen und Register Zuweisungen enthält, ist nicht mehr vorhanden.
ms.assetid: f94264f8-121a-4bb7-bf1f-cc5d2cac6cd2
title: D3DX10DisassembleShader-Funktion (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10DisassembleShader
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 13716fd5d25e2e8602379ea3864c516fa5388475
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354979"
---
# <a name="d3dx10disassembleshader-function"></a>D3DX10DisassembleShader-Funktion

> [!Note]  
> Anstatt diese Legacy Funktion zu verwenden, empfiehlt es sich, die [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) -API zu verwenden.

 

Diese Funktion, die einen kompilierten Shader in eine Text Zeichenfolge disassembliert, die Assemblyanweisungen und Register Zuweisungen enthält, ist nicht mehr vorhanden. Verwenden Sie stattdessen [**D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect).

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10DisassembleShader(
  _In_  const void       *pShader,
  _In_        SIZE_T     BytecodeLength,
  _In_        BOOL       EnableColorCode,
  _In_        LPCSTR     pComments,
  _Out_       ID3D10Blob **ppDisassembly
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pshader* \[ in\]
</dt> <dd>

Typ: Konstante **void \***

Ein Zeiger auf den [**kompilierten Shader**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).

</dd> <dt>

*Bytecodelta ength* \[ in\]
</dt> <dd>

Typ: **[ **Größe \_ T**](../winprog/windows-data-types.md)**

Die Größe des pshader.

</dd> <dt>

*Enablecolorcode* \[ in\]
</dt> <dd>

Typ: **[ **bool**](../winprog/windows-data-types.md)**

Fügen Sie HTML-Tags in die Ausgabe ein, um das Ergebnis farblich zu färben.

</dd> <dt>

*pcomments* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Die Kommentar Zeichenfolge am Anfang des Shader, die die shaderkonstanten und Variablen identifiziert.

</dd> <dt>

*ppdisassembly* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Adresse eines Puffers (siehe [**ID3D10Blob Interface**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)), der den disassemblierten Shader enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt einen der folgenden [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)zurück.

## <a name="remarks"></a>Bemerkungen

Dieser zurückgegebene Text enthält einen Header mit der Version des HLSL-Compilers, der zum Generieren dieses Objekts verwendet wurde, Kommentare, die das Speicher Layout der vom Shader verwendeten Konstanten Puffer, Eingabe-und Ausgabe Signaturen und Ressourcen Bindungs Punkte beschreiben.

Im folgenden finden Sie ein Beispiel für die Disassemblierung eines kompilierten Shaders. Im Beispiel wird davon ausgegangen, dass Sie mit einem kompilierten Shader beginnen (als *pvsbuf* angezeigt, den Sie in [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)sehen können).


```
LPCSTR commentString = NULL;
ID3D10Blob* pIDisassembly = NULL;
char* pDisassembly = NULL;
if( pVSBuf )
{
    D3D10DisassembleShader( (UINT*) pVSBuf->GetBufferPointer(), 
        pVSBuf->GetBufferSize(), TRUE, commentString, &pIDisassembly );
    if( pIDisassembly )
    {
        FILE* pFile = fopen( "shader.htm", "w" );
        if( pFile)
        {
            fputs( (char*)pIDisassembly->GetBufferPointer(), pFile );
            fclose( pFile );
        }
    }
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Core. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Universell Funktionen](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
