---
description: In diesem Thema werden die Richtlinien beschrieben, die Sie beim Ausführen von asynchronen Windows Update-Agent (WUA)-Vorgängen befolgen sollten.
ms.assetid: 1fb16904-732d-4341-8267-ab8896fc0f7c
title: Richtlinien für asynchrone WUA-Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1a4b2198a235d9a03e3730e5d6dce2cd54c0e1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347060"
---
# <a name="guidelines-for-asynchronous-wua-operations"></a>Richtlinien für asynchrone WUA-Vorgänge

In diesem Thema werden die Richtlinien beschrieben, die Sie beim Ausführen von asynchronen Windows Update-Agent (WUA)-Vorgängen befolgen sollten.

-   Die asynchronen WUA-Vorgänge garantieren keine bestimmte Beendigungs Geschwindigkeit. Die Beendigungs Zeit für einen asynchronen WUA-Vorgang kann je nach Computer Hardware, Betriebssystemversion und Netzwerkkonfiguration stark variieren. Wie bei anderen Windows-APIs mit Netzwerk Abhängigkeiten, die keinen Timeout Parameter oder eine dokumentierte Timeout Dauer enthalten, empfiehlt es sich, ihre eigenen Timeout Mechanismen zu implementieren, wenn Sie garantierte Antwortzeiten benötigen. Beispielsweise können Sie einen Arbeits Thread erstellen, der eine asynchrone WUA-Methode aufruft und ein Ereignis oder ein anderes Synchronisierungs Objekt festlegt, wenn der asynchrone WUA-Vorgang abgeschlossen ist. der Haupt Thread kann dann die [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) -oder [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) -Funktion verwenden, die es Ihnen ermöglicht, einen Timeout Wert anzugeben.
-   Wenn Sie das suchen, herunterladen, installieren oder Deinstallieren von Updates beenden, können Sie [**iupdatesearcher:: endsearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-endsearch), [**iupdatedowloader:: EndDownload**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader), [**iupdateinstaller:: endinstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-endinstall) und [**iupdateinstaller:: enduninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-enduninstall) von einem beliebigen Thread aus verwenden.
-   Wenn Sie eine Suche, den Download, die Installation oder die Deinstallation von Updates mit [**iupdatesearcher:: beginsearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch), [**iupdatedownloader:: BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload), [**iupdateinstaller:: begininstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall)und [**iupdateinstaller:: beginuninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall)starten, stellen Sie sicher, dass Sie ausreichende Zugriffsberechtigungen behalten, wenn Sie Verweise auf WUA-API-Objekte freigeben.
    -   Stellen Sie sicher, dass auf alle im asynchronen Vorgang verwendeten Rückruf Objekte nicht verwiesen wird, bevor Sie sie zerstören. Warten Sie, bis der Verweis Zähler eines Rückruf Objekts zum ursprünglichen Wert zurückkehrt, bevor Sie ihn zerstören.
    -   Der Verweis auf das Auftrags Objekt, das von der entsprechenden **Begin** -Methode zurückgegeben wird, sollte von einem Objekt gesteuert werden, das sich von den Rückruf Objekten unterscheidet. Verwenden Sie ein Objekt, das von den Rückruf Objekten abweicht, um Zirkel Verweise zu vermeiden.
    -   Wenn Sie versuchen, den Verweis auf das Auftrags Objekt mithilfe eines Rückruf Objekts zu steuern, müssen Sie die [**idownloadjob:: Cleanup**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-cleanup)-, [**iinstallationjob:: Cleanup**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-cleanup)-oder [**isearchjob:: Cleanup**](/windows/desktop/api/Wuapi/nf-wuapi-isearchjob-cleanup) -Methode außerhalb der Callback-Funktion verwenden, um das Auftrags Objekt vom Rückruf Objekt zu trennen. Sie müssen dies tun, bevor Sie den Verweis auf das Auftrags Objekt freigeben, das von der **Begin** -Methode zurückgegeben wird.
-   Stellen Sie sicher, dass asynchrone WUA-Vorgänge beendet sind. Windows Script Host kann ein Skript beenden, wenn alle Befehle außerhalb einer beliebigen Funktion vollständig sind, auch wenn die WUA-API noch Verweise auf das Rückruf Objekt aufweist.
    -   Verwenden Sie eine der **Bereinigungs** Methoden, oder legen Sie fest, dass die Rückruffunktion beim Abschluss eine freigegebene globale Variable festgelegt hat
    -   Rufen Sie niemals [**idownloadjob:: Cleanup**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-cleanup), [**iinstallationjob:: Cleanup**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-cleanup)oder [**isearchjob:: Cleanup**](/windows/desktop/api/Wuapi/nf-wuapi-isearchjob-cleanup) für ein Auftrags Objekt in seiner Rückruffunktion auf.
    -   Um die richtige Bereinigungs Sequenz in einem Skript sicherzustellen, das unter Windows Internet Explorer ausgeführt wird, müssen Sie die **Cleanup** -Methode für alle Auftrags Objekte bei der Verarbeitung von "Window. onbeforeentladen" aufzurufen.
-   Verwenden Sie keine benutzerdefinierten Datentypen (User-Defined Data Types, UDT) für asynchrone WUA-Vorgänge. Der-Typ wird nicht von [**iupdatesearcher:: beginsearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch), [**iupdatedownloader:: BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload), [**iupdateinstaller:: begininstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall)oder [**iupdateinstaller:: beginuninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall)unterstützt.

 

 
