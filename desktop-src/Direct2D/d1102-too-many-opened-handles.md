---
title: D1102 zu viele geöffnete Handles
ms.assetid: a7e52926-a4e6-4030-9e90-9df2b3e3edde
description: Es wurde eine große Anzahl von nicht freigegebenen Schnittstellen gefunden. Derzeit sind von dieser DLL nicht freigegebene Schnittstellen zugeordnet.
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
ms.openlocfilehash: 2d59e110aece56a31af71e75e9a8eca0bb008961
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548685"
---
# <a name="d1102-too-many-opened-handles"></a><span data-ttu-id="c45a8-105">D1102: Zu viele geöffnete Handles</span><span class="sxs-lookup"><span data-stu-id="c45a8-105">D1102: Too Many Opened Handles</span></span>

<span data-ttu-id="c45a8-106">Es wurde eine große Anzahl von nicht freigegebenen Schnittstellen gefunden.</span><span class="sxs-lookup"><span data-stu-id="c45a8-106">A large number of unreleased interfaces were found.</span></span> <span data-ttu-id="c45a8-107">Derzeit sind \[ *von* dieser DLL nicht \] freigegebene Schnittstellen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c45a8-107">Currently there are \[*number*\] unreleased interfaces allocated by this DLL.</span></span>

## <a name="placeholders"></a><span data-ttu-id="c45a8-108">Platzhalter</span><span class="sxs-lookup"><span data-stu-id="c45a8-108">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="c45a8-109"><span id="number"></span><span id="NUMBER"></span>*Anzahl*</span><span class="sxs-lookup"><span data-stu-id="c45a8-109"><span id="number"></span><span id="NUMBER"></span>*number*</span></span>
</dt> <dd>

<span data-ttu-id="c45a8-110">Die Anzahl von nicht freigegebenen Schnittstellen, die von dieser DLL zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="c45a8-110">The number of unreleased interfaces allocated by this DLL.</span></span>

</dd> </dl> 

| &nbsp;      |  &nbsp; |
|-------------|---------|
| <span data-ttu-id="c45a8-111">Fehlerstufe</span><span class="sxs-lookup"><span data-stu-id="c45a8-111">Error Level</span></span> | <span data-ttu-id="c45a8-112">Warnung</span><span class="sxs-lookup"><span data-stu-id="c45a8-112">Warning</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="c45a8-113">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="c45a8-113">Possible Causes</span></span>

<span data-ttu-id="c45a8-114">Eine große Anzahl von Ressourcen wurde erstellt.</span><span class="sxs-lookup"><span data-stu-id="c45a8-114">A large number of resources were created.</span></span> <span data-ttu-id="c45a8-115">Obwohl Direct2D keine Obergrenze für die Anzahl der verfügbaren Ressourcen (außer Arbeitsspeicher) hat, gibt die Debugebene diese Informationsmeldung aus, wenn 1001 Liveobjekte, 2001 Liveobjekte oder 3001 Liveobjekte usw. auftreten, da dies auf einen Verlust in der Anwendung hinweisen kann.</span><span class="sxs-lookup"><span data-stu-id="c45a8-115">Although Direct2D has no upper bound on the number of available resources (except memory), the debug layer issues this informational message when it encounters 1001 live objects, 2001 live objects, or 3001 live objects etc, because this might indicate a leak in the application.</span></span>

 

 




