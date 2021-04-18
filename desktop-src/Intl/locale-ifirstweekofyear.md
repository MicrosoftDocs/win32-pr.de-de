---
description: Gebiets Schema \_ ifirstweekosyear
ms.assetid: 866a28b7-e0b8-4b99-96df-345791a24833
title: LOCALE_IFIRSTWEEKOFYEAR
ms.topic: article
ms.date: 03/04/2020
ms.openlocfilehash: 7f391fb167a9362fc8770bbcc5a495170148b489
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "106351821"
---
# <a name="locale_ifirstweekofyear"></a><span data-ttu-id="6afb7-103">Gebiets Schema \_ ifirstweekosyear</span><span class="sxs-lookup"><span data-stu-id="6afb7-103">LOCALE\_IFIRSTWEEKOFYEAR</span></span>

<span data-ttu-id="6afb7-104">Die erste Woche des Jahres.</span><span class="sxs-lookup"><span data-stu-id="6afb7-104">The first week of the year.</span></span>



| <span data-ttu-id="6afb7-105">Wert</span><span class="sxs-lookup"><span data-stu-id="6afb7-105">Value</span></span> | <span data-ttu-id="6afb7-106">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6afb7-106">Meaning</span></span>                                                                                                                          |
|-------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6afb7-107">0</span><span class="sxs-lookup"><span data-stu-id="6afb7-107">0</span></span>     | <span data-ttu-id="6afb7-108">Woche, die 1/1 enthält, ist die erste Woche des Jahres.</span><span class="sxs-lookup"><span data-stu-id="6afb7-108">Week containing 1/1 is the first week of the year.</span></span> <span data-ttu-id="6afb7-109">Beachten Sie, dass dies ein einzelner Tag sein kann, wenn 1/1 auf den letzten Tag der Woche fällt.</span><span class="sxs-lookup"><span data-stu-id="6afb7-109">Note that this can be a single day, if 1/1 falls on the last day of the week.</span></span> |
| <span data-ttu-id="6afb7-110">1</span><span class="sxs-lookup"><span data-stu-id="6afb7-110">1</span></span>     | <span data-ttu-id="6afb7-111">Die erste vollständige Woche nach 1/1 ist die erste Woche des Jahres.</span><span class="sxs-lookup"><span data-stu-id="6afb7-111">First full week following 1/1 is the first week of the year.</span></span>                                                                     |
| <span data-ttu-id="6afb7-112">2</span><span class="sxs-lookup"><span data-stu-id="6afb7-112">2</span></span>     | <span data-ttu-id="6afb7-113">Die erste Woche mit mindestens vier Tagen ist die erste Woche des Jahres.</span><span class="sxs-lookup"><span data-stu-id="6afb7-113">First week containing at least four days is the first week of the year.</span></span> <span data-ttu-id="6afb7-114">ISO 8601-kompatibel.</span><span class="sxs-lookup"><span data-stu-id="6afb7-114">ISO 8601 compatible.</span></span>                                     |

<span data-ttu-id="6afb7-115">Wenn LOCALE_IFIRSTWEEKOFYEAR 2 ist, LOCALE_IFIRSTDAYOFWEEK den Wert 0 (Montag) hat und LOCALE_ICALENDARTYPE Gregorianisch ist, dann folgt die erste Woche der ISO 8601-Definition, wobei die erste Woche die Woche mit dem ersten Donnerstag des gregorianischen Jahres ist.</span><span class="sxs-lookup"><span data-stu-id="6afb7-115">If LOCALE_IFIRSTWEEKOFYEAR is 2, LOCALE_IFIRSTDAYOFWEEK is 0 (Monday), and LOCALE_ICALENDARTYPE is Gregorian, then the first week follows the ISO 8601 definition where the first week is the week with the first Thursday of the Gregorian year in it.</span></span>


 

 

 



