---
description: Erstellen Sie einen Effekt aus dem Arbeitsspeicher.
ms.assetid: 6903a695-bb87-45fe-9913-25beeaf17233
title: D3DX10CreateEffectFromMemory-Funktion (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectFromMemory
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 3bcc32e94d6329d42edd27f1daf39e40d28b71ba65cc32fd88d4ae3951d5012e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989240"
---
# <a name="d3dx10createeffectfrommemory-function"></a>D3DX10CreateEffectFromMemory-Funktion

Erstellen Sie einen Effekt aus dem Arbeitsspeicher.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10CreateEffectFromMemory(
  _In_        LPCVOID            pData,
  _In_        SIZE_T             DataLength,
  _In_        LPCSTR             pSrcFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
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

*pData* \[ In\]
</dt> <dd>

Typ: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Zeiger auf den Effekt im Arbeitsspeicher.

</dd> <dt>

*DataLength* \[ In\]
</dt> <dd>

Typ: **[ **SIZE \_ T**](../winprog/windows-data-types.md)**

Größe des Effekts im Arbeitsspeicher.

</dd> <dt>

*pSrcFileName* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Name der Effektdatei im Arbeitsspeicher.

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

Effect-Kompilierungsoptionen (siehe [D3D10 \_ EFFECT-Konstanten](d3d10-effect.md)).

</dd> <dt>

*pDevice* \[ In\]
</dt> <dd>

Typ: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***

Ein Zeiger auf das Gerät (siehe [**ID3D10Device Interface),**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)das die Ressourcen verwendet.

</dd> <dt>

*pEffectPool* \[ In\]
</dt> <dd>

Typ: **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***

Zeiger auf einen Effektpool (siehe [**ID3D10EffectPool-Schnittstelle**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) zum Freigeben von Variablen zwischen Effekten.

</dd> <dt>

*pPump* \[ In\]
</dt> <dd>

Typ: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

Ein Zeiger auf eine Threadpumpschnittstelle (siehe [**ID3DX10ThreadPump-Schnittstelle**](id3dx10threadpump.md)). Verwenden **Sie NULL,** um anzugeben, dass diese Funktion erst zurückgegeben werden soll, wenn sie abgeschlossen ist.

</dd> <dt>

*ppEffect* \[ out\]
</dt> <dd>

Typ: **[ **ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)\*\***

Adresse eines Zeigers auf den Effekt (siehe [**ID3D10Effect-Schnittstelle**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)), der erstellt wird.

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

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Async.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Universell Functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
