---
description: Apps können die Druckertreiberisolation in ihrem App-Manifest deklarieren, um die App vom Druckertreiber zu isolieren und die Zuverlässigkeit der Apps zu verbessern.
ms.assetid: 80650C46-AC96-46FD-894A-4F34B056AB79
ms.topic: article
title: 'How To: Verwenden der Anwendungsisolation'
ms.date: 05/31/2018
ms.openlocfilehash: 818ba30e7b294c695b2f67bb9bccc485959db43818bb95aedaa67cafc26d3559
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118233830"
---
# <a name="how-to-use-application-isolation"></a>How To: Verwenden der Anwendungsisolation

Apps können die Druckertreiberisolation in ihrem App-Manifest deklarieren, um die App vom Druckertreiber zu isolieren und die Zuverlässigkeit der App zu verbessern. Mit Windows Druckdienst können Druckertreiber in Prozessen ausgeführt werden, die von dem Prozess getrennt sind, in dem der Druckspooler ausgeführt wird. Wenn Sie dieses Feature verwenden, verhindert Ihre App, dass sie abstürzt, wenn der Druckertreiber einen Fehler hat.

Die Druckertreiberisolation ist in Windows 7 und Windows Server 2008 R2 implementiert.

### <a name="prerequisites"></a>Voraussetzungen

-   Eine verwaltete Code- oder Windows Store-App, die Windows verwendet.

## <a name="instructions"></a>Anweisungen

### <a name="update-the-app-manifest"></a>Aktualisieren des App-Manifests

Zum Aktivieren der Druckertreiberisolation müssen Sie das **PrinterDriverIsolation-Element** zum Manifest der App hinzufügen. Dazu gehen Sie wie folgt vor:

1.  Bearbeiten Sie das App-Manifest, und fügen Sie dem **windowsSettings-Element** des  Anwendungselements das **PrinterDriverIsolation-Element** mit dem Wert **true** hinzu, wie in diesem Beispiel gezeigt.
    ```XML
    <application xmlns="urn:schemas-microsoft-com:asm.v3">
        <windowsSettings>
            <printerDriverIsolation xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">true</printerDriverIsolation>
        </windowsSettings>
    </application>
    ```

    

2.  Erstellen Sie Ihre App neu.

 

 



