---
description: Gibt die Stärke der Linie an.
ms.assetid: cedf9217-2b47-40c3-a64c-9872c1083d71
title: ID3DXLine::-Methode (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetWidth
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d357d7516233caf6ef9206aa2aecc2a98a435cde
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050922"
---
# <a name="id3dxlinesetwidth-method"></a>ID3DXLine:: stwidth-Methode

Gibt die Stärke der Linie an.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetWidth(
  [in] FLOAT fWidth
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Breite* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Beschreibt die Linienstärke.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> </dl>

 

 
