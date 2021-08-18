---
title: Verwenden von WMI Windows PowerShell Cmdlets zum Verwalten des BITS Compact-Servers
description: Windows PowerShell bietet einen einfachen Mechanismus, um eine Verbindung mit Windows Management Instrumentation (WMI) auf einem Remotecomputer herzustellen und den Background Intelligent Transfer Service (BITS) Compact Server zu verwalten.
ms.assetid: fe174d2f-4ca0-431e-b1b8-1893ec54147a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e82401e80b5e49b7d2b964ec910d15d70aea7ce9c782a0173bef97aa8b3a5c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021078"
---
# <a name="using-wmi-windows-powershell-cmdlets-to-manage-the-bits-compact-server"></a>Verwenden von WMI Windows PowerShell Cmdlets zum Verwalten des BITS Compact-Servers

Windows PowerShell bietet einen einfachen Mechanismus, um eine Verbindung mit Windows Management Instrumentation (WMI) auf einem Remotecomputer herzustellen und den Background Intelligent Transfer Service (BITS) Compact Server zu verwalten. Der BITS Compact Server ist eine optionale Serverkomponente, die separat installiert werden muss. Informationen zum Installieren des Compact-Servers finden Sie in der Dokumentation zu [BITS Compact Server.](bits-compact-server.md)

1.  Verbinden an den BITS-Anbieter.

    ```PowerShell
    $cred = Get-Credential
    $bcs = Get-WmiObject -Namespace "root\Microsoft\BITS" -Class "BITSCompactServerUrlGroup" `
    -List -ComputerName Server1 -Credential $cred
    ```

    

    Das Cmdlet [Get-Credential](/previous-versions//dd315327(v=technet.10)) fordert die Anmeldeinformationen des Benutzers an, eine Verbindung mit dem Remotecomputer herzustellen, und weist die Anmeldeinformationen dem $cred-Objekt zu.

    Die vom [Cmdlet Get-WmiObject](/previous-versions//dd315295(v=technet.10)) zurückgegebenen Objekte werden der $bcs Variablen zugewiesen. Im vorherigen Beispiel ruft das [Cmdlet Get-WmiObject](/previous-versions//dd315295(v=technet.10)) die [BITSCompactServerUrlGroup-Klasse](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) im \\ Microsoft \\ BITS-Stammnamespace Server1 ab. Statische Methoden, die von der [BITSCompactServerUrlGroup-Klasse](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) verfügbar gemacht werden, können für das $bcs-Objekt aufgerufen werden. Weitere Informationen zur BITS-Remoteverwaltung finden Sie unter [BITS-Anbieter](/previous-versions/windows/desktop/bitsprov/bits-provider) und [BITS-Anbieterklassen.]( /previous-versions//dd904507(v=vs.85))

    > [!Note]  
    > Das Akzentzeichen \` () wird verwendet, um einen Zeilenbruch anzugeben.

     

2.  Erstellen Sie eine URL-Gruppe auf dem Server.

    ```PowerShell
    $URLGroup = "https://Server1:80/testurlgroup" 
    $bcs.CreateUrlGroup($URLGroup)
    ```

    

    Die https://Server1:80/testurlgroup URL-Präfixzeichenfolge "" wird der variablen $URLGroup zugewiesen. Die $URLGroup Variable wird an die [CreateUrlGroup-Methode](/previous-versions/windows/desktop/bitsprov/createurlgroup-bitslightweightserverurlgroup) übergeben, die die URL-Gruppe auf Server1 erstellt.

    Sie können eine andere URL-Gruppe angeben. Die URL-Gruppe muss einer gültigen URL-Präfixzeichenfolge entsprechen. Weitere Informationen zu URL-Präfixen finden Sie unter [UrlPrefix-Zeichenfolgen.](../http/urlprefix-strings.md)

3.  Hosten Sie eine Datei in der URL-Gruppe.

    ```PowerShell
    $bcsObj = Get-WmiObject -Namespace "root\Microsoft\BITS" -Class "BITSCompactServerUrlGroup" -filter ("UrlGroup='" + $URLGroup + "'") -ComputerName Server1 -Credential $cred
    $bcsObj.CreateURL("url.txt", "c:\\temp\\1.txt", "") -ComputerName Server1 -Credential $cred
    ```

    

    Die vom [Cmdlet Get-WmiObject](/previous-versions//dd315295(v=technet.10)) zurückgegebene BITSCompactServerUrlGroup-Instanz wird der $bcsObj Variablen zugewiesen. Die [CreateUrl-Methode](/previous-versions/windows/desktop/bitsprov/createurl-bitslightweightserverurlgroup) wird für die $bcsObj mit dem URL-Suffix "url.txt", dem Quellpfad "c: \\ \\ temp \\ \\1.txt" für die Datei und einer leeren Sicherheitsbeschreibungszeichenfolge als Parameter aufgerufen. Das Suffix "url.txt" wird dem URL-Gruppenpräfix hinzugefügt. Clients können die Datei von der folgenden Adresse herunterladen: https://Server1:80/testurlgroup/url.txt .

4.  Bereinigen Sie die URL und die URL-Gruppe.

    ```PowerShell
    $bcsObj.Delete()
    ```

    

    Die **methode system.object Delete** löscht das $bcsObj Objekt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[BITS Compact Server](./bits-compact-server.md)
</dt> <dt>

[BITS-Anbieter](/previous-versions/windows/desktop/bitsprov/bits-provider)
</dt> <dt>

[BITS-Anbieterklassen]( /previous-versions//dd904507(v=vs.85))
</dt> <dt>

[Get-Credential](/previous-versions//dd315327(v=technet.10))
</dt> <dt>

[Get-WmiObject](/previous-versions//dd315295(v=technet.10))
</dt> </dl>

 

 