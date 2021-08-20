---
title: ID3DX11EffectGroup GetTechniqueByName-Methode (D3dx11effect.h)
description: Abrufen einer Technik anhand des Namens. | ID3DX11EffectGroup GetTechniqueByName-Methode (D3dx11effect.h)
ms.assetid: 160c6d57-bec4-4718-8fad-fc9c0746736c
keywords:
- GetTechniqueByName-Methode Direct3D 11
- GetTechniqueByName-Methode Direct3D 11 , ID3DX11EffectGroup-Schnittstelle
- ID3DX11EffectGroup-Schnittstelle Direct3D 11 , GetTechniqueByName-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetTechniqueByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 590defa7477ad41d1e861dc7a8afa05370f4d83d7846c99fa1086aae94c57c1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046258"
---
# <a name="id3dx11effectgroupgettechniquebyname-method"></a>ID3DX11EffectGroup::GetTechniqueByName-Methode

Abrufen einer Technik anhand des Namens.

## <a name="syntax"></a>Syntax


```C++
ID3DX11EffectTechnique* GetTechniqueByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Name* 
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Der Name der Technik.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***

Ein Zeiger auf eine [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)oder **NULL,** wenn die Technik nicht gefunden wird.

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

[ID3DX11EffectGroup](id3dx11effectgroup.md)
</dt> </dl>

 

