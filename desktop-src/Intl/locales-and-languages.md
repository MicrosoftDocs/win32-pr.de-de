---
description: Der Begriff &\# 0034; Sprache&\# 0034; gibt eine Sammlung von Eigenschaften an, die bei der gesprochenen und geschriebenen Kommunikation verwendet werden.
ms.assetid: 8214c00d-4ec6-4597-8088-7819a160f0dc
title: Gebiets Schemas und Sprachen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2c0d0fa41b9186b2135d9497d52de24577bbae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357412"
---
# <a name="locales-and-languages"></a><span data-ttu-id="62cf7-103">Gebiets Schemas und Sprachen</span><span class="sxs-lookup"><span data-stu-id="62cf7-103">Locales and Languages</span></span>

<span data-ttu-id="62cf7-104">Der Begriff "Sprache" gibt eine Sammlung von Eigenschaften an, die bei der gesprochenen und geschriebenen Kommunikation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="62cf7-104">The term "language" indicates a collection of properties used in spoken and written communication.</span></span> <span data-ttu-id="62cf7-105">Jede Sprache verfügt über einen Sprachnamen und einen sprach Bezeichner, der die jeweilige [Codepage](code-pages.md) (ANSI, DOS, Macintosh) angibt, die zum Darstellen des [geografischen Standorts](table-of-geographical-locations.md) für die Sprache des Betriebssystems verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="62cf7-105">Each language has a language name and a language identifier that indicate the particular [code page](code-pages.md) (ANSI, DOS, Macintosh) used to represent the [geographical location](table-of-geographical-locations.md) for the language on the operating system.</span></span> <span data-ttu-id="62cf7-106">Eine neutrale Sprache wird durch einen Namen wie "en" für Englisch angegeben.</span><span class="sxs-lookup"><span data-stu-id="62cf7-106">A neutral language is indicated by a name such as "en" for English.</span></span> <span data-ttu-id="62cf7-107">Eine geografisch spezifischere Sprache kann durch einen Namen angegeben werden, der sowohl Gebiets Schema-als auch Land-/Regionsinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="62cf7-107">A more geographically specific language can be indicated by a name that includes both locale and country/region information.</span></span> <span data-ttu-id="62cf7-108">Beispielsweise hat das Gebiets Schema Englisch (USA) den Sprachen Namen "en-US".</span><span class="sxs-lookup"><span data-stu-id="62cf7-108">For example, the locale English (United States) has the language name "en-US".</span></span>

<span data-ttu-id="62cf7-109">Ein "Gebiets Schema" ist eine Sammlung von sprachbezogenen Benutzer Einstellungs Informationen, die als Liste von Werten dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="62cf7-109">A "locale" is a collection of language-related user preference information represented as a list of values.</span></span> <span data-ttu-id="62cf7-110">Windows XP unterstützt mehr als 150 Gebiets Schemas, und Windows Vista unterstützt etwa 200.</span><span class="sxs-lookup"><span data-stu-id="62cf7-110">Windows XP supports more than 150 locales, and Windows Vista supports about 200.</span></span> <span data-ttu-id="62cf7-111">Jedes Gebiets Schema wird durch eine Sprache und eine Sortierreihenfolge definiert und verfügt sowohl über einen Gebiets Schema Namen als auch über einen Gebiets Schema Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="62cf7-111">Each locale is defined by a language and a sort order, and has both a locale name and a locale identifier.</span></span> <span data-ttu-id="62cf7-112">Ein Beispiel für einen Gebiets Schema Namen für Deutsch (Deutschland) ist "de-de \_ Phonebook".</span><span class="sxs-lookup"><span data-stu-id="62cf7-112">An example of a locale name for German (Germany) is "de-DE\_phonebook".</span></span>

