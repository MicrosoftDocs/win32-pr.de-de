---
title: Installieren des Anbieters
description: Das Verfahren zum Installieren des DNS-WMI-Anbieters hängt von der Version der Windows ab, auf der er installiert ist.
ms.assetid: 5f2bd11a-bc1d-4a43-92d4-26392d2504e7
keywords:
- Domain Name System, WMI-Anbieter, Installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a9b4b976ccb1a600f56042cb75b500577335059966a82dbb1f9e77b04f7a4df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693040"
---
# <a name="installing-the-provider"></a>Installieren des Anbieters

Das Verfahren zum Installieren des DNS-WMI-Anbieters hängt von der Version der Windows ab, auf der er installiert ist. Im folgenden Verfahren wird beschrieben, wie Sie den DNS-WMI-Anbieter auf Windows 2000 installieren und einrichten. Laden Sie die folgende Datei herunter, um den DNS-WMI-Anbieter für Windows 2000 abzurufen:

**WARNUNG:** DNS-WMI-Anbieterdateien sind nicht austauschbar. Windows 2000-DNS-Server erfordern andere Dateien und ein anderes Verfahren als Windows Server 2003-DNS-Server. Das Jeweilige Verfahren wird bereitgestellt.

**So installieren Sie den DNS-WMI-Anbieter auf Windows 2000-Server**

1.  Rufen Sie den DNS-WMI-Anbieter für Windows 2000 aus dem Windows 2000 Server Resource Kit ab, oder laden Sie die Datei Dnsprov.zip von folgendem Ftp://ftp.microsoft.com/reskit/win2000/ herunter:
2.  Kopieren Sie die Dateien DNS WMI Provider (Dnsprov.dll) und Dnsschema.mof in das <winntdir> \\ Verzeichnis system32 \\ wbem.
3.  Kompilieren Sie die MOF-Datei. Dadurch wird das Schema an den Server angepasst.

    **mofcomp dnsschema.mof**

4.  Registrieren Sie die DLL auf dem DNS-Server.

    **regsvr32 dnsprov.dll**

5.  Skripts oder Programme, die den DNS-WMI-Anbieter zum Verwalten von DNS-Servern verwenden, können dann verwendet werden. Die Skripts oder Programme können entweder vom DNS-Server oder von einem Clientcomputer aus ausgeführt werden.
    > [!Note]  
    > Das WMI SDK ist zum Ausführen des DNS-WMI-Anbieters nicht erforderlich, enthält jedoch viele nützliche Tools.

     

Der DNS-WMI-Anbieter muss auf jedem DNS-Server installiert sein, der verwaltet werden soll. Die DNS-Skripts können jedoch auf dem DNS-Server oder auf einem Remotehost ausgeführt werden.

**So installieren Sie den DNS-WMI-Anbieter auf Windows Server 2003**

-   Bei Windows Server 2003-Betriebssystemen wird der DNS-WMI-Anbieter automatisch installiert und registriert, und die MOF-Datei wird kompiliert, wenn der DNS-Serverdienst installiert wird.

 

 




