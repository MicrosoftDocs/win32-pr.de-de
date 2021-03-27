---
title: ID3DX11Effect getgroupbyname-Methode (D3dx11effect. h)
description: Ruft eine Effekt Gruppe nach dem Namen ab.
ms.assetid: 14b4b484-848a-409c-9a99-207ab25b7566
keywords:
- Getgroupbyname-Methode Direct3D 11
- Getgroupbyname-Methode Direct3D 11, ID3DX11Effect-Schnittstelle
- ID3DX11Effect-Schnittstelle Direct3D 11, getgroupbyname-Methode
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetGroupByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1c2132dedb34fe71db30bf82b1c6d336f110a8f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996115"
---
# <a name="id3dx11effectgetgroupbyname-method"></a>ID3DX11Effect:: getgroupbyname-Methode

Ruft eine Effekt Gruppe nach dem Namen ab.

## <a name="syntax"></a>Syntax


```C++
ID3DX11EffectGroup* GetGroupByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Name* 
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Der Name der Effekt Gruppe.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **ID3DX11EffectGroup**](id3dx11effectgroup.md)\***

Ein Zeiger auf eine [**ID3DX11EffectGroup**](id3dx11effectgroup.md) -Schnittstelle.

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

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

