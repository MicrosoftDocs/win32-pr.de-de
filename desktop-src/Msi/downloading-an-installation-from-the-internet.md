---
description: Windows Das Installationsprogramm akzeptiert eine Uniform Resource Locator (URL) als gültige Quelle für eine Installation.
ms.assetid: f1bb2dc0-4236-4bd7-89a2-f4416b5b9dda
title: Herunterladen einer Installation aus dem Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5195b0ec0e5c36e7b6866232c498c02a9f4022d207cd86cc229a49ec5a5e8bac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637767"
---
# <a name="downloading-an-installation-from-the-internet"></a>Herunterladen einer Installation aus dem Internet

Windows Das Installationsprogramm akzeptiert eine Uniform Resource Locator (URL) als gültige Quelle für eine Installation. Windows Das Installationsprogramm kann Pakete, Patches und Transformationen über einen URL-Speicherort installieren.

Wenn sich die Installationsdatenbank unter einer URL befindet, lädt das Installationsprogramm die Datenbank an einen Cachespeicherort herunter, bevor die Installation gestartet wird. Das Installationsprogramm lädt auch die Dateien und Cab-Dateien aus der Internetquelle herunter, die für die Auswahl des Benutzers geeignet sind. Weitere Informationen finden Sie unter Beispiel für die [Installation eines URL-basierten Windows Installers.](a-url-based-windows-installer-installation-example.md)

Um beispielsweise ein Paket mit einer Quelle auf einem Webserver unter zu installieren, https://server/share/package.msi können Sie die [Befehlszeilenoptionen](command-line-options.md) verwenden, um das Paket zu installieren und [öffentliche](public-properties.md) Eigenschaften festzulegen.

msiexec /i https://server/share/package.msi *PROPERTY=VALUE*

Eine Befehlszeile wie die zuvor gezeigte sollte an das Installationsprogramm übergeben werden, um eine Installation über einen Webbrowser zu starten. Im Allgemeinen sollten Sie das Paket nicht herunterladen und installieren, indem Sie einfach im Browser auf die datei .msi doppelklicken. Dadurch wird die .msi-Datei in den temporären Ordner Internetdateien heruntergeladen und der folgende Befehl an das Installationsprogramm übergeben:

**msiexec /i c: \\ \\ temporäre Windows-Internetdateien \\package.msi**

Die Installation schlägt fehl, wenn das Paket externe Quelldateien oder Schränke erfordert, da sich diese nicht am gleichen Speicherort wie die .msi Befinden.

Da das [**Installer-Objekt**](installer-object.md) auf dem Computer des Benutzers nicht als [SafeForScripting](safeforscripting.md) gekennzeichnet ist, müssen Benutzer ihre Browsersicherheitseinstellungen anpassen, damit das Beispiel ordnungsgemäß funktioniert.

Die [**InstallProduct-Methode**](installer-installproduct.md) kann verwendet werden, um den vorherigen Befehl in einem Browser als Ein-Klick-Ereignis auszuführen.


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



Da bei einigen Webservern die Groß-/Kleinschreibung beachtet wird, muss das Feld FileName in der [Dateitabelle](file-table.md) genau mit der Groß-/Kleinschreibung der Quelldateien übereinstimmen, um die Unterstützung von Internetdownloads sicherzustellen.

Weitere Informationen finden [Sie unter Herunterladen und Installieren eines Patches aus dem Internet.](downloading-and-installing-a-patch-from-the-internet.md) Weitere Informationen zum Sichern von Installationen und zur Verwendung digitaler Zertifikate finden Sie unter [Richtlinien für die Erstellung sicherer Installationen](guidelines-for-authoring-secure-installations.md) und digitaler [Signaturen und Windows Installer.](digital-signatures-and-windows-installer.md) Weitere Informationen zum Erstellen einer Webinstallation eines Windows Installer-Pakets finden Sie unter [InternetDownload Bootstrapping](internet-download-bootstrapping.md).

## <a name="available-internet-protocols"></a>Verfügbare Internetprotokolle

Ab Windows Server 2003 und Windows XP kann das Installationsprogramm die Protokolle HTTP, HTTPS und FILE verwenden. Das Installationsprogramm unterstützt die Protokolle FTP und GOPHER nicht.

Windows Die Installationsprogrammversion 2.0 kann die PROTOKOLLE HTTP, FILE und FTP und nicht die Protokolle HTTPS und GOPHER verwenden.

 

 



