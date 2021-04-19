---
description: Die subpicturestreamsavailable-Eigenschaft ruft die Anzahl der im aktuellen Titel verfügbaren teilbildstreams ab.
ms.assetid: 6a6d9d15-2f56-47fc-a7bb-2cf33f384f41
title: Subpicturestreamsavailable (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e34f780a726966580a72d87b6f7900bb73c1a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360813"
---
# <a name="subpicturestreamsavailable-property"></a><span data-ttu-id="42ae4-103">Subpicturestreamsavailable (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="42ae4-103">SubpictureStreamsAvailable Property</span></span>

> [!Note]  
> <span data-ttu-id="42ae4-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="42ae4-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="42ae4-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="42ae4-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="42ae4-106">Die- `SubpictureStreamsAvailable` Eigenschaft ruft die Anzahl der im aktuellen Titel verfügbaren teilbildstreams ab.</span><span class="sxs-lookup"><span data-stu-id="42ae4-106">The `SubpictureStreamsAvailable` property retrieves the number of subpicture streams available in the current title.</span></span>

``` syntax
[ iStreams = ] MSWebDVD.SubpictureStreamsAvailable
```

## <a name="return-value"></a><span data-ttu-id="42ae4-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="42ae4-107">Return Value</span></span>

<span data-ttu-id="42ae4-108">Gibt die Anzahl der verfügbaren Streams als Ganzzahl zurück.</span><span class="sxs-lookup"><span data-stu-id="42ae4-108">Returns the number of available streams as an Integer.</span></span>

## <a name="remarks"></a><span data-ttu-id="42ae4-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="42ae4-109">Remarks</span></span>

<span data-ttu-id="42ae4-110">Diese Eigenschaft ist schreibgeschützt und weist keinen Standardwert auf.</span><span class="sxs-lookup"><span data-stu-id="42ae4-110">This property is read-only with no default value.</span></span> <span data-ttu-id="42ae4-111">Um jeden Stream für sein sprach Attribut abzufragen, müssen Sie zuerst diese Methode zum Abrufen der oberen Grenze aufruft.</span><span class="sxs-lookup"><span data-stu-id="42ae4-111">To query each stream for its language attribute, first call this method to get the upper bound.</span></span>

<span data-ttu-id="42ae4-112">Die Datenstrom Nummerierung ist NULL basiert.</span><span class="sxs-lookup"><span data-stu-id="42ae4-112">Stream numbering is zero-based.</span></span>

 

 



