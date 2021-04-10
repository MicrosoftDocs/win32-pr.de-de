---
title: Schachtelung im gemischten Modus
description: In diesem Thema werden die Einschränkungen von Sicherheitsgruppen in einer Domäne im gemischten Modus aufgeführt.
ms.assetid: e9f50485-db09-4d8c-8cf4-0ee7e78cb133
ms.tgt_platform: multiple
keywords:
- Schachteln im gemischten Modus (AD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e54d63d475edf77398a69a519a08f3803f69d67d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855400"
---
# <a name="nesting-in-mixed-mode"></a><span data-ttu-id="02a0f-104">Schachtelung im gemischten Modus</span><span class="sxs-lookup"><span data-stu-id="02a0f-104">Nesting in Mixed Mode</span></span>

<span data-ttu-id="02a0f-105">In diesem Thema werden die Einschränkungen von Sicherheitsgruppen in einer Domäne im gemischten Modus aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="02a0f-105">This topic lists the restrictions of security groups in a mixed-mode domain.</span></span>

<span data-ttu-id="02a0f-106">Für Sicherheitsgruppen in einer Domäne im gemischten Modus gelten die folgenden Einschränkungen:</span><span class="sxs-lookup"><span data-stu-id="02a0f-106">Security groups in a mixed-mode domain have the following restrictions:</span></span>

-   <span data-ttu-id="02a0f-107">Universelle Gruppen können nicht in Domänen mit gemischtem Modus erstellt werden, da der universelle Bereich nur in Windows 2000-Domänen im einheitlichen Modus unterstützt wird</span><span class="sxs-lookup"><span data-stu-id="02a0f-107">Universal groups cannot be created in mixed-mode domains because the universal scope is supported only in Windows 2000 native-mode domains.</span></span>
-   <span data-ttu-id="02a0f-108">Eine globale Gruppe kann Konten aus derselben Domäne enthalten, zu der die Gruppe gehört.</span><span class="sxs-lookup"><span data-stu-id="02a0f-108">A global group can contain accounts from the same domain to which the group belongs.</span></span> <span data-ttu-id="02a0f-109">Eine globale Gruppe darf keine universellen Gruppen, keine globale Gruppe oder kein Konto aus einer anderen Domäne enthalten.</span><span class="sxs-lookup"><span data-stu-id="02a0f-109">A global group cannot contain any universal groups, any global group, or an account from another domain.</span></span>
-   <span data-ttu-id="02a0f-110">Eine lokale Gruppe der Domäne kann globale Gruppen und Konten aus beliebigen Domänen oder Gesamtstrukturen enthalten.</span><span class="sxs-lookup"><span data-stu-id="02a0f-110">A domain local group can contain global groups and accounts from any domain or forest.</span></span> <span data-ttu-id="02a0f-111">Eine lokale Domänen Gruppe darf keine andere lokale Domänen Gruppe enthalten.</span><span class="sxs-lookup"><span data-stu-id="02a0f-111">A domain local group cannot contain any other domain local group.</span></span>

<span data-ttu-id="02a0f-112">Beachten Sie, dass Verteiler Gruppen gemäß den Schachtelungs Regeln für den einheitlichen Modus geschachtelt werden können.</span><span class="sxs-lookup"><span data-stu-id="02a0f-112">Be aware that distribution groups can be nested according to the nesting rules for native mode.</span></span>

 

 




