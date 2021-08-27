---
title: ID3DX11EffectBlendVariable UndoSetBlendState-Methode (D3dx11effect.h)
description: Setzt einen zuvor festgelegten Überblendungszustand zurück.
ms.assetid: 375c225b-558f-4ad0-81e7-62eff3e28cf1
keywords:
- UndoSetBlendState-Methode Direct3D 11
- UndoSetBlendState-Methode Direct3D 11, ID3DX11EffectBlendVariable-Schnittstelle
- ID3DX11EffectBlendVariable-Schnittstelle Direct3D 11 , UndoSetBlendState-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable.UndoSetBlendState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fefb1e59ef3ef30bcd21700a2573830e3178f574fe631ab4c7373b0bddd5fdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046478"
---
# <a name="id3dx11effectblendvariableundosetblendstate-method"></a>ID3DX11EffectBlendVariable::UndoSetBlendState-Methode

Setzt einen zuvor festgelegten Überblendungszustand zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT UndoSetBlendState(
   UINT Index
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indizieren sie in ein Array von Blendzustandsschnittstellen. Wenn nur eine Blendzustandsschnittstelle verfügbar ist, verwenden Sie 0.

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

[ID3DX11EffectBlendVariable](id3dx11effectblendvariable.md)
</dt> </dl>

 

