---
title: Replikations Verhalten in Active Directory Domain Services
description: Replikations Verhalten ist konsistent und vorhersagbar. Wenn ein bestimmtes Replikat eine Reihe von Änderungen enthält, kann das Ergebnis vorhergesagt werden 8212; die Änderungen werden an alle anderen Replikate weitergegeben.
ms.assetid: 4e9f2e43-6375-4663-93ca-55112fd00abe
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services Active Directory, Replikation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41009a733f99366e499a25baca989f4f28794aea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855387"
---
# <a name="replication-behavior-in-active-directory-domain-services"></a><span data-ttu-id="b9f32-104">Replikations Verhalten in Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="b9f32-104">Replication Behavior in Active Directory Domain Services</span></span>

<span data-ttu-id="b9f32-105">Replikations Verhalten ist konsistent und vorhersagbar. Wenn ein bestimmtes Replikat eine Reihe von Änderungen enthält, kann das Ergebnis vorhergesagt werden – die Änderungen werden an alle anderen Replikate weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="b9f32-105">Replication behavior is consistent and predictable; given a set of changes to a given replica, the outcome can be predicted—the changes will be propagated to all other replicas.</span></span> <span data-ttu-id="b9f32-106">Die Entwicklung eines zuverlässigen allgemeinen Modells für die Vorhersage, wann die Änderungen auf alle anderen Replikate oder auf ein bestimmtes Replikat angewendet werden, ist nicht möglich, da der zukünftige Status des verteilten Systems als Ganzes nicht bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="b9f32-106">Devising a reliable general model for predicting when the changes will be applied at all other replicas, or at a particular replica, is impossible, because the future state of the distributed system as a whole cannot be known.</span></span> <span data-ttu-id="b9f32-107">Dies wird als "nicht deterministische Latenz" bezeichnet, und Anwendungen, die das Verzeichnis verwenden, müssen es verstehen und zulassen.</span><span class="sxs-lookup"><span data-stu-id="b9f32-107">This is called "nondeterministic latency," and applications that use the directory must understand and allow for it.</span></span>

<span data-ttu-id="b9f32-108">Die Situation ist nicht so komplex, dass Sie möglicherweise angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b9f32-108">The situation is not as complex at it might appear.</span></span> <span data-ttu-id="b9f32-109">Es gibt nur drei Zustände, die eine Anwendung erfüllen muss:</span><span class="sxs-lookup"><span data-stu-id="b9f32-109">There are only three states that an application must accommodate:</span></span>

-   <span data-ttu-id="b9f32-110">Versions Schiefe: keine der Änderungen, die auf ein bestimmtes Quell Replikat angewendet werden, wurde an ein bestimmtes Ziel Replikat weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="b9f32-110">Version Skew: None of the changes that are applied to a given source replica have propagated to a given destination replica.</span></span> <span data-ttu-id="b9f32-111">Eine Anwendung, die das Quell Replikat liest, sieht die neue Version der Informationen, während eine Anwendung, die das Ziel liest, die alte Version sieht (oder nichts, wenn die neuen Informationen zum ersten Mal hinzugefügt wurden).</span><span class="sxs-lookup"><span data-stu-id="b9f32-111">An application reading the source replica sees the new version of the information, while an application reading the destination sees the old version (or nothing, if the new information was added for the first time).</span></span> <span data-ttu-id="b9f32-112">Die Versions Neigung gilt für alle Verzeichnis Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="b9f32-112">Version skew applies to all directory service consumers.</span></span>
-   <span data-ttu-id="b9f32-113">Teilweises Update: einige der Änderungen, die auf ein bestimmtes Quell Replikat angewendet werden, wurden an ein bestimmtes Ziel Replikat weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="b9f32-113">Partial Update: Some of the changes that are applied to a given source replica have propagated to a given destination replica.</span></span> <span data-ttu-id="b9f32-114">Bei einer Anwendung, die das Quell Replikat liest, werden die neuen Informationen angezeigt, während eine Anwendung, die das Ziel liest, eine Mischung aus alten und neuen Informationen (oder nur einige der neuen Informationen) sieht, wenn die neuen Informationen zum ersten Mal hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="b9f32-114">An application reading the source replica sees the new information, while an application reading the destination sees a mix of old and new information (or only some of the new information, if the new information was added for the first time).</span></span> <span data-ttu-id="b9f32-115">Teil Updates gelten für Verzeichnis Dienstanbieter, die zwei oder mehr verwandte Objekte zum Speichern Ihrer Informationen verwenden.</span><span class="sxs-lookup"><span data-stu-id="b9f32-115">Partial update applies to directory service consumers that use two or more related objects to store their information.</span></span>
-   <span data-ttu-id="b9f32-116">Vollständig replizierter Status: alle Änderungen, die auf ein bestimmtes Quell Replikat angewendet werden, wurden an ein bestimmtes Ziel Replikat weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="b9f32-116">Fully Replicated State: All of the changes that are applied to a given source replica have propagated to a given destination replica.</span></span> <span data-ttu-id="b9f32-117">Anwendungen an den Quell-und Ziel Replikaten sehen die gleichen Informationen.</span><span class="sxs-lookup"><span data-stu-id="b9f32-117">Applications at the source and destination replicas see the same information.</span></span>

 

 




