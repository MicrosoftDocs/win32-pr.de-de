---
title: Erkennen und vermeiden von Replikations Latenz
description: Die Replikations Latenz ist ein Fakt in einem locker gekoppelten verteilten System.
ms.assetid: ea65759b-2bfa-4859-8d2a-5949bbb9adef
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 271b4d84689068824a6e46095a5ed93462f49e2f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707721"
---
# <a name="detecting-and-avoiding-replication-latency"></a><span data-ttu-id="02ecf-103">Erkennen und vermeiden von Replikations Latenz</span><span class="sxs-lookup"><span data-stu-id="02ecf-103">Detecting and Avoiding Replication Latency</span></span>

<span data-ttu-id="02ecf-104">Die Replikations Latenz ist ein Fakt in einem locker gekoppelten verteilten System.</span><span class="sxs-lookup"><span data-stu-id="02ecf-104">Replication latency is a fact of life in a loosely coupled distributed system.</span></span> <span data-ttu-id="02ecf-105">Anwendungen müssen dies aufnehmen.</span><span class="sxs-lookup"><span data-stu-id="02ecf-105">Applications must accommodate this.</span></span> <span data-ttu-id="02ecf-106">Die beste Möglichkeit für die Replikations Latenz ist das Entwerfen von Anwendungen, um die Auswirkungen zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="02ecf-106">The best way to accommodate replication latency is to design applications to minimize the effects.</span></span> <span data-ttu-id="02ecf-107">Die ideale, Verzeichnis aktivierte Anwendung:</span><span class="sxs-lookup"><span data-stu-id="02ecf-107">The ideal directory-enabled application:</span></span>

-   <span data-ttu-id="02ecf-108">Hat keine Unterscheidung zu Versions Schiefe.</span><span class="sxs-lookup"><span data-stu-id="02ecf-108">Is insensitive to version skew.</span></span>
-   <span data-ttu-id="02ecf-109">Hängt nicht von Beziehungen zwischen mehreren Objekten ab.</span><span class="sxs-lookup"><span data-stu-id="02ecf-109">Does not depend on relationships among multiple objects.</span></span>
-   <span data-ttu-id="02ecf-110">Verfügt über keine internen oder Objekt übergreifenden Konsistenz Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="02ecf-110">Has no intra- or inter-object consistency requirements.</span></span>

<span data-ttu-id="02ecf-111">Anwendungen und Dienste, die diesem Profil entsprechen, müssen sich nicht mit der Replikations Latenz beschäftigen.</span><span class="sxs-lookup"><span data-stu-id="02ecf-111">Applications and services that fit this profile need not be concerned with replication latency.</span></span> <span data-ttu-id="02ecf-112">Andere Anwendungen müssen im Hinblick auf die Replikations Wartezeit entworfen werden.</span><span class="sxs-lookup"><span data-stu-id="02ecf-112">Other applications must be designed with replication latency in mind.</span></span> <span data-ttu-id="02ecf-113">Der Schlüssel zum Erfolg beim Entwerfen einer solchen Anwendung ist das Bewusstsein des Replikations Prozesses.</span><span class="sxs-lookup"><span data-stu-id="02ecf-113">The key to success in designing such an application is awareness of the replication process.</span></span> <span data-ttu-id="02ecf-114">Schritte zur Entwurfszeit zum Reduzieren von Objekt übergreifenden Abhängigkeiten und minimieren von Teil Update Fenstern werden zur Laufzeit große Dividenden bezahlen.</span><span class="sxs-lookup"><span data-stu-id="02ecf-114">Steps taken at design time to reduce inter-object dependencies and minimize partial update windows will pay large dividends at run time.</span></span> <span data-ttu-id="02ecf-115">Ansätze zum Umgang mit Replikations Latenz sind in zwei Klassen unterteilt – Vermeidungsstrategien, die die Auswirkungen von Latenz und Erkennungs Strategien verringern, die es einer Anwendung ermöglichen, von der Latenz verursachende Zustände zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="02ecf-115">Approaches to dealing with replication latency are divided into two classes—avoidance strategies that reduce the impact of latency and detection strategies that allow an application to detect latency-induced states.</span></span>

 

 




