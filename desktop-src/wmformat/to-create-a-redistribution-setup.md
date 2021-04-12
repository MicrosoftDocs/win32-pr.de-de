---
title: So erstellen Sie eine weitergabeeinrichtung
description: So erstellen Sie eine weitergabeeinrichtung
ms.assetid: cf2c8fa1-cfd6-47cc-b572-ba1b95d59105
keywords:
- Windows Media-Format-SDK, Software Verteilung
- Advanced Systems Format (ASF), Software Verteilung
- ASF (Advanced Systems Format), Software Verteilung
- SDK für Windows Media-Format, Neuverteilung
- Advanced Systems Format (ASF), Verteilung
- ASF (Advanced Systems Format), Verteilung
- Software Verteilung, erstellen
- Software Verteilung, WMFDist.exe
- Verteilung, erstellen
- Neuverteilung, WMFDist.exe
- WMFDist.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70f0c2f241d8c1ad164bc14608103f423a7aba78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206689"
---
# <a name="to-create-a-redistribution-setup"></a>So erstellen Sie eine weitergabeeinrichtung

1.  Lassen Sie Ihre Anwendungs Dateien von der Setup Routine installieren, und nehmen Sie vor dem Aufrufen des Verteilungs Pakets die erforderlichen Einstellungen vor.
2.  Installieren Sie WMFDist.exe. Sie können das Flag "/Q: a" verwenden, um eine unbeaufsichtigte Installation durchzuführen und die Benutzeroberfläche der weitergabeeinrichtung während der Installation der Anwendung zu unterdrücken. Ihre Routine muss dann erkennen, ob ein Neustart am Ende erforderlich ist.

    Beispiel:

    ```C++
    WMFDist.exe /Q:A
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Software Verteilung**](software-redistribution.md)
</dt> </dl>

 

 




