---
title: ID3DX11EffectType GetMemberName-Methode (D3dx11effect.h)
description: Abrufen des Namens eines Members.
ms.assetid: cd231741-09e1-4e69-9384-5cdfbf83fc8b
keywords:
- GetMemberName-Methode Direct3D 11
- GetMemberName-Methode Direct3D 11 , ID3DX11EffectType-Schnittstelle
- ID3DX11EffectType-Schnittstelle Direct3D 11 , GetMemberName-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db740b11e8da886d1c2b3339b1cdf64fa941dcb4947e9f399be8b49b2747bbe5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118532342"
---
# <a name="id3dx11effecttypegetmembername-method"></a>ID3DX11EffectType::GetMemberName-Methode

Abrufen des Namens eines Members.

## <a name="syntax"></a>Syntax


```C++
LPCSTR GetMemberName(
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

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Der Name des Members.

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

 

