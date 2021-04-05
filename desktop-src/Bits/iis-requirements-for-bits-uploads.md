---
title: IIS-Anforderungen für BITS-Uploads
description: Für Uploads erfordert BITS IIS 6,0 unter Windows Server 2003 und IIS 7,0 unter Windows Server 2008; IIS 5,1 wird von Bits unter Windows XP nicht unterstützt.
ms.assetid: 8ab07af5-3b59-4c98-8e57-f614deb8b594
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8fc1eb9bae86e7bb2635b3a250e8a9efe1bc630
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708118"
---
# <a name="iis-requirements-for-bits-uploads"></a>IIS-Anforderungen für BITS-Uploads

Für Uploads erfordert BITS IIS 6,0 unter Windows Server 2003 und IIS 7,0 unter Windows Server 2008; IIS 5,1 wird von Bits unter Windows XP nicht unterstützt. Das virtuelle IIS-Verzeichnis muss für Uploads aktiviert sein, und die BITS-IIS-Erweiterungen müssen konfiguriert sein.

**Core-Installationen von Windows Server:** BITS-IIS-Erweiterungen werden nicht unterstützt.

Verwenden Sie unter Windows Server 2008 die **Server-Manager** , um das Feature für BITS-Server Erweiterungen zu installieren. Klicken Sie im linken Bereich von **Server-Manager** auf **Features** . Überprüfen Sie im **Assistenten zum Hinzufügen von Features** BITS-Server Erweiterungen. Beachten Sie, dass die IIS 6-Verwaltungs Kompatibilitäts Rollen installiert werden müssen.

Verwenden Sie unter Windows Server 2003 den **Assistenten für Windows-Komponenten** , um die BITS-Server Erweiterung zu installieren. Wählen Sie in der **Systemsteuerung** die Option **Programme hinzufügen oder entfernen** aus. Wählen Sie dann **Windows-Komponenten hinzufügen/entfernen** aus, um den **Assistenten für Windows-Komponenten** anzuzeigen. Die BITS-Server Erweiterung ist eine Unterkomponente von Internetinformationsdienste (IIS), bei der es sich um eine Unterkomponente des Webanwendungs Servers handelt.

> [!Note]  
> Wenn der IISAdmin-Dienst neu gestartet wird, muss der IIS-Arbeitsprozess wieder verwendet werden, bevor der BITS-Dienst Uploads fortsetzen kann. Der IIS-Arbeitsprozess kann mithilfe des Befehlszeilen-Hilfsprogramms **IISReset.exe** manuell wieder verwendet werden.

 

Weitere Informationen zum Konfigurieren von IIS für Uploads finden [Sie unter Einrichten des Servers für Uploads](setting-up-the-server-for-uploads.md).

Ausführliche Informationen zu den Eigenschaften, die von Bits zu IIS hinzugefügt werden, finden Sie unter [BITS-Server Einstellungen für Upload-Aufträge](bits-server-settings-for-upload-jobs.md).

 

 




