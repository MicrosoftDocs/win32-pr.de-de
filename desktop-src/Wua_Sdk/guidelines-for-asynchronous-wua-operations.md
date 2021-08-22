---
description: In diesem Thema werden Richtlinien für die folgenden Vorgänge beschrieben, wenn Sie asynchrone WUA-Vorgänge (Windows Update Agent) ausführen.
ms.assetid: 1fb16904-732d-4341-8267-ab8896fc0f7c
title: Richtlinien für asynchrone WUA-Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24801c7639e75f34f1517ee626ff7acb7c1d13f85a6ebf57e7d824f7f0d3191d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049488"
---
# <a name="guidelines-for-asynchronous-wua-operations"></a>Richtlinien für asynchrone WUA-Vorgänge

In diesem Thema werden Richtlinien für die folgenden Vorgänge beschrieben, wenn Sie asynchrone WUA-Vorgänge (Windows Update Agent) ausführen.

-   Die asynchronen WUA-Vorgänge garantieren keine bestimmte Abschlussgeschwindigkeit. Die Abschlusszeit für einen asynchronen WUA-Vorgang kann je nach Computerhardware, Betriebssystemversion und Netzwerkkonfiguration stark variieren. Wie bei anderen Windows-APIs, die über Netzwerkabhängigkeiten verfügen und keinen Time out-Parameter oder eine dokumentierte Time out-Dauer enthalten, empfiehlt es sich, eigene Time out-Mechanismen zu implementieren, wenn Sie garantierte Antwortzeiten benötigen. Beispielsweise können Sie einen Arbeitsthread erstellen, der eine asynchrone WUA-Methode aufruft und ein Ereignis oder ein anderes Synchronisierungsobjekt festlegt, wenn der asynchrone WUA-Vorgang abgeschlossen ist. Der Hauptthread kann dann die Funktion [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) oder [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) verwenden, mit der Sie einen Time out-Wert angeben können.
-   Wenn Sie eine Suche, einen Download, eine Installation oder deinstallation von Updates beenden, können Sie [**IUpdateSearcher::EndSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-endsearch), [**IUpdateDowloader::EndDownload**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader), [**IUpdateInstaller::EndInstaller**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-endinstall) und [**IUpdateInstaller::EndUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-enduninstall) aus einem beliebigen Thread verwenden.
-   Wenn Sie mithilfe von [**IUpdateSearcher::BeginSearch,**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) [**IUpdateDownloader::BeginDownload,**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) [**IUpdateInstaller::BeginInstaller::BeginInstaller**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall)und [**IUpdateInstaller::BeginInstaller::BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall)eine Suche, einen Download, eine Installation oder Deinstallation von Updates starten, stellen Sie sicher, dass Sie ausreichende Zugriffsberechtigungen beibehalten, wenn Sie Verweise auf WUA-API-Objekte freigeben.
    -   Stellen Sie sicher, dass alle Rückrufobjekte, die im asynchronen Vorgang verwendet werden, nicht erkannt werden, bevor Sie sie zerstören. Warten Sie, bis der Verweiszähler eines Rückrufobjekts zum Anfangswert zurückkehrt, bevor Sie ihn zerstören.
    -   Der Verweis auf das Auftragsobjekt, das von der entsprechenden **Begin-Methode** zurückgegeben wird, sollte von einem -Objekt gesteuert werden, das sich von den Rückrufobjekten unterscheidet. Verwenden Sie ein Objekt, das sich von den Rückrufobjekten unterscheidet, um Zirkelverweise zu vermeiden.
    -   Wenn Sie versuchen, den Verweis auf das Auftragsobjekt mithilfe eines Rückrufobjekts zu steuern, müssen Sie die [**Methode IDownloadJob::CleanUp**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-cleanup), [**IInstallationJob::CleanUp**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-cleanup)oder [**ISearchJob::CleanUp**](/windows/desktop/api/Wuapi/nf-wuapi-isearchjob-cleanup) außerhalb der Rückruffunktion aufrufen, um das Auftragsobjekt vom Rückrufobjekt zu trennen. Sie müssen dies tun, bevor Sie den Verweis auf das Auftragsobjekt freigeben, das von der **Begin-Methode** zurückgegeben wird.
-   Stellen Sie sicher, dass asynchrone WUA-Vorgänge abgeschlossen sind. Windows Der Skripthost kann ein Skript beenden, wenn alle Befehle außerhalb einer Funktion abgeschlossen sind, auch wenn die WUA-API weiterhin Über Verweise auf das Rückrufobjekt verfügt.
    -   Verwenden Sie eine der **CleanUp-Methoden,** oder lassen Sie die Rückruffunktion nach Abschluss eine freigegebene globale Variable festlegen.
    -   Rufen Sie niemals [**IDownloadJob::CleanUp**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-cleanup), [**IInstallationJob::CleanUp**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-cleanup)oder [**ISearchJob::CleanUp**](/windows/desktop/api/Wuapi/nf-wuapi-isearchjob-cleanup) für ein Auftragsobjekt in seiner Rückruffunktion auf.
    -   Um die richtige Bereinigungssequenz in einem Skript sicherzustellen, das auf Windows Internet Explorer ausgeführt wird, rufen Sie die **CleanUp-Methode** für alle Auftragsobjekte auf, wenn Sie window.onbeforeunload verarbeiten.
-   Verwenden Sie keine benutzerdefinierten Datentypen (USER-Defined Data Types, UDT) für asynchrone WUA-Vorgänge. Der Typ wird von [**IUpdateSearcher::BeginSearch,**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) [**IUpdateDownloader::BeginDownload,**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) [**IUpdateInstaller::BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall)oder [**IUpdateInstaller::BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall)nicht unterstützt.

 

 
