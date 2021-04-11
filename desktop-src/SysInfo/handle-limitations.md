---
description: Einige Objekte unterstützen jeweils nur ein handle.
ms.assetid: 3eafd0e0-3923-4489-8a0a-63007dd3183a
title: Einschränkungen behandeln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99caa991b1ffa0a4e0c02ff32225c3260eb4a016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217983"
---
# <a name="handle-limitations"></a>Einschränkungen behandeln

Einige Objekte unterstützen jeweils nur ein handle. Das System stellt das Handle bereit, wenn eine Anwendung das Objekt erstellt, und macht das Handle ungültig, wenn die Anwendung das Objekt zerstört. Andere Objekte unterstützen mehrere Handles für ein einzelnes Objekt. Das Betriebssystem entfernt das-Objekt automatisch aus dem Arbeitsspeicher, nachdem das letzte Handle für das-Objekt geschlossen wurde.

Die Gesamtanzahl der geöffneten Handles im System wird nur durch die verfügbare Menge an Arbeitsspeicher beschränkt. Einige Objekttypen unterstützen eine begrenzte Anzahl von Handles pro Sitzung oder pro Prozess.

 

 



