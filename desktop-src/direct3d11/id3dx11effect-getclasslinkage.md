---
title: ID3DX11Effect GetClassLinkage-Methode (D3dx11effect.h)
description: Ruft eine Klassenverknüpfungsschnittstelle ab.
ms.assetid: 006c900d-3464-4666-9fe9-d62ba8cb2b7f
keywords:
- GetClassLinkage-Methode Direct3D 11
- GetClassLinkage-Methode Direct3D 11, ID3DX11Effect-Schnittstelle
- ID3DX11Effect-Schnittstelle Direct3D 11 , GetClassLinkage-Methode
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetClassLinkage
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17f4a34ad8ff2e53d521d4fd7a1510332dddf8ff7197eac17bf4231a26e98f4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632660"
---
# <a name="id3dx11effectgetclasslinkage-method"></a>ID3DX11Effect::GetClassLinkage-Methode

Ruft eine Klassenverknüpfungsschnittstelle ab.

## <a name="syntax"></a>Syntax


```C++
ID3D11ClassLinkage* GetClassLinkage();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage)\***

Gibt einen Zeiger auf eine [**ID3D11ClassLinkage-Schnittstelle**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage) zurück.

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

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

 





