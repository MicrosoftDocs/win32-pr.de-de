---
title: Aufgerufenen Aufrufe von srsettrestorepoint
description: In diesem Thema wird die Unterstützung für die Verwendung von nsted-Aufrufen von SRSetRestorePoint durch die Ereignis Typen "geänderter \_ \_ System \_ Änderungs Vorgang und-Ende- \_ \_ System \_ Änderung" beschrieben
ms.assetid: ee2dea47-f95d-4293-ac33-eff622b84db6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5654dc7bb6e42ae55cbad18fc2418df3bdd942d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206862"
---
# <a name="nested-calls-to-srsetrestorepoint"></a><span data-ttu-id="e5f4d-103">Aufgerufenen Aufrufe von srsettrestorepoint</span><span class="sxs-lookup"><span data-stu-id="e5f4d-103">Nested Calls to SRSetRestorePoint</span></span>

<span data-ttu-id="e5f4d-104">In diesem Thema wird die Unterstützung für die Verwendung von nsted-Aufrufen von [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) durch die Ereignis Typen "geänderter \_ \_ System \_ Änderungs Vorgang und-Ende- \_ \_ System \_ Änderung" beschrieben</span><span class="sxs-lookup"><span data-stu-id="e5f4d-104">This topic describes support for nested calls to [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) through the BEGIN\_NESTED\_SYSTEM\_CHANGE and END\_NESTED\_SYSTEM\_CHANGE event types.</span></span>

<span data-ttu-id="e5f4d-105">Anwendungen können [**srtartrestorepoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) bei Verwendung dieser Ereignis Typen sicher aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="e5f4d-105">Applications can safely call [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) when using these event types.</span></span> <span data-ttu-id="e5f4d-106">Der erste Aufrufe der-Funktion erstellt einen Wiederherstellungspunkt.</span><span class="sxs-lookup"><span data-stu-id="e5f4d-106">The first call to the function creates a restore point.</span></span> <span data-ttu-id="e5f4d-107">Nachfolgende, in der Funktion ausgehosterte Aufrufe erstellen keine Wiederherstellungspunkte.</span><span class="sxs-lookup"><span data-stu-id="e5f4d-107">Subsequent nested calls to the function do not create restore points.</span></span> <span data-ttu-id="e5f4d-108">Nehmen Sie z. b. an, eine Anwendung führt die folgenden Aufrufe von **SRSetRestorePoint** aus:</span><span class="sxs-lookup"><span data-stu-id="e5f4d-108">For example, suppose an application makes the following calls to **SRSetRestorePoint**:</span></span><dl> <span data-ttu-id="e5f4d-109">Für Wiederherstellungspunkt A mit dwEventType = geänderte \_ \_ System \_ Änderung starten</span><span class="sxs-lookup"><span data-stu-id="e5f4d-109">For restore point A with dwEventType = BEGIN\_NESTED\_SYSTEM\_CHANGE</span></span>  
<span data-ttu-id="e5f4d-110">Für Wiederherstellungspunkt B mit dwEventType = \_ \_ System Änderung für \_ "Anfang"</span><span class="sxs-lookup"><span data-stu-id="e5f4d-110">For restore point B with dwEventType = BEGIN\_NESTED\_SYSTEM\_CHANGE</span></span>  
<span data-ttu-id="e5f4d-111">Für Wiederherstellungspunkt B mit dwEventType = \_ \_ System Änderung am Ende des Systems \_</span><span class="sxs-lookup"><span data-stu-id="e5f4d-111">For restore point B with dwEventType = END\_NESTED\_SYSTEM\_CHANGE</span></span>  
<span data-ttu-id="e5f4d-112">Für Wiederherstellungspunkt A mit dwEventType = \_ \_ System Änderung am Ende des Systems \_</span><span class="sxs-lookup"><span data-stu-id="e5f4d-112">For restore point A with dwEventType = END\_NESTED\_SYSTEM\_CHANGE</span></span>  
</dl>

<span data-ttu-id="e5f4d-113">Beim zweiten-Befehl wird kein neuer Wiederherstellungspunkt erstellt, da der-aufzurufende aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e5f4d-113">The second call does not create a new restore point because the call is nested.</span></span>

 

 




