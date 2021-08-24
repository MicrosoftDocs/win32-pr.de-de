---
description: Erstellen sie einen asynchronen Datenprozessor für einen Speicherpool.
ms.assetid: 3985a5e5-492e-4003-9d10-6e34620de69f
title: D3DX10CreateAsyncEffectPoolCreateProcessor-Funktion (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncEffectPoolCreateProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 00cced370cee4ffc0e233798f9c8e1df9970244a3398c79d27eb3a61e44b704b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753380"
---
# <a name="d3dx10createasynceffectpoolcreateprocessor-function"></a>D3DX10CreateAsyncEffectPoolCreateProcessor-Funktion

Erstellen sie einen asynchronen Datenprozessor für einen Speicherpool.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10CreateAsyncEffectPoolCreateProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags,
  _In_        UINT                 FXFlags,
  _In_        ID3D10Device         *pDevice,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pFileName* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Eine Zeichenfolge, die den Effektdateinamen enthält.

</dd> <dt>

*pDefine* \[ In\]
</dt> <dd>

Typ: **const [**D3D \_ SHADER \_ MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***

Ein MIT NULL endendes Array von Shadermakros (siehe [**D3D-SHADER-MAKRO); \_ \_**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)legen Sie diesen Wert auf **NULL** fest, um keine Makros anzugeben.

</dd> <dt>

*pInclude* \[ In\]
</dt> <dd>

Typ: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

Ein Zeiger auf eine Includeschnittstelle (siehe [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); Legen Sie diesen Wert auf **NULL** fest, um anzugeben, dass keine Includedatei vorhanden ist.

</dd> <dt>

*pProfile* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Eine Zeichenfolge, die das [Shaderprofil oder Shadermodell](../direct3dhlsl/dx-graphics-hlsl-models.md) angibt.

</dd> <dt>

*Flags* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

HLSL-Kompilierungsoptionen (siehe [Shaderflags](d3d10-graphics-reference-effect-constants.md)).

</dd> <dt>

*FXFlags* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Optionen für die Effektkompilierung (siehe [Kompilieren und Effektflags).](d3d10-graphics-reference-effect-constants.md)

</dd> <dt>

*pDevice* \[ In\]
</dt> <dd>

Typ: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***

Ein Zeiger auf das Gerät (siehe [**ID3D10Device-Schnittstelle),**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)das die Ressourcen verwendet.

</dd> <dt>

*ppErrorBuffer* \[ out\]
</dt> <dd>

Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Die Adresse eines Zeigers auf den Arbeitsspeicher (siehe [**ID3D10Blob-Schnittstelle),**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)der Kompilierungsfehler enthält, sofern vorhanden.

</dd> <dt>

*ppDataProcessor* \[ out\]
</dt> <dd>

Typ: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***

Adresse eines Zeigers auf einen Puffer, der den erstellten Datenprozessor enthält (siehe [**ID3DX10DataProcessor-Schnittstelle).**](id3dx10dataprocessor.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der In [Direct3D 10-Rückgabecodes aufgeführten](d3d10-graphics-reference-returnvalues.md)Werte.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Async.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Universell Functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
