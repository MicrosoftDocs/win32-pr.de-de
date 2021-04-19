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
# <a name="downloading-an-installation-from-the-internet"></a><span data-ttu-id="91cfc-103">Herunterladen einer Installation aus dem Internet</span><span class="sxs-lookup"><span data-stu-id="91cfc-103">Downloading an Installation from the Internet</span></span>

<span data-ttu-id="91cfc-104">Windows Installer akzeptiert eine Uniform Resource Locator (URL) als gültige Quelle für eine-Installation.</span><span class="sxs-lookup"><span data-stu-id="91cfc-104">Windows Installer accepts a Uniform Resource Locator (URL) as a valid source for an installation.</span></span> <span data-ttu-id="91cfc-105">Windows Installer können Pakete, Patches und Transformationen von einem URL-Speicherort installieren.</span><span class="sxs-lookup"><span data-stu-id="91cfc-105">Windows Installer can install packages, patches, and transforms from a URL location.</span></span>

<span data-ttu-id="91cfc-106">Wenn sich die Installations Datenbank an einer URL befindet, lädt das Installationsprogramm die Datenbank an einen Cache Speicherort herunter, bevor die Installation gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="91cfc-106">If the installation database is at a URL, the installer downloads the database to a cache location before starting the installation.</span></span> <span data-ttu-id="91cfc-107">Das Installationsprogramm lädt auch die Dateien und CAB-Dateien aus der Internet Quelle herunter, die für die Auswahl des Benutzers geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="91cfc-107">The installer also downloads the files and cabinet files from the Internet source that are appropriate for the user's selections.</span></span> <span data-ttu-id="91cfc-108">Weitere Informationen finden Sie unter [Beispiel für eine URL-basierte Windows Installer Installation](a-url-based-windows-installer-installation-example.md) .</span><span class="sxs-lookup"><span data-stu-id="91cfc-108">See [A URL-based Windows Installer Installation Example](a-url-based-windows-installer-installation-example.md) for more information.</span></span>

<span data-ttu-id="91cfc-109">Zum Installieren eines Pakets mit einer Quelle, die sich auf einem Webserver unter befindet https://server/share/package.msi , können Sie beispielsweise die [Befehlszeilen](command-line-options.md) Optionen verwenden, um das Paket zu installieren und [öffentliche](public-properties.md) Eigenschaften festzulegen.</span><span class="sxs-lookup"><span data-stu-id="91cfc-109">For example, to install a package with a source located on a web server at https://server/share/package.msi, you can use the [command line](command-line-options.md) options to install the package and set [public](public-properties.md) properties.</span></span>

<span data-ttu-id="91cfc-110">msiexec/i https://server/share/package.msi *Eigenschaft = Wert*</span><span class="sxs-lookup"><span data-stu-id="91cfc-110">msiexec /i https://server/share/package.msi *PROPERTY=VALUE*</span></span>

<span data-ttu-id="91cfc-111">Eine Befehlszeile wie die oben gezeigte sollte an das Installationsprogramm weitergegeben werden, um eine Installation über einen Webbrowser zu starten.</span><span class="sxs-lookup"><span data-stu-id="91cfc-111">A command line like the one previously shown should be passed to the installer to start an installation from a web browser.</span></span> <span data-ttu-id="91cfc-112">Im Allgemeinen sollten Sie das Paket nicht herunterladen und installieren, indem Sie einfach im Browser auf die MSI-Datei doppelklicken.</span><span class="sxs-lookup"><span data-stu-id="91cfc-112">In general, you should not download and install the package simply by double-clicking the .msi file from within the browser.</span></span> <span data-ttu-id="91cfc-113">Dadurch wird die MSI-Datei in den Ordner "temporäre Internet Dateien" heruntergeladen, und der Befehl übergibt den folgenden Befehl an das Installationsprogramm:</span><span class="sxs-lookup"><span data-stu-id="91cfc-113">This downloads the .msi file to the temporary Internet files folder and passes the following command to the installer:</span></span>

<span data-ttu-id="91cfc-114">**msiexec/i c: \\ temporäre Windows- \\ Internetdateien \\package.msi**</span><span class="sxs-lookup"><span data-stu-id="91cfc-114">**msiexec /i c:\\windows\\temporary internet files\\package.msi**</span></span>

