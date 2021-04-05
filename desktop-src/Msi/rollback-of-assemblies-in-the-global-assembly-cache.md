---
description: Ein zweistufiger Prozess erweitert das Transaktionsmodell des Windows Installer auf Produkte, die Common Language Runtime Assemblys enthalten. Dadurch kann das Installationsprogramm nicht erfolgreiche Installationen und Entfernungen von Assemblys zurücksetzen.
ms.assetid: 065a380c-4eb5-48a5-ab0a-7f1229b77898
title: Rollback von Assemblys im globalen Assemblycache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c84bc3107355cb50c17043ee571edff708ba3f6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751120"
---
# <a name="rollback-of-assemblies-in-the-global-assembly-cache"></a><span data-ttu-id="c5323-104">Rollback von Assemblys im globalen Assemblycache</span><span class="sxs-lookup"><span data-stu-id="c5323-104">Rollback of Assemblies in the Global Assembly Cache</span></span>

<span data-ttu-id="c5323-105">Ein zweistufiger Prozess erweitert das Transaktionsmodell des Windows Installer auf Produkte, die Common Language Runtime Assemblys enthalten.</span><span class="sxs-lookup"><span data-stu-id="c5323-105">A two-step process extends the Windows Installer's transaction model to products containing common language runtime assemblies.</span></span> <span data-ttu-id="c5323-106">Dadurch kann das Installationsprogramm nicht erfolgreiche Installationen und Entfernungen von Assemblys zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="c5323-106">This enables the installer to rollback unsuccessful installations and removals of assemblies.</span></span>

<span data-ttu-id="c5323-107">Im ersten Schritt verwendet die Windows Installer das Microsoft .NET Framework, um eine Schnittstelle für jede Assembly zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c5323-107">During the first step, the Windows Installer uses the Microsoft .NET Framework to create one interface for each assembly.</span></span> <span data-ttu-id="c5323-108">Die Windows Installer verwendet so viele Schnittstellen, wie Assemblys installiert werden.</span><span class="sxs-lookup"><span data-stu-id="c5323-108">The Windows Installer uses as many interfaces as there are assemblies being installed.</span></span> <span data-ttu-id="c5323-109">Das Ausführen eines Commits für eine Assembly über eine dieser Schnittstellen bedeutet lediglich, dass die Assembly bereit ist, vorhandene Assemblys mit demselben Namen zu ersetzen, Sie wird jedoch noch nicht ersetzt.</span><span class="sxs-lookup"><span data-stu-id="c5323-109">Committing an assembly using one of these interfaces only means that the assembly is ready to replace any existing assembly with the same name, it does not yet replace it.</span></span> <span data-ttu-id="c5323-110">Wenn der Benutzer die Installation abbricht oder ein schwerwiegender Installationsfehler vorliegt, kann die Windows Installer weiterhin die Assembly auf den vorherigen Zustand zurücksetzen, indem Sie diese Schnittstellen freigeben.</span><span class="sxs-lookup"><span data-stu-id="c5323-110">If the user cancels the installation, or if there is a fatal installation error, the Windows Installer can still rollback the assembly to its previous state by releasing these interfaces.</span></span>

<span data-ttu-id="c5323-111">Nachdem der Windows Installer die Installation aller Assemblys und Windows Installer Komponenten abgeschlossen hat, kann das Installationsprogramm den zweiten Schritt der Installation einleiten.</span><span class="sxs-lookup"><span data-stu-id="c5323-111">After the Windows Installer completes installing all assemblies and Windows Installer components, the installer may initiate the second step of the installation.</span></span> <span data-ttu-id="c5323-112">Im zweiten Schritt wird eine separate Funktion verwendet, um den endgültigen Commit aller neuen Common Language Runtime Assemblys durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="c5323-112">The second step uses a separate function to do the final commit of all the new common language runtime assemblies.</span></span> <span data-ttu-id="c5323-113">Dadurch werden alle vorhandenen Assemblys mit demselben Namen ersetzt.</span><span class="sxs-lookup"><span data-stu-id="c5323-113">This replaces any existing assemblies with the same name.</span></span>

 

 



