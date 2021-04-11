---
description: Die Unterstützung von Telefongeräten ist ergänzend und nicht einfach, sodass Dienstanbieter keine Telefongeräte unterstützen müssen.
ms.assetid: 4d9f3b32-20d0-4550-9b3d-db97df8ea289
title: Telefongeräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f406442e43d8d4f31a89bfc0ccb1e59916d33e0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959102"
---
# <a name="phone-devices"></a>Telefongeräte

Die Unterstützung von Telefongeräten ist ergänzend und nicht einfach, sodass Dienstanbieter keine Telefongeräte unterstützen müssen.

Ebenso wie eine Line-Device-Klasse eine Abstraktion eines physischen Geräte Geräts ist, stellt die Phone-Geräteklasse eine geräteunabhängige Abstraktion eines Telefon Sets dar. TAPI behandelt Linien-und Telefongeräte als Geräte, die unabhängig voneinander sind. Anders ausgedrückt: Sie können ein Telefon (Gerät) verwenden, ohne eine zugehörige Zeile zu verwenden, und Sie können eine Linie (Gerät) ohne Telefon verwenden.

Dienstanbieter, die diese Unabhängigkeit vollständig implementieren, können für diese Geräte verwendet werden, die nicht durch herkömmliche Telefonieprotokolle definiert werden. Eine Person kann z. b. das Mobiltelefon des Desktops als Wellenform-Audiogerät für die Sprachaufzeichnung oder Wiedergabe verwenden, möglicherweise ohne das Wissen des Schalters, dass das Telefon verwendet wird. In einer solchen Implementierung muss bei der Aufhebung des lokalen Telefon Telefons nicht automatisch ein OFFHOOK-Signal an den Switch gesendet werden.

Diese Unabhängigkeit ermöglicht es einer Anwendung auch, das lokale Telefon auf eine Weise zu klingeln, die von eingehenden aufrufen unabhängig ist. Die Funktionen von Dienstanbietern sind durch die Funktionen der Hardware und Software beschränkt, die für die Verbindung zwischen dem Switch, dem Telefon und dem Computer verwendet werden.

TAPI umfasst Funktionen zum Abrufen von Gerätefunktionen, mit denen Clients ermitteln können, ob ein solches Verwendungs Modell unterstützt wird.

In diesem Abschnitt werden Telefongeräte beschrieben und erläutert, wie die TAPI-Telefonfunktionen für den Zugriff auf diese Geräte verwendet werden.

-   [Telefongerät](phone-device-elements.md)
-   [Initialisierung und Herunterfahren](initialization-and-shutdown.md)

 

 



