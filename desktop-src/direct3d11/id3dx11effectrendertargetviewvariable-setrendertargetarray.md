---
title: ID3DX11EffectRenderTargetViewVariable SetRenderTargetArray-Methode (D3dx11effect.h)
description: Legen Sie ein Array von Renderzielen fest.
ms.assetid: 03e1c4ea-292c-439f-a647-070b9e91a044
keywords:
- SetRenderTargetArray-Methode Direct3D 11
- SetRenderTargetArray-Methode Direct3D 11 , ID3DX11EffectRenderTargetViewVariable-Schnittstelle
- ID3DX11EffectRenderTargetViewVariable-Schnittstelle Direct3D 11 , SetRenderTargetArray-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectRenderTargetViewVariable.SetRenderTargetArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33259ba97979130968ad67b3609f31d6549e6a62449d3bcadd80bb52cb3d8593
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118534146"
---
# <a name="id3dx11effectrendertargetviewvariablesetrendertargetarray-method"></a>ID3DX11EffectRenderTargetViewVariable::SetRenderTargetArray-Methode

Legen Sie ein Array von Renderzielen fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetRenderTargetArray(
   ID3D11RenderTargetView **ppResources,
   UINT                   Offset,
   UINT                   Count
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppResources* 
</dt> <dd>

Typ: **[ **ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\*\***

Legen Sie ein Array von Schnittstellen für render-target-view fest. Siehe [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).

</dd> <dt>

*Offset* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Der nullbasierte Arrayindex zum Speichern der ersten Schnittstelle.

</dd> <dt>

*Count* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Die Anzahl der Elemente im Array.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX11EffectRenderTargetViewVariable](id3dx11effectrendertargetviewvariable.md)
</dt> </dl>

 

