---
description: Telefon Geräteunterstützung ist eher ergänzend als einfach, sodass Dienstanbieter keine Telefongeräte unterstützen müssen.
ms.assetid: 4d9f3b32-20d0-4550-9b3d-db97df8ea289
title: Telefon Geräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d11aa269e17d74fbaf74c701c954ced734ef33900198a7c9e30a044f5ebd32e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873280"
---
# <a name="phone-devices"></a>Telefon Geräte

Telefon Geräteunterstützung ist eher ergänzend als einfach, sodass Dienstanbieter keine Telefongeräte unterstützen müssen.

So wie eine Geräteklasse eine Abstraktion eines physischen Liniengeräts ist, stellt die Geräteklasse phone eine geräteunabhängige Abstraktion eines Telefonsets dar. TAPI behandelt Zeilen- und Telefongeräte als Geräte, die voneinander unabhängig sind. Anders ausgedrückt: Sie können ein Telefon (Gerät) verwenden, ohne eine zugeordnete Zeile zu verwenden, und Sie können eine Zeile (gerät) verwenden, ohne ein Telefon zu verwenden.

Dienstanbieter, die diese Eigenständigkeit vollständig implementieren, können Verwendungsmöglichkeiten für diese Geräte anbieten, die nicht durch herkömmliche Telefonieprotokolle definiert sind. Beispielsweise kann eine Person das Mobiltelefon des Desktops als Waveform-Audiogerät für die Sprachaufzeichnung oder Wiedergabe verwenden, möglicherweise ohne das Wissen des Schalters, dass das Telefon verwendet wird. In einer solchen Implementierung muss das Heben des handsets des lokalen Telefons nicht automatisch ein Offhooksignal an den Switch senden.

Diese Unabhängigkeit ermöglicht es einer Anwendung auch, das lokale Telefon auf eine Weise zu anrufen, die unabhängig von eingehenden Anrufen ist. Die Funktionen von Dienstanbietern werden durch die Funktionen der Hardware und Software eingeschränkt, die zum Verbinden des Switches, des Telefons und des Computers verwendet werden.

TAPI enthält Funktionen zum Abrufen von Gerätefunktionen, mit denen Clients bestimmen können, ob ein solches Nutzungsmodell unterstützt wird.

In diesem Abschnitt werden Telefongeräte und die Verwendung der TAPI-Telefonfunktionen für den Zugriff auf diese Geräte beschrieben.

-   [Telefon Gerät](phone-device-elements.md)
-   [Initialisierung und Herunterfahren](initialization-and-shutdown.md)

 

 



