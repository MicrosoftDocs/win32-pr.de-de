---
title: ID3DX11EffectGroup gettechniquebyname-Methode (D3dx11effect. h)
description: Holen Sie sich eine Technik anhand des Namens. | ID3DX11EffectGroup gettechniquebyname-Methode (D3dx11effect. h)
ms.assetid: 160c6d57-bec4-4718-8fad-fc9c0746736c
keywords:
- Gettechniquebyname-Methode Direct3D 11
- Gettechniquebyname-Methode Direct3D 11, ID3DX11EffectGroup-Schnittstelle
- ID3DX11EffectGroup-Schnittstelle Direct3D 11, gettechniquebyname-Methode
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
ms.openlocfilehash: c5121f67345ba863d773d8e7a73a5d6fa8b69895
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982293"
---
# <a name="id3dx11effectgroupgettechniquebyname-method"></a>ID3DX11EffectGroup:: gettechniquebyname-Methode

Holen Sie sich eine Technik anhand des Namens.

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

Ein Zeiger auf ein [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)-oder **null** -Wert, wenn die Technik nicht gefunden wurde.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen. Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX11EffectGroup](id3dx11effectgroup.md)
</dt> </dl>

 

