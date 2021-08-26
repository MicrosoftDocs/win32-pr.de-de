---
title: IIS-Anforderungen für BITS-Uploads
description: Für Uploads erfordert BITS IIS 6.0 auf Windows Server 2003 und IIS 7.0 auf Windows Server 2008. BITS unterstützt IIS 5.1 nicht auf Windows XP.
ms.assetid: 8ab07af5-3b59-4c98-8e57-f614deb8b594
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb09ec8c55cce592baf48b4b39faf031e5d6c98909927c0e597be6aaae8712e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004990"
---
# <a name="iis-requirements-for-bits-uploads"></a>IIS-Anforderungen für BITS-Uploads

Für Uploads erfordert BITS IIS 6.0 auf Windows Server 2003 und IIS 7.0 auf Windows Server 2008. BITS unterstützt IIS 5.1 nicht auf Windows XP. Das virtuelle IIS-Verzeichnis muss für Uploads aktiviert sein und die BITS IIS-Erweiterungen konfiguriert haben.

**Kerninstallationen von Windows Server:** BITS IIS-Erweiterungen werden nicht unterstützt.

Verwenden Windows Server 2008 die **Server-Manager,** um das Feature BITS-Servererweiterungen zu installieren. Klicken **Server-Manager** im linken Bereich **auf Features.** Aktivieren Sie **im Assistenten zum Hinzufügen** von Funktionen bits-Servererweiterungen. Beachten Sie, dass die IIS 6-Verwaltungskompatibilitätsrollen installiert sein müssen.

Verwenden Windows Server 2003 den Assistenten Windows **Komponenten,** um die BITS-Servererweiterung zu installieren. Wählen **Systemsteuerung** die Option Software hinzufügen **oder entfernen aus.** Wählen Sie dann **Add/Remove Windows Components (Komponenten hinzufügen/entfernen) aus,** um den **assistenten Windows anzuzeigen.** Die BITS-Servererweiterung ist eine Unterkomponente von Internetinformationsdienste (IIS), die eine Unterkomponente des Webanwendungsservers ist.

> [!Note]  
> Wenn der IISAdmin-Dienst neu gestartet wird, muss der IIS-Arbeitsprozess wiederverwendet werden, bevor der BITS-Dienst uploads fortsetzen kann. Der IIS-Workerprozess kann manuell mithilfe des BefehlszeilenprogrammsIISReset.exe **werden.**

 

Informationen zum Konfigurieren von IIS für Uploads finden Sie unter [Einrichten des Servers für Uploads.](setting-up-the-server-for-uploads.md)

Weitere Informationen zu den Eigenschaften, die BITS IIS hinzufügt, finden Sie unter [BITS Server Einstellungen for Hochladen Jobs](bits-server-settings-for-upload-jobs.md).

 

 




