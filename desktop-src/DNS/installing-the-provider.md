---
title: Installieren des Anbieters
description: Die Vorgehensweise zum Installieren des DNS-WMI-Anbieters unterscheidet sich abhängig von der Windows-Version, auf der Sie installiert ist.
ms.assetid: 5f2bd11a-bc1d-4a43-92d4-26392d2504e7
keywords:
- Domain Name System, WMI-Anbieter, installieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b1c9dbdaf6d3ad55247d0b978c0a422361a2f04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708646"
---
# <a name="installing-the-provider"></a>Installieren des Anbieters

Die Vorgehensweise zum Installieren des DNS-WMI-Anbieters unterscheidet sich abhängig von der Windows-Version, auf der Sie installiert ist. Im folgenden Verfahren wird beschrieben, wie der DNS-WMI-Anbieter unter Windows 2000 installiert und eingerichtet wird. Um den DNS-WMI-Anbieter für Windows 2000 zu erhalten, laden Sie die folgende Datei herunter:

**Warnung:** DNS-WMI-Anbieter Dateien sind nicht austauschbar. Für Windows 2000-DNS-Server sind unterschiedliche Dateien und eine andere Prozedur als Windows Server 2003 DNS-Server erforderlich. Das jeweilige Verfahren wird bereitgestellt.

**So installieren Sie den DNS-WMI-Anbieter unter Windows 2000 Server**

1.  Rufen Sie den DNS-WMI-Anbieter für Windows 2000 aus dem Windows 2000 Server Resource Kit ab, oder laden Sie die Datei Dnsprov.zip herunter, von: FTP://FTP.Microsoft.com/reskit/Win2000/
2.  Kopieren Sie den DNS-WMI-Anbieter (Dnsprov.dll) und die Datei dnsschema. MOF in das <winntdir> \\ \\ Verzeichnis System32 WBEM.
3.  Kompilieren Sie die MOF-Datei. Dadurch wird das Schema so angepasst, dass es dem Server entspricht.

    **"wmacomp dnsschema. mof"**

4.  Registrieren Sie die dll auf dem DNS-Server.

    **regsvr32 dnsprov.dll**

5.  Skripts oder Programme, die zum Verwalten von DNS-Servern den DNS-WMI-Anbieter verwenden, können dann verwendet werden. Die Skripts oder Programme können entweder vom DNS-Server oder von einem Client Computer aus ausgeführt werden.
    > [!Note]  
    > Das WMI-SDK ist nicht erforderlich, um den DNS-WMI-Anbieter auszuführen, aber es enthält viele nützliche Tools.

     

Der DNS-WMI-Anbieter muss auf jedem zu verwaltenden DNS-Server installiert sein. die DNS-Skripts können jedoch auf dem DNS-Server oder auf einem Remote Host ausgeführt werden.

**So installieren Sie den DNS-WMI-Anbieter unter Windows Server 2003**

-   Bei Windows Server 2003-Betriebssystemen wird der DNS-WMI-Anbieter automatisch installiert und registriert, und die zugehörige MOF-Datei wird bei der Installation des DNS-Server Dienstanbieters kompiliert.

 

 




