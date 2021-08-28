---
title: Starten und Beenden des Microsoft-Locators
description: Die RPC-Laufzeitbibliotheken starten den Microsoft Locator bei Bedarf automatisch. Sie können den Locator manuell beenden und starten, wenn Sie z. B. die Datenbank beim Debuggen einer verteilten Anwendung löschen müssen.
ms.assetid: 06b50a9f-b640-45b2-86e2-2bcea6c16c5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e281419bc2a869d43863f946c1fcb172da2f86c04186ba775766233d4caa65c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017550"
---
# <a name="starting-and-stopping-microsoft-locator"></a>Starten und Beenden des Microsoft-Locators

Die RPC-Laufzeitbibliotheken starten den Microsoft Locator bei Bedarf automatisch. Sie können den Locator manuell beenden und starten, wenn Sie z. B. die Datenbank beim Debuggen einer verteilten Anwendung löschen müssen.

**So beenden und starten Sie den Microsoft Locator**

1.  Klicken Systemsteuerung auf das Symbol Dienste.

    Das **Dialogfeld Dienste** wird angezeigt.

2.  Wählen Sie **im Dialogfeld** Dienst die Option **Microsoft Locator** aus, und klicken Sie dann **auf Starten** oder **Beenden.**

Sie können den Microsoft Locator auch über die Befehlszeile starten und beenden, indem Sie Folgendes eingeben:

**net \[ start/stop \] rpclocator**

Nur ein Administrator kann den Microsoft-Locator starten, nachdem er beendet wurde. Wenn der Dienst beendet wird, wird er nach Bedarf von den RPC-Laufzeitbibliotheken neu gestartet.

 

 




