---
title: Informationen über Windows-Netzwerke
description: Anwendungen können die WNET-Funktionen zum Hinzufügen und Abbrechen von Netzwerkverbindungen und zum Abrufen von Informationen über die aktuelle Netzwerkkonfiguration verwenden.
ms.assetid: 37ce0762-b0b2-4d68-9942-b7034f1b76b7
keywords:
- WNET für Windows-Netzwerke, beschrieben
- WNET WNET, beschrieben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c91f7c8f58d4e44439bac18a2b7d7b850b21f955
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037568"
---
# <a name="about-windows-networking"></a><span data-ttu-id="f9f4f-105">Informationen über Windows-Netzwerke</span><span class="sxs-lookup"><span data-stu-id="f9f4f-105">About Windows Networking</span></span>

<span data-ttu-id="f9f4f-106">Anwendungen können die WNET-Funktionen zum Hinzufügen und Abbrechen von Netzwerkverbindungen und zum Abrufen von Informationen über die aktuelle Netzwerkkonfiguration verwenden.</span><span class="sxs-lookup"><span data-stu-id="f9f4f-106">Applications can use the WNet functions to add and cancel network connections and to retrieve information about the current configuration of the network.</span></span>

<span data-ttu-id="f9f4f-107">Die folgende Abbildung zeigt die Struktur eines typischen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="f9f4f-107">The following figure shows the structure of a typical network.</span></span>

![Typische Netzwerkstruktur](images/csnet-01.png)

<span data-ttu-id="f9f4f-109">In der obigen Abbildung wird die Hierarchie für Windows NT Server/Windows 2000-Server Ressourcen ausführlich als Netzwerkanbieter \# 1 angegeben.</span><span class="sxs-lookup"><span data-stu-id="f9f4f-109">In the preceding figure, the hierarchy for Windows NT Server/Windows 2000 Server resources is given in detail as Network provider \#1.</span></span> <span data-ttu-id="f9f4f-110">Netzwerkressourcen von anderen Anbietern verfügen über unterschiedliche hierarchische Systeme.</span><span class="sxs-lookup"><span data-stu-id="f9f4f-110">Network resources from other providers have different hierarchical systems.</span></span> <span data-ttu-id="f9f4f-111">Eine Anwendung benötigt keine Informationen über die Hierarchie, bevor Sie mit einem Netzwerk funktioniert.</span><span class="sxs-lookup"><span data-stu-id="f9f4f-111">An application does not need information about the hierarchy before it begins to work with a network.</span></span> <span data-ttu-id="f9f4f-112">Der Vorgang kann vom Netzwerk Stamm (d. h. der obersten Container Ressource) fortgesetzt werden, und es werden Informationen zu den Ressourcen des Netzwerks abgerufen, wenn die Informationen benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="f9f4f-112">It can proceed from the network root (that is, the topmost container resource) and retrieve information about the network's resources as the information is required.</span></span>

<span data-ttu-id="f9f4f-113">Netzwerkressourcen, die andere Ressourcen enthalten, werden als *Container* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="f9f4f-113">Network resources that contain other resources are called *containers*.</span></span> <span data-ttu-id="f9f4f-114">Container Ressourcen befinden sich in den Feldern in der obigen Abbildung.</span><span class="sxs-lookup"><span data-stu-id="f9f4f-114">Container resources are in boxes in the preceding figure.</span></span>

<span data-ttu-id="f9f4f-115">Ressourcen, die keine anderen Ressourcen enthalten, werden als *Objekte* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="f9f4f-115">Resources that do not contain other resources are called *objects*.</span></span> <span data-ttu-id="f9f4f-116">In der obigen Abbildung sind SharePoint \# 1 und SharePoint \# 2 Objekte.</span><span class="sxs-lookup"><span data-stu-id="f9f4f-116">In the preceding figure, Sharepoint \#1 and Sharepoint \#2 are objects.</span></span> <span data-ttu-id="f9f4f-117">Ein *SharePoint* ist ein Objekt, auf das über das Netzwerk zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="f9f4f-117">A *sharepoint* is an object that is accessible across the network.</span></span> <span data-ttu-id="f9f4f-118">Beispiele für Share Points sind Drucker und freigegebene Verzeichnisse.</span><span class="sxs-lookup"><span data-stu-id="f9f4f-118">Examples of sharepoints include printers and shared directories.</span></span>

 

 




