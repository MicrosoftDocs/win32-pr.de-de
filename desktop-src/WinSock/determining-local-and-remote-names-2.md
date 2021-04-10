---
description: Wspgetsockname wird verwendet, um die lokale Adresse für gebundene Sockets abzurufen.
ms.assetid: 5f3c9aa8-97fe-48a1-a3f5-156c9bddb1b2
title: Bestimmen von lokalen und Remote Namen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 265cf8013dcadaedbef786ab78f48e63de81a992
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041732"
---
# <a name="determining-local-and-remote-names"></a>Bestimmen von lokalen und Remote Namen

[**Wspgetsockname**](/previous-versions/windows/desktop/legacy/ms742280(v=vs.85)) wird verwendet, um die lokale Adresse für gebundene Sockets abzurufen. Dies ist besonders nützlich, wenn ein [**wspconnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) -Befehl ausgeführt wurde, ohne zuerst [**wspbind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85)) durchgeführt zu haben. **Wspgetsockname** stellt die einzige Möglichkeit dar, die lokale Zuordnung zu bestimmen, die vom Anbieter implizit festgelegt wurde.

Nachdem eine Verbindung eingerichtet wurde, kann [**wspgetpeername**](/previous-versions/windows/desktop/legacy/ms742278(v=vs.85)) verwendet werden, um die Adresse des Peers zu ermitteln, mit dem ein Socket verbunden ist.

 

 
