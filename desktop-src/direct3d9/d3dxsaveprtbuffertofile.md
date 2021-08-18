---
description: Speichert einen prt-Puffer (Precomputed Radiance Transfer) auf dem Datenträger.
ms.assetid: 1fca69bd-6729-45af-981f-b7480c741bc2
title: D3DXSavePRTBufferToFile-Funktion (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSavePRTBufferToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0bfa3d06970d138ff1c868403c20bb41cf14f0a5cbb7116cbe0f0843a51258dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524530"
---
# <a name="d3dxsaveprtbuffertofile-function"></a>D3DXSavePRTBufferToFile-Funktion

Speichert einen prt-Puffer (Precomputed Radiance Transfer) auf dem Datenträger.

## <a name="syntax"></a>Syntax

```cpp
HRESULT D3DXSavePRTBufferToFile(
  _In_ LPCSTR          pFileName,
  _In_ LPD3DXPRTBUFFER pBuffer
);
```

## <a name="parameters"></a>Parameter

*pFileName* \[ In\]

Typ: **[LPCSTR](../winprog/windows-data-types.md)**

Name der Datei, in der der Puffer gespeichert werden soll.

*pBuffer* \[ In\]

Typ: **[LPD3DXPRTBUFFER](id3dxprtbuffer.md)**

Adresse eines Zeigers auf das [**Eingabeobjekt ID3DXPRTBuffer.**](id3dxprtbuffer.md)

## <a name="return-value"></a>Rückgabewert

Typ: **[HRESULT](../com/structure-of-com-error-codes.md)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert **D3D \_ OK.** Wenn die Methode fehlschlägt, kann der Rückgabewert **D3DERR \_ INVALIDCALL sein.**

## <a name="remarks"></a>Hinweise

Die Compilereinstellung bestimmt auch die Funktionsversion. Wenn Unicode definiert ist, wird der Funktionsaufruf in [D3DXSavePRTBufferToFileW auflösen.]() Andernfalls wird der Funktionsaufruf in **D3DXSavePRTBufferToFileA auflösen.**

Das PRT-Dateiformat ist eine Binärdatei in Form eines Headers und dann eines Datenblocks.

```cpp
struct PRTHeader
{
    UINT NumSamples;
    UINT NumCoeffs;
    UINT NumChannels;
    UINT TexWidth;
    UINT TexHeight;
    UINT bIsTex;
};
```

Wenn *bIsTex* nicht 0 (null) ist, sollte *NumSamples* gleich `TexWidth * TexHeight` sein.

Der Datenblock, der dem Header folgt, ist `NumSamples * NumCoeffs * NumChannels * sizeof(float)` bytes.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |

## <a name="see-also"></a>Weitere Informationen

[Vorausberechnungsfunktionen für die Übertragung von Radiance](dx9-graphics-reference-d3dx-functions-prt.md)
