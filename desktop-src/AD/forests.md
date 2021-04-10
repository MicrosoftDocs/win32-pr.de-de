---
title: Gesamtstrukturen
description: Eine Gesamtstruktur ist ein Satz von mindestens einer Domänen Struktur, die keinen zusammenhängenden Namespace bilden.
ms.assetid: b7beb305-0022-477a-85bf-779821202b26
ms.tgt_platform: multiple
keywords:
- Gesamtstruktur Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc84fca35ce90b20582bd62a675e6cf8d0285f7e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103948570"
---
# <a name="forests"></a><span data-ttu-id="8c5dc-104">Gesamtstrukturen</span><span class="sxs-lookup"><span data-stu-id="8c5dc-104">Forests</span></span>

<span data-ttu-id="8c5dc-105">Eine Gesamt [*Struktur ist ein*](/previous-versions/windows/desktop/legacy/ms681904(v=vs.85)) Satz von mindestens einer Domänen Struktur, die keinen zusammenhängenden Namespace bilden.</span><span class="sxs-lookup"><span data-stu-id="8c5dc-105">A [*forest*](/previous-versions/windows/desktop/legacy/ms681904(v=vs.85)) is a set of one or more domain trees that do not form a contiguous namespace.</span></span> <span data-ttu-id="8c5dc-106">Alle Strukturen in einer Gesamtstruktur verfügen über ein gemeinsames Schema, eine gemeinsame Konfiguration und einen globalen Katalog.</span><span class="sxs-lookup"><span data-stu-id="8c5dc-106">All trees in a forest share a common schema, configuration, and global catalog.</span></span> <span data-ttu-id="8c5dc-107">Alle Strukturen in einer bestimmten Gesamtstruktur tauschen eine Vertrauensstellung gemäß transitiven hierarchischen Kerberos-Vertrauens Stellungen aus.</span><span class="sxs-lookup"><span data-stu-id="8c5dc-107">All trees in a given forest exchange trust according to transitive hierarchical Kerberos trust relationships.</span></span> <span data-ttu-id="8c5dc-108">Im Gegensatz zu Strukturen ist für eine Gesamtstruktur kein eindeutiger Name erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8c5dc-108">Unlike trees, a forest does not require a distinct name.</span></span> <span data-ttu-id="8c5dc-109">Eine Gesamtstruktur ist als Satz von Querverweis Objekten und Kerberos-Vertrauens Stellungen vorhanden, die von den Mitglieds Strukturen erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="8c5dc-109">A forest exists as a set of cross-reference objects and Kerberos trust relationships recognized by the member trees.</span></span> <span data-ttu-id="8c5dc-110">Strukturen in einer Gesamtstruktur bilden eine Hierarchie für die Kerberos-Vertrauensstellung. der Struktur Name im Stammverzeichnis der Vertrauens Struktur verweist auf eine angegebene Gesamtstruktur.</span><span class="sxs-lookup"><span data-stu-id="8c5dc-110">Trees in a forest form a hierarchy for the purposes of Kerberos trust; the tree name at the root of the trust tree refers to a given forest.</span></span>

<span data-ttu-id="8c5dc-111">Die folgende Abbildung zeigt eine Gesamtstruktur von nicht zusammenhängenden Namespaces.</span><span class="sxs-lookup"><span data-stu-id="8c5dc-111">The following figure shows a forest of noncontiguous namespaces.</span></span>

![Gesamtstruktur von nicht zusammenhängenden Namespaces](images/forests.png)

 

 