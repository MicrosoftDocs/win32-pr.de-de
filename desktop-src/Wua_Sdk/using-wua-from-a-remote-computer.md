---
description: Die Windows Update-Agent-API (WUA) kann von einem Benutzer auf einem Remote Computer oder von einer Anwendung verwendet werden, die auf einem Remote Computer ausgeführt wird. Der Remote Benutzer oder die Anwendung muss jedoch über Administratorrechte verfügen.
ms.assetid: 15f86590-bed8-4506-916d-43b0bac5db2a
title: Verwenden von WUA auf einem Remote Computer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb14c019e48d6c36b210633ab9d57dcd157585a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344401"
---
# <a name="using-wua-from-a-remote-computer"></a>Verwenden von WUA auf einem Remote Computer

Die Windows Update-Agent-API (WUA) kann von einem Benutzer auf einem Remote Computer oder von einer Anwendung verwendet werden, die auf einem Remote Computer ausgeführt wird. Der Remote Benutzer oder die Anwendung muss jedoch über Administratorrechte verfügen.

Die folgende Liste enthält Schnittstellen, die für Remote Benutzer und Anwendungen verfügbar sind:

-   [**Iupdatesession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)
-   [**IUpdateSession2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)
-   [**Iupdatesearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher)
-   [**Iautomaticupdates**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdates)
-   [**Isearchresult**](/windows/desktop/api/Wuapi/nn-wuapi-isearchresult)
-   [**Iupdatecollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection)
-   [**Iupdate**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate)
-   [**IUpdate2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate2)
-   [**Iwindowsdriverupdate**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate)
-   [**IWindowsDriverUpdate2**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate2)
-   [**Iupdateidentity**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateidentity)
-   [**Iimageinformation**](/windows/desktop/api/Wuapi/nn-wuapi-iimageinformation)
-   [**Iinstallationbehavior**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationbehavior)
-   [**Istringcollection**](/windows/desktop/api/Wuapi/nn-wuapi-istringcollection)
-   [**Iupdatehistoryentrycollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection)
-   [**Iupdatehistoryentry**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentry)
-   [**Icategorycollection**](/windows/desktop/api/Wuapi/nn-wuapi-icategorycollection)
-   [**Icategory**](/windows/desktop/api/Wuapi/nn-wuapi-icategory)
-   [**Iupdateexceptioncollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexceptioncollection)
-   [**Iupdateexception**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexception)
-   [**Iupdatedownloadcontentcollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloadcontentcollection)
-   [**Iupdatedownloadcontent**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloadcontent)
-   [**Iupdateservicemanager**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager)
-   [**Iupdateservicecollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicecollection)
-   [**Iupdateservice**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice)
-   [**Iwindowsupdateagentinfo**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsupdateagentinfo)

In der folgenden Liste sind Schnittstellen und Eigenschaften enthalten, die für Remote Benutzer und-Anwendungen nicht verfügbar sind:

-   [**Iupdatesession:: kreateupdatedownloader**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession-createupdatedownloader)
-   [**Iupdatesession:: kreateupdateinstaller**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession-createupdateinstaller)
-   [**WebProxy-Eigenschaft von iupdatesession**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession-get_webproxy)
-   [**Iupdatesearcher:: beginsearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch)
-   [**Iupdatesearcher:: endsearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-endsearch)
-   Die [**IsHidden-Eigenschaft von iupdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden) (**IsHidden** ist schreibgeschützt, wenn Sie Remote aufgerufen wird.)
-   [**Iupdate:: akzepteula**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula)
-   [**Iupdate:: copyfromcache**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-copyfromcache)
-   [**IUpdate2:: copytocache**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate2-copytocache)
-   [**IWindowsDriverUpdate2:: copytocache**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate2-copytocache)
-   [**Iupdateservicemanager:: AddService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addservice)
-   [**Iupdateservicemanager:: registerservicewithau**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-registerservicewithau)
-   [**Iupdateservicemanager:: unregisterservicewithau**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-unregisterservicewithau)
-   [**Iautomaticupdate::P ause**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-pause)
-   [**Iautomaticupdates:: Resume**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-resume)
-   [**Iautomaticupdates:: showsettingsdialog**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-showsettingsdialog)
-   [**Settings-Eigenschaft von iautomaticupdates**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-get_settings)
-   [**Serviceaktivierte Eigenschaft von iautomaticupdates**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-get_serviceenabled)
-   [**Iautomaticupdates:: enableservice**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-enableservice)
-   [**Isysteminformation**](/windows/desktop/api/Wuapi/nn-wuapi-isysteminformation)

Die folgenden Ports und Ausnahmen müssen den Windows-Firewall-Einstellungen für Windows Vista und Windows Server 2008 hinzugefügt werden, damit die WUA-API Remote aufgerufen wird.

<dl> <dt>

<span id="Exception_1"></span><span id="exception_1"></span><span id="EXCEPTION_1"></span>Ausnahme 1
</dt> <dd> <dl> <dd>Lokaler Port: 135</dd> <dd>Remoteport: alle</dd> <dd>Protokollnummer: 6</dd> <dd>Ausführbare Datei:% windir% \\ system32 \\svchost.exe</dd> <dd>Dienst: RPCSS</dd> <dd>Remote Berechtigung: Administrator</dd> </dl> </dd> <dt>

<span id="Exception_2"></span><span id="exception_2"></span><span id="EXCEPTION_2"></span>Ausnahme 2
</dt> <dd> <dl> <dd>Lokaler Port: dynamisches RPC</dd> <dd>Remoteport: alle</dd> <dd>Protokollnummer: 6</dd> <dd>Ausführbare Datei:% windir% \\ system32 \\dllhost.exe</dd> <dd>Remote Berechtigung: Administrator</dd> </dl> </dd> </dl>

Die folgende Liste enthält Tools, die zum Konfigurieren der Windows-Firewall-Einstellungen verwendet werden können:

-   Windows-Firewall mit erweitertem Sicherheits-Snap-In
-   Gruppenrichtlinie
-   Netsh advfirewall-Befehlszeilen Tool

Weitere Informationen zur Verwendung von Tools zum Konfigurieren der Windows-Firewall-Einstellungen finden Sie unter [Getting Started with Windows Firewall with Advanced Security](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748991(v=ws.10)).

 

 
