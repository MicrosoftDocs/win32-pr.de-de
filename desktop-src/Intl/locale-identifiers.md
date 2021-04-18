---
description: Jedes Gebiets Schema hat einen eindeutigen Bezeichner, einen 32-Bit-Wert, der aus einer Sprach-ID und einer Sortierreihenfolge-ID besteht.
ms.assetid: ea45b0e5-7df7-47fb-8dad-fccfbe53fec0
title: Gebiets Schema Bezeichner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7b2f11189f44b8555081d589f3e9ba2ed131cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339729"
---
# <a name="locale-identifiers"></a><span data-ttu-id="80345-103">Gebiets Schema Bezeichner</span><span class="sxs-lookup"><span data-stu-id="80345-103">Locale Identifiers</span></span>

<span data-ttu-id="80345-104">Jedes [Gebiets](locales-and-languages.md) Schema hat einen eindeutigen Bezeichner, einen 32-Bit-Wert, der aus einer [sprach](language-identifiers.md) -ID und einer [Sortierreihenfolge](sort-order-identifiers.md)-ID besteht.</span><span class="sxs-lookup"><span data-stu-id="80345-104">Each [locale](locales-and-languages.md) has a unique identifier, a 32-bit value that consists of a [language identifier](language-identifiers.md) and a [sort order identifier](sort-order-identifiers.md).</span></span> <span data-ttu-id="80345-105">Der Gebiets Schema Bezeichner ist eine standardmäßige internationale numerische Abkürzung und verfügt über die Komponenten, die zur eindeutigen Identifizierung eines der installierten, Betriebssystem definierten Gebiets Schemas erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="80345-105">The locale identifier is a standard international numeric abbreviation and has the components necessary to uniquely identify one of the installed operating system-defined locales.</span></span> <span data-ttu-id="80345-106">NLS unterstützt sowohl vordefinierte Gebiets Schema Bezeichner als auch benutzerdefinierte Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="80345-106">NLS supports both predefined locale identifiers and custom identifiers.</span></span>

> [!Note]  
> <span data-ttu-id="80345-107">Gebiets Schema Namen können mit in Windows Vista eingeführten Funktionen verwendet werden, die anstelle eines Gebiets Schema Bezeichners einen Gebiets Schema [Namen](locale-names.md) als Parameter annehmen.</span><span class="sxs-lookup"><span data-stu-id="80345-107">Locale names can be used with functions introduced in Windows Vista that take a [locale name](locale-names.md) as a parameter, instead of a locale identifier.</span></span> <span data-ttu-id="80345-108">Weitere Informationen finden Sie unter [Aufrufen der "locale Name"-Funktionen](calling-the--locale-name--functions.md).</span><span class="sxs-lookup"><span data-stu-id="80345-108">For more information, see [Calling the "Locale Name" Functions](calling-the--locale-name--functions.md).</span></span> <span data-ttu-id="80345-109">Die Verwendung von Gebiets Schema Namen anstelle von Gebiets Schema bezeichnermerkmalen ist immer vorzuziehen.</span><span class="sxs-lookup"><span data-stu-id="80345-109">Use of locale names instead of locale identifiers is always preferable.</span></span>

 

<span data-ttu-id="80345-110">Die folgende Abbildung zeigt das Format der Bits in einem Gebiets Schema Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="80345-110">The following illustration shows the format of the bits in a locale identifier.</span></span>

``` syntax
+-------------+---------+-------------------------+
|   Reserved  | Sort ID |      Language ID        |
+-------------+---------+-------------------------+
31         20 19     16 15                      0   bit
```

## <a name="predefined-locale-identifiers"></a><span data-ttu-id="80345-111">Vordefinierte Gebiets Schema Bezeichner</span><span class="sxs-lookup"><span data-stu-id="80345-111">Predefined Locale Identifiers</span></span>

<span data-ttu-id="80345-112">Die von NLS unterstützten vordefinierten Gebiets Schema Bezeichner sind in der API-Referenz für die [National Language Support (NLS)](/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c)definiert.</span><span class="sxs-lookup"><span data-stu-id="80345-112">The predefined locale identifiers supported by NLS are defined in the [National Language Support (NLS) API Reference](/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c).</span></span>

<span data-ttu-id="80345-113">NLS verwendet die folgenden Gebiets Schema Informations Konstanten zur Darstellung von Gebiets Schema Bezeichners.</span><span class="sxs-lookup"><span data-stu-id="80345-113">NLS uses the following locale information constants to represent locale identifiers.</span></span>

-   <span data-ttu-id="80345-114">Gebiets Schema [ \_ SLanguage](locale-slanguage.md) oder [locale \_ slocalizedlanguagename](locale-slocalized-constants.md)</span><span class="sxs-lookup"><span data-stu-id="80345-114">[LOCALE\_SLANGUAGE](locale-slanguage.md) or [LOCALE\_SLOCALIZEDLANGUAGENAME](locale-slocalized-constants.md)</span></span>
-   [<span data-ttu-id="80345-115">Name des Gebiets Schemas \_</span><span class="sxs-lookup"><span data-stu-id="80345-115">LOCALE\_SNAME</span></span>](locale-sname.md)
-   [<span data-ttu-id="80345-116">Gebiets Schema- \_ sscripts</span><span class="sxs-lookup"><span data-stu-id="80345-116">LOCALE\_SSCRIPTS</span></span>](locale-sscripts.md)
-   [<span data-ttu-id="80345-117">Gebiets Schema \_ idefaultansicodepage</span><span class="sxs-lookup"><span data-stu-id="80345-117">LOCALE\_IDEFAULTANSICODEPAGE</span></span>](locale-idefault-constants.md)

