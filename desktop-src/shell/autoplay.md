---
description: Autorun ist eine Funktion des Windows-Betriebssystems.
title: Erstellen einer Autorun-aktivierten CD-ROM-Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 5c583c1d-a4eb-4291-a839-c1ca7c51342c
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 33f3ccc0a253690cd377cad908f87b43ac1ea304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214444"
---
# <a name="creating-an-autorun-enabled-cd-rom-application"></a><span data-ttu-id="b02ca-103">Erstellen einer Autorun-aktivierten CD-ROM-Anwendung</span><span class="sxs-lookup"><span data-stu-id="b02ca-103">Creating an AutoRun-enabled CD-ROM Application</span></span>

<span data-ttu-id="b02ca-104">Autorun ist eine Funktion des Windows-Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="b02ca-104">AutoRun is a feature of the Windows operating system.</span></span> <span data-ttu-id="b02ca-105">Es automatisiert die Verfahren zum Installieren und Konfigurieren von Produkten, die für Windows-basierte Plattformen entworfen wurden, die auf CD-ROMs verteilt sind.</span><span class="sxs-lookup"><span data-stu-id="b02ca-105">It automates the procedures for installing and configuring products designed for Windows-based platforms that are distributed on CD-ROMs.</span></span> <span data-ttu-id="b02ca-106">Wenn Benutzer eine autornicht aktivierte Compact-CD in das CD-ROM-Laufwerk einfügen, führt Autorun automatisch eine Anwendung auf der CD-ROM aus, die das ausgewählte Produkt installiert, konfiguriert oder ausführt.</span><span class="sxs-lookup"><span data-stu-id="b02ca-106">When users insert an AutoRun-enabled compact disc into their CD-ROM drive, AutoRun automatically runs an application on the CD-ROM that installs, configures, or runs the selected product.</span></span>

<span data-ttu-id="b02ca-107">Autorun kann zum Installieren und Ausführen von CD-ROM-Anwendungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b02ca-107">AutoRun can be used to install and run CD-ROM applications.</span></span> <span data-ttu-id="b02ca-108">Obwohl Autorun am häufigsten für Windows-Anwendungen verwendet wird, kann es auch zum Installieren, konfigurieren oder Ausführen von MS-DOS-basierten Anwendungen in einer Windows-MS-DOS-Sitzung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b02ca-108">Although AutoRun is most commonly used for Windows applications, it can also be used to install, configure, or run MS-DOS-based applications in a Windows Microsoft MS-DOS session.</span></span> <span data-ttu-id="b02ca-109">Sie können jede MS-DOS-basierte Anwendung mit einem eigenen eindeutigen Symbol, Config.sys Datei und Autoexec.bat Datei konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="b02ca-109">You can configure each MS-DOS-based application with its own unique icon, Config.sys file, and Autoexec.bat file.</span></span> <span data-ttu-id="b02ca-110">Windows erstellt die richtigen Konfigurationsdateien für die MS-DOS-basierte Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b02ca-110">Windows creates the correct configuration files for the MS-DOS-based application.</span></span> <span data-ttu-id="b02ca-111">Die Start Anwendung startet dann die MS-DOS-basierte Anwendung in einem-Fenster.</span><span class="sxs-lookup"><span data-stu-id="b02ca-111">The startup application then starts the MS-DOS-based application in a window.</span></span>

> [!Note]  
> <span data-ttu-id="b02ca-112">Damit Autorun funktioniert, muss das CD-ROM-Laufwerk über 32-oder 64-Bit-Gerätetreiber verfügen, die erkennen, wenn ein Benutzer eine kompakte CD einfügt und das System benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="b02ca-112">For AutoRun to work, the CD-ROM drive must have 32 or 64-bit device drivers that detect when a user inserts a compact disc and notify the system.</span></span>

 

<span data-ttu-id="b02ca-113">In den folgenden Abschnitten wird erläutert, wie eine Autorun-fähige CD-ROM-Anwendung implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="b02ca-113">The following sections discuss how to implement an AutoRun-enabled CD-ROM application.</span></span>

-   [<span data-ttu-id="b02ca-114">Erstellen einer AutoRun-Enabled Anwendung</span><span class="sxs-lookup"><span data-stu-id="b02ca-114">Creating an AutoRun-Enabled Application</span></span>](autoplay-works.md)
-   [<span data-ttu-id="b02ca-115">Autorun. inf-Einträge</span><span class="sxs-lookup"><span data-stu-id="b02ca-115">Autorun.inf Entries</span></span>](autorun-cmds.md)
-   [<span data-ttu-id="b02ca-116">Aktivieren und Deaktivieren von Autorun</span><span class="sxs-lookup"><span data-stu-id="b02ca-116">Enabling and Disabling AutoRun</span></span>](autoplay-reg.md)

 

 



