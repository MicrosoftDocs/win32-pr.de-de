---
title: ID3DX11EffectTechnique GetDesc-Methode (D3dx11effect.h)
description: Erhalten Sie eine Technikbeschreibung.
ms.assetid: ed82d873-0540-4aa8-ac0f-198852b886ad
keywords:
- GetDesc-Methode Direct3D 11
- GetDesc-Methode Direct3D 11, ID3DX11EffectTechnique-Schnittstelle
- ID3DX11EffectTechnique-Schnittstelle Direct3D 11 , GetDesc-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad72387b59690d747d5b86927062e8ee8a0ec51ba2f81d746112d65e72d5782f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118532528"
---
# <a name="id3dx11effecttechniquegetdesc-method"></a>ID3DX11EffectTechnique::GetDesc-Methode

Erhalten Sie eine Technikbeschreibung.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDesc(
   D3DX11_TECHNIQUE_DESC *pDesc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDesc* 
</dt> <dd>

Typ: **[ **D3DX11 \_ TECHNIQUE \_ DESC**](d3dx11-technique-desc.md)\***

Ein Zeiger auf eine Technikbeschreibung (siehe [**D3DX11 \_ TECHNIQUE \_ DESC**](d3dx11-technique-desc.md)).

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

[ID3DX11EffectTechnique](id3dx11effecttechnique.md)
</dt> </dl>

 

 