## <a name="custom-locale-identifiers"></a><span data-ttu-id="80345-118">Benutzerdefinierte Gebiets Schema Bezeichner</span><span class="sxs-lookup"><span data-stu-id="80345-118">Custom Locale Identifiers</span></span>

<span data-ttu-id="80345-119">**Windows Vista:** NLS unterstützt die benutzerdefinierten Gebiets Schema Bezeichner, die durch die folgenden Gebiets Schema Informations Konstanten dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="80345-119">**Windows Vista:** NLS supports the custom locale identifiers represented by the following locale information constants.</span></span>

-   [<span data-ttu-id="80345-120">\_benutzerdefinierter locale- \_ Standard</span><span class="sxs-lookup"><span data-stu-id="80345-120">LOCALE\_CUSTOM\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="80345-121">benutzerdefinierte Benutzeroberflächen- \_ \_ \_ Standardeinstellung</span><span class="sxs-lookup"><span data-stu-id="80345-121">LOCALE\_CUSTOM\_UI\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="80345-122">Gebiets Schema \_ Benutzer \_ definiert nicht angegeben</span><span class="sxs-lookup"><span data-stu-id="80345-122">LOCALE\_CUSTOM\_UNSPECIFIED</span></span>](locale-custom-constants.md)

## <a name="building-a-locale"></a><span data-ttu-id="80345-123">Aufbauen eines Gebiets Schemas</span><span class="sxs-lookup"><span data-stu-id="80345-123">Building a Locale</span></span>

<span data-ttu-id="80345-124">Zum Erstellen von Gebiets Schemas können Sie das von NLS bereitgestellte Hilfsprogramm "Locale Builder" verwenden.</span><span class="sxs-lookup"><span data-stu-id="80345-124">You can use the Locale Builder utility provided by NLS to build locales.</span></span> <span data-ttu-id="80345-125">Weitere Informationen finden Sie unter [Microsoft Locale Builder](https://www.microsoft.com/download/details.aspx?id=41158).</span><span class="sxs-lookup"><span data-stu-id="80345-125">For more information, see [Microsoft Locale Builder](https://www.microsoft.com/download/details.aspx?id=41158).</span></span>

<span data-ttu-id="80345-126">Die Anwendung kann einen Gebiets Schema Bezeichner mit dem [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) -Makro erstellen.</span><span class="sxs-lookup"><span data-stu-id="80345-126">Your application can construct a locale identifier using the [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) macro.</span></span> <span data-ttu-id="80345-127">Alternativ kann Sie einen der Standard Bezeichner verwenden, die den unten aufgeführten Konstanten entsprechen.</span><span class="sxs-lookup"><span data-stu-id="80345-127">Alternatively it can use one of the default identifiers corresponding to the constants listed below.</span></span>

-   [<span data-ttu-id="80345-128">Gebiets Schema \_ invariant</span><span class="sxs-lookup"><span data-stu-id="80345-128">LOCALE\_INVARIANT</span></span>](locale-invariant.md)
-   [<span data-ttu-id="80345-129">Standard für Gebiets Schema \_ System \_</span><span class="sxs-lookup"><span data-stu-id="80345-129">LOCALE\_SYSTEM\_DEFAULT</span></span>](locale-system-default.md)
-   [<span data-ttu-id="80345-130">\_Standardbenutzer Name für locale \_</span><span class="sxs-lookup"><span data-stu-id="80345-130">LOCALE\_USER\_DEFAULT</span></span>](locale-user-default.md)

## <a name="retrieval-of-locale-identifiers"></a><span data-ttu-id="80345-131">Abrufen von Gebiets Schema Bezeichnerzeichen</span><span class="sxs-lookup"><span data-stu-id="80345-131">Retrieval of Locale Identifiers</span></span>

<span data-ttu-id="80345-132">Eine Anwendung kann die aktuellen Gebiets Schema Bezeichner mithilfe der Funktionen [**GetSystemDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlcid) und [**GetUserDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlcid) abrufen.</span><span class="sxs-lookup"><span data-stu-id="80345-132">An application can retrieve the current locale identifiers by using the [**GetSystemDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlcid) and [**GetUserDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlcid) functions.</span></span> <span data-ttu-id="80345-133">Jeder Thread kann sein eigenes Gebiets Schema mit [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) und [**getthreadlocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale)festlegen und abrufen.</span><span class="sxs-lookup"><span data-stu-id="80345-133">Each thread can set and retrieve its own locale with [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) and [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale).</span></span>

## <a name="related-topics"></a><span data-ttu-id="80345-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="80345-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80345-135">Gebiets Schemas und Sprachen</span><span class="sxs-lookup"><span data-stu-id="80345-135">Locales and Languages</span></span>](locales-and-languages.md)
</dt> <dt>

[<span data-ttu-id="80345-136">Sprachen-IDs</span><span class="sxs-lookup"><span data-stu-id="80345-136">Language Identifiers</span></span>](language-identifiers.md)
</dt> <dt>

[<span data-ttu-id="80345-137">Gebiets Schema Namen</span><span class="sxs-lookup"><span data-stu-id="80345-137">Locale Names</span></span>](locale-names.md)
</dt> <dt>

[<span data-ttu-id="80345-138">Sortierreihenfolge-IDs</span><span class="sxs-lookup"><span data-stu-id="80345-138">Sort Order Identifiers</span></span>](sort-order-identifiers.md)
</dt> <dt>

[<span data-ttu-id="80345-139">**MAKELCID**</span><span class="sxs-lookup"><span data-stu-id="80345-139">**MAKELCID**</span></span>](/windows/desktop/api/Winnt/nf-winnt-makelcid)
</dt> </dl>

 

 
