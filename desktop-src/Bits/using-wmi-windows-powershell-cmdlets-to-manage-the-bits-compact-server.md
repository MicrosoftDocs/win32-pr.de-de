---
title: Verwenden von WMI-Windows PowerShell-Cmdlets zum Verwalten des BITS Compact-Servers
description: Windows PowerShell bietet einen einfachen Mechanismus zum Herstellen einer Verbindung mit Windows-Verwaltungsinstrumentation (WMI) auf einem Remote Computer und zum Verwalten des Background Intelligent Transfer Service (Bits) Compact-Servers.
ms.assetid: fe174d2f-4ca0-431e-b1b8-1893ec54147a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c3c942672c147ec5daa0caa2a370e487be80809
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948910"
---
# <a name="using-wmi-windows-powershell-cmdlets-to-manage-the-bits-compact-server"></a>Verwenden von WMI-Windows PowerShell-Cmdlets zum Verwalten des BITS Compact-Servers

Windows PowerShell bietet einen einfachen Mechanismus zum Herstellen einer Verbindung mit Windows-Verwaltungsinstrumentation (WMI) auf einem Remote Computer und zum Verwalten des Background Intelligent Transfer Service (Bits) Compact-Servers. Der BITS Compact-Server ist eine optionale Serverkomponente, die separat installiert werden muss. Informationen zum Installieren des Compact-Servers finden Sie in der Dokumentation zu [BITS Compact Server](bits-compact-server.md) .

1.  Stellen Sie eine Verbindung zum Bits-Anbieter her.

    ```PowerShell
    $cred = Get-Credential
    $bcs = Get-WmiObject -Namespace "root\Microsoft\BITS" -Class "BITSCompactServerUrlGroup" `
    -List -ComputerName Server1 -Credential $cred
    ```

    

    Das [Get-Credential-](/previous-versions//dd315327(v=technet.10)) Cmdlet fordert die Anmelde Informationen des Benutzers auf, um eine Verbindung mit dem Remote Computer herzustellen, und weist die Anmelde Informationen dem $cred-Objekt zu.

    Die vom [Get-WMIObject-](/previous-versions//dd315295(v=technet.10)) Cmdlet zurückgegebenen Objekte werden der $BCS Variablen zugewiesen. Im vorherigen Beispiel ruft das [Get-WMIObject-](/previous-versions//dd315295(v=technet.10)) Cmdlet die [BITSCompactServerUrlGroup](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) -Klasse im Microsoft Bits- \\ Stamm \\ Namespace von Server1 ab. Statische Methoden, die von der [BITSCompactServerUrlGroup](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) -Klasse verfügbar gemacht werden, können für das $BCS Objekt aufgerufen werden. Weitere Informationen zur Bits-Remote Verwaltung finden Sie unter [Bits-Anbieter](/previous-versions/windows/desktop/bitsprov/bits-provider) -und Bits- [Anbieter Klassen]( /previous-versions//dd904507(v=vs.85)).

    > [!Note]  
    > Das Zeichen mit einem Doppel Akzent ( \` ) wird verwendet, um einen Zeilenumbruch anzugeben.

     

2.  Erstellen Sie eine URL-Gruppe auf dem Server.

    ```PowerShell
    $URLGroup = "https://Server1:80/testurlgroup" 
    $bcs.CreateUrlGroup($URLGroup)
    ```

    

    Die https://Server1:80/testurlgroup URL-Präfix Zeichenfolge "" wird der $URLGroup Variablen zugewiesen. Die $URLGroup Variable wird an die Methode " [kreateurlgroup](/previous-versions/windows/desktop/bitsprov/createurlgroup-bitslightweightserverurlgroup) " übergeben, die die URL-Gruppe auf Server1 erstellt.

    Sie können eine andere URL-Gruppe angeben. Die URL-Gruppe muss einer gültigen URL-Präfix Zeichenfolge entsprechen. Weitere Informationen zu URL-Präfixen finden Sie unter [URLPrefix](../http/urlprefix-strings.md)-Zeichen folgen.

3.  Hosten Sie eine Datei in der URL-Gruppe.

    ```PowerShell
    $bcsObj = Get-WmiObject -Namespace "root\Microsoft\BITS" -Class "BITSCompactServerUrlGroup" -filter ("UrlGroup='" + $URLGroup + "'") -ComputerName Server1 -Credential $cred
    $bcsObj.CreateURL("url.txt", "c:\\temp\\1.txt", "") -ComputerName Server1 -Credential $cred
    ```

    

    Die BITSCompactServerUrlGroup-Instanz, die vom [Get-WMIObject](/previous-versions//dd315295(v=technet.10)) -Cmdlet zurückgegeben wird, wird der $bcsObj-Variablen zugewiesen. Die Methode " [kreateurl](/previous-versions/windows/desktop/bitsprov/createurl-bitslightweightserverurlgroup) " wird für die $bcsObj mit dem URL-Suffix "url.txt", dem Quellpfad "c: \\ \\ Temp \\ \\1.txt" für die Datei und einer leeren Sicherheits beschreibungerzeichenfolge als Parameter aufgerufen. Das Suffix "url.txt" wird dem URL-Gruppen Präfix hinzugefügt. Clients können die Datei von folgender Adresse herunterladen: https://Server1:80/testurlgroup/url.txt .

4.  Bereinigen Sie die URL und die URL-Gruppe.

    ```PowerShell
    $bcsObj.Delete()
    ```

    

    Die " **System. Object DELETE** "-Methode löscht das $bcsObj Objekt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[BITS Compact Server](./bits-compact-server.md)
</dt> <dt>

[Bits-Anbieter](/previous-versions/windows/desktop/bitsprov/bits-provider)
</dt> <dt>

[Bits-Anbieter Klassen]( /previous-versions//dd904507(v=vs.85))
</dt> <dt>

[Get-Credential](/previous-versions//dd315327(v=technet.10))
</dt> <dt>

[Get-WmiObject](/previous-versions//dd315295(v=technet.10))
</dt> </dl>

 

 