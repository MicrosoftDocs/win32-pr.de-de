---
title: Installieren und Konfigurieren von RPC-Anwendungen
description: Wenn das Microsoft Windows-Betriebssystem auf einem Server oder Client installiert ist, werden die RPC-Laufzeitdateien von Setup automatisch installiert.
ms.assetid: cfcada3d-cf7c-42a9-9ed4-0b1bba7a98cf
keywords:
- Remote Prozedur Aufruf RPC, Tasks, installieren und Konfigurieren von Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90837261c571276a74bb3a5354c7b9a5db2da6cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471757"
---
# <a name="installing-and-configuring-rpc-applications"></a><span data-ttu-id="7c0c5-104">Installieren und Konfigurieren von RPC-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="7c0c5-104">Installing and Configuring RPC Applications</span></span>

<span data-ttu-id="7c0c5-105">Wenn das Microsoft Windows-Betriebssystem auf einem Server oder Client installiert ist, werden die RPC-Laufzeitdateien von Setup automatisch installiert.</span><span class="sxs-lookup"><span data-stu-id="7c0c5-105">When the Microsoft Windows operating system is installed on a server or client, setup automatically installs the RPC run-time files.</span></span> <span data-ttu-id="7c0c5-106">Es ist keine weitere RPC-Installation erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7c0c5-106">No further RPC installation is required.</span></span> <span data-ttu-id="7c0c5-107">Sie müssen jedoch sicherstellen, dass die von Ihnen installierte Version von Windows alle Features unterstützt, die in der verteilten Anwendung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7c0c5-107">You must ensure, however, that the version of Windows you install supports all the features used in your distributed application.</span></span>

<span data-ttu-id="7c0c5-108">Wenn Sie eine RPC-Anwendung auf einem Windows 3. x-oder Microsoft MS-DOS-Betriebssystem verwenden, müssen Sie die ausführbaren RPC-Laufzeitdateien auf die Windows 3. x-oder MS-DOS-Computer kopieren, die die Anwendung verwenden werden.</span><span class="sxs-lookup"><span data-stu-id="7c0c5-108">When you use an RPC application on a Windows 3.x or Microsoft MS-DOS operating system, you must copy the RPC run-time executable files to the Windows 3.x or MS-DOS computers that will be using the application.</span></span> <span data-ttu-id="7c0c5-109">Das Verzeichnis \\ msetups \\ RPC \_ rt16 auf der Platform Software Development Kit (SDK)-CD enthält ein Datenträger Abbild dieser Dateien zusammen mit einem Setup Programm, um die Dateien zu installieren.</span><span class="sxs-lookup"><span data-stu-id="7c0c5-109">The directory \\mstools\\rpc\_rt16 on the Platform Software Development Kit (SDK) CD contains a disk image of these files along with a setup program to install the files.</span></span> <span data-ttu-id="7c0c5-110">Verwenden Sie dieses Datenträger Image zum Erstellen eines Installations Datenträgers für die Verteilung mit der RPC-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="7c0c5-110">Use this disk image to create an install disk for distribution with your RPC application.</span></span> <span data-ttu-id="7c0c5-111">Sie können auch 16-Bit-Client Anwendungen verwenden, die auf MS-DOS oder Windows auf einem 32-Bit-oder 64-Bit-Windows-Betriebssystem ausgerichtet sind.</span><span class="sxs-lookup"><span data-stu-id="7c0c5-111">You can also use 16-bit client applications targeted toward MS-DOS or Windows on a 32-bit/64-bit Windows operating system.</span></span> <span data-ttu-id="7c0c5-112">Allerdings muss das Installationsprogramm Ihrer Anwendung die ausführbaren Dateien installieren, die in diesem Datenträger Image enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="7c0c5-112">However, your application's installation program must install the executable files contained in this disk image.</span></span>

<span data-ttu-id="7c0c5-113">Wenn Sie eine RPC-Anwendung für einen Macintosh-Client erstellen, müssen Sie die erforderlichen Dateien zum Zeitpunkt der Erstellung mit der Anwendung verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="7c0c5-113">When you build an RPC application for a Macintosh client, you must link the necessary files to the application at build time.</span></span> <span data-ttu-id="7c0c5-114">Es ist keine zusätzliche RPC-Installation erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7c0c5-114">No additional RPC installation is needed.</span></span>

<span data-ttu-id="7c0c5-115">Weitere Informationen zu verteilbaren Dateien und Lizenzverträgen finden Sie unter \\ Lizenz \\Redist.txt und \\ Lizenz \\License.txt auf der Plattform-SDK-CD.</span><span class="sxs-lookup"><span data-stu-id="7c0c5-115">For more details about redistributable files and licensing agreements, see \\LICENSE\\Redist.txt and \\LICENSE\\License.txt on the Platform SDK CD.</span></span>

<span data-ttu-id="7c0c5-116">Dieser Abschnitt enthält Informationen zum Einrichten von RPC-Anwendungen auf einer Vielzahl von Hardware-und Softwareplattformen.</span><span class="sxs-lookup"><span data-stu-id="7c0c5-116">This section contains information about setting up RPC applications on a variety of hardware and software platforms.</span></span> <span data-ttu-id="7c0c5-117">Die Diskussion ist in den folgenden Abschnitten dargestellt:</span><span class="sxs-lookup"><span data-stu-id="7c0c5-117">It presents the discussion in the following sections:</span></span>

-   [<span data-ttu-id="7c0c5-118">Konfigurieren des Name Service-Anbieters</span><span class="sxs-lookup"><span data-stu-id="7c0c5-118">Configuring the Name Service Provider</span></span>](configuring-the-name-service-provider.md)
-   [<span data-ttu-id="7c0c5-119">Registrierungsinformationen</span><span class="sxs-lookup"><span data-stu-id="7c0c5-119">Registry Information</span></span>](registry-information.md)
-   [<span data-ttu-id="7c0c5-120">Verwenden von RPC mit Winsock-Proxy</span><span class="sxs-lookup"><span data-stu-id="7c0c5-120">Using RPC with Winsock Proxy</span></span>](using-rpc-with-winsock-proxy.md)
-   [<span data-ttu-id="7c0c5-121">SPX/IPX-Installation</span><span class="sxs-lookup"><span data-stu-id="7c0c5-121">SPX/IPX Installation</span></span>](spx-ipx-installation.md)
-   [<span data-ttu-id="7c0c5-122">Konfigurieren des Sicherheits Servers</span><span class="sxs-lookup"><span data-stu-id="7c0c5-122">Configuring the Security Server</span></span>](configuring-the-security-server.md)

 

 




