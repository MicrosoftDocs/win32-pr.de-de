---
description: Erstellen Sie einen Effektpool aus einer Effektdatei.
ms.assetid: be738374-a91e-43d3-9cec-14882e6317ee
title: D3DX10CreateEffectPoolFromFile-Funktion (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectPoolFromFile
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 500e0a72bc239b6c3f67011ed7abc0421f11cd8b9e4f67cbc86087e45027522d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753400"
---
# <a name="d3dx10createeffectpoolfromfile-function"></a>D3DX10CreateEffectPoolFromFile-Funktion

Erstellen Sie einen Effektpool aus einer Effektdatei.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10CreateEffectPoolFromFile(
  _In_        LPCTSTR            pFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        ID3D10Include      *pInclude,
  _In_        LPCSTR             pProfile,
  _In_        UINT               HLSLFlags,
  _In_        UINT               FXFlags,
  _In_        ID3D10Device       *pDevice,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10EffectPool   **ppEffectPool,
  _Out_       ID3D10Blob         **ppErrors,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pFileName* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Der Dateiname des Effekts. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR auflösen. Andernfalls wird der Datentyp in LPCSTR auflösen.

</dd> <dt>

*pDefdefine* \[ In\]
</dt> <dd>

Typ: **const [**D3D \_ SHADER \_ MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***

Ein auf NULL terminiertes Array von Shadermakros (siehe [**D3D-SHADER-MAKRO). \_ \_**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)Legen Sie diesen Wert auf **NULL** fest, um keine Makros anzugeben.

</dd> <dt>

*pInclude* \[ In\]
</dt> <dd>

Typ: **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***

Ein Zeiger auf eine Includeschnittstelle (siehe [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))). Dieser Parameter kann **NULL** sein.

</dd> <dt>

*pProfile* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Eine Zeichenfolge, die das [Shaderprofil oder](../direct3dhlsl/dx-graphics-hlsl-models.md)das Shadermodell angibt.

</dd> <dt>

*HLSLFlags* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

HLSL-Kompilierungsoptionen (siehe [D3D10-SHADER-Konstanten \_ ](d3d10-shader.md)).

</dd> <dt>

*FXFlags* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Effect-Kompilierungsoptionen (siehe [Kompilierungs- und Effektflags](d3d10-graphics-reference-effect-constants.md)).

</dd> <dt>

*pDevice* \[ In\]
</dt> <dd>

Typ: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***

Ein Zeiger auf das Gerät (siehe [**ID3D10Device Interface),**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)das die Ressourcen verwendet.

</dd> <dt>

*pPump* \[ In\]
</dt> <dd>

Typ: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

Ein Zeiger auf eine Threadpumpschnittstelle (siehe [**ID3DX10ThreadPump-Schnittstelle**](id3dx10threadpump.md)). Verwenden **Sie NULL,** um anzugeben, dass diese Funktion erst zurückgegeben werden soll, wenn sie abgeschlossen ist.

</dd> <dt>

*ppEffectPool* \[ out\]
</dt> <dd>

Typ: **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***

Die Adresse eines Zeigers auf den Effektpool (siehe [**ID3D10EffectPool-Schnittstelle**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)).

</dd> <dt>

*ppErrors* \[ out\]
</dt> <dd>

Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Die Adresse eines Zeigers auf den Arbeitsspeicher (siehe [**ID3D10Blob-Schnittstelle**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)), der Kompilierungsfehler für Auswirkungen enthält, sofern diese aufgetreten sind.

</dd> <dt>

*pHResult* \[ out\]
</dt> <dd>

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Ein Zeiger auf den Rückgabewert. Kann NULL **sein.** Wenn *pPump* nicht **NULL ist,** muss *pHResult* ein gültiger Speicherort sein, bis die asynchrone Ausführung abgeschlossen ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Unter [Direct3D 10-Rückgabecodes aufgeführten Werte.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Hinweise

In diesem Beispiel wird ein Effektpool aus dem Effekt erstellt, der im [BasicHLSL10-Beispiel verwendet wird.](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)


```
   
// Create an effect pool from an effect in memory
ID3D10EffectPool * l_pEffectPool = NULL;
ID3D10Blob* l_pBlob_Errors = NULL;
WCHAR str[MAX_PATH];
hr = DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );
hr = D3DX10CreateEffectPoolFromFile( str, 
    NULL, NULL, D3D10_SHADER_ENABLE_STRICTNESS, 
    0, pd3dDevice, NULL, &l_pEffectPool,
    &l_pBlob_Errors );
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Async.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Universell Functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
