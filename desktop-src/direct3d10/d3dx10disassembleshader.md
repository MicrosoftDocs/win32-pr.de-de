---
description: Hinweis Anstatt diese Legacyfunktion zu verwenden, wird empfohlen, die D3DDisassemble-API zu verwenden. Diese Funktion , die einen kompilierten Shader in eine Textzeichenfolge disassembliert, die Assemblyanweisungen und Registerzuweisungen enthält, ist nicht mehr vorhanden.
ms.assetid: f94264f8-121a-4bb7-bf1f-cc5d2cac6cd2
title: D3DX10DisassembleShader-Funktion (D3DX10Core.h)
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
ms.openlocfilehash: bd69b6dc2cede96e6ca07983195d202cfd248633f44a13fe1967393c446ca329
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753220"
---
# <a name="d3dx10disassembleshader-function"></a>D3DX10DisassembleShader-Funktion

> [!Note]  
> Anstatt diese Legacyfunktion zu verwenden, wird empfohlen, die [**D3DDisassemble-API**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) zu verwenden.

 

Diese Funktion , die einen kompilierten Shader in eine Textzeichenfolge disassembliert, die Assemblyanweisungen und Registerzuweisungen enthält, ist nicht mehr vorhanden. Verwenden Sie stattdessen [**D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect).

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

*pShader* \[ In\]
</dt> <dd>

Typ: **const \* void**

Ein Zeiger auf den [**kompilierten Shader**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).

</dd> <dt>

*BytecodeLength* \[ In\]
</dt> <dd>

Typ: **[ **SIZE \_ T**](../winprog/windows-data-types.md)**

Die Größe von pShader.

</dd> <dt>

*EnableColorCode* \[ In\]
</dt> <dd>

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

Fügen Sie HTML-Tags in die Ausgabe ein, um das Ergebnis mit Farbcode zu versehen.

</dd> <dt>

*pComments* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Die Kommentarzeichenfolge am oberen Rand des Shaders, die die Shaderkonstanten und -variablen identifiziert.

</dd> <dt>

*ppDisassembly* \[ out\]
</dt> <dd>

Typ: **[ **ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Adresse eines Puffers (siehe [**ID3D10Blob-Schnittstelle),**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)der den disassemblierten Shader enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt einen der folgenden [Direct3D 10-Rückgabecodes zurück.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Hinweise

Dieser zurückgegebene Text enthält einen Header mit der Version des HLSL-Compilers, der zum Generieren dieses Objekts verwendet wird, Kommentare, die das Speicherlayout der konstanten Puffer beschreiben, die vom Shader verwendet werden, Eingabe- und Ausgabesignaturen sowie Ressourcenbindungspunkte.

Hier sehen Sie ein Beispiel für die Disassemblierung eines kompilierten Shaders. Im Beispiel wird davon ausgegangen, dass Sie mit einem kompilierten Shader beginnen (dargestellt als *pVSBuf,* der im [HLSLWithoutFX10-Beispiel angezeigt wird).](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)


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
| Header<br/> | <dl> <dt>D3DX10Core.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Universell Functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
