---
title: Vollständige und teilweise gebundene Handles
description: Wenn Sie dynamische Endpunkte verwenden, erhalten die Laufzeitbibliotheken Endpunkt Informationen, die Sie benötigen.
ms.assetid: 13f2f783-2c10-4122-ba4d-a97b9c0378c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc1f434ec53ebcfd992b0090ed9066dce2ec627
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471324"
---
# <a name="fully-and-partially-bound-handles"></a>Vollständige und teilweise gebundene Handles

Wenn Sie dynamische Endpunkte verwenden, erhalten die Laufzeitbibliotheken Endpunkt Informationen, die Sie benötigen. Die-Laufzeitbibliotheken unterscheiden zwischen einem *vollständig gebundenen handle* (eines mit Endpunkt Informationen) und einem *teilweise gebundenen handle* (eines, das keine Endpunkt Informationen enthält).

Die Client Lauf Zeit Bibliothek muss das teilweise gebundene Handle in ein vollständig gebundenes handle konvertieren, bevor der Client an den Server gebunden werden kann. Die Client Lauf Zeit Bibliothek versucht, das teilweise gebundene Handle für die Client Anwendung zu konvertieren, indem die Endpunkt Informationen wie gezeigt erhalten werden:

-   Aus der Schnittstellen Spezifikation des Clients
-   Von einem Endpunkt Zuordnungsdienst, der auf dem Server ausgeführt wird

Wenn der Client versucht, ein teilweise gebundenes Handle zu verwenden, wenn die Endpunkt Informationen in der Schnittstellen Spezifikation nicht verfügbar sind und der Endpunkt-Mapper des Servers keine Informationen zum Server Endpunkt hat, verfügt der Client nicht über genügend Informationen, um den Remote Prozedur aufzurufen, und dieser Rückruf schlägt fehl. Um dies zu verhindern, müssen Sie den Endpunkt in der Endpunkt Zuordnung registrieren, wenn die verteilte Anwendung teilweise gebundene Handles verwendet. Weitere Informationen zum Endpunkt Mapper finden Sie unter [angeben dynamischer Endpunkte](specifying-endpoints.md).

Wenn ein Remote Prozedur Rückruf fehlschlägt, kann die Client Anwendung [**rpcbindingreset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset) abrufen, um veraltete Endpunkt Informationen zu entfernen. Wenn der Client versucht, die Remote Prozedur aufzurufen, versucht die Client Lauf Zeit Bibliothek erneut, das vollständig gebundene Handle in ein teilweise gebundenes Handle zu konvertieren. Dies ist hilfreich, wenn der Server mit einem anderen dynamischen Endpunkt beendet und neu gestartet wurde.

 

 




