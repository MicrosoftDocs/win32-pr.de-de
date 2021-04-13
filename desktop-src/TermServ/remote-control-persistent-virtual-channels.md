---
title: Persistente virtuelle Kanäle für die Remote Steuerung
description: Ein persistenter virtueller Kanal für die Remote Steuerung wird nicht geschlossen, wenn eine Remote Steuerung die Verbindung mit dem Client herstellt oder die Verbindung trennt. Daten werden weiterhin über diesen Kanal übertragen und empfangen.
ms.assetid: 0c3d5429-250e-4272-8cdd-69097acfaff4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d87054a79863df5816b30fced648ab40251a80e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388694"
---
# <a name="remote-control-persistent-virtual-channels"></a>Persistente virtuelle Kanäle für die Remote Steuerung

Unter Windows XP kann eine DLL einen oder mehrere virtuelle Kanäle als *persistente Remote Steuerung* angeben. Ein persistenter virtueller Kanal für die Remote Steuerung wird nicht geschlossen, wenn eine Remote Steuerung die Verbindung mit dem Client herstellt oder die Verbindung trennt. Daten werden weiterhin über diesen Kanal übertragen und empfangen. Virtuelle Kanäle, die von der dll nicht als persistente Remote Steuerung angegeben werden, werden in diesem Szenario geschlossen.

Persistente virtuelle Kanäle für die Remote Steuerung werden während des Aufrufes von **virtualchannelinit** angegeben. Spezifische Informationen hierzu finden Sie auf der Referenzseite für [**virtualchannelinit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit) .

 

 




