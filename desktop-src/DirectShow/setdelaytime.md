---
description: Die setdelta-Time-Methode legt die Verzögerungszeit für die dem mswebdvd-Objekt zugeordnete QuickInfo fest.
ms.assetid: bb1086e1-57e2-495a-9b7b-2d349a516e72
title: Setdelta-Zeit
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c7653777be7e6603494d9ba04a671ed46d3d949
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480587"
---
# <a name="setdelaytime"></a><span data-ttu-id="f5aef-103">Setdelta-Zeit</span><span class="sxs-lookup"><span data-stu-id="f5aef-103">SetDelayTime</span></span>

> [!Note]  
> <span data-ttu-id="f5aef-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f5aef-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="f5aef-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="f5aef-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="f5aef-106">Die- `SetDelayTime` Methode legt die Verzögerungszeit für die dem **mswebdvd** -Objekt zugeordnete QuickInfo fest.</span><span class="sxs-lookup"><span data-stu-id="f5aef-106">The `SetDelayTime` method sets the delay time for the ToolTip associated with the **MSWebDVD** object.</span></span>

``` syntax
MSWebDVD.SetDelayTime(iDelayType, iNewVal)
```

## <a name="parameters"></a><span data-ttu-id="f5aef-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5aef-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5aef-108"><span id="iDelayType"></span><span id="idelaytype"></span><span id="IDELAYTYPE"></span>*idelta-Type*</span><span class="sxs-lookup"><span data-stu-id="f5aef-108"><span id="iDelayType"></span><span id="idelaytype"></span><span id="IDELAYTYPE"></span>*iDelayType*</span></span>
</dt> <dd>

<span data-ttu-id="f5aef-109">Gibt den Typ der Verzögerung als Ganzzahl an.</span><span class="sxs-lookup"><span data-stu-id="f5aef-109">Specifies the type of delay as an Integer.</span></span>



| <span data-ttu-id="f5aef-110">Wert</span><span class="sxs-lookup"><span data-stu-id="f5aef-110">Value</span></span> | <span data-ttu-id="f5aef-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f5aef-111">Description</span></span>                                                                                                                                                                                                                                      |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5aef-112">-1</span><span class="sxs-lookup"><span data-stu-id="f5aef-112">-1</span></span>    | <span data-ttu-id="f5aef-113">Um die Zeit für die autopop-Verzögerung auf den Standardwert zurückzusetzen, legen Sie " *inewval* " auf-1 fest.</span><span class="sxs-lookup"><span data-stu-id="f5aef-113">To reset the autopop delay time to its default value, set *iNewVal* to -1.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="f5aef-114">0</span><span class="sxs-lookup"><span data-stu-id="f5aef-114">0</span></span>     | <span data-ttu-id="f5aef-115">Legen Sie die Zeitspanne fest, die ein QuickInfo-Fenster sichtbar bleibt, wenn der Zeiger innerhalb des umgebenden Rechtecks eines Tools stationär ist.</span><span class="sxs-lookup"><span data-stu-id="f5aef-115">Set the length of time a ToolTip window remains visible if the pointer is stationary within a tool's bounding rectangle.</span></span>                                                                                                                         |
| <span data-ttu-id="f5aef-116">1</span><span class="sxs-lookup"><span data-stu-id="f5aef-116">1</span></span>     | <span data-ttu-id="f5aef-117">Legen Sie den Zeitraum fest, in dem ein Zeiger innerhalb des umgebenden Rechtecks eines Tools stationär bleiben muss, bevor das QuickInfo-Fenster angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f5aef-117">Set the length of time a pointer must remain stationary within a tool's bounding rectangle before the ToolTip window appears.</span></span>                                                                                                                    |
| <span data-ttu-id="f5aef-118">2</span><span class="sxs-lookup"><span data-stu-id="f5aef-118">2</span></span>     | <span data-ttu-id="f5aef-119">Legen Sie die Zeitspanne fest, die für nachfolgende QuickInfo-Fenster benötigt wird, wenn der Zeiger von einem Tool zu einem anderen verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="f5aef-119">Set the length of time it takes for subsequent ToolTip windows to appear as the pointer moves from one tool to another.</span></span>                                                                                                                          |
| <span data-ttu-id="f5aef-120">3</span><span class="sxs-lookup"><span data-stu-id="f5aef-120">3</span></span>     | <span data-ttu-id="f5aef-121">Legen Sie alle Verzögerungszeiten auf Standard Proportionen fest.</span><span class="sxs-lookup"><span data-stu-id="f5aef-121">Set all delay times to default proportions.</span></span> <span data-ttu-id="f5aef-122">Die autopop-Zeit ist zehnmal so oft wie die Anfangszeit, und die reshow-Zeit ist ein Fünftel der Anfangszeit.</span><span class="sxs-lookup"><span data-stu-id="f5aef-122">The autopop time is ten times the initial time and the reshow time is one-fifth the initial time.</span></span> <span data-ttu-id="f5aef-123">Wenn dieses Flag festgelegt ist, geben Sie mit einem positiven Wert von inewval die anfängliche Zeit in Millisekunden an.</span><span class="sxs-lookup"><span data-stu-id="f5aef-123">If this flag is set, use a positive value of iNewVal to specify the initial time, in milliseconds.</span></span> |



 

</dd> <dt>

<span data-ttu-id="f5aef-124"><span id="iNewVal"></span><span id="inewval"></span><span id="INEWVAL"></span>*inewval*</span><span class="sxs-lookup"><span data-stu-id="f5aef-124"><span id="iNewVal"></span><span id="inewval"></span><span id="INEWVAL"></span>*iNewVal*</span></span>
</dt> <dd>

<span data-ttu-id="f5aef-125">Gibt die Verzögerung (in Millisekunden) als ganze Zahl an.</span><span class="sxs-lookup"><span data-stu-id="f5aef-125">Specifies the delay, in milliseconds, as an Integer.</span></span>



| <span data-ttu-id="f5aef-126">Wert</span><span class="sxs-lookup"><span data-stu-id="f5aef-126">Value</span></span>                    | <span data-ttu-id="f5aef-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f5aef-127">Description</span></span>                                                   |
|--------------------------|---------------------------------------------------------------|
| <span data-ttu-id="f5aef-128">-1</span><span class="sxs-lookup"><span data-stu-id="f5aef-128">-1</span></span>                       | <span data-ttu-id="f5aef-129">Legt die in *idelta Type* angegebene Verzögerung auf den Standardwert fest.</span><span class="sxs-lookup"><span data-stu-id="f5aef-129">Sets the delay specified in *iDelayType* to its default value</span></span> |
| <span data-ttu-id="f5aef-130">ein beliebiger anderer negativer Wert</span><span class="sxs-lookup"><span data-stu-id="f5aef-130">any other negative value</span></span> | <span data-ttu-id="f5aef-131">Legt alle Verzögerungs Typen auf ihren Standardwert fest.</span><span class="sxs-lookup"><span data-stu-id="f5aef-131">Sets all delay types to their default value.</span></span>                  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5aef-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f5aef-132">Return Value</span></span>

<span data-ttu-id="f5aef-133">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="f5aef-133">No return value.</span></span>

 

 



