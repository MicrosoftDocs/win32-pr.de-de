---
description: NLS umfasst eine Reihe von API-Funktionen, die Ihre Anwendungen verwenden können, um Gebiets Schema Daten zwischen Gebiets Schema Bezeichners und Gebiets Schema Namen zuzuordnen und neutrale Gebiets Schemas aufzulisten.
ms.assetid: 01bc261d-dfee-430e-86c9-cfafe82856c8
title: Zuordnung von Gebiets Schema Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec2b4ec93efab1cc9023bedfa5479c3a1fc81987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214958"
---
# <a name="mapping-locale-data"></a><span data-ttu-id="c55c6-103">Zuordnung von Gebiets Schema Daten</span><span class="sxs-lookup"><span data-stu-id="c55c6-103">Mapping Locale Data</span></span>

<span data-ttu-id="c55c6-104">NLS umfasst eine Reihe von API-Funktionen, die Ihre Anwendungen verwenden können, um Gebiets Schema Daten zwischen Gebiets Schema Bezeichners und Gebiets Schema [Namen](locale-names.md) [zuzuordnen und neutrale](locale-identifiers.md) Gebiets Schemas aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="c55c6-104">NLS includes a number of API functions that your applications can use to map locale data between [locale identifiers](locale-identifiers.md) and [locale names](locale-names.md), and list neutral locales.</span></span> <span data-ttu-id="c55c6-105">In diesem Thema wird die Verwendung dieser Funktionen unter Windows Vista und höher und unter Windows Vista-Betriebssystemen (manchmal auch als "downlevelsysteme" bezeichnet) erörtert.</span><span class="sxs-lookup"><span data-stu-id="c55c6-105">This topic discusses the use of these functions on Windows Vista and later and on pre-Windows Vista operating systems (sometimes called "downlevel systems").</span></span>

## <a name="map-locale-data-on-windows-vista-and-later"></a><span data-ttu-id="c55c6-106">Zuordnen von Gebiets Schema Daten unter Windows Vista und höher</span><span class="sxs-lookup"><span data-stu-id="c55c6-106">Map Locale Data on Windows Vista and Later</span></span>

<span data-ttu-id="c55c6-107">NLS bietet verschiedene Funktionen für die Gebiets Schema Zuordnung, die von Anwendungen verwendet werden können, die Sie für die unter Windows Vista und höher entwickeln.</span><span class="sxs-lookup"><span data-stu-id="c55c6-107">NLS provides several locale mapping functions for use by applications that you develop to run on Windows Vista and later.</span></span> <span data-ttu-id="c55c6-108">Sie enthält auch Funktionen, die Ihre Anwendungen verwenden können, um neutrale Gebiets Schemas aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="c55c6-108">It also includes functions that your applications can use to enumerate neutral locales.</span></span>

<span data-ttu-id="c55c6-109">**Verwenden der Standard Konvertierungs Funktionen für die Datenzuordnung**</span><span class="sxs-lookup"><span data-stu-id="c55c6-109">**Use the Standard Conversion Functions for Data Mapping**</span></span>

<span data-ttu-id="c55c6-110">Um zwischen einem Gebiets Schema Namen und einem Gebiets Schema Bezeichner zuzuordnen, kann die Anwendung die [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) -Funktion abrufen.</span><span class="sxs-lookup"><span data-stu-id="c55c6-110">To map between a locale name and a locale identifier, your application can call the [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) function.</span></span> <span data-ttu-id="c55c6-111">Die Anwendung verwendet [**lcidtolocalename**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) , um eine Zuordnung zwischen einem Gebiets Schema Bezeichner und einem Gebiets Schema Namen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c55c6-111">The application uses [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) to map between a locale identifier and a locale name.</span></span>

<span data-ttu-id="c55c6-112">**Auflisten neutraler Gebiets Schemas**</span><span class="sxs-lookup"><span data-stu-id="c55c6-112">**List Neutral Locales**</span></span>

<span data-ttu-id="c55c6-113">Um neutrale Gebiets Schemata für Windows 7 und höher aufzulisten, kann die Anwendung [**enumsystemlocalesex**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) mit *dwFlags* aufrufen, die auf [**locale \_ neutraldata**](locale-neutraldata.md)festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="c55c6-113">To enumerate neutral locales for Windows 7 and later, your application can call [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) with *dwFlags* set to [**LOCALE\_NEUTRALDATA**](locale-neutraldata.md).</span></span> <span data-ttu-id="c55c6-114">Außerdem kann [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) verwendet werden, wobei *LCTYPE* auf [**locale \_ ineutral**](locale-ineutral.md)festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c55c6-114">It can also use [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) with *LCType* set to [**LOCALE\_INEUTRAL**](locale-ineutral.md).</span></span>

