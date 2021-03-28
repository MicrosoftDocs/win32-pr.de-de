---
title: ID3DX11EffectVariable getmembership byname-Methode (D3dx11effect. h)
description: Einen Strukturmember anhand des Namens erhalten.
ms.assetid: 09f7f2f8-f55f-411c-8130-6ae44015d58a
keywords:
- Getmembership byname-Methode Direct3D 11
- Getmembership byname-Methode Direct3D 11, ID3DX11EffectVariable-Schnittstelle
- ID3DX11EffectVariable Interface Direct3D 11, getmembership byname-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetMemberByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9851a2f74502a79b5cc85c494e468c4a346798f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996282"
---
# <a name="id3dx11effectvariablegetmemberbyname-method"></a>ID3DX11EffectVariable:: getmembership byname-Methode

Einen Strukturmember anhand des Namens erhalten.

## <a name="syntax"></a>Syntax


```C++
ID3DX11EffectVariable* GetMemberByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Name* 
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Elementname.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Ein Zeiger auf eine [**ID3DX11EffectVariable**](id3dx11effectvariable.md).

## <a name="remarks"></a>Bemerkungen

Wenn die Effekt Variable eine Struktur ist, verwenden Sie diese Methode, um einen Member nach Namen zu suchen.

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen. Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

