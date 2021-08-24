---
title: ID3DX11EffectTechnique GetPassByIndex-Methode (D3dx11effect.h)
description: Abrufen eines Durchlaufs nach Index.
ms.assetid: 3c9452f5-c94a-4951-bdd2-e8891b7ceb34
keywords:
- GetPassByIndex-Methode Direct3D 11
- GetPassByIndex-Methode Direct3D 11 , ID3DX11EffectTechnique-Schnittstelle
- ID3DX11EffectTechnique-Schnittstelle Direct3D 11 , GetPassByIndex-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetPassByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efd22cd5e7745b8e5a11018b930f6b544036780b118e9c745b67e730b693cdd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565790"
---
# <a name="id3dx11effecttechniquegetpassbyindex-method"></a>ID3DX11EffectTechnique::GetPassByIndex-Methode

Abrufen eines Durchlaufs nach Index.

## <a name="syntax"></a>Syntax


```C++
ID3DX11EffectPass* GetPassByIndex(
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

Typ: **[ **ID3DX11EffectPass**](id3dx11effectpass.md)\***

Ein Zeiger auf einen [**ID3DX11EffectPass**](id3dx11effectpass.md).

## <a name="remarks"></a>Hinweise

Eine Technik enthält einen oder mehrere Durchläufe. Abrufen eines Durchlaufs mithilfe eines Namens oder Indexes.

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte zur Verfügung. Sie müssen die Effects 11-Quelle verwenden, um ihre Effekte-Typ-Anwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>N/A (Eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX11EffectTechnique](id3dx11effecttechnique.md)
</dt> </dl>

 

