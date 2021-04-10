---
description: Speichert einen komprimierten PRT-Puffer (preberechneten Radiance Transfer) auf dem Datenträger.
ms.assetid: cc94a83e-f755-411d-a993-4529c5d53cd5
title: D3DXSavePRTCompBufferToFile-Funktion (D3DX9Mesh. h)
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
ms.openlocfilehash: d06629185637ce6fa0d7d33d5454282d2bbb8ec2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961592"
---
# <a name="d3dxsaveprtcompbuffertofile-function"></a>D3DXSavePRTCompBufferToFile-Funktion

Speichert einen komprimierten PRT-Puffer (preberechneten Radiance Transfer) auf dem Datenträger.

## <a name="syntax"></a>Syntax

```cpp
HRESULT D3DXSavePRTCompBufferToFile(
  _In_ LPCSTR              pFileName,
  _In_ LPD3DXPRTCOMPBUFFER pBuffer
);
```

## <a name="parameters"></a>Parameter

*pfilename* \[ in\]

Typ: **[LPCSTR](../winprog/windows-data-types.md)**

Der Name der Datei, in der der komprimierte Puffer gespeichert werden soll.

*pbuffer* \[ in\]

Typ: **[LPD3DXPRTCOMPBUFFER](id3dxprtcompbuffer.md)**

Adresse eines Zeigers auf das Eingabe- [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) -Objekt.

## <a name="return-value"></a>Rückgabewert

Typ: **[HRESULT](../com/structure-of-com-error-codes.md)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert **D3D \_ OK**. Wenn die Methode fehlschlägt, kann der Rückgabewert " **D3DERR \_ invalidcall"** lauten.

## <a name="remarks"></a>Bemerkungen

Die Compilereinstellung bestimmt auch die Funktions Version. Wenn Unicode definiert ist, wird der Funktions aufzurufen in [D3DXSavePRTCompBufferToFileW]()aufgelöst. Andernfalls wird der Funktions aufrufin **D3DXSavePRTCompBufferToFileA** aufgelöst.

Beim PCA-Dateiformat handelt es sich um eine Binärdatei in Form eines Headers und dann um zwei oder drei Datenblöcke.

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

Wenn " *bistex* " ungleich 0 (null) ist, sollten die *NumSamples* gleich sein `TexWidth * TexHeight` .

Der Basisdaten Block, der auf den Header folgt, ist `NumCoeffs * NumChannels * (NumPCA + 1) * NumClusters * sizeof(float)` Bytes.

Dabei handelt es sich um den Datenblock für PCA-Gewichtungen, der `NumPCA * NumSamples * sizeof(float)` Bytes ist.

Wenn *numclusters* größer als 1 ist, endet die Datei mit dem Cluster-IDs-Datenblock von `NumSamples * sizeof(UINT)` Bytes.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |

## <a name="see-also"></a>Siehe auch

[Voraus berechnete Strahlungs Übertragungsfunktionen](dx9-graphics-reference-d3dx-functions-prt.md)
