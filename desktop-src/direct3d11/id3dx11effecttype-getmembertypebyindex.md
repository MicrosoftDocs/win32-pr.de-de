---
title: ID3DX11EffectType GetMemberTypeByIndex-Methode (D3dx11effect.h)
description: Abrufen eines Membertyps nach Index.
ms.assetid: 6421f08f-0236-4d8f-b3c2-ef7ec5ffe2a1
keywords:
- GetMemberTypeByIndex-Methode Direct3D 11
- GetMemberTypeByIndex-Methode Direct3D 11 , ID3DX11EffectType-Schnittstelle
- ID3DX11EffectType-Schnittstelle Direct3D 11 , GetMemberTypeByIndex-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberTypeByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53500ec94791ff534bf6b3c9a2e7d46a51b7b69bc889f35515e9b653c5bbb422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118532322"
---
# <a name="id3dx11effecttypegetmembertypebyindex-method"></a>ID3DX11EffectType::GetMemberTypeByIndex-Methode

Abrufen eines Membertyps nach Index.

## <a name="syntax"></a>Syntax


```C++
ID3DX11EffectType* GetMemberTypeByIndex(
   UINT Index
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Ein nullbasierter Index.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **ID3DX11EffectType**](id3dx11effecttype.md)\***

Ein Zeiger auf einen [**ID3DX11EffectType**](id3dx11effecttype.md).

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

[ID3DX11EffectType](id3dx11effecttype.md)
</dt> </dl>

 

