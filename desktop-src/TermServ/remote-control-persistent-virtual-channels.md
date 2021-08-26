---
title: Persistente virtuelle Kanäle für die Remotesteuerung
description: Ein persistenter virtueller Remotesteuerungskanal wird nicht geschlossen, wenn eine Remotesteuerung für die mit dem Client verbundene Sitzung eine Verbindung herstellt oder trennt. Daten werden weiterhin über diesen Kanal übertragen und empfangen.
ms.assetid: 0c3d5429-250e-4272-8cdd-69097acfaff4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71206b8272fb516da9a3c39bed7f7d54edbc5227958d975bf11b114db9c13869
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988780"
---
# <a name="remote-control-persistent-virtual-channels"></a>Persistente virtuelle Kanäle für die Remotesteuerung

Auf Windows XP kann eine DLL mindestens einen virtuellen Kanal als *persistente Remotesteuerung angeben.* Ein persistenter virtueller Remotesteuerungskanal wird nicht geschlossen, wenn eine Remotesteuerung für die mit dem Client verbundene Sitzung eine Verbindung herstellt oder trennt. Daten werden weiterhin über diesen Kanal übertragen und empfangen. Virtuelle Kanäle, die von der DLL nicht als persistente Remotesteuerung angegeben werden, werden in diesem Szenario geschlossen.

Persistente virtuelle Remotesteuerungskanäle werden während des Aufrufs von **VirtualChannelInit angegeben.** Spezifische Informationen hierzu finden Sie auf der Referenzseite für [**VirtualChannelInit.**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit)

 

 




