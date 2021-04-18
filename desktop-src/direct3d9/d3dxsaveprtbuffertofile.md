---
description: Speichert einen PRT-Puffer (preberechneten Radiance Transfer) auf dem Datenträger.
ms.assetid: 1fca69bd-6729-45af-981f-b7480c741bc2
title: D3DXSavePRTBufferToFile-Funktion (D3DX9Mesh. h)
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
ms.openlocfilehash: b796ee24be44bf65be7df938bdfe85d6784cc5f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365086"
---
# <a name="d3dxsaveprtbuffertofile-function"></a>D3DXSavePRTBufferToFile-Funktion

Speichert einen PRT-Puffer (preberechneten Radiance Transfer) auf dem Datenträger.

## <a name="syntax"></a>Syntax

```cpp
HRESULT D3DXSavePRTBufferToFile(
  _In_ LPCSTR          pFileName,
  _In_ LPD3DXPRTBUFFER pBuffer
);
```

## <a name="parameters"></a>Parameter

*pfilename* \[ in\]

Typ: **[LPCSTR](../winprog/windows-data-types.md)**

Der Name der Datei, in der der Puffer gespeichert werden soll.

*pbuffer* \[ in\]

Typ: **[LPD3DXPRTBUFFER](id3dxprtbuffer.md)**

Adresse eines Zeigers auf das Eingabe- [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt.

## <a name="return-value"></a>Rückgabewert

Typ: **[HRESULT](../com/structure-of-com-error-codes.md)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert **D3D \_ OK**. Wenn die Methode fehlschlägt, kann der Rückgabewert " **D3DERR \_ invalidcall"** lauten.

## <a name="remarks"></a>Bemerkungen

Die Compilereinstellung bestimmt auch die Funktions Version. Wenn Unicode definiert ist, wird der Funktions aufzurufen in [D3DXSavePRTBufferToFileW]()aufgelöst. Andernfalls wird der Funktions aufrufin **D3DXSavePRTBufferToFileA** aufgelöst.

Das PRT-Dateiformat ist eine Binärdatei in Form eines-Headers und dann ein-Datenblock.

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

Wenn " *bistex* " ungleich 0 (null) ist, sollten die *NumSamples* gleich sein `TexWidth * TexHeight` .

Der Datenblock, der auf den Header folgt, ist `NumSamples * NumCoeffs * NumChannels * sizeof(float)` Bytes.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |

## <a name="see-also"></a>Siehe auch

[Voraus berechnete Strahlungs Übertragungsfunktionen](dx9-graphics-reference-d3dx-functions-prt.md)
