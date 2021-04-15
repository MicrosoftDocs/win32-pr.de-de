---
description: Legt einen normalen Vektor für jeden Texttyp in einem Textur Objekt fest. Diese Methode wird verwendet, um Scheitelpunkt normale Vektoren aus einem Mesh (oder interpoliert Vertex-Normale) zu speichern, wenn die pixelbasierte Voraus berechnete Strahlungs Übertragung (PRT) berechnet wird).
ms.assetid: 165a3ef6-c142-4988-b4fb-5aafd8ff11fe
title: 'ID3DXPRTEngine:: setpertexelnormal-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetPerTexelNormal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5220ad500312792cd158967e9502381f49b0e3e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394165"
---
# <a name="id3dxprtenginesetpertexelnormal-method"></a>ID3DXPRTEngine:: setpertexelnormal-Methode

Legt einen normalen Vektor für jeden Texttyp in einem Textur Objekt fest. Diese Methode wird verwendet, um Scheitelpunkt normale Vektoren aus einem Mesh (oder interpoliert Vertex-Normale) zu speichern, wenn die pixelbasierte Voraus berechnete Strahlungs Übertragung (PRT) berechnet wird).

## <a name="syntax"></a>Syntax


```C++
HRESULT SetPerTexelNormal(
  [in] LPDIRECT3DTEXTURE9 pNormalTexture
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pnormaltexture* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Ein Zeiger auf ein [**IDirect3DTexture9**](/windows/desktop/api) -Textur Objekt, das als eine Objekt Raum normale Zuordnung fungiert, in der normale Vektoren gespeichert werden. Die Textur muss die gleichen Dimensionen wie [**ID3DXPRTBuffer**](id3dxprtbuffer.md) aufweisen und muss signierte Textur Formate speichern können.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