<span data-ttu-id="62cf7-113">Jedes Betriebssystem verfügt über mindestens ein installiertes Gebiets Schema und verfügt häufig über viele Gebiets Schemas, aus denen der Benutzer auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="62cf7-113">Each operating system has at least one installed locale and often has many locales from which the user can select.</span></span> <span data-ttu-id="62cf7-114">Jedes Gebiets Schema verfügt über eine Vielzahl von Informationen, die mit dem Namen und Bezeichner verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="62cf7-114">Each locale has a variety of information associated with it, other than its name and identifier.</span></span> <span data-ttu-id="62cf7-115">Gebiets Schema Informationstypen werden unter "Gebiets Schema [Informations Konstanten](locale-information-constants.md)" beschrieben.</span><span class="sxs-lookup"><span data-stu-id="62cf7-115">Locale information types are described in [Locale Information Constants](locale-information-constants.md).</span></span>

<span data-ttu-id="62cf7-116">Das Betriebssystem weist jedem Thread ein Gebiets Schema zu und weist anfänglich das "System Standard Gebiets Schema" zu, das durch das Gebiets Schema [ \_ System \_ default](locale-system-default.md)definiert ist.</span><span class="sxs-lookup"><span data-stu-id="62cf7-116">The operating system assigns a locale to each thread, initially assigning the "system default locale," defined by [LOCALE\_SYSTEM\_DEFAULT](locale-system-default.md).</span></span> <span data-ttu-id="62cf7-117">Dieses Gebiets Schema wird festgelegt, wenn das Betriebssystem installiert wird, oder wenn der Benutzer es mithilfe der Optionen Regions-und Sprachoptionen der Systemsteuerung auswählt.</span><span class="sxs-lookup"><span data-stu-id="62cf7-117">This locale is set when the operating system is installed or when the user selects it using the regional and language options portion of the Control Panel.</span></span> <span data-ttu-id="62cf7-118">Beim Ausführen eines Threads in einem Prozess, der dem Benutzer angehört, weist das Betriebssystem dem Thread das Standard Gebiets Schema des Benutzers zu.</span><span class="sxs-lookup"><span data-stu-id="62cf7-118">When running a thread in a process belonging to the user, the operating system assigns the "user default locale" to the thread.</span></span> <span data-ttu-id="62cf7-119">Dieses Gebiets Schema wird von der [locale \_ User \_ default](locale-user-default.md)definiert.</span><span class="sxs-lookup"><span data-stu-id="62cf7-119">This locale is defined by [LOCALE\_USER\_DEFAULT](locale-user-default.md).</span></span> <span data-ttu-id="62cf7-120">Eine Anwendung kann beide Standardeinstellungen überschreiben, indem Sie die [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) -Funktion verwendet, um das Gebiets Schema für einen Thread explizit festzulegen.</span><span class="sxs-lookup"><span data-stu-id="62cf7-120">An application can override either default by using the [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) function to explicitly set the locale for a thread.</span></span>

<span data-ttu-id="62cf7-121">Die Implementierung einer Sprache erfordert ein entsprechendes Gebiets Schema.</span><span class="sxs-lookup"><span data-stu-id="62cf7-121">Implementation of a language requires a corresponding locale.</span></span> <span data-ttu-id="62cf7-122">Das Betriebssystem implementiert eine neutrale Sprache durch Auswahl der Daten für das Gebiets Schema, das einer bestimmten Version der Sprache zugeordnet ist, in der Regel das am weitesten verbreitete Gebiets Schema.</span><span class="sxs-lookup"><span data-stu-id="62cf7-122">The operating system implements a neutral language by selecting the data for the locale associated with a specific version of the language, usually the most widespread locale.</span></span>

<span data-ttu-id="62cf7-123">Ab Windows Vista ist es möglich, dass eine bestimmte Sprache einem ergänzenden Gebiets Schema entspricht, bei dem es sich um eine Art benutzerdefiniertes Gebiets Schema handelt.</span><span class="sxs-lookup"><span data-stu-id="62cf7-123">Starting with Windows Vista, it is possible for a particular language to correspond to a supplemental locale, which is a type of custom locale.</span></span> <span data-ttu-id="62cf7-124">Da ergänzende Gebiets Schemas alle einen einzelnen Gebiets Schema Bezeichner gemeinsam nutzen, sollten Ihre Anwendungen diese Gebiets Schemas und die entsprechenden Sprachen nach Namen anstelle von Bezeichner verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="62cf7-124">Since supplemental locales all share a single locale identifier, your applications should handle these locales and the corresponding languages by name instead of by identifier.</span></span>

