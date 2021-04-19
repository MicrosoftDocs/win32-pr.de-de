---
description: Die Methode "Rendering" initialisiert das DVD-Filter Diagramm.
ms.assetid: 910f1e3f-b3bb-498b-93da-3a974a3117e8
title: Render-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 677abab1c669642c1e51e0041c98949d923147c7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342546"
---
# <a name="render-method"></a><span data-ttu-id="8de78-103">Render-Methode</span><span class="sxs-lookup"><span data-stu-id="8de78-103">Render Method</span></span>

> [!Note]  
> <span data-ttu-id="8de78-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8de78-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="8de78-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="8de78-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="8de78-106">Die- `Render` Methode initialisiert das DVD-Filter Diagramm.</span><span class="sxs-lookup"><span data-stu-id="8de78-106">The `Render` method initializes the DVD filter graph.</span></span>

``` syntax
MSWebDVD.Render(iRender = 0)
```

## <a name="parameters"></a><span data-ttu-id="8de78-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8de78-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8de78-108"><span id="iRender"></span><span id="irender"></span><span id="IRENDER"></span>*nicht ender*</span><span class="sxs-lookup"><span data-stu-id="8de78-108"><span id="iRender"></span><span id="irender"></span><span id="IRENDER"></span>*iRender*</span></span>
</dt> <dd>

<span data-ttu-id="8de78-109">Gibt einen ganzzahligen Wert an, der angibt, ob das Filter Diagramm zerstört und neu erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="8de78-109">Specifies an integer value indicating whether the filter graph will be destroyed and rebuilt.</span></span>



| <span data-ttu-id="8de78-110">Wert</span><span class="sxs-lookup"><span data-stu-id="8de78-110">Value</span></span> | <span data-ttu-id="8de78-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8de78-111">Description</span></span>                                                                                         |
|-------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8de78-112">0</span><span class="sxs-lookup"><span data-stu-id="8de78-112">0</span></span>     | <span data-ttu-id="8de78-113">Das Filter Diagramm wird nicht zerstört und neu erstellt, wenn es bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="8de78-113">The filter graph will not be destroyed and rebuilt if it already exists.</span></span> <span data-ttu-id="8de78-114">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="8de78-114">This is the default value.</span></span> |
| <span data-ttu-id="8de78-115">1</span><span class="sxs-lookup"><span data-stu-id="8de78-115">1</span></span>     | <span data-ttu-id="8de78-116">Das Filter Diagramm wird zerstört und neu erstellt, wenn es bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="8de78-116">The filter graph will be destroyed and rebuilt if it already exists.</span></span>                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8de78-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8de78-117">Return Value</span></span>

<span data-ttu-id="8de78-118">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="8de78-118">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8de78-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8de78-119">Remarks</span></span>

<span data-ttu-id="8de78-120">Mit der- `Render` Methode kann das **mswebdvd** -Objekt beim Start das zugrunde liegende DirectShow-Filter Diagramm vollständig initialisieren.</span><span class="sxs-lookup"><span data-stu-id="8de78-120">The `Render` method enables the **MSWebDVD** object to fully initialize the underlying DirectShow filter graph on startup.</span></span> <span data-ttu-id="8de78-121">Dadurch entfällt die geringfügige Verzögerung, die andernfalls auftritt, wenn der Benutzer den ersten Befehl ausgibt, um eine CD wiederzugeben oder ein Menü anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8de78-121">This eliminates the slight delay that otherwise occurs when the user issues the first command to play a disc or show a menu.</span></span> <span data-ttu-id="8de78-122">Es gibt keinen Fall, in dem `Render` aufgerufen werden muss, bevor eine andere Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="8de78-122">There is no case in which `Render` needs to be called before calling any other method.</span></span> <span data-ttu-id="8de78-123">Wenn die Anwendung z. b. [**playtitle**](playtitle-method.md) aufruft, bevor das Filter Diagramm initialisiert wurde, ruft das **mswebdvd** -Objekt `Render` automatisch auf, bevor versucht wird, die Festplatte wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="8de78-123">For example, if the application calls [**PlayTitle**](playtitle-method.md) before the filter graph has been initialized, the **MSWebDVD** object calls `Render` automatically before attempting to play the disc.</span></span>

 

 



