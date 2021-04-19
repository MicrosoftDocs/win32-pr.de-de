---
description: Die volumesavailable-Eigenschaft ruft die Anzahl der Volumes in einem mehrteiligen Satz ab.
ms.assetid: d056b6d5-f4a4-480b-96a5-8e95dce23dfb
title: Volumesavailable (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccdcf32ba8b7bea3958ef469bc0f90f9d41ecc14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356260"
---
# <a name="volumesavailable-property"></a><span data-ttu-id="9c4b7-103">Volumesavailable (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9c4b7-103">VolumesAvailable Property</span></span>

> [!Note]  
> <span data-ttu-id="9c4b7-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9c4b7-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="9c4b7-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="9c4b7-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="9c4b7-106">Die- `VolumesAvailable` Eigenschaft ruft die Anzahl der Volumes in einem mehrteiligen Satz ab.</span><span class="sxs-lookup"><span data-stu-id="9c4b7-106">The `VolumesAvailable` property retrieves the number of volumes in a multivolume set.</span></span>

``` syntax
[ iVolumes = ] MSWebDVD.VolumesAvailable
```

## <a name="return-value"></a><span data-ttu-id="9c4b7-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9c4b7-107">Return Value</span></span>

<span data-ttu-id="9c4b7-108">Gibt die Anzahl der Volumes im Satz als Ganzzahl zurück.</span><span class="sxs-lookup"><span data-stu-id="9c4b7-108">Returns the number of volumes in the set as an Integer.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c4b7-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9c4b7-109">Remarks</span></span>

<span data-ttu-id="9c4b7-110">Diese Eigenschaft ist schreibgeschützt und weist keinen Standardwert auf.</span><span class="sxs-lookup"><span data-stu-id="9c4b7-110">This property is read-only with no default value.</span></span> <span data-ttu-id="9c4b7-111">Einige DVD-Titel können als Multidisk-Satz oder-Reihe freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9c4b7-111">Some DVD titles might be released as a multidisc set or series.</span></span> <span data-ttu-id="9c4b7-112">Verwenden Sie diese Methode, um die Volumenummer für den aktuellen Festplattenspeicher zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="9c4b7-112">Use this method to determine the volume number for the current disc.</span></span>

 

 



