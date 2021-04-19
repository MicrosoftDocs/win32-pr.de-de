---
description: Die anglesavailable-Eigenschaft ruft die Anzahl der derzeit verfügbaren Winkel ab.
ms.assetid: 1e2635d4-63f1-4c3d-a034-437489289bd7
title: Anglesavailable (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5b9d27806b314d89c68fcc4d1476a9918cd4446
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346608"
---
# <a name="anglesavailable-property"></a><span data-ttu-id="9e9be-103">Anglesavailable (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9e9be-103">AnglesAvailable Property</span></span>

> [!Note]  
> <span data-ttu-id="9e9be-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9e9be-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="9e9be-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="9e9be-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="9e9be-106">Die- `AnglesAvailable` Eigenschaft ruft die Anzahl der derzeit verfügbaren Winkel ab.</span><span class="sxs-lookup"><span data-stu-id="9e9be-106">The `AnglesAvailable` property retrieves the number of angles currently available.</span></span>

``` syntax
[ iAngles = ] MSWebDVD.AnglesAvailable
```

## <a name="return-value"></a><span data-ttu-id="9e9be-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9e9be-107">Return Value</span></span>

<span data-ttu-id="9e9be-108">Gibt einen ganzzahligen Wert zwischen 1 und 9 zurück, der die Anzahl der derzeit verfügbaren Winkel darstellt.</span><span class="sxs-lookup"><span data-stu-id="9e9be-108">Returns an integer value from 1 through 9 representing the number of angles currently available.</span></span> <span data-ttu-id="9e9be-109">Wenn</span><span class="sxs-lookup"><span data-stu-id="9e9be-109">If</span></span>


```
iAngles
```



<span data-ttu-id="9e9be-110">= 1, an der aktuellen Position ist kein Winkel Block vorhanden.</span><span class="sxs-lookup"><span data-stu-id="9e9be-110">= 1, there is no angle block at the current location.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e9be-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e9be-111">Remarks</span></span>

<span data-ttu-id="9e9be-112">Diese Eigenschaft ist schreibgeschützt und weist keinen Standardwert auf.</span><span class="sxs-lookup"><span data-stu-id="9e9be-112">This property is read-only with no default value.</span></span> <span data-ttu-id="9e9be-113">Ein *Winkel Block* ist ein Video Segment, das aus mehr als einem Kamerawinkel gedreht wurde.</span><span class="sxs-lookup"><span data-stu-id="9e9be-113">An *angle block* is a video segment that was shot from more than one camera angle.</span></span> <span data-ttu-id="9e9be-114">Ein Winkel Block kann bis zu neun Winkel aufweisen, nummeriert von 1 bis 9.</span><span class="sxs-lookup"><span data-stu-id="9e9be-114">There can be up to nine angles in an angle block, numbered from 1 through 9.</span></span> <span data-ttu-id="9e9be-115">Wenn der DVD-Navigator zum ersten Mal einen Winkel Block eingibt, sendet er ihrer Anwendung eine \_ \_ Verfügbare Ereignis Benachrichtigung für die EC-DVD-Winkel \_ mit der Anzahl von Winkeln in *lParam1*.</span><span class="sxs-lookup"><span data-stu-id="9e9be-115">When the DVD Navigator first enters an angle block, it sends your application an EC\_DVD\_ANGLES\_AVAILABLE event notification with the number of angles in *lParam1*.</span></span> <span data-ttu-id="9e9be-116">Ein Datenträger kann so erstellt werden, dass automatisch ein Menü für verfügbare Winkel angezeigt wird, wenn es in einen Winkel Block wechselt. im Allgemeinen muss eine Anwendung jedoch die Anzahl der verfügbaren Winkel ermitteln und dem Benutzer eine Möglichkeit zur Auswahl bieten.</span><span class="sxs-lookup"><span data-stu-id="9e9be-116">A disc can be authored to automatically show a menu for available angles when it enters an angle block, but generally an application must determine the number of angles available and offer the user a way to select one.</span></span>

## <a name="see-also"></a><span data-ttu-id="9e9be-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e9be-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e9be-118">**Currentangle**</span><span class="sxs-lookup"><span data-stu-id="9e9be-118">**CurrentAngle**</span></span>](currentangle-property.md)
</dt> </dl>

 

 



