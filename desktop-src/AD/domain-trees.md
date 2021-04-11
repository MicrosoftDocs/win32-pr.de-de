---
title: Domänen Strukturen
description: Eine Domänen Struktur besteht aus mehreren Domänen, die über ein gemeinsames Schema und eine gemeinsame Konfiguration verfügen und einen zusammenhängenden Namespace bilden.
ms.assetid: 3deb4053-3124-4180-8ab0-35fff689a37e
ms.tgt_platform: multiple
keywords:
- Domänen Struktur Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a21d2b36968615fd4e92912fdd94246ef8dda0c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206278"
---
# <a name="domain-trees"></a><span data-ttu-id="fabda-104">Domänen Strukturen</span><span class="sxs-lookup"><span data-stu-id="fabda-104">Domain Trees</span></span>

<span data-ttu-id="fabda-105">Eine *Domänen* Struktur besteht aus mehreren Domänen, die über ein gemeinsames Schema und eine gemeinsame Konfiguration verfügen und einen zusammenhängenden Namespace bilden.</span><span class="sxs-lookup"><span data-stu-id="fabda-105">A *domain tree* is made up of several domains that share a common schema and configuration, forming a contiguous namespace.</span></span> <span data-ttu-id="fabda-106">Domänen in einer Struktur werden auch über Vertrauens Stellungen miteinander verknüpft.</span><span class="sxs-lookup"><span data-stu-id="fabda-106">Domains in a tree are also linked together by trust relationships.</span></span> <span data-ttu-id="fabda-107">Active Directory ist ein Satz aus einer oder mehreren Strukturen.</span><span class="sxs-lookup"><span data-stu-id="fabda-107">Active Directory is a set of one or more trees.</span></span>

<span data-ttu-id="fabda-108">Strukturen können auf zwei Arten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="fabda-108">Trees can be viewed two ways.</span></span> <span data-ttu-id="fabda-109">Eine Ansicht sind die Vertrauens Stellungen zwischen Domänen.</span><span class="sxs-lookup"><span data-stu-id="fabda-109">One view is the trust relationships between domains.</span></span> <span data-ttu-id="fabda-110">Die andere Ansicht ist der Namespace der Domänen Struktur.</span><span class="sxs-lookup"><span data-stu-id="fabda-110">The other view is the namespace of the domain tree.</span></span>

## <a name="viewing-trust-relationships"></a><span data-ttu-id="fabda-111">Anzeigen von Vertrauens Stellungen</span><span class="sxs-lookup"><span data-stu-id="fabda-111">Viewing Trust Relationships</span></span>

<span data-ttu-id="fabda-112">Sie können ein Diagramm einer Domänen Struktur basierend auf den einzelnen Domänen und der vorhandenen Vertrauensbeziehung zeichnen.</span><span class="sxs-lookup"><span data-stu-id="fabda-112">You can draw a diagram of a domain tree based on the individual domains and the existing trust relationship.</span></span>

<span data-ttu-id="fabda-113">Windows 2000 richtet Vertrauens Stellungen zwischen Domänen basierend auf dem Kerberos-Sicherheitsprotokoll ein.</span><span class="sxs-lookup"><span data-stu-id="fabda-113">Windows 2000 establishes trust relationships between domains based on the Kerberos security protocol.</span></span> <span data-ttu-id="fabda-114">Die Kerberos-Vertrauensstellung ist transitiv und hierarchisch – Wenn Domäne a Domäne b vertraut und Domäne b Domäne c vertraut, vertraut Domäne a Domäne c.</span><span class="sxs-lookup"><span data-stu-id="fabda-114">Kerberos trust is transitive and hierarchical—if domain A trusts domain B, and domain B trusts domain C, then domain A trusts domain C.</span></span>

![Vertrauensbeziehung der Domänen Struktur](images/domain-trust.png)

## <a name="viewing-the-namespace"></a><span data-ttu-id="fabda-116">Anzeigen des Namespace</span><span class="sxs-lookup"><span data-stu-id="fabda-116">Viewing the Namespace</span></span>

<span data-ttu-id="fabda-117">Sie können auch ein Diagramm einer Domänen Struktur basierend auf dem-Namespace zeichnen.</span><span class="sxs-lookup"><span data-stu-id="fabda-117">You can also draw a diagram of a domain tree based on the namespace.</span></span> <span data-ttu-id="fabda-118">Sie können den Distinguished Name eines Objekts ermitteln, indem Sie dem Pfad in der Hierarchie des Domänen Struktur-Namespace folgen.</span><span class="sxs-lookup"><span data-stu-id="fabda-118">You can determine an object's distinguished name by following the path up the hierarchy of the domain tree namespace.</span></span> <span data-ttu-id="fabda-119">Diese Sicht ist nützlich für das Gruppieren von Objekten in einer logischen Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="fabda-119">This view is useful for grouping objects into a logical hierarchy.</span></span> <span data-ttu-id="fabda-120">Der Hauptvorteil eines zusammenhängenden Namespace besteht darin, dass eine Tiefe Suche aus dem Stamm des-Namespace die gesamte Hierarchie durchsucht.</span><span class="sxs-lookup"><span data-stu-id="fabda-120">The chief advantage of a contiguous namespace is that a deep search from the root of the namespace searches the entire hierarchy.</span></span>

![Namespace-Domänen Struktur](images/namespace.png)

 

 




