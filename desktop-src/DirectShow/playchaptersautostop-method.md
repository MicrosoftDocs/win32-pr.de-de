---
description: Die playchaptersauto-Methode startet die Wiedergabe im angegebenen Kapitel im angegebenen Titel und für die angegebene Anzahl von Kapiteln.
ms.assetid: ede19f02-6eda-42da-a108-06d78dc2e8a9
title: Playchaptersaudestoppt-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f542f890a54c755c9ea041c46f7cef3b4b7fd9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213886"
---
# <a name="playchaptersautostop-method"></a><span data-ttu-id="a561a-103">Playchaptersaudestoppt-Methode</span><span class="sxs-lookup"><span data-stu-id="a561a-103">PlayChaptersAutoStop Method</span></span>

> [!Note]  
> <span data-ttu-id="a561a-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a561a-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="a561a-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="a561a-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="a561a-106">Die `PlayChaptersAutoStop` -Methode startet die Wiedergabe im angegebenen Kapitel im angegebenen Titel und für die angegebene Anzahl von Kapiteln.</span><span class="sxs-lookup"><span data-stu-id="a561a-106">The `PlayChaptersAutoStop` method starts playback at the specified chapter in the specified title and for the number of chapters specified.</span></span>

``` syntax
MSWebDVD.PlayChaptersAutoStop(iTitle, iChapter, iChapterCount)
```

## <a name="parameters"></a><span data-ttu-id="a561a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a561a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a561a-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*ititle*</span><span class="sxs-lookup"><span data-stu-id="a561a-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span></span>
</dt> <dd>

<span data-ttu-id="a561a-109">Gibt den Titel als ganzzahligen Wert an.</span><span class="sxs-lookup"><span data-stu-id="a561a-109">Specifies the title as an Integer value.</span></span>

</dd> <dt>

<span data-ttu-id="a561a-110"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*ichapter*</span><span class="sxs-lookup"><span data-stu-id="a561a-110"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*</span></span>
</dt> <dd>

<span data-ttu-id="a561a-111">Gibt das Start Kapitel als ganzzahligen Wert an.</span><span class="sxs-lookup"><span data-stu-id="a561a-111">Specifies the start chapter as an Integer value.</span></span>

</dd> <dt>

<span data-ttu-id="a561a-112"><span id="iChapterCount"></span><span id="ichaptercount"></span><span id="ICHAPTERCOUNT"></span>*ichaptercount*</span><span class="sxs-lookup"><span data-stu-id="a561a-112"><span id="iChapterCount"></span><span id="ichaptercount"></span><span id="ICHAPTERCOUNT"></span>*iChapterCount*</span></span>
</dt> <dd>

<span data-ttu-id="a561a-113">Gibt die Anzahl der zu Wiedergabe enden Kapitel als ganzzahligen Wert an.</span><span class="sxs-lookup"><span data-stu-id="a561a-113">Specifies the number of chapters to play as an Integer value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a561a-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a561a-114">Return Value</span></span>

<span data-ttu-id="a561a-115">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="a561a-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a561a-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a561a-116">Remarks</span></span>

<span data-ttu-id="a561a-117">Wenn das letzte Kapitel wiedergegeben wurde, bewirkt diese Methode, dass eine EC-DVD-Kapitel-Ereignis Benachrichtigung für [**\_ \_ \_ Automatische Stopps**](ec-dvd-chapter-autostop.md) an die Anwendung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="a561a-117">When the last chapter has played, this method causes an [**EC\_DVD\_CHAPTER\_AUTOSTOP**](ec-dvd-chapter-autostop.md) event notification to be sent to the application.</span></span>

 

 



