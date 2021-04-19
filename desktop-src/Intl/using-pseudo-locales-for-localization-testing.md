---
description: Unter Windows Vista und höher können Sie Pseudo Gebiets Schemata zum Testen der Lokalisier barkeit von Anwendungen verwenden. Dieses Thema enthält Verfahren für die Verwendung von Pseudo Codes.
ms.assetid: 1eccdbb9-a1bd-443a-a5f6-d64c9e5c87b3
title: Verwenden von Pseudo Gebiets Schemata für Lokalisier barkeits Tests
ms.topic: article
ms.date: 07/05/2018
ms.openlocfilehash: f8c6b435b85a5bef98eff9bf76681096779433e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357098"
---
# <a name="using-pseudo-locales-for-localizability-testing"></a><span data-ttu-id="40eaf-104">Verwenden von Pseudo Gebiets Schemata für Lokalisier barkeits Tests</span><span class="sxs-lookup"><span data-stu-id="40eaf-104">Using pseudo-locales for localizability testing</span></span>

<span data-ttu-id="40eaf-105">[Pseudo](pseudo-locales.md) Gebiets Schemas sind in Windows Vista und höher integriert, sodass Sie über APIs für die nationale Sprachunterstützung (NLS) darauf zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="40eaf-105">[Pseudo-locales](pseudo-locales.md) are built in to Windows Vista and later, so that you can access them via National Language Support (NLS) APIs.</span></span> <span data-ttu-id="40eaf-106">Sie können Pseudo Gebiets Schemas verwenden, um die [Lokalisier barkeit](/windows/uwp/design/globalizing/globalizing-portal) Ihrer Anwendungen zu testen.</span><span class="sxs-lookup"><span data-stu-id="40eaf-106">You can use pseudo-locales to test the [localizability](/windows/uwp/design/globalizing/globalizing-portal) of your applications.</span></span> <span data-ttu-id="40eaf-107">Dieses Thema enthält Verfahren für die Verwendung von Pseudo Codes.</span><span class="sxs-lookup"><span data-stu-id="40eaf-107">This topic includes procedures for using pseudo-codes.</span></span>

> [!NOTE]
> <span data-ttu-id="40eaf-108">Eine Aufgabe, die bei Pseudo Gebiets Schemata besonders berücksichtigt werden muss, besteht darin, Sie aufzulisten. ob in Ihrem Code oder in den Regions-und Sprachoptionen in der Systemsteuerung.</span><span class="sxs-lookup"><span data-stu-id="40eaf-108">One task that needs special consideration when it comes to pseudo-locales is enumerating them; whether in your code, or in the regional and language options portion of the Control Panel.</span></span> <span data-ttu-id="40eaf-109">Weitere Informationen dazu weiter unten in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="40eaf-109">More on that later in this topic.</span></span>

<span data-ttu-id="40eaf-110">Die Namen der Pseudo Gebiets Schemata lauten "QPS-ploc", "QPS-Ploca" und "QPS-plocm".</span><span class="sxs-lookup"><span data-stu-id="40eaf-110">The names of the pseudo-locales are "qps-ploc", "qps-ploca", and "qps-plocm".</span></span> <span data-ttu-id="40eaf-111">Ab Windows 10 ist auch das Pseudo Gebiets Schema "QPS-Latn-x-sh" verfügbar.</span><span class="sxs-lookup"><span data-stu-id="40eaf-111">As of Windows 10, the pseudo-locale "qps-Latn-x-sh" is also available.</span></span>

## <a name="retrieve-information-about-pseudo-locales"></a><span data-ttu-id="40eaf-112">Abrufen von Informationen zu Pseudo Gebiets Schemata</span><span class="sxs-lookup"><span data-stu-id="40eaf-112">Retrieve information about pseudo-locales</span></span>

<span data-ttu-id="40eaf-113">Sie können [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) zum Abrufen von Informationen zu einem Pseudo Gebiets Schema verwenden.</span><span class="sxs-lookup"><span data-stu-id="40eaf-113">You can use [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) to retrieve information about a pseudo-locale.</span></span> <span data-ttu-id="40eaf-114">Übergeben Sie den Namen des jeweiligen Pseudo Gebiets Schemas an die Funktion (siehe oben genannte Liste der Namen).</span><span class="sxs-lookup"><span data-stu-id="40eaf-114">Pass into the function the name of the particular pseudo-locale (see the list of names above).</span></span> <span data-ttu-id="40eaf-115">Beispiel: "QPS-plocm" für das gespiegelte Pseudo Gebiets Schema.</span><span class="sxs-lookup"><span data-stu-id="40eaf-115">For example, "qps-plocm" for the mirrored pseudo-locale.</span></span>

```cpp
wchar_t languageIdentifier[5];
int rc{ ::GetLocaleInfoEx(L"qps-plocm", LOCALE_ILANGUAGE, languageIdentifier, 5) };
```

## <a name="use-localenametolcid-with-pseudo-locales"></a><span data-ttu-id="40eaf-116">Verwenden von LocaleNameToLCID mit Pseudo Gebiets Schemata</span><span class="sxs-lookup"><span data-stu-id="40eaf-116">Use LocaleNameToLCID with pseudo-locales</span></span>

<span data-ttu-id="40eaf-117">Sie können die NLS-Mapping-Funktion [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) mit dem Namen eines Pseudo Gebiets Schemas aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="40eaf-117">You can call the NLS mapping function [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) with the name of a pseudo-locale.</span></span>

