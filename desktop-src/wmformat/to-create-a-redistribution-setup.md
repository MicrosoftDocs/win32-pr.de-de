---
title: So erstellen Sie ein Neuverteilungssetup
description: So erstellen Sie ein Neuverteilungssetup
ms.assetid: cf2c8fa1-cfd6-47cc-b572-ba1b95d59105
keywords:
- Windows Medienformat-SDK, Softwareverteilung
- Advanced Systems Format (ASF), Softwareverteilung
- ASF (Advanced Systems Format), Softwareverteilung
- Windows Medienformat-SDK, Neuverteilung
- Advanced Systems Format (ASF), Redistribution
- ASF (Advanced Systems Format), Redistribution
- Softwareverteilung, Erstellen
- Softwareverteilung, WMFDist.exe
- redistribution,creating
- Redistribution,WMFDist.exe
- WMFDist.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bb26b63a2379a72e2d97df876d91d8c57a6da9249c4e40525e81edacaf86542
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027298"
---
# <a name="to-create-a-redistribution-setup"></a>So erstellen Sie ein Neuverteilungssetup

1.  Lassen Sie ihre Setuproutine die Anwendungsdateien installieren und die erforderlichen Einstellungen vornehmen, bevor Sie das Weiterverteilungspaket aufrufen.
2.  Installieren Sie WMFDist.exe. Sie können das /Q:A-Flag verwenden, um eine stille, unbeaufsichtigte Installation zu durchführen und die Benutzeroberfläche des Verteilungssetups während der Installation Ihrer Anwendung zu unterdrücken. Ihre Routine muss dann erkennen, ob am Ende ein Neustart erforderlich ist.

    Beispiel:

    ```C++
    WMFDist.exe /Q:A
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Softwareverteilung**](software-redistribution.md)
</dt> </dl>

 

 