<span data-ttu-id="91cfc-115">Die Installation schlägt fehl, wenn das Paket externe Quelldateien oder-Schränke erfordert, da diese sich nicht am selben Speicherort wie die MSI-Datei befinden.</span><span class="sxs-lookup"><span data-stu-id="91cfc-115">The installation fails if the package requires any external source files or cabinets because these are not located in the same location as the .msi file.</span></span>

<span data-ttu-id="91cfc-116">Beachten Sie Folgendes: da das [**Installer**](installer-object.md) -Objekt auf dem Computer des Benutzers nicht als " [safeforscripting](safeforscripting.md) " gekennzeichnet ist, müssen die Benutzer die Sicherheitseinstellungen des Browsers anpassen, damit das Beispiel ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="91cfc-116">Note that because the [**Installer**](installer-object.md) object is not marked as [SafeForScripting](safeforscripting.md) on the user's computer, users need to adjust their browser security settings for the example to work correctly.</span></span>

<span data-ttu-id="91cfc-117">Die [**installproduct**](installer-installproduct.md) -Methode kann verwendet werden, um den vorherigen Befehl in einem Browser als On-Click-Ereignis auszuführen.</span><span class="sxs-lookup"><span data-stu-id="91cfc-117">The [**InstallProduct**](installer-installproduct.md) method could be used to run the previous command from a browser as an on-click event.</span></span>


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



<span data-ttu-id="91cfc-118">Beachten Sie, dass das fileName-Feld in der [Datei](file-table.md) Tabelle genau mit der Groß-/Kleinschreibung der Quelldateien übereinstimmen muss, da bei manchen Webservern die Groß-/Kleinschreibung beachtet wird.</span><span class="sxs-lookup"><span data-stu-id="91cfc-118">Note that because some web servers are case sensitive, the FileName field in the [File](file-table.md) table must match the case of the source files exactly to ensure support of Internet downloads.</span></span>

<span data-ttu-id="91cfc-119">Weitere [Informationen finden Sie unter herunterladen und Installieren eines Patches aus dem Internet](downloading-and-installing-a-patch-from-the-internet.md).</span><span class="sxs-lookup"><span data-stu-id="91cfc-119">See [Downloading and Installing a Patch from the Internet](downloading-and-installing-a-patch-from-the-internet.md).</span></span> <span data-ttu-id="91cfc-120">Weitere Informationen zum Sichern von Installationen und zum Verwenden digitaler Zertifikate finden Sie unter [Richtlinien für die Erstellung sicherer Installationen](guidelines-for-authoring-secure-installations.md) und [digitaler Signaturen und Windows Installer](digital-signatures-and-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="91cfc-120">For more information about securing installations and using digital certificates, see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md).</span></span> <span data-ttu-id="91cfc-121">Weitere Informationen zum Erstellen einer Webinstallation eines Windows Installer Pakets finden [Sie unter Internet Download Bootstrapping](internet-download-bootstrapping.md).</span><span class="sxs-lookup"><span data-stu-id="91cfc-121">For more information about how to create a web installation of a Windows Installer package, see [Internet Download Bootstrapping](internet-download-bootstrapping.md).</span></span>

## <a name="available-internet-protocols"></a><span data-ttu-id="91cfc-122">Verfügbare Internet Protokolle</span><span class="sxs-lookup"><span data-stu-id="91cfc-122">Available Internet Protocols</span></span>

<span data-ttu-id="91cfc-123">Ab Windows Server 2003 und Windows XP kann das Installationsprogramm die HTTP-, HTTPS-und Datei Protokolle verwenden.</span><span class="sxs-lookup"><span data-stu-id="91cfc-123">Beginning with Windows Server 2003 and Windows XP, the installer can use the HTTP, HTTPS and FILE protocols.</span></span> <span data-ttu-id="91cfc-124">Das Installationsprogramm unterstützt das FTP-und das Gopher-Protokoll nicht.</span><span class="sxs-lookup"><span data-stu-id="91cfc-124">The installer does not support the FTP and GOPHER protocols.</span></span>

<span data-ttu-id="91cfc-125">In Windows Installer Version 2,0 können http-, Datei-und FTP-Protokolle verwendet werden. die Protokolle HTTPS und Gopher können nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="91cfc-125">Windows Installer version 2.0 can use the HTTP, FILE, and FTP protocols and cannot use the HTTPS and GOPHER protocols.</span></span>

 

 



