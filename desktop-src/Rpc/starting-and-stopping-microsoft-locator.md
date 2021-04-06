---
title: Starten und Beenden von Microsoft Locator
description: Die RPC-Laufzeitbibliotheken starten Microsoft Locator bei Bedarf automatisch. Sie können den Locator manuell beenden und starten, wenn Sie z. b. die Datenbank beim Debuggen einer verteilten Anwendung löschen müssen.
ms.assetid: 06b50a9f-b640-45b2-86e2-2bcea6c16c5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 433ffdb11e86b06ee53d9b01f7f7755758538f22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036247"
---
# <a name="starting-and-stopping-microsoft-locator"></a>Starten und Beenden von Microsoft Locator

Die RPC-Laufzeitbibliotheken starten Microsoft Locator bei Bedarf automatisch. Sie können den Locator manuell beenden und starten, wenn Sie z. b. die Datenbank beim Debuggen einer verteilten Anwendung löschen müssen.

**So starten Sie den Microsoft-Locator und starten ihn**

1.  Klicken Sie in der Systemsteuerung auf das Symbol "Dienste".

    Das Dialogfeld **Dienste** wird angezeigt.

2.  Wählen Sie im Dialogfeld **Dienst** die Option **Microsoft Locator** aus, und klicken Sie dann auf **starten oder starten** .

Sie können den Microsoft-Locator auch über die Befehlszeile starten und Abbrechen, indem Sie Folgendes eingeben:

**NET \[ Start/-Vorgang zum Abbrechen von \] RpcLocator**

Nur ein Administrator kann den Microsoft-Locator starten, nachdem er beendet wurde. Wenn Sie beendet ist, wird Sie nach Bedarf von den RPC-Laufzeitbibliotheken neu gestartet.

 

 