```cpp
LCID lcid{ ::LocaleNameToLCID(L"qps-plocm", 0) };
```

## <a name="enable-pseudo-locales-for-enumeration"></a><span data-ttu-id="40eaf-118">Pseudo Gebiets Schemas für Enumeration aktivieren</span><span class="sxs-lookup"><span data-stu-id="40eaf-118">Enable pseudo-locales for enumeration</span></span>

<span data-ttu-id="40eaf-119">In Ihrer Anwendung können Sie [**enumsystemlocalesex**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) aufrufen, um die Gebiets Schemas aufzulisten, die vom System erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="40eaf-119">In your application, you can call [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) to enumerate the locales that the system recognizes.</span></span> <span data-ttu-id="40eaf-120">Der Bereich Regions-und Sprachoptionen in der Systemsteuerung ruft auch **enumsystemlocalesex** auf, um die Liste der Gebiets Schemas, die es anzeigt, zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="40eaf-120">The regional and language options portion of the Control Panel also calls **EnumSystemLocalesEx** to build the list of locales that it displays.</span></span> <span data-ttu-id="40eaf-121">Die vier oben aufgeführten Pseudo Gebiets Schemas werden jedoch standardmäßig nicht vom System erkannt, sodass Sie nicht von **enumsystemlocalesex** zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="40eaf-121">However, by default, the four pseudo-locales listed above are not recognized by the system, so they won't be returned by **EnumSystemLocalesEx**.</span></span> <span data-ttu-id="40eaf-122">Für Systeme von Windows Vista bis einschließlich Windows 10, Version 1709, besteht die Lösung darin, Pseudo Gebiets Schemata durch Hinzufügen von Schlüsseln zur Windows-Registrierung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="40eaf-122">For systems from Windows Vista up to and including Windows 10, version 1709, the solution is to enable pseudo-locales by adding keys to the Windows Registry.</span></span>

<span data-ttu-id="40eaf-123">Die bearbeitvorgänge werden unter dem lokalen HKEY- \_ \_ Computer \\ System \\ CurrentControlSet \\ Control \\ nls Key für die auf dem Betriebs System installierten Sprachen vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="40eaf-123">The edits are made under the HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\Nls key for the languages installed on the operating system.</span></span> <span data-ttu-id="40eaf-124">Sie können diese Einstellungen vornehmen, um die Pseudo Gebiets Schemas zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="40eaf-124">You can make these settings to enable the pseudo-locales.</span></span> <span data-ttu-id="40eaf-125">Jeder unten gezeigte Schlüssel ist die hexadezimale LCID, die dem aktivierten Pseudo Gebiets Schema entspricht.</span><span class="sxs-lookup"><span data-stu-id="40eaf-125">Each key shown below is the hexadecimal LCID corresponding to the pseudo-locale being enabled.</span></span> <span data-ttu-id="40eaf-126">Jeder Wert ist vom Typ Zeichenfolge (reg \_ SZ).</span><span class="sxs-lookup"><span data-stu-id="40eaf-126">Each value is of type string (REG\_SZ).</span></span>

```
[HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\Nls\Locale]
"00000501"="1" // qps-ploc (Windows Vista and later)
"000005fe"="7" // qps-ploca (Windows Vista and later)
"00000901"="1" // qps-Latn-x-sh (Windows 10 and later)
"000009ff"="d" // qps-plocm (Windows Vista and later)
```

<span data-ttu-id="40eaf-127">Für Windows 10, Version 1803, wirkt sich die Bearbeitung der Windows-Registrierung wie folgt nicht aus.</span><span class="sxs-lookup"><span data-stu-id="40eaf-127">For Windows 10, version 1803, editing the Windows Registry like this has no effect.</span></span> <span data-ttu-id="40eaf-128">Sie können jedoch weiterhin die nicht aufzurufenden nls-APIs mit den Namen der Pseudo Gebiets Schemata (siehe die obigen Codebeispiele) zum Auffüllen Ihrer Benutzeroberfläche (UI) aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="40eaf-128">But you can still call the non-enumerating NLS APIs with the names of the pseudo-locales (see the code examples above) to populate your user interface (UI).</span></span>

## <a name="related-topics"></a><span data-ttu-id="40eaf-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="40eaf-129">Related topics</span></span>

* [<span data-ttu-id="40eaf-130">Verwenden der Unterstützung für nationale Sprache</span><span class="sxs-lookup"><span data-stu-id="40eaf-130">Using National Language Support</span></span>](using-national-language-support.md)
* [<span data-ttu-id="40eaf-131">Pseudo Gebiets Schemata</span><span class="sxs-lookup"><span data-stu-id="40eaf-131">Pseudo-Locales</span></span>](pseudo-locales.md)
* [<span data-ttu-id="40eaf-132">Enumsystemlocalesex</span><span class="sxs-lookup"><span data-stu-id="40eaf-132">EnumSystemLocalesEx</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex)
* [<span data-ttu-id="40eaf-133">GetLocaleInfoEx</span><span class="sxs-lookup"><span data-stu-id="40eaf-133">GetLocaleInfoEx</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)
* [<span data-ttu-id="40eaf-134">LocaleNameToLCID</span><span class="sxs-lookup"><span data-stu-id="40eaf-134">LocaleNameToLCID</span></span>](/windows/desktop/api/Winnls/nf-winnls-localenametolcid)
