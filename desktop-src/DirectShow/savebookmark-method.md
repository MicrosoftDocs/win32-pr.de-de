---
description: Die savebookmark-Methode speichert die aktuelle Position und den Zustand des mswebdvd-Objekts, sodass der Benutzer später zum gleichen Ort zurückkehren kann.
ms.assetid: 975687c5-f93e-4473-b23b-63e0ae6bbb5d
title: Savebookmark-Methode (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2013a56d3f6885f7a4235497ad42bb03f0ebf7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364662"
---
# <a name="savebookmark-method"></a><span data-ttu-id="4a182-103">Savebookmark-Methode</span><span class="sxs-lookup"><span data-stu-id="4a182-103">SaveBookmark Method</span></span>

> [!Note]  
> <span data-ttu-id="4a182-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4a182-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="4a182-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="4a182-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="4a182-106">Die `SaveBookmark` -Methode speichert die aktuelle Position und den Zustand des **mswebdvd** -Objekts, sodass der Benutzer später zum gleichen Ort zurückkehren kann.</span><span class="sxs-lookup"><span data-stu-id="4a182-106">The `SaveBookmark` method saves the current disc position and state of the **MSWebDVD** object so the user can return to the same place later.</span></span>

``` syntax
MSWebDVD.SaveBookmark()
```

## <a name="return-value"></a><span data-ttu-id="4a182-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4a182-107">Return Value</span></span>

<span data-ttu-id="4a182-108">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="4a182-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a182-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a182-109">Remarks</span></span>

<span data-ttu-id="4a182-110">Ein Lesezeichen ist eine Momentaufnahme des aktuellen Zustands des DVD-Navigators.</span><span class="sxs-lookup"><span data-stu-id="4a182-110">A bookmark is a snapshot of the DVD Navigator's current state.</span></span> <span data-ttu-id="4a182-111">Hierzu gehören Informationen wie z. b. der Speicherort auf der Festplatte und welche Audiodaten Ströme ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="4a182-111">This includes information such as where it is playing on the disc, and which audio and subpictures streams are selected.</span></span> <span data-ttu-id="4a182-112">Durch das Speichern eines Lesezeichens kann der Benutzer die Anwendung schließen, den Computer Herunterfahren und später zurückkehren, um die CD direkt dort anzuzeigen, wo Sie aufgehört hat, und alle Einstellungen so wie zuvor.</span><span class="sxs-lookup"><span data-stu-id="4a182-112">By saving a bookmark, the user can close the application, shut down the computer, and come back later to continue viewing the disc right where he or she left off, with all settings just as they were before.</span></span> <span data-ttu-id="4a182-113">Es kann immer nur ein Lesezeichen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="4a182-113">Only one bookmark can be saved at any given time.</span></span> <span data-ttu-id="4a182-114">Wenn Sie anrufen `SaveBookmark` , wird das alte Lesezeichen überschrieben.</span><span class="sxs-lookup"><span data-stu-id="4a182-114">When you call `SaveBookmark`, the old bookmark is overwritten.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a182-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a182-115">Requirements</span></span>



| <span data-ttu-id="4a182-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4a182-116">Requirement</span></span> | <span data-ttu-id="4a182-117">Wert</span><span class="sxs-lookup"><span data-stu-id="4a182-117">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4a182-118">Header</span><span class="sxs-lookup"><span data-stu-id="4a182-118">Header</span></span><br/> | <dl> <span data-ttu-id="4a182-119"><dt>Segment. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a182-119"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a182-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a182-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a182-121">**Restorebookmark**</span><span class="sxs-lookup"><span data-stu-id="4a182-121">**RestoreBookmark**</span></span>](restorebookmark-method.md)
</dt> </dl>

 

 




