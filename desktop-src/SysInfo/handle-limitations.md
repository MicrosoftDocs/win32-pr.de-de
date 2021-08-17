---
description: Einige Objekte unterstützen jeweils nur ein Handle.
ms.assetid: 3eafd0e0-3923-4489-8a0a-63007dd3183a
title: Behandeln von Einschränkungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f194ed8464d2731c15e9b88ae62549f9fa090928c14cf7dc66e139944863b72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764408"
---
# <a name="handle-limitations"></a>Behandeln von Einschränkungen

Einige Objekte unterstützen jeweils nur ein Handle. Das System stellt das Handle bereit, wenn eine Anwendung das -Objekt erstellt, und macht das Handle ungültig, wenn die Anwendung das Objekt zerstört. Andere Objekte unterstützen mehrere Handles für ein einzelnes Objekt. Das Betriebssystem entfernt das Objekt automatisch aus dem Arbeitsspeicher, nachdem das letzte Handle für das Objekt geschlossen wurde.

Die Gesamtanzahl der geöffneten Handles im System wird nur durch die Menge des verfügbaren Arbeitsspeichers beschränkt. Einige Objekttypen unterstützen eine begrenzte Anzahl von Handles pro Sitzung oder pro Prozess.

 

 



