---
description: Apps können die Druckertreiber Isolation in Ihrem App-Manifest deklarieren, um die APP vom Druckertreiber zu isolieren und die Zuverlässigkeit der apps zu verbessern.
ms.assetid: 80650C46-AC96-46FD-894A-4F34B056AB79
ms.topic: article
title: 'Gewusst wie: Verwenden der Anwendungs Isolation'
ms.date: 05/31/2018
ms.openlocfilehash: 28c2a143406e9501662e0ddf7294abfb25e362b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215965"
---
# <a name="how-to-use-application-isolation"></a>Gewusst wie: Verwenden der Anwendungs Isolation

Apps können die Druckertreiber Isolation in Ihrem App-Manifest deklarieren, um die APP vom Druckertreiber zu isolieren und die Zuverlässigkeit der APP zu verbessern. Der Windows-Druckdienst ermöglicht die Ausführung von Druckertreibern in Prozessen, die von dem Prozess getrennt sind, in dem der Druck Spooler ausgeführt wird. Wenn Sie diese Funktion verwenden, verhindert Ihre APP, dass Sie abstürzt, wenn der Druckertreiber einen Fehler aufweist.

Die Druckertreiber Isolation ist in Windows 7 und Windows Server 2008 R2 implementiert.

### <a name="prerequisites"></a>Voraussetzungen

-   Eine verwaltete Code-oder Windows Store-App, die die Druckfunktion von Windows verwendet.

## <a name="instructions"></a>Anweisungen

### <a name="update-the-app-manifest"></a>Aktualisieren des App-Manifests

Wenn Sie die Druckertreiber Isolation aktivieren, müssen Sie das **printerdriverisolation** -Element dem App-Manifest hinzufügen. Gehen Sie dazu wie folgt vor:

1.  Bearbeiten Sie das App-Manifest, und fügen Sie das **printerdriverisolation** -Element mit dem Wert **true** zum **Windows Settings** -Element des **Application** -Elements hinzu, wie in diesem Beispiel gezeigt.
    ```XML
    <application xmlns="urn:schemas-microsoft-com:asm.v3">
        <windowsSettings>
            <printerDriverIsolation xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">true</printerDriverIsolation>
        </windowsSettings>
    </application>
    ```

    

2.  Erstellen Sie die APP neu.

 

 



