---
description: Windows Installer akzeptiert eine Uniform Resource Locator (URL) als gültige Quelle für eine-Installation.
ms.assetid: f1bb2dc0-4236-4bd7-89a2-f4416b5b9dda
title: Herunterladen einer Installation aus dem Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b971129aa2df30bf567be67f0f244b60868ec11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356862"
---
# <a name="downloading-an-installation-from-the-internet"></a>Herunterladen einer Installation aus dem Internet

Windows Installer akzeptiert eine Uniform Resource Locator (URL) als gültige Quelle für eine-Installation. Windows Installer können Pakete, Patches und Transformationen von einem URL-Speicherort installieren.

Wenn sich die Installations Datenbank an einer URL befindet, lädt das Installationsprogramm die Datenbank an einen Cache Speicherort herunter, bevor die Installation gestartet wird. Das Installationsprogramm lädt auch die Dateien und CAB-Dateien aus der Internet Quelle herunter, die für die Auswahl des Benutzers geeignet sind. Weitere Informationen finden Sie unter [Beispiel für eine URL-basierte Windows Installer Installation](a-url-based-windows-installer-installation-example.md) .

Zum Installieren eines Pakets mit einer Quelle, die sich auf einem Webserver unter befindet https://server/share/package.msi , können Sie beispielsweise die [Befehlszeilen](command-line-options.md) Optionen verwenden, um das Paket zu installieren und [öffentliche](public-properties.md) Eigenschaften festzulegen.

msiexec/i https://server/share/package.msi *Eigenschaft = Wert*

Eine Befehlszeile wie die oben gezeigte sollte an das Installationsprogramm weitergegeben werden, um eine Installation über einen Webbrowser zu starten. Im Allgemeinen sollten Sie das Paket nicht herunterladen und installieren, indem Sie einfach im Browser auf die MSI-Datei doppelklicken. Dadurch wird die MSI-Datei in den Ordner "temporäre Internet Dateien" heruntergeladen, und der Befehl übergibt den folgenden Befehl an das Installationsprogramm:

**msiexec/i c: \\ temporäre Windows- \\ Internetdateien \\package.msi**

Die Installation schlägt fehl, wenn das Paket externe Quelldateien oder-Schränke erfordert, da diese sich nicht am selben Speicherort wie die MSI-Datei befinden.

Beachten Sie Folgendes: da das [**Installer**](installer-object.md) -Objekt auf dem Computer des Benutzers nicht als " [safeforscripting](safeforscripting.md) " gekennzeichnet ist, müssen die Benutzer die Sicherheitseinstellungen des Browsers anpassen, damit das Beispiel ordnungsgemäß funktioniert.

Die [**installproduct**](installer-installproduct.md) -Methode kann verwendet werden, um den vorherigen Befehl in einem Browser als On-Click-Ereignis auszuführen.


```VB
'Downloading an Installation from the Internet
'The InstallProduct method could be used to run 
'the previous command from a browser as an on-click event.

<SCRIPT LANGUAGE="VBScript"> 
<!-- 
Dim Installer
On Error Resume Next
set Installer=CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "https://server/share/package.msi", "PROPERTY=VALUE "
set Installer=Nothing
-->
</SCRIPT>
```



Beachten Sie, dass das fileName-Feld in der [Datei](file-table.md) Tabelle genau mit der Groß-/Kleinschreibung der Quelldateien übereinstimmen muss, da bei manchen Webservern die Groß-/Kleinschreibung beachtet wird.

Weitere [Informationen finden Sie unter herunterladen und Installieren eines Patches aus dem Internet](downloading-and-installing-a-patch-from-the-internet.md). Weitere Informationen zum Sichern von Installationen und zum Verwenden digitaler Zertifikate finden Sie unter [Richtlinien für die Erstellung sicherer Installationen](guidelines-for-authoring-secure-installations.md) und [digitaler Signaturen und Windows Installer](digital-signatures-and-windows-installer.md). Weitere Informationen zum Erstellen einer Webinstallation eines Windows Installer Pakets finden [Sie unter Internet Download Bootstrapping](internet-download-bootstrapping.md).

## <a name="available-internet-protocols"></a>Verfügbare Internet Protokolle

Ab Windows Server 2003 und Windows XP kann das Installationsprogramm die HTTP-, HTTPS-und Datei Protokolle verwenden. Das Installationsprogramm unterstützt das FTP-und das Gopher-Protokoll nicht.

In Windows Installer Version 2,0 können http-, Datei-und FTP-Protokolle verwendet werden. die Protokolle HTTPS und Gopher können nicht verwendet werden.

 

 



