---
description: Legt Samplingeigenschaften fest, die vom PRT-Simulator (Precomputed Radiance Transfer) verwendet werden.
ms.assetid: a33963a7-fbcb-4e1c-a4f3-fb20a99fcf9f
title: ID3DXPRTEngine::SetSamplingInfo-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetSamplingInfo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: db15bc2120f90cf52aa4f3c41eccecc7d308cc8392ae368cd4423a90f218f6ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118293364"
---
# <a name="id3dxprtenginesetsamplinginfo-method"></a>ID3DXPRTEngine::SetSamplingInfo-Methode

Legt Samplingeigenschaften fest, die vom PRT-Simulator (Precomputed Radiance Transfer) verwendet werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetSamplingInfo(
  [in] UINT  NumRays,
  [in] BOOL  UseSphere,
  [in] BOOL  UseCosine,
  [in] BOOL  Adaptive,
  [in] FLOAT AdaptiveThresh
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NumRays* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der Lichtlichtlichter, die an jede Stichprobe zu richten sind. Muss größer sein als Null.

</dd> <dt>

*UseSphere* \[ In\]
</dt> <dd>

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

True **gibt an,** dass Stichproben über eine vollständige Kugel berechnet werden. False **gibt an,** dass Stichproben über eine Hemimihäe berechnet werden.

</dd> <dt>

*UseCosine* \[ In\]
</dt> <dd>

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

True **gibt an,** dass eine Kosinusgewichtung von Stichproben verwendet wird. Wenn sowohl UseCosine als auch UseSphere **TRUE sind,** tritt bei der Methode ein Fehler auf, und es wird ein Fehler zurückgegeben.

</dd> <dt>

*Adaptiver Modus* \[ In\]
</dt> <dd>

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

Muss FALSE **sein.** Die adaptive Stichprobenentnahme ist derzeit nicht implementiert.

</dd> <dt>

*AdaptiveThresh* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert wie folgt sein: D3DERR \_ INVALIDCALL, E \_ NOTIMPL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
