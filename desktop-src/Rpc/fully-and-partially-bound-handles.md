---
title: Vollständig und teilweise gebundene Handles
description: Wenn Sie dynamische Endpunkte verwenden, rufen die Laufzeitbibliotheken Endpunktinformationen nach Bedarf ab.
ms.assetid: 13f2f783-2c10-4122-ba4d-a97b9c0378c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f711955cedfba4359b910271f3ec5d77f4b383017eed8144e5201bb2d11cd3e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929648"
---
# <a name="fully-and-partially-bound-handles"></a>Vollständig und teilweise gebundene Handles

Wenn Sie dynamische Endpunkte verwenden, rufen die Laufzeitbibliotheken Endpunktinformationen nach Bedarf ab. Die Laufzeitbibliotheken unterscheiden zwischen einem *vollständig gebundenen Handle* (ein Handle, das Endpunktinformationen enthält) und einem teilweise gebundenen Handle (ein *Handle,* das keine Endpunktinformationen enthält).

Die Clientlaufzeitbibliothek muss das teilweise gebundene Handle in ein vollständig gebundenes Handle konvertieren, bevor der Client eine Bindung an den Server herstellen kann. Die Clientlaufzeitbibliothek versucht, das teilweise gebundene Handle für die Clientanwendung zu konvertieren, indem sie die Endpunktinformationen wie gezeigt erhält:

-   Aus der Schnittstellenspezifikation des Clients
-   Aus einem Endpunktzuordnungsdienst, der auf dem Server ausgeführt wird

Wenn der Client versucht, ein teilweise gebundenes Handle zu verwenden, wenn die Endpunktinformationen in der Schnittstellenspezifikation nicht verfügbar sind und die Endpunktzuordnung des Servers keine Informationen zum Serverendpunkt enthält, verfügt der Client nicht über genügend Informationen, um seinen Remoteprozeduraufruf durchzuführen, und dieser Aufruf schlägt fehl. Um dies zu verhindern, müssen Sie den Endpunkt in der Endpunktzuordnung registrieren, wenn Ihre verteilte Anwendung teilweise gebundene Handles verwendet. Weitere Informationen zur Endpunktzuordnung finden Sie unter [Angeben dynamischer Endpunkte.](specifying-endpoints.md)

Wenn ein Remoteprozeduraufruf fehlschlägt, kann die Clientanwendung [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset) aufrufen, um veraltete Endpunktinformationen zu entfernen. Wenn der Client versucht, die Remoteprozedur aufzurufen, versucht die Clientlaufzeitbibliothek erneut, das vollständig gebundene Handle in ein teilweise gebundenes Handle zu konvertieren. Dies ist nützlich, wenn der Server mithilfe eines anderen dynamischen Endpunkts beendet und neu gestartet wurde.

 

 