<span data-ttu-id="62cf7-125">Sprach Konzepte sind eng mit Gebiets Schema Konzepten verknüpft, aber die beiden Begriffe sind nicht austauschbar.</span><span class="sxs-lookup"><span data-stu-id="62cf7-125">Language concepts are closely related to locale concepts, but the two terms are not interchangeable.</span></span> <span data-ttu-id="62cf7-126">Im Allgemeinen sind Funktionen, die sich auf die [mehrsprachige Benutzeroberfläche](multilingual-user-interface.md) beziehen, mit Sprachen zu tun, während die NLS-Funktionen auf Gebiets Schemas reagieren.</span><span class="sxs-lookup"><span data-stu-id="62cf7-126">As a general rule, functions related to the [Multilingual User Interface](multilingual-user-interface.md) deal with languages, while the NLS functions act upon locales.</span></span>

<span data-ttu-id="62cf7-127">In diesem Abschnitt werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="62cf7-127">The following topics are covered in this section:</span></span>

-   [<span data-ttu-id="62cf7-128">Benutzerdefinierte Gebiets Schemata</span><span class="sxs-lookup"><span data-stu-id="62cf7-128">Custom Locales</span></span>](custom-locales.md)
-   [<span data-ttu-id="62cf7-129">Sprachen-IDs</span><span class="sxs-lookup"><span data-stu-id="62cf7-129">Language Identifiers</span></span>](language-identifiers.md)
-   [<span data-ttu-id="62cf7-130">Sprachnamen</span><span class="sxs-lookup"><span data-stu-id="62cf7-130">Language Names</span></span>](language-names.md)
-   [<span data-ttu-id="62cf7-131">Gebiets Schema Bezeichner</span><span class="sxs-lookup"><span data-stu-id="62cf7-131">Locale Identifiers</span></span>](locale-identifiers.md)
-   [<span data-ttu-id="62cf7-132">Gebiets Schema Namen</span><span class="sxs-lookup"><span data-stu-id="62cf7-132">Locale Names</span></span>](locale-names.md)
-   [<span data-ttu-id="62cf7-133">Pseudo Gebiets Schemata</span><span class="sxs-lookup"><span data-stu-id="62cf7-133">Pseudo-Locales</span></span>](pseudo-locales.md)

## <a name="related-topics"></a><span data-ttu-id="62cf7-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="62cf7-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62cf7-135">Informationen zur Unterstützung der Landessprache</span><span class="sxs-lookup"><span data-stu-id="62cf7-135">About National Language Support</span></span>](about-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="62cf7-136">Codepages</span><span class="sxs-lookup"><span data-stu-id="62cf7-136">Code Pages</span></span>](code-pages.md)
</dt> <dt>

[<span data-ttu-id="62cf7-137">Gebiets Schema Informations Konstanten</span><span class="sxs-lookup"><span data-stu-id="62cf7-137">Locale Information Constants</span></span>](locale-information-constants.md)
</dt> <dt>

[<span data-ttu-id="62cf7-138">Multilingual User Interface</span><span class="sxs-lookup"><span data-stu-id="62cf7-138">Multilingual User Interface</span></span>](multilingual-user-interface.md)
</dt> <dt>

[<span data-ttu-id="62cf7-139">Tabelle der geografischen Standorte</span><span class="sxs-lookup"><span data-stu-id="62cf7-139">Table of Geographical Locations</span></span>](table-of-geographical-locations.md)
</dt> <dt>

[<span data-ttu-id="62cf7-140">Sprach Verwaltung in der Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="62cf7-140">User Interface Language Management</span></span>](user-interface-language-management.md)
</dt> <dt>

[<span data-ttu-id="62cf7-141">**SetThreadLocale**</span><span class="sxs-lookup"><span data-stu-id="62cf7-141">**SetThreadLocale**</span></span>](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale)
</dt> </dl>

 

 



