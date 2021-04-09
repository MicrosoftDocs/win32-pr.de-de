---
description: Verwenden von persistenten Gebiets Schema Daten
ms.assetid: f62402d6-31de-4ff7-9538-7925a007a089
title: Verwenden von persistenten Gebiets Schema Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4fe4990da53e4db9f71b2feffbd9eb40aedee9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869076"
---
# <a name="using-persistent-locale-data"></a><span data-ttu-id="6315a-103">Verwenden von persistenten Gebiets Schema Daten</span><span class="sxs-lookup"><span data-stu-id="6315a-103">Using Persistent Locale Data</span></span>

<span data-ttu-id="6315a-104">Eine globalisierte Anwendung speichert oder überträgt häufig Daten, z. b. Datum und Uhrzeit.</span><span class="sxs-lookup"><span data-stu-id="6315a-104">A globalized application often persists or transmits data, for example, time and date.</span></span> <span data-ttu-id="6315a-105">Beachten Sie bei der Entscheidung, wie Ihre Anwendung die Daten Persistenz verarbeiten soll,, dass die Daten nicht garantiert identisch mit dem Computer oder zwischen den Ausführungen der Anwendung sind.</span><span class="sxs-lookup"><span data-stu-id="6315a-105">When deciding how your application should handle data persistence, remember that data is not guaranteed to be the same from computer to computer or between runs of the application.</span></span> <span data-ttu-id="6315a-106">Dies gilt [für beide Gebiets](locales-and-languages.md) Schemas, die mit Windows und [benutzerdefinierten](custom-locales.md)Gebiets Schemata ausgeliefert werden.</span><span class="sxs-lookup"><span data-stu-id="6315a-106">This is true for both [locales](locales-and-languages.md) that ship with Windows and [custom locales](custom-locales.md).</span></span>

<span data-ttu-id="6315a-107">Beim Entwerfen der Anwendung müssen eine Vielzahl von Gebiets Schema bezogenen Datenänderungen berücksichtigt werden, die auftreten können.</span><span class="sxs-lookup"><span data-stu-id="6315a-107">Design of the application must take into account a variety of locale-related data changes that can occur.</span></span> <span data-ttu-id="6315a-108">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="6315a-108">For example:</span></span>

-   <span data-ttu-id="6315a-109">Währungssymbole können sich ändern, wenn Länder den Euro annehmen.</span><span class="sxs-lookup"><span data-stu-id="6315a-109">Currency symbols can change as countries adopt the Euro.</span></span>
-   <span data-ttu-id="6315a-110">Regionale Einstellungen können sich ändern.</span><span class="sxs-lookup"><span data-stu-id="6315a-110">Regional preferences can change.</span></span> <span data-ttu-id="6315a-111">Beispielsweise kann das Format d/m/y für ein bestimmtes Gebiets Schema in das Format m/d/y geändert werden.</span><span class="sxs-lookup"><span data-stu-id="6315a-111">For example, the format d/m/y might change to the format m/d/y for a particular locale.</span></span>
-   <span data-ttu-id="6315a-112">Die Schreibweise von Tagnamen kann aufgrund von Rechtschreibreform geändert werden.</span><span class="sxs-lookup"><span data-stu-id="6315a-112">The spelling of day names can change due to spelling reforms.</span></span> <span data-ttu-id="6315a-113">Außerdem können sich die Groß-/Kleinschreibung für Monats-oder Tages Namen ändern</span><span class="sxs-lookup"><span data-stu-id="6315a-113">Additionally, casing can change for month or day names.</span></span>

## <a name="use-locale-independent-formats-for-storage-and-data-interchange"></a><span data-ttu-id="6315a-114">Verwenden von Locale-Independent Formaten für den Speicher-und Datenaustausch</span><span class="sxs-lookup"><span data-stu-id="6315a-114">Use Locale-Independent Formats for Storage and Data Interchange</span></span>

<span data-ttu-id="6315a-115">Eine Anwendung, die Daten beibehält, sollte Gebiets Schema unabhängige Formate für den Speicher-und Datenaustausch verwenden.</span><span class="sxs-lookup"><span data-stu-id="6315a-115">An application that persists data should use locale-independent formats for storage and data interchange.</span></span> <span data-ttu-id="6315a-116">Beispiele sind hart codierte oder Standardformate. Der invariante Gebiets [Schema \_ Name \_ ](locale-name-constants.md)für das Gebiets Schema und binäre Speicherformate.</span><span class="sxs-lookup"><span data-stu-id="6315a-116">Examples are hard-coded or standard formats; the invariant locale [LOCALE\_NAME\_INVARIANT](locale-name-constants.md); and binary storage formats.</span></span>

<span data-ttu-id="6315a-117">Wenn persistente Sortier Daten erforderlich sind, muss die Anwendung die [**comparestringordinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="6315a-117">If persistent sorting data is required, the application must use the [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) function.</span></span> <span data-ttu-id="6315a-118">Beachten Sie, dass ein invarianter Format nicht für die [Sortierung](sorting.md)invariante bleibt, sondern nur für Gebiets Schema-und Kalenderdaten.</span><span class="sxs-lookup"><span data-stu-id="6315a-118">Remember that an invariant format does not remain invariant for [sorting](sorting.md), only for locale and calendar data.</span></span>

## <a name="use-the-user-default-locale-for-data-presentation"></a><span data-ttu-id="6315a-119">Verwenden des Standard Gebiets Schemas für die Datenpräsentation</span><span class="sxs-lookup"><span data-stu-id="6315a-119">Use the User Default Locale for Data Presentation</span></span>

<span data-ttu-id="6315a-120">Um persistente Daten darzustellen, empfiehlt es sich, die Daten mit dem Standard Gebiets Schema des Benutzers neu zu formatieren.</span><span class="sxs-lookup"><span data-stu-id="6315a-120">To present persistent data, it is best for the application to reformat the data using the user default locale.</span></span> <span data-ttu-id="6315a-121">Die Verwendung dieses Gebiets Schemas ermöglicht Benutzer Überschreibungen.</span><span class="sxs-lookup"><span data-stu-id="6315a-121">Use of this locale allows user overrides.</span></span> <span data-ttu-id="6315a-122">Weitere Informationen finden Sie unter [locale \_ User \_ default](locale-user-default.md).</span><span class="sxs-lookup"><span data-stu-id="6315a-122">For more information, see [LOCALE\_USER\_DEFAULT](locale-user-default.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6315a-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6315a-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6315a-124">Verwenden der Unterstützung für nationale Sprache</span><span class="sxs-lookup"><span data-stu-id="6315a-124">Using National Language Support</span></span>](using-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="6315a-125">Benutzerdefinierte Gebiets Schemata</span><span class="sxs-lookup"><span data-stu-id="6315a-125">Custom Locales</span></span>](custom-locales.md)
</dt> <dt>

[<span data-ttu-id="6315a-126">Sortierung</span><span class="sxs-lookup"><span data-stu-id="6315a-126">Sorting</span></span>](sorting.md)
</dt> </dl>

 

 



