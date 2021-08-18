---
description: Die Ws2-32.dll (und mehrschichtige Protokolle) rufen WSPCleanup einmal für jeden Aufruf von \_ WSPStartup auf.
ms.assetid: c3b7b648-5727-47d6-9ddc-9d9f6511949d
title: Cleanup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aefac8f58b7d6eed0380b7aa0e7759ff07e5af2a2762cde7d8e9bab445ca1fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741434"
---
# <a name="cleanup"></a>Cleanup

Die Ws2-32.dll (und mehrschichtige Protokolle) rufen WSPCleanup einmal für jeden Aufruf von \_ [**WSPStartup auf.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) [](/previous-versions/windows/hardware/network/ff566270(v=vs.85)) Bei jedem Aufruf sollte **WSPCleanup** einen Prozessspezifischen Verweiszähler dekrementieren, und wenn der Leistungsindikator null erreicht, muss sich der Dienstanbieter darauf vorbereiten, aus dem Arbeitsspeicher entladen zu werden. Die erste Ordnung besteht in der Übermittlung nicht zu sendender Daten auf Sockets, die für einen ordnungsgemäßen Abschluss konfiguriert sind. Danach müssen alle vom Anbieter gespeicherten Ressourcen frei werden. Der Dienstanbieter muss in einem Zustand bleiben, in dem er sofort durch einen Aufruf von **WSPStartup erneut initialisiert werden kann.**

 

 
