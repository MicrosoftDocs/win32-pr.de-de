---
title: Playerapplication-Objekt
description: Das playerapplication-Objekt bietet eine Möglichkeit, den Wechsel zwischen einem remoten Windows Media Player-Steuerelement und dem vollständigen Modus von Windows Media Player zu koordinieren.
ms.assetid: 904bb30c-939d-4aeb-ba4b-c27afee471ea
keywords:
- Playerapplication-Objekt Windows-Media Player
topic_type:
- apiref
api_name:
- PlayerApplication Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 950efeb0a84f43dec904b3ffd21f715061e50d4d
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "104313242"
---
# <a name="playerapplication-object"></a>Playerapplication-Objekt

Das **playerapplication** -Objekt bietet eine Möglichkeit, den Wechsel zwischen einem remoten Windows Media Player-Steuerelement und dem vollständigen Modus von Windows Media Player zu koordinieren. Dieses Objekt wird nur in C++-Programmen verwendet, die die **iwmpremotemediaservices** -Schnittstelle implementieren und das Player-Steuerelement in den Remote Modus einbetten. Skin-Dateien, die als benutzerdefinierte Schnittstellen für die Remote-Windows-Media Player Steuerung verwendet werden, greifen in Skriptcode über das globale Attribut **playerapplication** auf dieses Objekt zu

Das **playerapplication** -Objekt unterstützt die folgenden Eigenschaften.



| Eigenschaft                                           | BESCHREIBUNG                                                                                              |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [hasdisplay](playerapplication-hasdisplay.md)     | Ruft einen Wert ab, der angibt, ob Videos über das Remote Fenster Media Player-Steuerelement angezeigt werden können. |
| [playerdocked](playerapplication-playerdocked.md) | Ruft einen Wert ab, der angibt, ob sich Windows Media Player in einem angedockten Zustand befindet.                          |



 

Das **playerapplication** -Objekt unterstützt die folgenden Methoden.



| Methode                                                                       | BESCHREIBUNG                                                                     |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [SwitchTo-Control](playerapplication-switchtocontrol.md)                     | Schaltet ein Remotes Windows Media Player-Steuerelement in den angedockten Zustand.            |
| [switchtoplayerapplication](playerapplication-switchtoplayerapplication.md) | Schaltet ein Remotes Windows Media Player-Steuerelement in den vollständigen Modus des Players. |



 

Der Zugriff auf das **playerapplication** -Objekt erfolgt über die folgende Eigenschaft.



| Object                      | Eigenschaft                                          |
|-----------------------------|---------------------------------------------------|
| [Player](player-object.md) | [playerapplication](player-playerapplication.md) |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Objektmodell Referenz für die Skripterstellung**](object-model-reference-for-scripting.md)
</dt> <dt>

[**Remoting des Windows Media Player-Steuerelements**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




