---
title: ID3DX11EffectDepthStencilViewVariable SetDepthStencilArray-Methode (D3dx11effect.h)
description: Legen Sie ein Array von Ressourcen für die Tiefen-Schablonenansicht fest.
ms.assetid: 7a00ca3e-fb07-4185-a361-36228f72dcea
keywords:
- SetDepthStencilArray-Methode Direct3D 11
- SetDepthStencilArray-Methode Direct3D 11, ID3DX11EffectDepthStencilViewVariable-Schnittstelle
- ID3DX11EffectDepthStencilViewVariable-Schnittstelle Direct3D 11 , SetDepthStencilArray-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable.SetDepthStencilArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97e6588a039d77730c42e68a977fe16e8126cf54ab502a6806a45a5190e57b26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858130"
---
# <a name="id3dx11effectdepthstencilviewvariablesetdepthstencilarray-method"></a>ID3DX11EffectDepthStencilViewVariable::SetDepthStencilArray-Methode

Legen Sie ein Array von Ressourcen für die Tiefen-Schablonenansicht fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetDepthStencilArray(
   ID3D11DepthStencilView **ppResources,
   UINT                   Offset,
   UINT                   Count
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppResources* 
</dt> <dd>

Typ: **[ **ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\*\***

Ein Zeiger auf ein Array von Tiefen-Schablonen-Ansichtsschnittstellen. Siehe [**ID3D11DepthStencilView.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)

</dd> <dt>

*Offset* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Der nullbasierte Arrayindex zum Festlegen der ersten Schnittstelle.

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
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Quelle Effects 11 verwenden, um Ihre Effekttypanwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>Nicht verfügbar (eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX11EffectDepthStencilViewVariable](id3dx11effectdepthstencilviewvariable.md)
</dt> </dl>

 

