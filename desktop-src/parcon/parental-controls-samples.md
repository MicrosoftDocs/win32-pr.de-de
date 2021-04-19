---
description: Beispiele für Eltern Steuerelemente
ms.assetid: 19dac95c-2279-4bf9-a58c-dd30177c0c9d
title: Beispiele für Eltern Steuerelemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26962f4edd16e1e860883607316d5a7cbf3d9122
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352474"
---
# <a name="parental-controls-samples"></a><span data-ttu-id="58cea-103">Beispiele für Eltern Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="58cea-103">Parental Controls Samples</span></span>

<span data-ttu-id="58cea-104">Beispielcode für die Jugendschutz Steuerelemente finden Sie unter Pfad <installation directory> \\ Windows \\ <version number> \\ Samples \\ \\ samentalcontrols.</span><span class="sxs-lookup"><span data-stu-id="58cea-104">Sample code for Parental Controls is available under path <installation directory>\\Windows\\<version number>\\Samples\\Security\\ParentalControls.</span></span> <span data-ttu-id="58cea-105">Die Beispiele lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="58cea-105">The samples are as follows:</span></span>

## <a name="utilities"></a><span data-ttu-id="58cea-106">Versorgungsunternehmen</span><span class="sxs-lookup"><span data-stu-id="58cea-106">Utilities</span></span>

<span data-ttu-id="58cea-107">Hilfsfunktionen für grundlegende com-Verwaltung, sid-Zeichen folgen Vorgänge und WMI-Lese-und Schreibfunktionen.</span><span class="sxs-lookup"><span data-stu-id="58cea-107">Helper functionality for basic COM management, SID string operations, and WMI read and write functionality.</span></span> <span data-ttu-id="58cea-108">Alle anderen Beispiele sind von diesem Projekt abhängig, sofern nicht anders angegeben.</span><span class="sxs-lookup"><span data-stu-id="58cea-108">All of the other samples depend on this project unless otherwise specified.</span></span>

## <a name="complianceapi"></a><span data-ttu-id="58cea-109">Complianceapi</span><span class="sxs-lookup"><span data-stu-id="58cea-109">ComplianceAPI</span></span>

<span data-ttu-id="58cea-110">Befehlszeilen gesteuerte Konsolenanwendung, die zeigt, wie die Kompatibilitäts-API verwendet wird, um eine Schlüssel Teilmenge von Einstellungen für einen Benutzer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="58cea-110">Command-line driven console application demonstrating how to use the Compliance API to retrieve a key subset of settings for a user.</span></span>

## <a name="complianceapp"></a><span data-ttu-id="58cea-111">Complianceapp</span><span class="sxs-lookup"><span data-stu-id="58cea-111">ComplianceApp</span></span>

<span data-ttu-id="58cea-112">Einfache Konsolenanwendung, die die Verwendung der Konformitäts-API veranschaulicht, um die Protokollierung erforderlicher und spezifischer Einschränkungen zu prüfen.</span><span class="sxs-lookup"><span data-stu-id="58cea-112">Simple console application demonstrating use of the Compliance API to check for logging required and specific restrictions.</span></span> <span data-ttu-id="58cea-113">Wenn Zeitbeschränkungen aktiviert sind, wartet die Anwendung auch auf die bevorstehenden Abmelde-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="58cea-113">If time restrictions are enabled, the application also waits for the impending logout events.</span></span>

## <a name="uiextensibility"></a><span data-ttu-id="58cea-114">Uiextensibility</span><span class="sxs-lookup"><span data-stu-id="58cea-114">UIExtensibility</span></span>

<span data-ttu-id="58cea-115">Befehlszeilen gesteuerte Konsolenanwendung, die die Verwendung der WMI-APIs und des WPC-Schemas veranschaulicht, um Verknüpfungen von Benutzeroberflächen-Erweiterbarkeit aufzulisten, abzufragen, hinzuzufügen, zu ändern und zu löschen.</span><span class="sxs-lookup"><span data-stu-id="58cea-115">Command-line driven console application demonstrating use of the WMI APIs and WPC schema to list, query, add, modify, and delete UI Extensibility link entries.</span></span>

<span data-ttu-id="58cea-116">Beispiel Befehlszeile für Beispiel:</span><span class="sxs-lookup"><span data-stu-id="58cea-116">Example command line for sample:</span></span>

<span data-ttu-id="58cea-117">"D: \\ WPC \\ - \\ Beispiele \\ sicherheitsparametrialcontrols \\ uiextensibility \\ Debug \\ uiextensibility" Add/g: {FD59BB7F-54AB-11dB-9666-00E08161165F}/c: 0/n: D:/WPC/Samples/Security/bientalcontrols/uiextrc/Debug/UiExtRC.dll,-101/s: d:/WPC/Samples/Security/parameentalcontrols/uiextrc/Debug/UiExtRC.dll,-103/i: d:/WPC/Samples/Security/parameentalcontrols/uiextrc/Debug/UiExtRC.dll,-104/d: D:/WPC/Samples/Security/parameentalcontrols/uiextrc/Debug/UiExtRC.dll,-106/e: c: \\ Windows \\Notepad.exe</span><span class="sxs-lookup"><span data-stu-id="58cea-117">"D:\\WPC\\Samples\\Security\\ParentalControls\\UIExtensibility\\debug\\UIExtensibility" add /g:{FD59BB7F-54AB-11DB-9666-00E08161165F} /c:0 /n:D:/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll,-101 /s:D:/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll,-103 /i:D:/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll,-104 /d:D:/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll,-106 /e:c:\\windows\\Notepad.exe</span></span>

<span data-ttu-id="58cea-118">Dabei ist uiextrc eine einfache Ressourcen-DLL mit Zeichen folgen Ressourcen für die 101-und 103-ID und rund 32 um die Uhr mit Alpha Bitmaps für die Ressourcen 104 und 106.</span><span class="sxs-lookup"><span data-stu-id="58cea-118">where UiExtRC is a simple resource DLL with string resources for ID's 101 and 103, and 24x24 pixel 32-bit with alpha bitmaps for resources 104 and 106.</span></span>

## <a name="webextensibility"></a><span data-ttu-id="58cea-119">Webextensibility</span><span class="sxs-lookup"><span data-stu-id="58cea-119">WebExtensibility</span></span>

<span data-ttu-id="58cea-120">Eine Befehlszeilen gesteuerte Konsolenanwendung, die zeigt, wie die WMI-APIs und das WPC-Schema zum Auflisten, hinzufügen und Löschen von http-Anwendungs-oder URL-Ausnahme Einträgen und zum Festlegen und Zurücksetzen eines Webinhalts Filters mit den Eigenschaften filterid und Filter Name verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="58cea-120">Command-line driven console application demonstrating how to use the WMI APIs and WPC schema to list, add, and delete HTTP application or URL exemption entries, and to set and reset a Web Content Filter override with the FilterID and FilterName properties.</span></span>

<span data-ttu-id="58cea-121">Der Zugriff auf die schreibgeschützten http-Anwendungs-und URL-Ausnahme Listen wird nicht angezeigt, aber der Code zum Lesen der Listen ist mit dem des Lese-/schreibfalls identisch, mit Ausnahme der Änderung des WMI-Parameters.</span><span class="sxs-lookup"><span data-stu-id="58cea-121">Access to the read-only HTTP application and URL exemption lists is not shown, but the code to read the lists would be the same as for the read/write case except for modification of the WMI parameter.</span></span>

 

 



