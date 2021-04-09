---
description: Eine Anwendung, die als Standardbenutzer ausgeführt wird, führt Vorgänge aus, die Administratorrechte erfordern, indem ein Objekt mit Component Object Model erhöhten Rechten erstellt wird.
ms.assetid: 246fdf74-cc5b-47b1-b3a8-20441544e7be
title: COM-Objektmodell für Administratoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6c7d73cf31ce86c4788675374f34d04f6acf106
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867224"
---
# <a name="administrator-com-object-model"></a>COM-Objektmodell für Administratoren

Im COM-Objektmodell des Administrators führt eine Anwendung, die als Standardbenutzer ausgeführt wird, Vorgänge durch, die Administratorrechte erfordern, indem ein [Component Object Model](/windows/desktop/com/component-object-model--com--portal) Objekt mit erhöhten Rechten erstellt wird. Weitere Informationen zum Erstellen eines COM-Objekts mit erhöhten Rechten finden Sie [unter com-Erweiterungs Moniker](../com/the-com-elevation-moniker.md).

Ein Nachteil bei der Verwendung des com-Objektmodells für den Administrator ist, dass der Benutzer jedes Mal aufgefordert wird, wenn ein privilegierter Vorgang durchgeführt wird.

Jede Benutzeroberfläche, die das COM-Objekt steuern kann, muss vom COM-Objekt selbst dargestellt werden. Andernfalls könnte ein nicht privilegierter Prozess bewirken, dass das COM-Objekt mit erhöhten Berechtigungen privilegierte Vorgänge durchführt, ohne dass der Benutzer dazu aufgefordert wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwickeln von Anwendungen, für die Administrator Rechte erforderlich sind](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[Administrator Broker Modell](administrator-broker-model.md)
</dt> <dt>

[Modell mit erhöhten Rechten](elevated-task-model.md)
</dt> <dt>

[Betriebs System-Dienstmodell](operating-system-service-model.md)
</dt> </dl>

 

 
