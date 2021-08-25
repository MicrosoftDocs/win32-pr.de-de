---
description: Erstellen sie einen Effekt aus einer Ressource.
ms.assetid: 239a3b14-9eea-4a0f-96b5-3959b7be3e19
title: D3DX10CreateEffectFromResource-Funktion (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectFromResource
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: a94fd466194de6942fb2dee2968d738513743b043b18310ffabaf80fe73fc76a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852340"
---
# <a name="d3dx10createeffectfromresource-function"></a>D3DX10CreateEffectFromResource-Funktion

Erstellen sie einen Effekt aus einer Ressource.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10CreateEffectFromResource(
  _In_        HMODULE            hModule,
  _In_        LPCTSTR            pResourceName,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D10_SHADER_MACRO *pDefines,
  _In_        ID3D10Include      *pInclude,
  _In_        LPCSTR             pProfile,
  _In_        UINT               HLSLFlags,
  _In_        UINT               FXFlags,
  _In_        ID3D10Device       *pDevice,
  _In_        ID3D10EffectPool   *pEffectPool,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Effect       **ppEffect,
  _Out_       ID3D10Blob         **ppErrors,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hModule* \[ In\]
</dt> <dd>

Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**

Ein Handle für das Ressourcenmodul, das den Effekt enthält. HMODULE kann mit der [GetModuleHandle-Funktion](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea)abgerufen werden.

</dd> <dt>

*pResourceName* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Name der Ressource in hModule. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst. Andernfalls wird der Datentyp in LPCSTR aufgelöst.

</dd> <dt>

*pSrcFileName* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Optional. Auswirkungsdateiname, der nur für Fehlermeldungen verwendet wird. Kann **NULL** sein.

</dd> <dt>

*pDefine* \[ In\]
</dt> <dd>

Typ: **const [**D3D \_ SHADER \_ MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***

Ein MIT NULL endendes Array von Shadermakros (siehe [**D3D-SHADER-MAKRO); \_ \_**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)legen Sie diesen Wert auf **NULL** fest, um keine Makros anzugeben.

</dd> <dt>

*pInclude* \[ In\]
</dt> <dd>

Typ: **[ **ID3D10Einschluss**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***

Ein Zeiger auf eine Includeschnittstelle (siehe [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))). Dieser Parameter kann **NULL** sein.

</dd> <dt>

*pProfile* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Eine Zeichenfolge, die das [Shaderprofil oder Shadermodell](../direct3dhlsl/dx-graphics-hlsl-models.md)angibt.

</dd> <dt>

*HLSLFlags* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

HLSL-Kompilierungsoptionen (siehe [D3D10 \_ SHADER-Konstanten).](d3d10-shader.md)

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

*pEffectPool* \[ In\]
</dt> <dd>

Typ: **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***

Zeiger auf einen Effektpool (siehe [**ID3D10EffectPool-Schnittstelle)**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)zum Freigeben von Variablen zwischen Effekten.

</dd> <dt>

*pPump* \[ In\]
</dt> <dd>

Typ: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

Ein Zeiger auf eine Threadpumpschnittstelle (siehe [**ID3DX10ThreadPump-Schnittstelle).**](id3dx10threadpump.md) Geben Sie mit **NULL** an, dass diese Funktion erst zurückgegeben werden soll, wenn sie abgeschlossen ist.

</dd> <dt>

*ppEffect* \[ out\]
</dt> <dd>

Typ: **[ **ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)\*\***

Adresse eines Zeigers auf den Effekt (siehe [**ID3D10Effect-Schnittstelle),**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)der erstellt wird.

</dd> <dt>

*ppErrors* \[ out\]
</dt> <dd>

Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Die Adresse eines Zeigers auf den Arbeitsspeicher (siehe [**ID3D10Blob-Schnittstelle),**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)der Kompilierungsfehler enthält, sofern vorhanden.

</dd> <dt>

*pHResult* \[ out\]
</dt> <dd>

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Ein Zeiger auf den Rückgabewert. Kann **NULL** sein. Wenn *pPump* nicht **NULL** ist, muss *pHResult* ein gültiger Speicherort sein, bis die asynchrone Ausführung abgeschlossen ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der In [Direct3D 10-Rückgabecodes aufgeführten](d3d10-graphics-reference-returnvalues.md)Werte.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Async.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Universell Functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
