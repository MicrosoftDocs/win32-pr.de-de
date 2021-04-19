---
description: Eine Anwendung verwendet die Methoden dieser Schnittstelle zum Implementieren eines Keyframe-Animations Satzes, der in einem komprimierten Datenformat gespeichert ist.
ms.assetid: 858f09b7-c3b6-4e22-8017-ce2d6188ba80
title: ID3DXCompressedAnimationSet-Schnittstelle (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXCompressedAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 33dd1017859be14924d8d40265696cfb552754ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363980"
---
# <a name="id3dxcompressedanimationset-interface"></a>ID3DXCompressedAnimationSet-Schnittstelle

Eine Anwendung verwendet die Methoden dieser Schnittstelle zum Implementieren eines Keyframe-Animations Satzes, der in einem komprimierten Datenformat gespeichert ist.

## <a name="members"></a>Member

Die **ID3DXCompressedAnimationSet** -Schnittstelle erbt von [**ID3DXAnimationSet**](id3dxanimationset.md). **ID3DXCompressedAnimationSet** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXCompressedAnimationSet** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                  | BESCHREIBUNG                                                                      |
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**Getcallbackkeys**](id3dxcompressedanimationset--getcallbackkeys.md)                 | Füllt ein Array mit Rückruf Schlüsseldaten, die für die Keyframe-Animation verwendet werden.<br/>   |
| [**Getcompresseddata**](id3dxcompressedanimationset--getcompresseddata.md)             | Ruft den Datenpuffer ab, in dem komprimierte Keyframe-Animationsdaten gespeichert werden.<br/> |
| [**Getnumcallbackkeys**](id3dxcompressedanimationset--getnumcallbackkeys.md)           | Ruft die Anzahl der Rückruf Schlüssel im Animations Satz ab.<br/>                |
| [**Getplaybacktype**](id3dxcompressedanimationset--getplaybacktype.md)                 | Ruft den Typ der Wiedergabe Schleife für Animations Sätze ab.<br/>                     |
| [**Getsourcetickspersecond**](id3dxcompressedanimationset--getsourcetickspersecond.md) | Ruft die Anzahl der pro Sekunde auftretenden Animations Tastatur-Frame Ticks ab.<br/>   |



 

## <a name="remarks"></a>Bemerkungen

Erstellen Sie mit [**D3DXCreateCompressedAnimationSet**](d3dxcreatecompressedanimationset.md)einen Keyframe-Animations Satz mit komprimiertem Format.

Der LPD3DXCOMPRESSEDANIMATIONSET-Typ wird als Zeiger auf diese Schnittstelle definiert.


```
typedef interface ID3DXCompressedAnimationSet ID3DXCompressedAnimationSet;
typedef interface ID3DXCompressedAnimationSet *LPD3DXCOMPRESSEDANIMATIONSET;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID3DXAnimationSet**](id3dxanimationset.md)
</dt> <dt>

[D3DX-Schnittstellen](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 




