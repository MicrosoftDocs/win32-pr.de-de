---
description: Die currentvolume-Eigenschaft ruft die Volumenummer für das aktuelle Stammverzeichnis ab.
ms.assetid: f8d06a30-d6d5-43b9-b838-741d781f8d01
title: Currentvolume (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7b91c394be620dfc3f00b8793222848131355f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345387"
---
# <a name="currentvolume-property"></a><span data-ttu-id="6f2af-103">Currentvolume (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6f2af-103">CurrentVolume Property</span></span>

> [!Note]  
> <span data-ttu-id="6f2af-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6f2af-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="6f2af-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="6f2af-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="6f2af-106">Die- `CurrentVolume` Eigenschaft ruft die Volumenummer für das aktuelle Stammverzeichnis ab.</span><span class="sxs-lookup"><span data-stu-id="6f2af-106">The `CurrentVolume` property retrieves the volume number for the current root directory.</span></span>

``` syntax
[ iCurVolume = ] MSWebDVD.CurrentVolume
```

## <a name="return-value"></a><span data-ttu-id="6f2af-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6f2af-107">Return Value</span></span>

<span data-ttu-id="6f2af-108">Gibt einen Integer-Wert zurück, der das aktuelle DVD-Volume darstellt.</span><span class="sxs-lookup"><span data-stu-id="6f2af-108">Returns an integer value representing the current DVD volume.</span></span> <span data-ttu-id="6f2af-109">Wenn eine Festplatte Teil eines Satzes mit mehreren Volumes ist, sollte der ganzzahlige Wert größer als 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="6f2af-109">If a disc is part of a multi-volume set, then the integer value should be greater than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f2af-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6f2af-110">Remarks</span></span>

<span data-ttu-id="6f2af-111">Diese Eigenschaft ist schreibgeschützt und weist keinen Standardwert auf.</span><span class="sxs-lookup"><span data-stu-id="6f2af-111">This property is read-only with no default value.</span></span>

## <a name="see-also"></a><span data-ttu-id="6f2af-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f2af-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f2af-113">**Volumesesverfügbar**</span><span class="sxs-lookup"><span data-stu-id="6f2af-113">**VolumesAvailable**</span></span>](volumesavailable-property.md)
</dt> </dl>

 

 



