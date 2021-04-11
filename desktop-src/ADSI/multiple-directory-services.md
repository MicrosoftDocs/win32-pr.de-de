---
title: Mehrere Verzeichnisdienste
description: Eine Herausforderung bei der Arbeit in einer verteilten Computerumgebung besteht darin, Ressourcen wie Benutzer, Gruppen, Druck Warteschlangen und Dokumente zu identifizieren und zu suchen.
ms.assetid: 66929290-b830-4768-a2ae-604d1a9de5c4
ms.tgt_platform: multiple
keywords:
- ADSI für mehrere Verzeichnisdienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccc2e174fc1b07564f1cca6c12093a289a0c865a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309247"
---
# <a name="multiple-directory-services"></a><span data-ttu-id="35282-104">Mehrere Verzeichnisdienste</span><span class="sxs-lookup"><span data-stu-id="35282-104">Multiple Directory Services</span></span>

<span data-ttu-id="35282-105">Eine Herausforderung bei der Arbeit in einer verteilten Computerumgebung besteht darin, Ressourcen wie Benutzer, Gruppen, Druck Warteschlangen und Dokumente zu identifizieren und zu suchen.</span><span class="sxs-lookup"><span data-stu-id="35282-105">One challenge of working within a distributed computing environment is identifying and locating resources such as users, groups, print queues, and documents.</span></span> <span data-ttu-id="35282-106">Ein Verzeichnisdienst ist der Teil einer verteilten Computerumgebung, die eine Möglichkeit bietet, die im System verfügbaren Benutzer und Ressourcen zu finden und zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="35282-106">A directory service is the part of a distributed computing environment that provides a way to locate and identify the users and resources available in the system.</span></span> <span data-ttu-id="35282-107">Ein Verzeichnisdienst ist wie ein Telefonverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="35282-107">A directory service is like a phone directory.</span></span> <span data-ttu-id="35282-108">Wenn ein Name für eine Person oder eine Ressource angegeben ist, werden die Daten bereitgestellt, die für den Zugriff auf diese Person oder Ressource erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="35282-108">Given a name for a person or a resource, it provides the data necessary to access that person or resource.</span></span> <span data-ttu-id="35282-109">Sie müssen nicht mit der Bindung von Daten beginnen, um auf eine Ressource im Netzwerk zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="35282-109">You do not have to start with binding data to access a resource on the network.</span></span>

<span data-ttu-id="35282-110">Die meisten Unternehmen verfügen bereits über viele verschiedene Verzeichnisse.</span><span class="sxs-lookup"><span data-stu-id="35282-110">Most enterprises already have many different directories in place.</span></span> <span data-ttu-id="35282-111">Beispielsweise verfügen Netzwerk Betriebssysteme, elektronische e-Mail-Systeme und "Groupware"-Produkte über eigene Verzeichnisse.</span><span class="sxs-lookup"><span data-stu-id="35282-111">For example, network operating systems, electronic mail systems, and "groupware" products all have their own directories.</span></span> <span data-ttu-id="35282-112">Viele Probleme treten auf, wenn ein einzelnes Unternehmen mehrere Verzeichnisse bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="35282-112">Many issues arise when a single enterprise deploys multiple directories.</span></span> <span data-ttu-id="35282-113">Diese Probleme umfassen u. a. Nutzbarkeit, Datenkonsistenz, Entwicklungskosten und Supportkosten.</span><span class="sxs-lookup"><span data-stu-id="35282-113">These issues include usability, data consistency, development cost, and support cost, among others.</span></span>

<span data-ttu-id="35282-114">Diese Probleme werden in ADSI behoben, da es einen einzelnen, konsistenten, offenen Satz von Schnittstellen gibt, der zum Verwalten und Verwenden eines beliebigen Verzeichnis Dienstanbieters mit einem ADSI-Anbieter verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="35282-114">These issues are addressed in ADSI, in that there is provided a single, consistent, open set of interfaces that can be used for managing and using any directory service that has an ADSI provider.</span></span>

 

 




