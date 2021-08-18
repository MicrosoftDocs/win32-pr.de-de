---
title: Gemeinsame Nutzung der Internetverbindung
description: BITS kann eine DFÜ-Verbindung für Heimnetzwerke erzwingen, die die Microsoft-Internetverbindungsfreigabe verwenden, wenn die Verbindungsfreigabe so konfiguriert ist, dass sie auswählt, wenn Computer im Netzwerk auf das Internet zugreifen.
ms.assetid: a0a05ddb-6ce4-4cf5-8953-cb7122702d17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8736144b74d12666c4a364ac5b644ead35f8d1ec28aa03926bb7b691c8218f3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588620"
---
# <a name="internet-connection-sharing"></a>Gemeinsame Nutzung der Internetverbindung

BITS kann eine DFÜ-Verbindung für Heimnetzwerke erzwingen, die die Microsoft-Internetverbindungsfreigabe verwenden, wenn die Verbindungsfreigabe so konfiguriert ist, dass sie auswählt, wenn Computer im Netzwerk auf das Internet zugreifen. Um eine erzwungene DFÜ-Verbindung zu verhindern, deaktivieren Sie die Option **DFÜ-Verbindung** herstellen, wenn ein Computer in meinem Netzwerk versucht, auf das Internet auf dem Hostcomputer für die Verbindungsfreigabe zu zugreifen, der seine Internetverbindung gemeinsam verwendet.

Computer, die mit dem Hostcomputer für die Verbindungsfreigabe verbunden sind, gehen davon aus, dass sie über eine Netzwerkverbindung verfügen, sodass BITS versucht, Dateien zu übertragen. Wenn die DFÜ-Option auf dem Hostcomputer deaktiviert ist und der Hostcomputer keine aktive Verbindung hat, tritt bei den Übertragungen ein vorübergehender Fehler auf. BITS wird die Übertragungen in regelmäßigen Abständen wiederholen.

 

 




