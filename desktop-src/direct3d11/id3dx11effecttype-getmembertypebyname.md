---
title: ID3DX11EffectType GetMemberTypeByName-Methode (D3dx11effect.h)
description: Hier erhalten Sie einen Membertyp nach Namen.
ms.assetid: 0c5a732b-7c3a-41da-b7de-dc464eed814a
keywords:
- GetMemberTypeByName-Methode Direct3D 11
- GetMemberTypeByName-Methode Direct3D 11, ID3DX11EffectType-Schnittstelle
- ID3DX11EffectType-Schnittstelle Direct3D 11 , GetMemberTypeByName-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberTypeByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b5988a987816ad7e5a1797d60619605228647c3dd81945b63bac9c74701bf77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460710"
---
# <a name="id3dx11effecttypegetmembertypebyname-method"></a>ID3DX11EffectType::GetMemberTypeByName-Methode

Hier erhalten Sie einen Membertyp nach Namen.

## <a name="syntax"></a>Syntax


```C++
ID3DX11EffectType* GetMemberTypeByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Name* 
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Der Name eines Mitglieds.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **ID3DX11EffectType**](id3dx11effecttype.md)\***

Ein Zeiger auf einen [**ID3DX11EffectType**](id3dx11effecttype.md).

## <a name="remarks"></a>Hinweise

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Quelle Effects 11 verwenden, um Ihre Effekttypanwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>Nicht verfügbar (eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX11EffectType](id3dx11effecttype.md)
</dt> </dl>

 

