---
title: ID3DX11Effect GetDevice-Methode (D3dx11effect.h)
description: Sie erhalten das Gerät, das den Effekt erstellt hat.
ms.assetid: efcc0358-9842-46eb-a521-ea220ec18735
keywords:
- GetDevice-Methode Direct3D 11
- GetDevice-Methode Direct3D 11, ID3DX11Effect-Schnittstelle
- ID3DX11Effect-Schnittstelle Direct3D 11 , GetDevice-Methode
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetDevice
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54a27dece1915373699d130f8a537a22045f7e86f246402d85bbb400ceb1d8cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124515"
---
# <a name="id3dx11effectgetdevice-method"></a>ID3DX11Effect::GetDevice-Methode

Sie erhalten das Gerät, das den Effekt erstellt hat.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDevice(
   ID3D11Device **ppDevice
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppDevice* 
</dt> <dd>

Typ: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\*\***

Ein Zeiger auf eine [**ID3D11Device.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt einen der folgenden [Direct3D 11-Rückgabecodes zurück.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Hinweise

Ein Effekt wird für ein bestimmtes Gerät durch Aufrufen einer Funktion wie [**D3DX11CreateEffectFromMemory erstellt.**](d3dx11createeffectfrommemory.md)

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Quelle Effects 11 verwenden, um Ihre Effekttypanwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>Nicht verfügbar (eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

 





