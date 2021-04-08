---
description: Jedem Gebiets Schema ist ein Standard Kalendertyp (Datentyp "caltype") zugeordnet. Ein Gebiets Schema kann auch einen alternativen Kalendertyp aufweisen. Ausführliche Informationen zu Kalender Typen finden Sie unter Calendar Type-Informationen.
ms.assetid: 32772cba-eb30-4cd3-adaf-57fb8425a6d5
title: Datum und Kalender
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96a3c21965bfbf8c4215b478e5c3b4adbae579ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867936"
---
# <a name="date-and-calendar"></a><span data-ttu-id="b0383-105">Datum und Kalender</span><span class="sxs-lookup"><span data-stu-id="b0383-105">Date and Calendar</span></span>

<span data-ttu-id="b0383-106">Jedem [Gebiets](locales-and-languages.md) Schema ist ein Standard Kalendertyp (Datentyp "caltype") zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="b0383-106">Each [locale](locales-and-languages.md) has a default calendar type (data type CALTYPE) associated with it.</span></span> <span data-ttu-id="b0383-107">Ein Gebiets Schema kann auch einen alternativen Kalendertyp aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b0383-107">A locale can also have an alternate calendar type.</span></span> <span data-ttu-id="b0383-108">Ausführliche Informationen zu Kalender Typen finden Sie unter [Calendar Type-Informationen](calendar-type-information.md).</span><span class="sxs-lookup"><span data-stu-id="b0383-108">For details of calendar types, see [Calendar Type Information](calendar-type-information.md).</span></span>

> [!Note]  
> <span data-ttu-id="b0383-109">Um einen alternativen Kalendertyp für ein Gebiets Schema zu verwenden, muss die Anwendung das Gebiets Schema [ \_ ioptionalcalendar](locale-ioptionalcalendar.md) -Konstante auf den alternativen Kalendertyp für das Gebiets Schema festlegen.</span><span class="sxs-lookup"><span data-stu-id="b0383-109">To use an alternate calendar type for a locale, your application must set the [LOCALE\_IOPTIONALCALENDAR](locale-ioptionalcalendar.md) constant to the alternate calendar type for the locale.</span></span>

 

<span data-ttu-id="b0383-110">Die meisten Gebiets Schemas verwenden den gregorianischen Standardkalender und eine festgelegte Anzahl von Datumsformaten.</span><span class="sxs-lookup"><span data-stu-id="b0383-110">Most locales use the standard Gregorian calendar and a set number of date formats.</span></span> <span data-ttu-id="b0383-111">Diese Standardoptionen für Datumsformate können mithilfe der Funktion " [**enumdateformatsex**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa) " oder " [**enumdateformatsexex**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex) " angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b0383-111">These default choices for date formats are available for display by using the [**EnumDateFormatsEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa) or [**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex) function.</span></span>

<span data-ttu-id="b0383-112">Bei einigen Gebiets Schemas müssen beim Erstellen einer kompletten Liste von Formatoptionen besondere Aspekte berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="b0383-112">Some locales require special considerations when creating a complete list of format choices.</span></span> <span data-ttu-id="b0383-113">Für einige dieser Gebiets Schemas müssen Text Zeichenfolgen in die Datumsformat Zeichenfolge eingefügt werden, während andere eine völlig andere Berechnungsmethode für die Werte benötigen.</span><span class="sxs-lookup"><span data-stu-id="b0383-113">Some of these locales require text strings to be inserted in the date format string, while others require a completely different method of computation of the values.</span></span> <span data-ttu-id="b0383-114">Eine Anwendung adressiert diese speziellen Anforderungen durch das Hinzufügen bestimmter Gebiets Schema-Informationstypen und Kalender Typen.</span><span class="sxs-lookup"><span data-stu-id="b0383-114">An application addresses these special requirements by the addition of certain locale information types and calendar types.</span></span>

<span data-ttu-id="b0383-115">Ausführliche Informationen zum Implementieren von Datumsangaben und Kalender in Ihren Anwendungen finden Sie unter [Abrufen von Zeit-und Datumsangaben](retrieving-time-and-date-information.md).</span><span class="sxs-lookup"><span data-stu-id="b0383-115">For details about implementing dates and calendars in your applications, see [Retrieving Time and Date Information](retrieving-time-and-date-information.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0383-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b0383-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0383-117">Informationen zur Unterstützung der Landessprache</span><span class="sxs-lookup"><span data-stu-id="b0383-117">About National Language Support</span></span>](about-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="b0383-118">Kalendertyp Informationen</span><span class="sxs-lookup"><span data-stu-id="b0383-118">Calendar Type Information</span></span>](calendar-type-information.md)
</dt> <dt>

[<span data-ttu-id="b0383-119">Abrufen von Zeit-und Datumsinformationen</span><span class="sxs-lookup"><span data-stu-id="b0383-119">Retrieving Time and Date Information</span></span>](retrieving-time-and-date-information.md)
</dt> <dt>

[<span data-ttu-id="b0383-120">**Enumdateformatsex**</span><span class="sxs-lookup"><span data-stu-id="b0383-120">**EnumDateFormatsEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)
</dt> <dt>

[<span data-ttu-id="b0383-121">**Enumdateformatsexex**</span><span class="sxs-lookup"><span data-stu-id="b0383-121">**EnumDateFormatsExEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)
</dt> </dl>

 

 



