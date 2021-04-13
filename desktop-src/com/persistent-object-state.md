---
title: Persistentes Objektstatus
description: Persistentes Objektstatus
ms.assetid: 731fef03-d204-48e7-b33a-801e97a9d2c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c08d4dd1175b5a7681f79fa9049772af245a031
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309531"
---
# <a name="persistent-object-state"></a>Persistentes Objektstatus

Einige COM-Objekte können Ihren internen Zustand speichern, wenn Sie von einem Client angefordert werden.

COM definiert Standards, über die Clients anfordern können, dass Objekte initialisiert, geladen und in und aus einem Datenspeicher (z. b. Flatfile, strukturierter Speicher oder Arbeitsspeicher) gespeichert werden. Der Client ist dafür verantwortlich, den Speicherort zu verwalten, an dem die persistenten Daten des Objekts gespeichert werden, aber nicht das Format der Daten. COM-Objekte, die diesen Standards entsprechen, werden als *persistente Objekte* bezeichnet.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Persistente Objekt Schnittstellen](persistent-object-interfaces.md)
-   [Initialisieren von persistenten Objekten](initializing-persistent-objects.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM-Clients und-Server](com-clients-and-servers.md)
</dt> </dl>

 

 




