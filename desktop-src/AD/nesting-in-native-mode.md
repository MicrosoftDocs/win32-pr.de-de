---
title: Schachtelung im einheitlichen Modus
description: In der folgenden Liste wird beschrieben, was in einer Gruppe enthalten sein kann, die in einer Domäne im einheitlichen Modus vorhanden ist.
ms.assetid: 7992ef2d-9dcf-4087-b09a-35235b23e499
ms.tgt_platform: multiple
keywords:
- Schachtelung im einheitlichen Modus von AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69dba115bb705fe706a049e85136475c6d5b3a16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855399"
---
# <a name="nesting-in-native-mode"></a><span data-ttu-id="5438c-104">Schachtelung im einheitlichen Modus</span><span class="sxs-lookup"><span data-stu-id="5438c-104">Nesting in Native Mode</span></span>

<span data-ttu-id="5438c-105">In der folgenden Liste wird beschrieben, was in einer Gruppe enthalten sein kann, die in einer Domäne im einheitlichen Modus vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5438c-105">The following list describes what can be contained in a group that exists in a native-mode domain.</span></span> <span data-ttu-id="5438c-106">Diese Liste gilt auch für Verteiler Gruppen in Domänen mit gemischtem Modus.</span><span class="sxs-lookup"><span data-stu-id="5438c-106">This same list also applies to distribution groups in mixed-mode domains.</span></span> <span data-ttu-id="5438c-107">Der Bereich der Gruppe bestimmt diese Kapselungs Regeln.</span><span class="sxs-lookup"><span data-stu-id="5438c-107">The scope of the group determines these containment rules.</span></span>

-   <span data-ttu-id="5438c-108">Eine universelle Gruppe kann andere universelle Gruppen, globale Gruppen und Konten aus beliebigen Domänen innerhalb der Gesamtstruktur enthalten, in der sich diese universelle Gruppe befindet.</span><span class="sxs-lookup"><span data-stu-id="5438c-108">A universal group can contain other universal groups, global groups and accounts from any domain within the forest in which this Universal Group resides.</span></span>
-   <span data-ttu-id="5438c-109">Eine globale Gruppe kann andere globale Gruppen und Konten aus derselben Domäne enthalten, zu der die Gruppe gehört.</span><span class="sxs-lookup"><span data-stu-id="5438c-109">A global group can contain other global groups and accounts from the same domain that the group belongs to.</span></span> <span data-ttu-id="5438c-110">Eine globale Gruppe darf keine universellen Gruppen oder eine globale Gruppe oder ein anderes Konto aus einer anderen Domäne enthalten.</span><span class="sxs-lookup"><span data-stu-id="5438c-110">A global group cannot contain any universal groups, or any global group or account from another domain.</span></span>
-   <span data-ttu-id="5438c-111">Eine lokale Gruppe der Domäne kann universelle Gruppen, globale Gruppen und Konten aus beliebigen Domänen oder Gesamtstrukturen enthalten.</span><span class="sxs-lookup"><span data-stu-id="5438c-111">A domain local group can contain universal groups, global groups and accounts from any domain or forest.</span></span> <span data-ttu-id="5438c-112">Eine lokale Gruppe der Domäne kann auch andere lokale Domänen Gruppen aus derselben Domäne enthalten, zu der die Gruppe gehört.</span><span class="sxs-lookup"><span data-stu-id="5438c-112">A domain local group can also contain other domain local groups from the same domain that the group belongs to.</span></span> <span data-ttu-id="5438c-113">Eine lokale Domänen Gruppe darf keine anderen lokalen Gruppen der Domäne aus einer anderen Domäne oder Gesamtstruktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="5438c-113">A domain local group cannot contain other domain local groups from any other domain or forest.</span></span>

 

 




