---
description: Die preferredsubpicturestream-Eigenschaft ruft den bevorzugten teilbildstream für die aktuelle Anzeige Sitzung ab.
ms.assetid: 9c15dc6f-c016-41bf-b03d-e8e5415215ae
title: Preferredsubpicturestream (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23377d74d3632c665b001ae415dc151ca73bd148
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860252"
---
# <a name="preferredsubpicturestream-property"></a><span data-ttu-id="e6813-103">Preferredsubpicturestream (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e6813-103">PreferredSubpictureStream Property</span></span>

> [!Note]  
> <span data-ttu-id="e6813-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e6813-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="e6813-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="e6813-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="e6813-106">Die- `PreferredSubpictureStream` Eigenschaft ruft den bevorzugten teilbildstream für die aktuelle Anzeige Sitzung ab.</span><span class="sxs-lookup"><span data-stu-id="e6813-106">The `PreferredSubpictureStream` property retrieves the preferred subpicture stream for the current viewing session.</span></span>

``` syntax
[iStream = ] MSWebDVD.PreferredSubpictureStream
```

## <a name="return-value"></a><span data-ttu-id="e6813-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e6813-107">Return Value</span></span>

<span data-ttu-id="e6813-108">Gibt einen ganzzahligen Wert zurück, der den aktuellen bevorzugten teilbildstream in der Systemregistrierung darstellt.</span><span class="sxs-lookup"><span data-stu-id="e6813-108">Returns an Integer value representing the current preferred subpicture stream in the system registry.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6813-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e6813-109">Remarks</span></span>

<span data-ttu-id="e6813-110">Der bevorzugte teilbildstream wird mit der [**defaultsubpicturelcid**](defaultsubpicturelcid-property.md)des [msdvdadm](msdvdadm-object.md) -Objekts festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e6813-110">The preferred subpicture stream is set with [MSDVDAdm](msdvdadm-object.md) object's [**DefaultSubpictureLCID**](defaultsubpicturelcid-property.md).</span></span>

 

 



