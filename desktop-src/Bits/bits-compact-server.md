---
title: BITS Compact Server
description: Der Background Intelligent Transfer Service (Bits) Compact Server ist ein eigenständiger HTTP/HTTPS-Dateiserver, der die Möglichkeit bietet, eine begrenzte Anzahl von großen Dateien asynchron zwischen Computern zu übertragen.
ms.assetid: ab4cf901-6d93-433c-b1b2-ffa54d10725c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b40e2840c24e15379fac11a5a12ed76c225e7be5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858370"
---
# <a name="bits-compact-server"></a>BITS Compact Server

Der Background Intelligent Transfer Service (Bits) Compact Server ist ein eigenständiger HTTP/HTTPS-Dateiserver, der die Möglichkeit bietet, eine begrenzte Anzahl von großen Dateien asynchron zwischen Computern zu übertragen. Der Compact Server wird als NT-Dienst erstellt und verwendet HTTP.SYS.

Der BITS Compact-Server ist für die Verwendung durch Kunden von Unternehmen und Kleinunternehmen unter folgenden Bedingungen bestimmt:

-   Die erwartete Verwendung beträgt maximal 25 URL-Gruppen, und jede URL-Gruppe unterstützt drei gleichzeitige Dateiübertragungen.
-   Dateiübertragungen erfolgen zwischen Computern in derselben Domäne oder in sich gegenseitig vertrauenswürdigen Domänen.
-   Dateiübertragungen sind nicht für Clients mit Internet Zugriff vorgesehen.

## <a name="installing-the-bits-compact-server"></a>Installieren des BITS Compact-Servers

Der BITS Compact-Server ist eine optionale Serverkomponente. Sie können eine der folgenden Optionen verwenden, um den BITS Compact-Server zu installieren:

-   Server-Manager

-   Windows PowerShell

-   Paket-Manager

**So installieren Sie den BITS Compact-Server mithilfe von Server-Manager**

1.  Klicken Sie im Abschnitt " **featurezusammenfassung** " des **Server-Manager** auf **Features hinzufügen**.
2.  Wählen Sie im Assistenten zum Hinzufügen von Features **Background Intelligent Transfer Service (Bits)** und **Compact Server** aus.
3.  Befolgen Sie die Anweisungen des Assistenten, einschließlich der Installation der erforderlichen Software, falls angegeben.

Weitere Informationen finden Sie in der **Server-Manager** -Online Hilfe.

**So installieren Sie den BITS Compact-Server mithilfe von Windows PowerShell**

1.  Geben Sie an einer Windows PowerShell-Eingabeaufforderung den folgenden Befehl ein: **Import-Module Server Manager**. Drücken Sie dann die Eingabetaste.
2.  Geben Sie den folgenden Befehl ein: **Add-Windows Feature BITS-Compact-Server**. Drücken Sie dann die Eingabetaste.

Im folgenden textbasierten Beispiel wird die Installation des BITS Compact-Servers mithilfe von Windows PowerShell-Cmdlets veranschaulicht.

``` syntax
PS C:\> Import-Module ServerManager
PS C:\> Add-WindowsFeature BITS-Compact-Server

Success Restart Needed Exit Code Feature Result
------- -------------- --------- --------------
True    No             Success   {Compact Server}


PS C:\>
```

Weitere Informationen zur Verwendung von Cmdlets finden Sie in der [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) -Dokumentation.

Weitere Informationen zum Cmdlet "Import-Module" finden Sie unter " [Import-Module](/previous-versions//dd347701(v=technet.10)) " in der Microsoft TechNet-Bibliothek. Um Hilfe in der Befehlszeile zu erhalten, geben **Sie Get-Help Import-Module** ein.

Weitere Informationen zum Cmdlet "Add-WindowsFeature" finden [Sie unter Add-Windows Feature](/previous-versions//dd347701(v=technet.10)) in der Microsoft TechNet-Bibliothek. Um Hilfe in der Befehlszeile zu erhalten, geben **Sie Get-Help Add-Windows Feature** ein.

**So installieren Sie den BITS Compact-Server mithilfe des Paket-Managers**

-   Geben Sie den folgenden Befehl ein: **PkgMgr.exe/IU: lightweightserver**.

> [!Note]  
> Die Einstellungen gehen verloren, wenn der Compact Server-Dienst neu gestartet wird oder wenn der Computer neu gestartet wird.

 

## <a name="bits-compact-server-remote-management"></a>BITS Compact Server-Remote Verwaltung

Der BITS Compact-Server mit Bits-Remote Verwaltung ermöglicht sicherere Remote Dateiübertragungen. Die Bits-Remote Verwaltung verwendet einen Windows-Verwaltungsinstrumentation (WMI)-Anbieter, um einem Systemadministrator oder einer Controller Anwendung das Remote Erstellen von Bits-Übertragungs Aufträgen auf den Clients und das Veröffentlichen von Dateien für das Hosting auf dem BITS Compact-Server zu ermöglichen. Der Bits-Anbieter kann auch verwendet werden, um einer Anwendung die Remote Verwendung des BITS-Clients in Verbindung mit dem BITS Compact-Server zu ermöglichen, um Dateien von einem Remote Computer auf einen anderen Remote Computer zu übertragen.

Weitere Informationen finden Sie in der Dokumentation zum [Bits-Anbieter](/previous-versions/windows/desktop/bitsprov/bits-provider) .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bits-Anbieter](/previous-versions/windows/desktop/bitsprov/bits-provider)
</dt> </dl>

 

 