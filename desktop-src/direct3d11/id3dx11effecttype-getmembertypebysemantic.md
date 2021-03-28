---
title: ID3DX11EffectType getmembership typebysemantic-Methode (D3dx11effect. h)
description: Einen Elementtyp nach Semantik erhalten.
ms.assetid: d5fea2d9-8d08-4e02-a9c6-dbcfaaf4a7d1
keywords:
- Getmembership typebysemantic-Methode Direct3D 11
- Getmembership typebysemantic-Methode Direct3D 11, ID3DX11EffectType-Schnittstelle
- ID3DX11EffectType-Schnittstelle Direct3D 11, getmembership typebysemantic-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberTypeBySemantic
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de5f0894c83ff2d0885ae3b951e0e324343fae8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996187"
---
# <a name="id3dx11effecttypegetmembertypebysemantic-method"></a>ID3DX11EffectType:: getmembership typebysemantic-Methode

Einen Elementtyp nach Semantik erhalten.

## <a name="syntax"></a>Syntax


```C++
ID3DX11EffectType* GetMemberTypeBySemantic(
   LPCSTR Semantic
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Tischer* 
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Eine Semantik.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **ID3DX11EffectType**](id3dx11effecttype.md)\***

Ein Zeiger auf eine [**ID3DX11EffectType**](id3dx11effecttype.md).

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

[ID3DX11EffectType](id3dx11effecttype.md)
</dt> </dl>

 

