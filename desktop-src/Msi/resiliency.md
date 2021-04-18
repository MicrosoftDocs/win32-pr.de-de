---
description: Resilienz ist die Fähigkeit einer Anwendung, ordnungsgemäß aus Situationen wiederherzustellen, in denen eine wichtige Komponente fehlt oder durch eine nicht kompatible Version ersetzt wurde.
ms.assetid: c0504a84-6d51-4734-a55d-f1d1ebcb3e73
title: Resilienz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc6d57e5c5a342a8e1c295afd97a69fe2828362a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352489"
---
# <a name="resiliency"></a><span data-ttu-id="2b991-103">Resilienz</span><span class="sxs-lookup"><span data-stu-id="2b991-103">Resiliency</span></span>

<span data-ttu-id="2b991-104">Resilienz ist die Fähigkeit einer Anwendung, ordnungsgemäß aus Situationen wiederherzustellen, in denen eine wichtige Komponente fehlt oder durch eine nicht kompatible Version ersetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="2b991-104">Resiliency is the ability of an application to recover gracefully from situations in which a vital component is missing, or has been replaced by an incompatible version.</span></span> <span data-ttu-id="2b991-105">Durch die Erstellung eines Installationspakets und die Verwendung der [Installer-Funktionen](installer-functions.md)können Entwickler die Windows Installer verwenden, um robuste Anwendungen zu erstellen, die aus solchen Situationen wieder hergestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="2b991-105">By authoring an installation package and using the [Installer Functions](installer-functions.md), developers can use the Windows Installer to produce resilient applications capable of recovering from such situations.</span></span>

-   <span data-ttu-id="2b991-106">Verwenden Sie die Quell Liste des Installers, um die Resilienz von Anwendungen zu erhöhen, die auf Netzwerkressourcen basieren.</span><span class="sxs-lookup"><span data-stu-id="2b991-106">Use the installer's source list to increase the resiliency of applications that rely on network resources.</span></span> <span data-ttu-id="2b991-107">Weitere Informationen finden Sie unter [Quellen Resilienz](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="2b991-107">For more information, see [Source Resiliency](source-resiliency.md).</span></span>
-   <span data-ttu-id="2b991-108">Verwenden Sie die-API des Installers, um zu überprüfen, ob ein wichtiges Feature, eine Komponente, eine Datei oder eine Dateiversion installiert ist.</span><span class="sxs-lookup"><span data-stu-id="2b991-108">Use the installer's API to check whether a vital feature, component, file, or file version is installed.</span></span>
-   <span data-ttu-id="2b991-109">Verwenden Sie die-API des Installers, um den Pfad zu einer Komponente zur Laufzeit zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="2b991-109">Use the installer's API to check the path to a component at run time.</span></span> <span data-ttu-id="2b991-110">Dadurch wird die Abhängigkeit ihrer Anwendung von statischen Dateipfaden verringert, die sich häufig zwischen den Computern unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="2b991-110">This reduces your application's dependency on static file paths, which commonly differ between computers.</span></span>
-   <span data-ttu-id="2b991-111">Verwenden Sie das Installationsprogramm, um beschädigte Verknüpfungen, Registrierungseinträge und andere Komponenten neu zu installieren, ohne Setup erneut ausführen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="2b991-111">Use the installer to reinstall damaged shortcuts, registry entries, and other components without having to rerun setup.</span></span>
-   <span data-ttu-id="2b991-112">Erhöhen Sie die Resilienz der Installation des Produkts, indem Sie die Roll Back Funktion des Installers aktivieren.</span><span class="sxs-lookup"><span data-stu-id="2b991-112">Increase the resiliency of your product's installation by leaving the rollback capability of the installer enabled.</span></span> <span data-ttu-id="2b991-113">Weitere Informationen finden Sie unter [Rollback-Installation](rollback-installation.md).</span><span class="sxs-lookup"><span data-stu-id="2b991-113">For more information, see [Rollback Installation](rollback-installation.md).</span></span>

 

 



