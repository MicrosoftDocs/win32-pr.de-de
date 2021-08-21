---
title: PlayerApplication-Objekt
description: Das PlayerApplication-Objekt bietet eine Möglichkeit, den Wechsel zwischen einem remoten Windows Media Player-Steuerelement und dem vollständigen Modus des Windows Media Player.
ms.assetid: 904bb30c-939d-4aeb-ba4b-c27afee471ea
keywords:
- PlayerApplication-Windows Media Player
topic_type:
- apiref
api_name:
- PlayerApplication Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 46ac009ead54fc4d32b1a302f9228f84484ba6911b353ebb5443653378d9ce61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118571831"
---
# <a name="playerapplication-object"></a>PlayerApplication-Objekt

Das **PlayerApplication-Objekt** bietet eine Möglichkeit, den Wechsel zwischen einem remoten Windows Media Player-Steuerelement und dem vollständigen Modus des Windows Media Player. Dieses Objekt wird nur mit C++-Programmen verwendet, die die **IWMPRemoteMediaServices-Schnittstelle** implementieren und das Player-Steuerelement im Remotemodus einbetten. Skindateien, die als benutzerdefinierte Schnittstellen für den Remotecomputer verwendet werden Windows Media Player über das globale **Attribut playerApplication** den Zugriff auf dieses Objekt im Skriptcode steuern.

Das **PlayerApplication-Objekt** unterstützt die folgenden Eigenschaften.



| Eigenschaft                                           | Beschreibung                                                                                              |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [hasDisplay](playerapplication-hasdisplay.md)     | Ruft einen Wert ab, der angibt, ob Videos über das Remotesteuersteuer Windows Media Player werden können. |
| [playerDocked](playerapplication-playerdocked.md) | Ruft einen Wert ab, der angibt, Windows Media Player sich im angedockten Zustand befindet.                          |



 

Das **PlayerApplication-Objekt** unterstützt die folgenden Methoden.



| Methode                                                                       | Beschreibung                                                                     |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [switchToControl](playerapplication-switchtocontrol.md)                     | Schaltet ein Remotesteuer Windows Media Player-Steuerelement in den angedockten Zustand um.            |
| [switchToPlayerApplication](playerapplication-switchtoplayerapplication.md) | Schaltet ein Remotesteuerfeld Windows Media Player in den vollständigen Modus des Players um. |



 

Auf **das PlayerApplication-Objekt** wird über die folgende Eigenschaft zugegriffen.



| Object                      | Eigenschaft                                          |
|-----------------------------|---------------------------------------------------|
| [Player](player-object.md) | [playerApplication](player-playerapplication.md) |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Objektmodellreferenz für die Skripterstellung**](object-model-reference-for-scripting.md)
</dt> <dt>

[**Remoting des Windows Media Player-Steuerelements**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




