---
description: Erstellen Sie einen asynchronen Datenprozessor für einen Speicherpool.
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
ms.openlocfilehash: 32e7c60f28a823c624b3866a8cdd46db659f8a49
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219572"
---
# <a name="d3dx10createasynceffectpoolcreateprocessor-function"></a>D3DX10CreateAsyncEffectPoolCreateProcessor-Funktion

Erstellen Sie einen asynchronen Datenprozessor für einen Speicherpool.

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

*pfilename* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Eine Zeichenfolge, die den Effekt Dateiname enthält.

</dd> <dt>

*pdefinitionen* \[ in\]
</dt> <dd>

Type: **Konstanten [**D3D \_ Shader- \_ Makro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***

Ein mit Null endendes Array von Shader-Makros (siehe [**D3D \_ Shader \_ Macro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); legen Sie diese Einstellung auf **null** fest, um keine Makros anzugeben.

</dd> <dt>

*pinclude* \[ in\]
</dt> <dd>

Typ: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

Ein Zeiger auf eine include-Schnittstelle (siehe [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); Legen Sie dies auf **null** fest, um anzugeben, dass keine Includedatei vorhanden ist.

</dd> <dt>

*pprofile* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Eine Zeichenfolge, die das [Shader-Profil](../direct3dhlsl/dx-graphics-hlsl-models.md) oder Shader-Modell angibt.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

HLSL-Kompilierungsoptionen (siehe [Shader-Flags](d3d10-graphics-reference-effect-constants.md)).

</dd> <dt>

*Fxflags* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Effekt Kompilierungsoptionen (siehe [Kompilierungs-und Wirkungs Flags](d3d10-graphics-reference-effect-constants.md)).

</dd> <dt>

*pdevice* \[ in\]
</dt> <dd>

Typ: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***

Ein Zeiger auf das Gerät (siehe [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)), von dem die Ressourcen verwendet werden.

</dd> <dt>

*pperrorbuffer* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Die Adresse eines Zeigers auf den Speicher (siehe [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)), die Auswirkungen auf Kompilierungsfehler enthält (sofern vorhanden).

</dd> <dt>

*ppdataprocessor* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***

Adresse eines Zeigers auf einen Puffer, der den erstellten Datenprozessor enthält (siehe [**ID3DX10DataProcessor-Schnittstelle**](id3dx10dataprocessor.md)).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Async. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Universell Funktionen](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
