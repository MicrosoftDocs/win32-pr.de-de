---
title: Autorisierungs-Plug-in-Methoden
description: Alle Autorisierungs-Plug-in-Einstiegspunkte verfügen über einen Rückrufmechanismus, um den Erfolg oder Misserfolg des Aufrufs zu melden. Einige Rückruf Mechanismen werden mehrmals aufgerufen, bis alle Ergebnisse gemeldet werden.
ms.assetid: 6d7c1c54-fab5-431b-b123-eee6fd4dfb92
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9253267b87a30c5cc2781440b0ecd430f244e90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338590"
---
# <a name="authorization-plug-in-methods"></a><span data-ttu-id="a991b-104">Autorisierungs-Plug-in-Methoden</span><span class="sxs-lookup"><span data-stu-id="a991b-104">Authorization Plug-in Methods</span></span>

<span data-ttu-id="a991b-105">Alle Autorisierungs-Plug-in-Einstiegspunkte verfügen über einen Rückrufmechanismus, um den Erfolg oder Misserfolg des Aufrufs zu melden.</span><span class="sxs-lookup"><span data-stu-id="a991b-105">All authorization plug-in entry points have a callback mechanism to report the success or failure of the call.</span></span> <span data-ttu-id="a991b-106">Einige Rückruf Mechanismen werden mehrmals aufgerufen, bis alle Ergebnisse gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="a991b-106">Some callback mechanisms are called multiple times until all of the results are reported.</span></span>

<span data-ttu-id="a991b-107">In der folgenden Tabelle finden Sie eine Übersicht über die Rückruf Methoden für die Autorisierung.</span><span class="sxs-lookup"><span data-stu-id="a991b-107">The following table provides an overview of the authorization callback methods.</span></span>



| <span data-ttu-id="a991b-108">Methode</span><span class="sxs-lookup"><span data-stu-id="a991b-108">Method</span></span>                                                                           | <span data-ttu-id="a991b-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a991b-109">Description</span></span>                                                          |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="a991b-110">**Wsmanpluginauthzoperationcomplete**</span><span class="sxs-lookup"><span data-stu-id="a991b-110">**WSManPluginAuthzOperationComplete**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzoperationcomplete)   | <span data-ttu-id="a991b-111">Meldet entweder einen erfolgreichen oder fehlgeschlagenen Benutzer Vorgang.</span><span class="sxs-lookup"><span data-stu-id="a991b-111">Reports either a successful or failed user operation.</span></span>                |
| [<span data-ttu-id="a991b-112">**Wsmanpluginauthzqueryquotacomplete**</span><span class="sxs-lookup"><span data-stu-id="a991b-112">**WSManPluginAuthzQueryQuotaComplete**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzqueryquotacomplete) | <span data-ttu-id="a991b-113">Meldet Kontingent Details, die für den angegebenen Benutzer relevant sind.</span><span class="sxs-lookup"><span data-stu-id="a991b-113">Reports quota details that are relevant for the specified user.</span></span>      |
| [<span data-ttu-id="a991b-114">**Wsmanpluginauthzusercomplete**</span><span class="sxs-lookup"><span data-stu-id="a991b-114">**WSManPluginAuthzUserComplete**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzusercomplete)             | <span data-ttu-id="a991b-115">Meldet entweder eine erfolgreiche oder fehlgeschlagene Autorisierung der Benutzer Verbindung.</span><span class="sxs-lookup"><span data-stu-id="a991b-115">Reports either a successful or failed user connection authorization.</span></span> |



 

 

 




