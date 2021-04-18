---
description: Die playchapter-Methode startet die Wiedergabe aus dem angegebenen Kapitel innerhalb des aktuellen Titels.
ms.assetid: d0318a0d-4ff4-42f2-b009-996b7ff0f632
title: Playchapter-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bab4600d8d4fc09c4b63fa423c66823e92e95a2a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106339644"
---
# <a name="playchapter-method"></a><span data-ttu-id="3e20c-103">Playchapter-Methode</span><span class="sxs-lookup"><span data-stu-id="3e20c-103">PlayChapter Method</span></span>

> [!Note]  
> <span data-ttu-id="3e20c-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3e20c-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="3e20c-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="3e20c-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="3e20c-106">Die- `PlayChapter` Methode startet die Wiedergabe aus dem angegebenen Kapitel innerhalb des aktuellen Titels.</span><span class="sxs-lookup"><span data-stu-id="3e20c-106">The `PlayChapter` method starts playback from the specified chapter within the current title.</span></span>

``` syntax
MSWebDVD.PlayChapter(iChapter)
```

## <a name="parameters"></a><span data-ttu-id="3e20c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e20c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e20c-108"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*ichapter*</span><span class="sxs-lookup"><span data-stu-id="3e20c-108"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*</span></span>
</dt> <dd>

<span data-ttu-id="3e20c-109">Gibt den Kapitel Index im aktuellen Titel als Ganzzahl an.</span><span class="sxs-lookup"><span data-stu-id="3e20c-109">Specifies the chapter index in the current title as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e20c-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3e20c-110">Return Value</span></span>

<span data-ttu-id="3e20c-111">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="3e20c-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e20c-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3e20c-112">Remarks</span></span>

<span data-ttu-id="3e20c-113">Wenn das Ende des angegebenen Kapitels erreicht ist, setzt diese Methode fort, wenn vorhandene Kapitel vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="3e20c-113">When the end of the specified chapter is reached, this method continues playing subsequent chapters, if any exist.</span></span> <span data-ttu-id="3e20c-114">Wenn Sie nur ein bestimmtes Kapitel wiedergeben möchten, verwenden Sie [**playchaptersauto stoppt**](playchaptersautostop-method.md).</span><span class="sxs-lookup"><span data-stu-id="3e20c-114">If you want to play only a specified chapter, use [**PlayChaptersAutoStop**](playchaptersautostop-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="3e20c-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e20c-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e20c-116">**Playchapterintitle**</span><span class="sxs-lookup"><span data-stu-id="3e20c-116">**PlayChapterInTitle**</span></span>](playchapterintitle-method.md)
</dt> </dl>

 

 



