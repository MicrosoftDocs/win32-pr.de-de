---
description: Parallele private Assemblys können verwendet werden, um Komponenten zu erstellen, die problemlos aktualisiert werden können, ohne auch die Hostinganwendung zu aktualisieren.
ms.assetid: 5a45ee79-3ae1-4e9b-a77e-d4209fb23fa8
title: Anwendungskomponenten werden aktualisiert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba559323c3272db96f0cd106f0fc61624519b770
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958846"
---
# <a name="updating-application-components"></a><span data-ttu-id="57666-103">Anwendungskomponenten werden aktualisiert</span><span class="sxs-lookup"><span data-stu-id="57666-103">Updating Application Components</span></span>

<span data-ttu-id="57666-104">Parallele private Assemblys können verwendet werden, um Komponenten zu erstellen, die problemlos aktualisiert werden können, ohne auch die Hostinganwendung zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="57666-104">Side-by-side private assemblies can be used to create components that can be easily updated without also updating the hosting application.</span></span> <span data-ttu-id="57666-105">Dies ermöglicht es einem aktualisierbaren Dienst, die aktualisierten Komponenten der Anwendung zu installieren, die Anwendung neu zu starten und die Anwendung die Änderungen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="57666-105">This allows an updating service to install the application's updated components, restart the application, and have the application use the changes.</span></span> <span data-ttu-id="57666-106">Wenn Anwendungs Manifeste verwendet werden, können die Funktionen von-Komponenten, die von einer Anwendung gehostet werden, aktualisiert werden, ohne dass der Code der Host Anwendung geändert werden muss.</span><span class="sxs-lookup"><span data-stu-id="57666-106">When using application manifests, the functionality of components hosted by an application can be updated without having to change the hosting application's code.</span></span>

<span data-ttu-id="57666-107">Diese Methode kann verwendet werden, um die Version der Ressourcen einer Anwendung zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="57666-107">This method can be used to update the version of an application's resources.</span></span> <span data-ttu-id="57666-108">Wenn eine Anwendung z. b. eine Assembly enthält, kann das Manifest der Anwendung eine Abhängigkeit von dieser Assembly angeben.</span><span class="sxs-lookup"><span data-stu-id="57666-108">For example, if an application contains an assembly, the application's manifest can specify a dependency on this assembly.</span></span> <span data-ttu-id="57666-109">Die Anwendung kann die Assembly abrufen, indem Sie [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) aufrufen, um die erforderlichen Dateien zu suchen und zu laden.</span><span class="sxs-lookup"><span data-stu-id="57666-109">The application can get the assembly by calling [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) to find and load the files it requires.</span></span> <span data-ttu-id="57666-110">Ein Updater muss einfach die neuesten Bits für die Assembly herunterladen, die nebeneinander mit einer früheren Version der Assembly vorhanden sein kann.</span><span class="sxs-lookup"><span data-stu-id="57666-110">An updater simply has to bring down the newest bits for the assembly, which can exist side-by-side with an earlier version of the assembly.</span></span>

 

 
