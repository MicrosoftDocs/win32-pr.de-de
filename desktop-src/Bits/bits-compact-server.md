---
title: BITS Compact Server
description: Der Background Intelligent Transfer Service Compact Server (BITS) ist ein eigenständiger HTTP/HTTPS-Dateiserver, der die Möglichkeit bietet, eine begrenzte Anzahl großer Dateien asynchron zwischen Computern zu übertragen.
ms.assetid: ab4cf901-6d93-433c-b1b2-ffa54d10725c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41cfbc18a8dc06bb474ab8df9df85fb7b8a96838db14bbc18aee4d94881985d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529190"
---
# <a name="bits-compact-server"></a>BITS Compact Server

Der Background Intelligent Transfer Service Compact Server (BITS) ist ein eigenständiger HTTP/HTTPS-Dateiserver, der die Möglichkeit bietet, eine begrenzte Anzahl großer Dateien asynchron zwischen Computern zu übertragen. Der Compact Server wird als NT-Dienst erstellt und verwendet HTTP.SYS.

Der BITS Compact Server ist für die Verwendung durch Unternehmenskunden und kleine Unternehmen unter den folgenden Bedingungen vorgesehen:

-   Die erwartete Nutzung beträgt maximal 25 URL-Gruppen, und jede URL-Gruppe unterstützt drei gleichzeitige Dateiübertragungen.
-   Dateiübertragungen erfolgen zwischen Computern in derselben Domäne oder gegenseitig vertrauenswürdigen Domänen.
-   Dateiübertragungen sind nicht für Clients mit Internetanternetverbindung vorgesehen.

## <a name="installing-the-bits-compact-server"></a>Installieren des BITS Compact-Servers

Der BITS Compact Server ist eine optionale Serverkomponente. Sie können eine der folgenden Optionen verwenden, um den BITS Compact Server zu installieren:

-   Server-Manager

-   Windows PowerShell

-   Paket-Manager

**So installieren Sie den BITS Compact Server mithilfe Server-Manager**

1.  Klicken Sie **im Abschnitt** Zusammenfassung der **Features** des Server-Manager auf **Features hinzufügen.**
2.  Wählen Sie im Assistenten zum Hinzufügen von Features **Background Intelligent Transfer Service (BITS) und** **Compact Server aus.**
3.  Befolgen Sie die Anweisungen des Assistenten, einschließlich der Installation der erforderlichen Software, falls angegeben.

Weitere Informationen finden Sie in der **Server-Manager** Onlinehilfe.

**So installieren Sie den BITS Compact Server mithilfe Windows PowerShell**

1.  Geben Sie in Windows PowerShell Eingabeaufforderung den folgenden Befehl ein: **Import-Module ServerManager**. Drücken Sie dann die Eingabetaste.
2.  Geben Sie den folgenden Befehl ein: **Add-WindowsFeature BITS-Compact-Server**. Drücken Sie dann die Eingabetaste.

Das folgende textbasierte Beispiel veranschaulicht die Installation des BITS Compact-Servers mithilfe Windows PowerShell Cmdlets.

``` syntax
PS C:\> Import-Module ServerManager
PS C:\> Add-WindowsFeature BITS-Compact-Server

Success Restart Needed Exit Code Feature Result
------- -------------- --------- --------------
True    No             Success   {Compact Server}


PS C:\>
```

Informationen zur Verwendung von Cmdlets finden Sie in der [Windows PowerShell Dokumentation.](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx)

Weitere Informationen zum cmdlet Import-Module finden Sie unter [Import-Module](/previous-versions//dd347701(v=technet.10)) in der Microsoft TechNet Library. Um Hilfe an der Befehlszeile zu erhalten, geben **Sie get-help import-module ein.**

Weitere Informationen zum Cmdlet Add-WindowsFeature finden Sie unter [Add-WindowsFeature](/previous-versions//dd347701(v=technet.10)) in der Microsoft TechNet Library. Um Hilfe über die Befehlszeile zu erhalten, geben **Sie get-help Add-WindowsFeature ein.**

**So installieren Sie den BITS Compact-Server mithilfe Paket-Manager**

-   Geben Sie den folgenden Befehl ein: **PkgMgr.exe /iu:LightweightServer**.

> [!Note]  
> Die Einstellungen gehen verloren, wenn der Compact Server-Dienst neu gestartet oder der Computer neu gestartet wird.

 

## <a name="bits-compact-server-remote-management"></a>BITS Compact Server-Remoteverwaltung

Der BITS Compact Server mit BITS-Remoteverwaltung ermöglicht sicherere Remotedateiübertragungen. Die BITS-Remoteverwaltung verwendet einen WMI-Anbieter (Windows Management Instrumentation), damit ein Systemadministrator oder eine Controlleranwendung BITS-Übertragungsaufträge remote auf den Clients erstellen und Dateien zum Hosten auf dem BITS Compact-Server veröffentlichen kann. Der BITS-Anbieter kann auch verwendet werden, um einer Anwendung die Remotenutzung des BITS-Clients in Verbindung mit dem BITS Compact Server zum Übertragen von Dateien von einem Remotecomputer auf einen anderen Remotecomputer zu ermöglichen.

Weitere Informationen finden Sie in der [Dokumentation zum BITS-Anbieter.](/previous-versions/windows/desktop/bitsprov/bits-provider)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[BITS-Anbieter](/previous-versions/windows/desktop/bitsprov/bits-provider)
</dt> </dl>

 

 