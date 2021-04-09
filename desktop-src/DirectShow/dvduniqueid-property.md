---
description: Die dvduniqueid-Eigenschaft ruft eine vom systemgenerierte Zahl ab, die die aktuelle Festplatte eindeutig identifiziert.
ms.assetid: 8ea6dd4d-6998-4212-8874-9c6cd93a1db3
title: Dvduniqueid (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23138f348ef1ec71f1506c8892532bd42f1c807d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860278"
---
# <a name="dvduniqueid-property"></a><span data-ttu-id="936e7-103">Dvduniqueid (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="936e7-103">DVDUniqueID Property</span></span>

> [!Note]  
> <span data-ttu-id="936e7-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="936e7-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="936e7-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="936e7-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="936e7-106">Die `DVDUniqueID` -Eigenschaft ruft eine vom systemgenerierte Zahl ab, die die aktuelle Festplatte eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="936e7-106">The `DVDUniqueID` property retrieves a system-generated number that uniquely identifies the current disc.</span></span>

``` syntax
[ iDiscID = ] MSWebDVD.DVDUniqueID
```

## <a name="return-value"></a><span data-ttu-id="936e7-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="936e7-107">Return Value</span></span>

<span data-ttu-id="936e7-108">Gibt einen ganzzahligen Wert zurück, der die aktuelle Festplatte eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="936e7-108">Returns an integer value that uniquely identifies the current disc.</span></span>

## <a name="remarks"></a><span data-ttu-id="936e7-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="936e7-109">Remarks</span></span>

<span data-ttu-id="936e7-110">Diese Eigenschaft ist schreibgeschützt und weist keinen Standardwert auf.</span><span class="sxs-lookup"><span data-stu-id="936e7-110">This property is read-only with no default value.</span></span> <span data-ttu-id="936e7-111">Die ID-Nummer (ID) ist nicht absolut eindeutig, aber Sie ist für alle praktischen Zwecke eindeutig.</span><span class="sxs-lookup"><span data-stu-id="936e7-111">The identifier (ID) number is not absolutely unique, but it is unique for all practical purposes.</span></span> <span data-ttu-id="936e7-112">Die ID gilt für alle replizierten Kopien eines Datenträgers. Anders ausgedrückt: alle Kopien eines bestimmten Films haben die gleiche ID.</span><span class="sxs-lookup"><span data-stu-id="936e7-112">The ID applies to all replicated copies of a disc. In other words, all copies of a specific movie have the same ID.</span></span> <span data-ttu-id="936e7-113">Die ID basiert auf Dateigrößen, Datumsangaben und anderen Informationen, nicht auf dem Wert der BCA.</span><span class="sxs-lookup"><span data-stu-id="936e7-113">The ID is based on file sizes, dates, and other information, and not the BCA value.</span></span>

 

 



