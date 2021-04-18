---
description: Definiert ein mobiles Breitband Profil.
ms.assetid: bfec0a1d-de17-4ebd-b9fb-570e230da317
title: Schema Referenz für mobile Breitband profile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 425db1d38002e40969bb47c03952330dd6ccd26d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347787"
---
# <a name="mobile-broadband-profile-schema-reference"></a><span data-ttu-id="f8651-103">Schema Referenz für mobile Breitband profile</span><span class="sxs-lookup"><span data-stu-id="f8651-103">Mobile Broadband Profile Schema Reference</span></span>

<span data-ttu-id="f8651-104">Das mobile Breitband Profil Schema definiert ein mobiles Breitband Profil.</span><span class="sxs-lookup"><span data-stu-id="f8651-104">The Mobile Broadband Profile Schema defines a Mobile Broadband Profile.</span></span>

<span data-ttu-id="f8651-105">Profile speichern Benutzer-und Netzwerk Konfigurationsparameter für mobile Breitbandverbindungen.</span><span class="sxs-lookup"><span data-stu-id="f8651-105">Profiles store Mobile Broadband connection related user and network configuration parameters.</span></span> <span data-ttu-id="f8651-106">Außerdem werden die Benutzereinstellungen für eine Verbindung gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f8651-106">They also store the user preferences for a connection.</span></span>

<span data-ttu-id="f8651-107">Das Stamm Element eines mobilen Breitband Profils ist das [**mbnprofile**](schema-mbnprofile-element.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="f8651-107">The root element of a Mobile Broadband profile is the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span> <span data-ttu-id="f8651-108">Jedes Profil weist genau ein Stamm Element auf.</span><span class="sxs-lookup"><span data-stu-id="f8651-108">Each profile has exactly one root element.</span></span> <span data-ttu-id="f8651-109">Alle von Windows 7 verwendeten Schema Elemente für das mobile Breitband Profil befinden sich im-Namespace, `https://www.microsoft.com/networking/WWAN/profile/v1` und die von Windows 8 verwendeten Elemente befinden sich im-Namespace `https://www.microsoft.com/networking/WWAN/profile/v2` .</span><span class="sxs-lookup"><span data-stu-id="f8651-109">All Mobile Broadband Profile Schema elements used by Windows 7 are in the namespace `https://www.microsoft.com/networking/WWAN/profile/v1` and the elements used by Windows 8 are in the namespace `https://www.microsoft.com/networking/WWAN/profile/v2`.</span></span>

<span data-ttu-id="f8651-110">Das mobile Breitband Profil Schema erzwingt strikt die Reihenfolge der Knoten.</span><span class="sxs-lookup"><span data-stu-id="f8651-110">The Mobile Broadband Profile Schema strictly enforces the order of the nodes.</span></span> <span data-ttu-id="f8651-111">Die in einem Profil angegebenen Knoten müssen dem **mobilen Breitband Profil Schema** entsprechen und in der in der Schema Definition vorgeschriebenen Reihenfolge angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f8651-111">Nodes specified in a profile must adhere to the **Mobile Broadband Profile Schema** and appear in the order prescribed in the schema definition.</span></span> <span data-ttu-id="f8651-112">Beispielsweise muss [**userlogonkred**](schema-userlogoncred-contexttype-element.md) unmittelbar nach [**accessstring**](schema-accessstring-contexttype-element.md)angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f8651-112">For example, [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) must be specified immediately after [**AccessString**](schema-accessstring-contexttype-element.md).</span></span>

-   [<span data-ttu-id="f8651-113">Mobiles Breitband Profil Schema v1</span><span class="sxs-lookup"><span data-stu-id="f8651-113">Mobile Broadband Profile Schema v1</span></span>](mobile-broadband-profile-schema.md)
-   [<span data-ttu-id="f8651-114">Mobiles Breitband Profil Schema v2</span><span class="sxs-lookup"><span data-stu-id="f8651-114">Mobile Broadband Profile Schema v2</span></span>](mobile-broadband-profile-schema-v2.md)
-   [<span data-ttu-id="f8651-115">Mobiles Breitband Profil Schema v3</span><span class="sxs-lookup"><span data-stu-id="f8651-115">Mobile Broadband Profile Schema v3</span></span>](mobile-broadband-profile-schema-v3.md)
-   <span data-ttu-id="f8651-116">[Mobiles Breitband Profil Schema v4](/previous-versions/windows/desktop/legacy/mt243438(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f8651-116">[Mobile Broadband Profile Schema v4](/previous-versions/windows/desktop/legacy/mt243438(v=vs.85))</span></span>

 

 
