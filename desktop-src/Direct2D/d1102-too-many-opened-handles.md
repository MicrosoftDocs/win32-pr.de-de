---
title: D1102 zu viele geöffnete Handles
ms.assetid: a7e52926-a4e6-4030-9e90-9df2b3e3edde
description: Eine große Anzahl nicht veröffentlichter Schnittstellen wurde gefunden. Aktuell sind von dieser DLL nicht freigegebene Schnittstellen zugeordnet.
keywords:
- D1102 zu viele geöffnete Handles Direct2D
topic_type:
- apiref
api_name:
- D1102 Too Many Opened Handles
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: e3c12c2e2a7b47535e830c6ed65a828a16672bbf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718053"
---
# <a name="d1102-too-many-opened-handles"></a><span data-ttu-id="85c16-105">D1102: zu viele geöffnete Handles</span><span class="sxs-lookup"><span data-stu-id="85c16-105">D1102: Too Many Opened Handles</span></span>

<span data-ttu-id="85c16-106">Eine große Anzahl nicht veröffentlichter Schnittstellen wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="85c16-106">A large number of unreleased interfaces were found.</span></span> <span data-ttu-id="85c16-107">Derzeit sind \[  \] von dieser DLL zahlreiche nicht freigegebene Schnittstellen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="85c16-107">Currently there are \[*number*\] unreleased interfaces allocated by this DLL.</span></span>

## <a name="placeholders"></a><span data-ttu-id="85c16-108">Platzhalter</span><span class="sxs-lookup"><span data-stu-id="85c16-108">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="85c16-109"><span id="number"></span><span id="NUMBER"></span>*einigen*</span><span class="sxs-lookup"><span data-stu-id="85c16-109"><span id="number"></span><span id="NUMBER"></span>*number*</span></span>
</dt> <dd>

<span data-ttu-id="85c16-110">Die Anzahl der nicht veröffentlichten Schnittstellen, die von dieser DLL zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="85c16-110">The number of unreleased interfaces allocated by this DLL.</span></span>

</dd> </dl> 

|             |         |
|-------------|---------|
| <span data-ttu-id="85c16-111">Fehlerstufe</span><span class="sxs-lookup"><span data-stu-id="85c16-111">Error Level</span></span> | <span data-ttu-id="85c16-112">Warnung</span><span class="sxs-lookup"><span data-stu-id="85c16-112">Warning</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="85c16-113">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="85c16-113">Possible Causes</span></span>

<span data-ttu-id="85c16-114">Es wurde eine große Anzahl von Ressourcen erstellt.</span><span class="sxs-lookup"><span data-stu-id="85c16-114">A large number of resources were created.</span></span> <span data-ttu-id="85c16-115">Obwohl Direct2D über keine Obergrenze für die Anzahl der verfügbaren Ressourcen (mit Ausnahme des Speichers) verfügt, gibt die debugschicht diese Informations Meldung aus, wenn 1001 Live-Objekte, 2001 Live-Objekte oder 3001 Live-Objekte usw. auftreten, da dies auf einen Fehler in der Anwendung hindeuten könnte.</span><span class="sxs-lookup"><span data-stu-id="85c16-115">Although Direct2D has no upper bound on the number of available resources (except memory), the debug layer issues this informational message when it encounters 1001 live objects, 2001 live objects, or 3001 live objects etc, because this might indicate a leak in the application.</span></span>

 

 