## <a name="map-locale-data-on-pre-windows-vista-operating-systems"></a><span data-ttu-id="c55c6-115">Zuordnen von Gebiets Schema Daten auf Betriebssystemen vor Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c55c6-115">Map Locale Data on Pre-Windows Vista Operating Systems</span></span>

<span data-ttu-id="c55c6-116">NLS enthält eine Direct Link Library (dll) zur Verwendung für Anwendungen, die Sie für die Betriebssysteme vor Windows Vista entwickeln.</span><span class="sxs-lookup"><span data-stu-id="c55c6-116">NLS includes a direct-link library (DLL) to use for applications that you develop to run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="c55c6-117">Die DLL unterstützt sowohl Konvertierungs-als auch Listen Funktionen für die Datenzuordnung.</span><span class="sxs-lookup"><span data-stu-id="c55c6-117">The DLL supports both conversion and listing functions for data mapping.</span></span>

> [!Note]  
> <span data-ttu-id="c55c6-118">Anwendungen, die nur unter Windows Vista und höher ausgeführt werden, sollten nicht die downlevelzuordnung oder die Auflistungs Funktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="c55c6-118">Applications that only run on Windows Vista and later should not use the downlevel mapping or listing functions.</span></span>

 

<span data-ttu-id="c55c6-119">**Verwenden der Downlevel-Konvertierungs Funktionen für die Datenzuordnung**</span><span class="sxs-lookup"><span data-stu-id="c55c6-119">**Use the Downlevel Conversion Functions for Data Mapping**</span></span>

<span data-ttu-id="c55c6-120">Ihre Anwendung, die auf ein downlevelsystem ausgerichtet ist, kann die [**downlevellcidtolocalename**](downlevellcidtolocalename.md) -Funktion zum Konvertieren eines Gebiets Schema Bezeichners in einen Gebiets Schema Namen abrufen.</span><span class="sxs-lookup"><span data-stu-id="c55c6-120">Your application targeted at a downlevel system can call the [**DownlevelLCIDToLocaleName**](downlevellcidtolocalename.md) function to convert a locale identifier to a locale name.</span></span> <span data-ttu-id="c55c6-121">Wenn ein Gebiets Schema Name in einen Gebiets Schema Bezeichner konvertiert werden muss, sollte er [**downlevellocalenametolcid**](downlevellocalenametolcid.md)nennen.</span><span class="sxs-lookup"><span data-stu-id="c55c6-121">If it needs to convert a locale name to a locale identifier, it should call [**DownlevelLocaleNameToLCID**](downlevellocalenametolcid.md).</span></span>

<span data-ttu-id="c55c6-122">**Verwenden der Funktionen für die downlevelauflistung zum Auflisten neutraler Gebiets Schemas**</span><span class="sxs-lookup"><span data-stu-id="c55c6-122">**Use the Downlevel Listing Functions to Enumerate Neutral Locales**</span></span>

<span data-ttu-id="c55c6-123">Die Anwendung sollte die [**downlevelgetparametrilocalelcid**](downlevelgetparentlocalelcid.md) aufrufen, um den Gebiets Schema Bezeichner des übergeordneten Elements für ein Gebiets Schema abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c55c6-123">Your application should call the [**DownlevelGetParentLocaleLCID**](downlevelgetparentlocalelcid.md) to retrieve the locale identifier of the parent for a locale.</span></span> <span data-ttu-id="c55c6-124">Wenn die Anwendung den Gebiets Schema Namen des übergeordneten Elements für das Gebiets Schema abrufen muss, sollte Sie [**downlevelgetparametrilocalename**](downlevelgetparentlocalename.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c55c6-124">If the application needs to get the locale name of the parent for the locale, it should call [**DownlevelGetParentLocaleName**](downlevelgetparentlocalename.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c55c6-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c55c6-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c55c6-126">Verwenden der Unterstützung für nationale Sprache</span><span class="sxs-lookup"><span data-stu-id="c55c6-126">Using National Language Support</span></span>](using-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="c55c6-127">Gebiets Schema Bezeichner</span><span class="sxs-lookup"><span data-stu-id="c55c6-127">Locale Identifiers</span></span>](locale-identifiers.md)
</dt> <dt>

[<span data-ttu-id="c55c6-128">Gebiets Schema Namen</span><span class="sxs-lookup"><span data-stu-id="c55c6-128">Locale Names</span></span>](locale-names.md)
</dt> </dl>

 

 



