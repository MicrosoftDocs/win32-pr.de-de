---
title: ID3DX11EffectDepthStencilVariable UndoSetDepthStencilState-Methode (D3dx11effect.h)
description: Setzt einen zuvor festgelegten Tiefenschablonenzustand zurück.
ms.assetid: 558bc777-a520-4235-84d3-db2d9f1ce4b6
keywords:
- UndoSetDepthStencilState-Methode Direct3D 11
- UndoSetDepthStencilState-Methode Direct3D 11 , ID3DX11EffectDepthStencilVariable-Schnittstelle
- ID3DX11EffectDepthStencilVariable-Schnittstelle Direct3D 11 , UndoSetDepthStencilState-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable.UndoSetDepthStencilState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 626c430c268c7c8c63e006bdde9e62a49d139d2212e08d7a3e4cedeea3d31722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989816"
---
# <a name="id3dx11effectdepthstencilvariableundosetdepthstencilstate-method"></a>ID3DX11EffectDepthStencilVariable::UndoSetDepthStencilState-Methode

Setzt einen zuvor festgelegten Tiefenschablonenzustand zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT UndoSetDepthStencilState(
   UINT Index
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Index in ein Array von Tiefenschablonenschnittstellen. Wenn nur eine Tiefenschablonenschnittstelle vorhanden ist, verwenden Sie 0.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt einen der folgenden [Direct3D 11-Rückgabecodes zurück.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Hinweise

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte zur Verfügung. Sie müssen die Effects 11-Quelle verwenden, um ihre Effekte-Typ-Anwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>N/A (Eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX11EffectDepthStencilVariable](id3dx11effectdepthstencilvariable.md)
</dt> </dl>

 

