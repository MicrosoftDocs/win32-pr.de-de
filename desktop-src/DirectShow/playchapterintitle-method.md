---
description: Die playchapterintitle-Methode gibt das angegebene Kapitel im angegebenen Titel wieder.
ms.assetid: 784b0612-133b-465c-b1da-d9dac26e1b20
title: Playchapterintitle-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 381a63c36c61a8853dcba6a587adb1f078b8cfaa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103859946"
---
# <a name="playchapterintitle-method"></a><span data-ttu-id="6986c-103">Playchapterintitle-Methode</span><span class="sxs-lookup"><span data-stu-id="6986c-103">PlayChapterInTitle Method</span></span>

> [!Note]  
> <span data-ttu-id="6986c-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6986c-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="6986c-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="6986c-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="6986c-106">Die- `PlayChapterInTitle` Methode gibt das angegebene Kapitel im angegebenen Titel wieder.</span><span class="sxs-lookup"><span data-stu-id="6986c-106">The `PlayChapterInTitle` method plays the specified chapter in the specified title.</span></span>

``` syntax
MSWebDVD.PlayChapterInTitle(iTitle, iChapter)
```

## <a name="parameters"></a><span data-ttu-id="6986c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6986c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6986c-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*ititle*</span><span class="sxs-lookup"><span data-stu-id="6986c-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span></span>
</dt> <dd>

<span data-ttu-id="6986c-109">Gibt den Titel als ganzzahligen Wert an.</span><span class="sxs-lookup"><span data-stu-id="6986c-109">Specifies the title as an Integer value.</span></span>

</dd> <dt>

<span data-ttu-id="6986c-110"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*ichapter*</span><span class="sxs-lookup"><span data-stu-id="6986c-110"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*</span></span>
</dt> <dd>

<span data-ttu-id="6986c-111">Gibt das Kapitel als ganzzahligen Wert an.</span><span class="sxs-lookup"><span data-stu-id="6986c-111">Specifies the chapter as an Integer value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6986c-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6986c-112">Return Value</span></span>

<span data-ttu-id="6986c-113">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="6986c-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6986c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6986c-114">Remarks</span></span>

<span data-ttu-id="6986c-115">Diese Methode startet die Wiedergabe im angegebenen Kapitel und wird dann unbegrenzt wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="6986c-115">This method starts playback at the specified chapter and then continues playing indefinitely.</span></span> <span data-ttu-id="6986c-116">Wenn Sie nur ein bestimmtes Kapitel wiedergeben möchten, verwenden Sie [**playchaptersauto stoppt**](playchaptersautostop-method.md).</span><span class="sxs-lookup"><span data-stu-id="6986c-116">If you want to play only a particular chapter, use [**PlayChaptersAutoStop**](playchaptersautostop-method.md).</span></span>

 

 



