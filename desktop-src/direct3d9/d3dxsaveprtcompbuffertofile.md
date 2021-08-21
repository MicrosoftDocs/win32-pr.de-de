---
description: Speichert einen komprimierten PRT-Puffer (Precomputed Radiance Transfer) auf den Datenträger.
ms.assetid: cc94a83e-f755-411d-a993-4529c5d53cd5
title: D3DXSavePRTCompBufferToFile-Funktion (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSavePRTCompBufferToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a62bd164ce8eb8175c62658b19dd5ce6282d6c75b081db45f8b0af4994322579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524510"
---
# <a name="d3dxsaveprtcompbuffertofile-function"></a>D3DXSavePRTCompBufferToFile-Funktion

Speichert einen komprimierten PRT-Puffer (Precomputed Radiance Transfer) auf den Datenträger.

## <a name="syntax"></a>Syntax

```cpp
HRESULT D3DXSavePRTCompBufferToFile(
  _In_ LPCSTR              pFileName,
  _In_ LPD3DXPRTCOMPBUFFER pBuffer
);
```

## <a name="parameters"></a>Parameter

*pFileName* \[ In\]

Typ: **[LPCSTR](../winprog/windows-data-types.md)**

Name der Datei, in der der komprimierte Puffer gespeichert werden soll.

*pBuffer* \[ In\]

Typ: **[LPD3DXPRTCOMPBUFFER](id3dxprtcompbuffer.md)**

Adresse eines Zeigers auf das [**Eingabeobjekt ID3DXPRTCompBuffer.**](id3dxprtcompbuffer.md)

## <a name="return-value"></a>Rückgabewert

Typ: **[HRESULT](../com/structure-of-com-error-codes.md)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert **D3D \_ OK.** Wenn die Methode fehlschlägt, kann der Rückgabewert **D3DERR \_ INVALIDCALL sein.**

## <a name="remarks"></a>Hinweise

Die Compilereinstellung bestimmt auch die Funktionsversion. Wenn Unicode definiert ist, wird der Funktionsaufruf in [D3DXSavePRTCompBufferToFileW auflösen.]() Andernfalls wird der Funktionsaufruf in **D3DXSavePRTCompBufferToFileA auflösen.**

Das PCA-Dateiformat ist eine Binärdatei in Form eines Headers und dann zwei oder drei Datenblöcke.

```cpp
struct PRTCompressHeader
{
    UINT NumSamples;
    UINT NumCoeffs;
    UINT NumChannels;
    UINT TexWidth;
    UINT TexHeight;
    UINT bIsTex;
    UINT NumClusters;
    UINT NumPCA;
};
```

Wenn *bIsTex* nicht 0 (null) ist, sollte *NumSamples* gleich `TexWidth * TexHeight` sein.

Der Basisdatenblock, der dem Header folgt, ist `NumCoeffs * NumChannels * (NumPCA + 1) * NumClusters * sizeof(float)` bytes.

Im Anschluss folgt der PCA-Gewichtungsdatenblock, der Bytes `NumPCA * NumSamples * sizeof(float)` ist.

Wenn *NumClusters* größer als 1 ist, endet die Datei mit dem Cluster-IDs-Datenblock von `NumSamples * sizeof(UINT)` Bytes.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |

## <a name="see-also"></a>Siehe auch

[Vorausberechnungsfunktionen für die Übertragung von Radiance](dx9-graphics-reference-d3dx-functions-prt.md)
