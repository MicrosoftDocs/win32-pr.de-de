---
title: Starten, anhalten und Fortsetzen der Wiedergabe
description: Starten, anhalten und Fortsetzen der Wiedergabe
ms.assetid: 4af92781-5461-4195-82f5-a9213a9bdbd7
keywords:
- Mciwndplay-Makro
- Mciwndpause-Makro
- Mciwndresume-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 734a186b90b8d6701923d0ffa1f743cc8c5ae378
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207387"
---
# <a name="starting-pausing-and-resuming-playback"></a>Starten, anhalten und Fortsetzen der Wiedergabe

[**Mciwndplay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) ist das allgemeinste Wiedergabe Makro. Mit diesem Makro können Sie eine Datei oder ein Gerät von der aktuellen Wiedergabe Position wiedergeben. Die Wiedergabe wird über das Ende des Inhalts ausgeführt, es sei denn, Sie wird unterbrochen.

Sie können ein Gerät, das mit dem [**mciwndpause**](/windows/desktop/api/Vfw/nf-vfw-mciwndpause) -Makro abgespielt wird, vorübergehend unterbrechen. Um die Wiedergabe an der angehaltenen Position fortzusetzen, verwenden Sie das [**mciwndresume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) -Makro. Einige Geräte unterstützen nicht die Befehle zum Anhalten und fortsetzen. Diese Geräte ordnen **mciwndpause** normalerweise dem [**mciwndstopp**](/windows/desktop/api/Vfw/nf-vfw-mciwndstop) -Makro zu, das die Wiedergabe oder Aufzeichnung beendet. Sie können ein Gerät, das Anhalten oder fortsetzen nicht unterstützt, mithilfe von **mciwndplay** neu starten, wodurch die Wiedergabe von der aktuellen Wiedergabe Position aus gestartet wird.

 

 




