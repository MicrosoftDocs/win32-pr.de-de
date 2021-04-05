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
# <a name="installing-the-provider"></a><span data-ttu-id="b26c5-104">Installieren des Anbieters</span><span class="sxs-lookup"><span data-stu-id="b26c5-104">Installing the Provider</span></span>

<span data-ttu-id="b26c5-105">Die Vorgehensweise zum Installieren des DNS-WMI-Anbieters unterscheidet sich abhängig von der Windows-Version, auf der Sie installiert ist.</span><span class="sxs-lookup"><span data-stu-id="b26c5-105">The procedure for installing the DNS WMI Provider differs based on the version of Windows on which it is installed.</span></span> <span data-ttu-id="b26c5-106">Im folgenden Verfahren wird beschrieben, wie der DNS-WMI-Anbieter unter Windows 2000 installiert und eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="b26c5-106">The following procedure describes how to install and set up the DNS WMI Provider on Windows 2000.</span></span> <span data-ttu-id="b26c5-107">Um den DNS-WMI-Anbieter für Windows 2000 zu erhalten, laden Sie die folgende Datei herunter:</span><span class="sxs-lookup"><span data-stu-id="b26c5-107">To obtain the DNS WMI Provider for Windows 2000, download the following file:</span></span>

<span data-ttu-id="b26c5-108">**Warnung:** DNS-WMI-Anbieter Dateien sind nicht austauschbar.</span><span class="sxs-lookup"><span data-stu-id="b26c5-108">**WARNING:** DNS WMI Provider files are not interchangeable.</span></span> <span data-ttu-id="b26c5-109">Für Windows 2000-DNS-Server sind unterschiedliche Dateien und eine andere Prozedur als Windows Server 2003 DNS-Server erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b26c5-109">Windows 2000 DNS Servers require different files and a different procedure than Windows Server 2003 DNS Servers.</span></span> <span data-ttu-id="b26c5-110">Das jeweilige Verfahren wird bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="b26c5-110">The procedure for each is provided.</span></span>

<span data-ttu-id="b26c5-111">**So installieren Sie den DNS-WMI-Anbieter unter Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b26c5-111">**To install the DNS WMI Provider on Windows 2000 Server**</span></span>

1.  <span data-ttu-id="b26c5-112">Rufen Sie den DNS-WMI-Anbieter für Windows 2000 aus dem Windows 2000 Server Resource Kit ab, oder laden Sie die Datei Dnsprov.zip herunter, von: FTP://FTP.Microsoft.com/reskit/Win2000/</span><span class="sxs-lookup"><span data-stu-id="b26c5-112">Obtain the DNS WMI Provider for Windows 2000 from the Windows 2000 Server Resource Kit, or download the file, Dnsprov.zip, from: ftp://ftp.microsoft.com/reskit/win2000/</span></span>
2.  <span data-ttu-id="b26c5-113">Kopieren Sie den DNS-WMI-Anbieter (Dnsprov.dll) und die Datei dnsschema. MOF in das <winntdir> \\ \\ Verzeichnis System32 WBEM.</span><span class="sxs-lookup"><span data-stu-id="b26c5-113">Copy the DNS WMI Provider (Dnsprov.dll) and Dnsschema.mof files to the <winntdir>\\system32\\wbem directory.</span></span>
3.  <span data-ttu-id="b26c5-114">Kompilieren Sie die MOF-Datei.</span><span class="sxs-lookup"><span data-stu-id="b26c5-114">Compile the MOF file.</span></span> <span data-ttu-id="b26c5-115">Dadurch wird das Schema so angepasst, dass es dem Server entspricht.</span><span class="sxs-lookup"><span data-stu-id="b26c5-115">Doing so customizes the schema to match the server.</span></span>

    <span data-ttu-id="b26c5-116">**"wmacomp dnsschema. mof"**</span><span class="sxs-lookup"><span data-stu-id="b26c5-116">**mofcomp dnsschema.mof**</span></span>

4.  <span data-ttu-id="b26c5-117">Registrieren Sie die dll auf dem DNS-Server.</span><span class="sxs-lookup"><span data-stu-id="b26c5-117">Register the DLL on the DNS Server.</span></span>

    <span data-ttu-id="b26c5-118">**regsvr32 dnsprov.dll**</span><span class="sxs-lookup"><span data-stu-id="b26c5-118">**regsvr32 dnsprov.dll**</span></span>

5.  <span data-ttu-id="b26c5-119">Skripts oder Programme, die zum Verwalten von DNS-Servern den DNS-WMI-Anbieter verwenden, können dann verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b26c5-119">Scripts or programs that use the DNS WMI Provider to manage DNS Servers can then be used.</span></span> <span data-ttu-id="b26c5-120">Die Skripts oder Programme können entweder vom DNS-Server oder von einem Client Computer aus ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b26c5-120">The scripts or programs can be run from either the DNS Server, or from a client computer.</span></span>
    > [!Note]  
    > <span data-ttu-id="b26c5-121">Das WMI-SDK ist nicht erforderlich, um den DNS-WMI-Anbieter auszuführen, aber es enthält viele nützliche Tools.</span><span class="sxs-lookup"><span data-stu-id="b26c5-121">The WMI SDK is not required to run the DNS WMI Provider, but it contains many useful tools.</span></span>

     

<span data-ttu-id="b26c5-122">Der DNS-WMI-Anbieter muss auf jedem zu verwaltenden DNS-Server installiert sein. die DNS-Skripts können jedoch auf dem DNS-Server oder auf einem Remote Host ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b26c5-122">The DNS WMI Provider must be installed on any DNS Server to be managed; the DNS scripts, however, can be run on the DNS Server or on a remote host.</span></span>

<span data-ttu-id="b26c5-123">**So installieren Sie den DNS-WMI-Anbieter unter Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b26c5-123">**To install the DNS WMI Provider on Windows Server 2003**</span></span>

-   <span data-ttu-id="b26c5-124">Bei Windows Server 2003-Betriebssystemen wird der DNS-WMI-Anbieter automatisch installiert und registriert, und die zugehörige MOF-Datei wird bei der Installation des DNS-Server Dienstanbieters kompiliert.</span><span class="sxs-lookup"><span data-stu-id="b26c5-124">For Windows Server 2003 operating systems, the DNS WMI Provider is automatically installed and registered, and its MOF file is compiled when the DNS Server service is installed.</span></span>

 

 




