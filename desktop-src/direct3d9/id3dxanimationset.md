---
description: Diese Schnittstelle kapselt die Mindestfunktionalität, die von einem Animations Controller festgelegt wurde.
ms.assetid: vs|directx_sdk|~\id3dxanimationset.htm
title: ID3DXAnimationSet-Schnittstelle (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b5aa27494931e8b6c528627fa8e96278a6d86b05
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219697"
---
# <a name="id3dxanimationset-interface"></a>ID3DXAnimationSet-Schnittstelle

Diese Schnittstelle kapselt die Mindestfunktionalität, die von einem Animations Controller festgelegt wurde. Fortgeschrittene Benutzer möchten diese Schnittstelle möglicherweise selbst implementieren, um Ihren speziellen Anforderungen gerecht zu werden. für die meisten Benutzer sollten jedoch die abgeleiteten [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) -und [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) -Schnittstellen ausreichen.

## <a name="members"></a>Member

Die **ID3DXAnimationSet** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ID3DXAnimationSet** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXAnimationSet** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                        | BESCHREIBUNG                                                                       |
|:------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [**Getanimationindexbyname**](id3dxanimationset--getanimationindexbyname.md) | Ruft den Index einer Animation ab, wenn der Name angegeben wird.<br/>                        |
| [**Getanimationnamebyindex**](id3dxanimationset--getanimationnamebyindex.md) | Ruft den Namen einer Animation ab, wenn der Index angegeben wird.<br/>                        |
| [**GetCallback**](id3dxanimationset--getcallback.md)                         | Ruft Informationen zu einem bestimmten Rückruf im Animations Satz ab.<br/>       |
| [**GetName**](id3dxanimationset--getname.md)                                 | Ruft den Namen des Animations Satzes ab.<br/>                                           |
| [**Getnumanimations**](id3dxanimationset--getnumanimations.md)               | Ruft die Anzahl der Animationen im Animations Satz ab.<br/>                    |
| [**GetPeriod**](id3dxanimationset--getperiod.md)                             | Ruft den Zeitraum des Animations Satzes ab.<br/>                                  |
| [**GetPeriodicPosition**](id3dxanimationset--getperiodicposition.md)         | Gibt die Uhrzeit Position im lokalen Zeitrahmen eines Animations Satzes zurück.<br/>      |
| [**Gewahrheits RT**](id3dxanimationset--getsrt.md)                                   | Ruft die Skalierungs-, Drehungs-und Übersetzungs Werte des Animations Satzes ab.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Ein Animations Satz besteht aus Animationen für viele Knoten für dieselbe Animation.

Der LPD3DXANIMATIONSET-Typ wird als Zeiger auf diese Schnittstelle definiert.


```
typedef interface ID3DXAnimationSet ID3DXAnimationSet;
typedef interface ID3DXAnimationSet *LPD3DXANIMATIONSET;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Schnittstellen](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
