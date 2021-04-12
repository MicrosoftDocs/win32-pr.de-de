---
description: Gebiets Schema- \_ snative \* Konstanten
ms.assetid: 560978d7-a33c-4e62-9abd-cbd3ec38f3b5
title: LOCALE_SNATIVE *-Konstanten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eaa6942b6ed114e6cbabdb48ae55ba8f8d7bb43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218697"
---
# <a name="locale_snative-constants"></a><span data-ttu-id="f9547-103">Gebiets Schema- \_ snative \* Konstanten</span><span class="sxs-lookup"><span data-stu-id="f9547-103">LOCALE\_SNATIVE\* Constants</span></span>

<span data-ttu-id="f9547-104">In diesem Thema werden die \_ von NLS verwendeten Gebiets Schema-snativen \* Konstanten zum Darstellen von systemeigenen Sprachen Namen definiert.</span><span class="sxs-lookup"><span data-stu-id="f9547-104">This topic defines the LOCALE\_SNATIVE\* constants used by NLS to represent native language names.</span></span>



| <span data-ttu-id="f9547-105">Wert</span><span class="sxs-lookup"><span data-stu-id="f9547-105">Value</span></span>                       | <span data-ttu-id="f9547-106">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f9547-106">Meaning</span></span>                                                                                                                                                                                                                                                            |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9547-107">Gebiets \_ Schema snativecountryname</span><span class="sxs-lookup"><span data-stu-id="f9547-107">LOCALE\_SNATIVECOUNTRYNAME</span></span>  | <span data-ttu-id="f9547-108">**Windows 7 und höher:** Der Native Name des Landes bzw. der Region, z. b. "España für Spanien".</span><span class="sxs-lookup"><span data-stu-id="f9547-108">**Windows 7 and later:** Native name of the country/region, for example, España for Spain.</span></span> <span data-ttu-id="f9547-109">Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig ist, ist 80, einschließlich eines abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="f9547-109">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span>                                                                 |
| <span data-ttu-id="f9547-110">Gebiets \_ Schema snativectryname</span><span class="sxs-lookup"><span data-stu-id="f9547-110">LOCALE\_SNATIVECTRYNAME</span></span>     | <span data-ttu-id="f9547-111">Veraltet für Windows 7 und höher.</span><span class="sxs-lookup"><span data-stu-id="f9547-111">Deprecated for Windows 7 and later.</span></span> <span data-ttu-id="f9547-112">Der Native Name des Landes bzw. der Region.</span><span class="sxs-lookup"><span data-stu-id="f9547-112">Native name of the country/region.</span></span> <span data-ttu-id="f9547-113">Siehe locale \_ snativecountryname.</span><span class="sxs-lookup"><span data-stu-id="f9547-113">See LOCALE\_SNATIVECOUNTRYNAME.</span></span>                                                                                                                                                             |
| <span data-ttu-id="f9547-114">LOCALE \_ snativecurrname</span><span class="sxs-lookup"><span data-stu-id="f9547-114">LOCALE\_SNATIVECURRNAME</span></span>     | <span data-ttu-id="f9547-115">**Windows Me/98, Windows 2000:** Der Native Name der dem Gebiets Schema zugeordneten Währung in der nativen Sprache des Gebiets Schemas.</span><span class="sxs-lookup"><span data-stu-id="f9547-115">**Windows Me/98, Windows 2000:** The native name of the currency associated with the locale, in the native language of the locale.</span></span> <span data-ttu-id="f9547-116">Es gibt keine Beschränkung für die Anzahl von Zeichen, die für diese Zeichenfolge zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="f9547-116">There is no limit on the number of characters allowed for this string.</span></span>                                                          |
| <span data-ttu-id="f9547-117">Gebiets \_ Schema-snativedigits</span><span class="sxs-lookup"><span data-stu-id="f9547-117">LOCALE\_SNATIVEDIGITS</span></span>       | <span data-ttu-id="f9547-118">Systemeigene Entsprechungen von ASCII 0 bis 9.</span><span class="sxs-lookup"><span data-stu-id="f9547-118">Native equivalents of ASCII 0 through 9.</span></span> <span data-ttu-id="f9547-119">Die maximal zulässige Anzahl von Zeichen für diese Zeichenfolge ist elf, einschließlich eines abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="f9547-119">The maximum number of characters allowed for this string is eleven, including a terminating null character.</span></span> <span data-ttu-id="f9547-120">Arabisch verwendet beispielsweise "012345 6789".</span><span class="sxs-lookup"><span data-stu-id="f9547-120">For example, Arabic uses "٠١٢٣٤٥ ٦٧٨٩".</span></span> <span data-ttu-id="f9547-121">Siehe auch [locale \_ idigitsubstitution](locale-idigitsubstitution.md).</span><span class="sxs-lookup"><span data-stu-id="f9547-121">See also [LOCALE\_IDIGITSUBSTITUTION](locale-idigitsubstitution.md).</span></span> |
| <span data-ttu-id="f9547-122">LOCALE \_ snativedisplayname</span><span class="sxs-lookup"><span data-stu-id="f9547-122">LOCALE\_SNATIVEDISPLAYNAME</span></span>  | <span data-ttu-id="f9547-123">**Windows 7 und höher:** Anzeige Name des Gebiets Schemas in der nativen Sprache, z. b. Deutsch (Deutschland) für das Gebiets Schema Deutsch (Deutschland).</span><span class="sxs-lookup"><span data-stu-id="f9547-123">**Windows 7 and later:** Display name of the locale in its native language, for example, Deutsch (Deutschland) for the locale German (Germany).</span></span> <br/>                                                                                                        |
| <span data-ttu-id="f9547-124">Gebiets \_ Schema snativelangname</span><span class="sxs-lookup"><span data-stu-id="f9547-124">LOCALE\_SNATIVELANGNAME</span></span>     | <span data-ttu-id="f9547-125">Veraltet für Windows 7 und höher.</span><span class="sxs-lookup"><span data-stu-id="f9547-125">Deprecated for Windows 7 and later.</span></span> <span data-ttu-id="f9547-126">Der Native Name der Sprache.</span><span class="sxs-lookup"><span data-stu-id="f9547-126">Native name of the language.</span></span> <span data-ttu-id="f9547-127">Siehe locale \_ snativelanguagename.</span><span class="sxs-lookup"><span data-stu-id="f9547-127">See LOCALE\_SNATIVELANGUAGENAME.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="f9547-128">LOCALE \_ snativelanguagename</span><span class="sxs-lookup"><span data-stu-id="f9547-128">LOCALE\_SNATIVELANGUAGENAME</span></span> | <span data-ttu-id="f9547-129">**Windows 7 und höher:** Der Native Name der Sprache, z. b. Հայերեն für Armenisch (Armenien).</span><span class="sxs-lookup"><span data-stu-id="f9547-129">**Windows 7 and later:** Native name of the language, for example, Հայերեն for Armenian (Armenia).</span></span> <span data-ttu-id="f9547-130">Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig ist, ist 80, einschließlich eines abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="f9547-130">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span>                                                         |



 

 

 




