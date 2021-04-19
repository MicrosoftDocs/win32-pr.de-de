---
description: Wird verwendet, um Effekte festzulegen und abzufragen und um Techniken auszuwählen. Ein Effect-Objekt kann mehrere Techniken enthalten, um denselben Effekt zu erzeugen.
ms.assetid: bffc64ab-12e7-44e9-b296-262b0459a68a
title: ID3DXEffect-Schnittstelle (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 275376234739964940d70381a34331ff5b89f2dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354996"
---
# <a name="id3dxeffect-interface"></a>ID3DXEffect-Schnittstelle

Wird verwendet, um Effekte festzulegen und abzufragen und um Techniken auszuwählen. Ein Effect-Objekt kann mehrere Techniken enthalten, um denselben Effekt zu erzeugen.

## <a name="members"></a>Member

Die **ID3DXEffect** -Schnittstelle erbt von [**ID3DXBaseEffect**](id3dxbaseeffect.md). **ID3DXEffect** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXEffect** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                | BESCHREIBUNG                                                                                                                                                                                      |
|:----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Applyparameterblock**](id3dxeffect--applyparameterblock.md)       | Wenden Sie die Werte in einem Zustands Block auf den Systemstatus aktueller Effekt an.<br/>                                                                                                                 |
| [**Starten**](id3dxeffect--begin.md)                                   | Startet ein aktives Verfahren.<br/>                                                                                                                                                           |
| [**Beginparameterblock**](id3dxeffect--beginparameterblock.md)       | Starten Sie die Erfassung von Zustandsänderungen in einem Parameter Block.<br/>                                                                                                                                   |
| [**Beginpass**](id3dxeffect--beginpass.md)                           | Startet einen Durchlauf innerhalb der aktiven Technik.<br/>                                                                                                                                           |
| [**Cloneeffect**](id3dxeffect--cloneeffect.md)                       | Erstellt eine Kopie eines Effekts.<br/>                                                                                                                                                          |
| [**CommitChanges**](id3dxeffect--commitchanges.md)                   | Weitergeben von Zustandsänderungen, die innerhalb eines aktiven Durchlaufs an das Gerät erfolgen, vor dem Rendering.<br/>                                                                                           |
| [**Deleteparameterblock**](id3dxeffect--deleteparameterblock.md)     | Löschen Sie einen Parameter Block.<br/>                                                                                                                                                             |
| [**ENDE**](id3dxeffect--end.md)                                       | Beendet eine aktive Technik.<br/>                                                                                                                                                             |
| [**Endparameterblock**](id3dxeffect--endparameterblock.md)           | Beendet die Erfassung von Effekt-Parameter Zustandsänderungen.<br/>                                                                                                                                        |
| [**Endpass**](id3dxeffect--endpass.md)                               | Beenden eines aktiven Pass.<br/>                                                                                                                                                                   |
| [**Findnextvalidtechnique**](id3dxeffect--findnextvalidtechnique.md) | Sucht das nächste gültige Verfahren, beginnend bei der Technik nach der angegebenen Technik.<br/>                                                                                       |
| [**Getcurrenttechnique**](id3dxeffect--getcurrenttechnique.md)       | Ruft die aktuelle Technik ab.<br/>                                                                                                                                                           |
| [**GetDevice**](id3dxeffect--getdevice.md)                           | Ruft das Gerät ab, das dem Effekt zugeordnet ist.<br/>                                                                                                                                      |
| [**Getpool)**](id3dxeffect--getpool.md)                               | Ruft einen Zeiger auf den Pool von freigegebenen Parametern ab.<br/>                                                                                                                                      |
| [**GetStatus Manager**](id3dxeffect--getstatemanager.md)               | Holen Sie sich den Effekt Zustands-Manager.<br/>                                                                                                                                                         |
| [**Isparameterused**](id3dxeffect--isparameterused.md)               | Bestimmt, ob ein Parameter von der Technik verwendet wird.<br/>                                                                                                                                   |
| [**OnLostDevice**](id3dxeffect--onlostdevice.md)                     | Verwenden Sie diese Methode, um alle Verweise auf Videospeicher Ressourcen freizugeben und alle stateblocks zu löschen. Diese Methode sollte immer dann aufgerufen werden, wenn ein Gerät verloren geht oder ein Gerät zurückgesetzt wird.<br/> |
| [**OnResetDevice**](id3dxeffect--onresetdevice.md)                   | Verwenden Sie diese Methode, um Ressourcen erneut abzurufen und den Anfangszustand zu speichern.<br/>                                                                                                                       |
| [**"Strawvalue"**](id3dxeffect--setrawvalue.md)                       | Legen Sie einen zusammenhängenden Bereich von shaderkonstanten mit einer Speicher Kopie fest.<br/>                                                                                                                        |
| [**SetStatus Manager**](id3dxeffect--setstatemanager.md)               | Legen Sie den Effekt Zustands-Manager fest.<br/>                                                                                                                                                         |
| [**Settechnique**](id3dxeffect--settechnique.md)                     | Legt die aktive Technik fest.<br/>                                                                                                                                                            |
| [**Validatetechnique**](id3dxeffect--validatetechnique.md)           | Überprüfen Sie eine Technik.<br/>                                                                                                                                                                 |



 

## <a name="remarks"></a>Bemerkungen

Die ID3DXEffect-Schnittstelle wird durch Aufrufen von [**D3DXCreateEffect**](d3dxcreateeffect.md), [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md)oder [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md)abgerufen.

Der LPD3DXEFFECT-Typ wird als Zeiger auf diese Schnittstelle definiert.


```
typedef interface ID3DXEffect ID3DXEffect;
typedef interface ID3DXEffect *LPD3DXEFFECT;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID3DXBaseEffect**](id3dxbaseeffect.md)
</dt> <dt>

[Effekt Schnittstellen](dx9-graphics-reference-effects-interfaces.md)
</dt> <dt>

[**D3DXCreateEffect**](d3dxcreateeffect.md)
</dt> <dt>

[**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md)
</dt> <dt>

[**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md)
</dt> </dl>

 

 




