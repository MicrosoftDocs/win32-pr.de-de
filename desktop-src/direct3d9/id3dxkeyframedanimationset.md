---
description: Eine Anwendung verwendet die Methoden dieser Schnittstelle, um einen Keyframe-Animations Satz zu implementieren.
ms.assetid: eeb7acd8-1017-4aca-9813-188fc6703837
title: ID3DXKeyframedAnimationSet-Schnittstelle (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0e45ab69b3a91461c947ce9c8a63885bb5ab0a8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106360232"
---
# <a name="id3dxkeyframedanimationset-interface"></a>ID3DXKeyframedAnimationSet-Schnittstelle

Eine Anwendung verwendet die Methoden dieser Schnittstelle, um einen Keyframe-Animations Satz zu implementieren.

## <a name="members"></a>Member

Die **ID3DXKeyframedAnimationSet** -Schnittstelle erbt von [**ID3DXAnimationSet**](id3dxanimationset.md). **ID3DXKeyframedAnimationSet** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXKeyframedAnimationSet** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                   | BESCHREIBUNG                                                                                                                                        |
|:-----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Komprimieren**](id3dxkeyframedanimationset--compress.md)                                 | Wandelt Animationen in einem Animations Satz in ein komprimiertes Format um und gibt einen Zeiger auf den Puffer zurück, in dem die komprimierten Daten gespeichert werden.<br/> |
| [**Getcallbackkey**](id3dxkeyframedanimationset--getcallbackkey.md)                     | Ruft Informationen zu einem bestimmten Rückruf im Animations Satz ab.<br/>                                                                        |
| [**Getcallbackkeys**](id3dxkeyframedanimationset--getcallbackkeys.md)                   | Füllt ein Array mit Rückruf Schlüsseldaten, die für die Keyframe-Animation verwendet werden.<br/>                                                                     |
| [**Getnumcallbackkeys**](id3dxkeyframedanimationset--getnumcallbackkeys.md)             | Ruft die Anzahl der Rückruf Schlüssel im Animations Satz ab.<br/>                                                                                  |
| [**Getnumrotationkeys**](id3dxkeyframedanimationset--getnumrotationkeys.md)             | Ruft die Anzahl von Rotations Schlüsseln in der angegebenen Keyframe-Animation ab.<br/>                                                                  |
| [**Getnumscalekeys**](id3dxkeyframedanimationset--getnumscalekeys.md)                   | Ruft die Anzahl der Skalierungs Schlüssel in der angegebenen Keyframe-Animation ab.<br/>                                                                     |
| [**Getnumtranslationkeys**](id3dxkeyframedanimationset--getnumtranslationkeys.md)       | Ruft die Anzahl der Übersetzungsschlüssel in der angegebenen Keyframe-Animation ab.<br/>                                                               |
| [**Getplaybacktype**](id3dxkeyframedanimationset--getplaybacktype.md)                   | Ruft den Typ der Wiedergabe Schleife für Animations Sätze ab.<br/>                                                                                       |
| [**Getrotationkey**](id3dxkeyframedanimationset--getrotationkey.md)                     | Sie erhalten die Rotations Informationen für einen bestimmten Keyframe im Animations Satz.<br/>                                                                 |
| [**Getrotationkeys**](id3dxkeyframedanimationset--getrotationkeys.md)                   | Füllt ein Array mit rotierenden Schlüsseldaten, die für die Keyframe-Animation verwendet werden.<br/>                                                                   |
| [**Getscalekey**](id3dxkeyframedanimationset--getscalekey.md)                           | Skalierungsinformationen für einen bestimmten Keyframe im Animations Satz erhalten.<br/>                                                                    |
| [**Getscalekeys**](id3dxkeyframedanimationset--getscalekeys.md)                         | Füllt ein Array mit Skalierungs Schlüsseldaten, die für die Keyframe-Animation verwendet werden.<br/>                                                                        |
| [**Getsourcetickspersecond**](id3dxkeyframedanimationset--getsourcetickspersecond.md)   | Ruft die Anzahl der pro Sekunde auftretenden Animations Tastatur-Frame Ticks ab.<br/>                                                                     |
| [**Gettranslationkey**](id3dxkeyframedanimationset--gettranslationkey.md)               | Sie erhalten Übersetzungs Informationen für einen bestimmten Keyframe im Animations Satz.<br/>                                                              |
| [**Gettranslationkeys**](id3dxkeyframedanimationset--gettranslationkeys.md)             | Füllt ein Array mit Translational Key-Daten, die für die Keyframe-Animation verwendet werden.<br/>                                                                |
| [**Registeranimationsrtkeys**](id3dxkeyframedanimationset--registeranimationsrtkeys.md) | Registrieren der schlüsselrahmen Daten für die Skalierung, Drehung und Übersetzung (SRT) für eine Animation.<br/>                                                        |
| [**Setcallbackkey**](id3dxkeyframedanimationset--setcallbackkey.md)                     | Legt Informationen zu einem bestimmten Rückruf im Animations Satz fest.<br/>                                                                        |
| [**"".**](id3dxkeyframedanimationset--setrotationkey.md)                     | Legen Sie die Rotations Informationen für einen bestimmten Keyframe im Animations Satz fest.<br/>                                                                 |
| [**Setscalekey**](id3dxkeyframedanimationset--setscalekey.md)                           | Legen Sie Skalierungsinformationen für einen bestimmten Keyframe im Animations Satz fest.<br/>                                                                    |
| [**Settranslationkey**](id3dxkeyframedanimationset--settranslationkey.md)               | Legen Sie Übersetzungs Informationen für einen bestimmten Keyframe im Animations Satz fest.<br/>                                                              |
| [**Unregisteranimation**](id3dxkeyframedanimationset--unregisteranimation.md)           | Entfernen Sie die Animationsdaten aus dem Animations Satz.<br/>                                                                                       |
| [**Unregisterrotationkey**](id3dxkeyframedanimationset--unregisterrotationkey.md)       | Entfernt die Rotationsdaten am angegebenen Keyframe.<br/>                                                                                   |
| [**Unregisterscalekey**](id3dxkeyframedanimationset--unregisterscalekey.md)             | Entfernt die Skalierungs Daten am angegebenen Keyframe.<br/>                                                                                      |
| [**Unregistertranslationkey**](id3dxkeyframedanimationset--unregistertranslationkey.md) | Entfernt die Übersetzungs Daten am angegebenen Keyframe.<br/>                                                                                |



 

## <a name="remarks"></a>Bemerkungen

Erstellen Sie einen keyframed-Animations Satz mit [**D3DXCreateKeyframedAnimationSet**](d3dxcreatekeyframedanimationset.md).

Der LPD3DXKEYFRAMEDANIMATIONSET-Typ wird als Zeiger auf diese Schnittstelle definiert.


```
typedef interface ID3DXKeyframedAnimationSet ID3DXKeyframedAnimationSet;
typedef interface ID3DXKeyframedAnimationSet *LPD3DXKEYFRAMEDANIMATIONSET;
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

 

 




