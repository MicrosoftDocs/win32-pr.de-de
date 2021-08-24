---
description: Wird verwendet, um Effekte festzulegen und abzufragen und Techniken auszuwählen. Ein Effektobjekt kann mehrere Techniken enthalten, um denselben Effekt zu rendern.
ms.assetid: bffc64ab-12e7-44e9-b296-262b0459a68a
title: ID3DXEffect-Schnittstelle (D3DX9Effect.h)
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
ms.openlocfilehash: c9f5bdcf90b3e0d317290a569984d1b72d248079de5b3b281325e66af6e443c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119494020"
---
# <a name="id3dxeffect-interface"></a>ID3DXEffect-Schnittstelle

Wird verwendet, um Effekte festzulegen und abzufragen und Techniken auszuwählen. Ein Effektobjekt kann mehrere Techniken enthalten, um denselben Effekt zu rendern.

## <a name="members"></a>Member

Die **ID3DXEffect-Schnittstelle** erbt von [**ID3DXBaseEffect.**](id3dxbaseeffect.md) **ID3DXEffect** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXEffect-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                | Beschreibung                                                                                                                                                                                      |
|:----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ApplyParameterBlock**](id3dxeffect--applyparameterblock.md)       | Wenden Sie die Werte in einem Zustandsblock auf den aktuellen Systemzustand der Auswirkung an.<br/>                                                                                                                 |
| [**Starten**](id3dxeffect--begin.md)                                   | Startet eine aktive Technik.<br/>                                                                                                                                                           |
| [**BeginParameterBlock**](id3dxeffect--beginparameterblock.md)       | Beginnen Sie mit der Erfassung von Zustandsänderungen in einem Parameterblock.<br/>                                                                                                                                   |
| [**BeginPass**](id3dxeffect--beginpass.md)                           | Startet einen Durchlauf innerhalb der aktiven Technik.<br/>                                                                                                                                           |
| [**CloneEffect**](id3dxeffect--cloneeffect.md)                       | Erstellt eine Kopie eines Effekts.<br/>                                                                                                                                                          |
| [**Commitchanges**](id3dxeffect--commitchanges.md)                   | Weitergeben von Zustandsänderungen, die innerhalb eines aktiven Durchlaufs an das Gerät auftreten, bevor das Rendering durchgeführt wird.<br/>                                                                                           |
| [**DeleteParameterBlock**](id3dxeffect--deleteparameterblock.md)     | Löscht einen Parameterblock.<br/>                                                                                                                                                             |
| [**Ende**](id3dxeffect--end.md)                                       | Beendet eine aktive Technik.<br/>                                                                                                                                                             |
| [**EndParameterBlock**](id3dxeffect--endparameterblock.md)           | Die Erfassung von Änderungen des Effektparameterzustands wird beendet.<br/>                                                                                                                                        |
| [**EndPass**](id3dxeffect--endpass.md)                               | Beenden Sie einen aktiven Durchlauf.<br/>                                                                                                                                                                   |
| [**FindNextValidTechnique**](id3dxeffect--findnextvalidtechnique.md) | Sucht nach der nächsten gültigen Technik, beginnend bei der Technik nach der angegebenen Technik.<br/>                                                                                       |
| [**GetCurrentTechnique**](id3dxeffect--getcurrenttechnique.md)       | Ruft die aktuelle Technik ab.<br/>                                                                                                                                                           |
| [**GetDevice**](id3dxeffect--getdevice.md)                           | Ruft das Gerät ab, das dem Effekt zugeordnet ist.<br/>                                                                                                                                      |
| [**GetPool**](id3dxeffect--getpool.md)                               | Ruft einen Zeiger auf den Pool der freigegebenen Parameter ab.<br/>                                                                                                                                      |
| [**GetStateManager**](id3dxeffect--getstatemanager.md)               | Abrufen des Zustands-Managers für den Effekt.<br/>                                                                                                                                                         |
| [**IsParameterUsed**](id3dxeffect--isparameterused.md)               | Bestimmt, ob ein Parameter von der Technik verwendet wird.<br/>                                                                                                                                   |
| [**OnLostDevice**](id3dxeffect--onlostdevice.md)                     | Verwenden Sie diese Methode, um alle Verweise auf Videospeicherressourcen freizugeben und alle Zustandsblöcke zu löschen. Diese Methode sollte immer dann aufgerufen werden, wenn ein Gerät verloren geht oder bevor ein Gerät zurückgesetzt wird.<br/> |
| [**OnResetDevice**](id3dxeffect--onresetdevice.md)                   | Verwenden Sie diese Methode, um Ressourcen erneut zu erhalten und den Anfangszustand zu speichern.<br/>                                                                                                                       |
| [**SetRawValue**](id3dxeffect--setrawvalue.md)                       | Legen Sie einen zusammenhängenden Bereich von Shaderkonstanten mit einer Speicherkopie fest.<br/>                                                                                                                        |
| [**SetStateManager**](id3dxeffect--setstatemanager.md)               | Legen Sie den Effektzustands-Manager fest.<br/>                                                                                                                                                         |
| [**SetTechnique**](id3dxeffect--settechnique.md)                     | Legt die aktive Technik fest.<br/>                                                                                                                                                            |
| [**ValidateTechnique**](id3dxeffect--validatetechnique.md)           | Überprüfen sie eine Technik.<br/>                                                                                                                                                                 |



 

## <a name="remarks"></a>Hinweise

Die ID3DXEffect-Schnittstelle wird durch Aufrufen von [**D3DXCreateEffect,**](d3dxcreateeffect.md) [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md)oder [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md)abgerufen.

Der LPD3DXEFFECT-Typ wird als Zeiger auf diese Schnittstelle definiert.


```
typedef interface ID3DXEffect ID3DXEffect;
typedef interface ID3DXEffect *LPD3DXEFFECT;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID3DXBaseEffect**](id3dxbaseeffect.md)
</dt> <dt>

[Effektschnittstellen](dx9-graphics-reference-effects-interfaces.md)
</dt> <dt>

[**D3DXCreateEffect**](d3dxcreateeffect.md)
</dt> <dt>

[**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md)
</dt> <dt>

[**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md)
</dt> </dl>

 

 




