---
description: Übersicht über die Eltern Steuerungs-API
ms.assetid: 647e5df8-7c6d-466a-a3d4-eac13efa797d
title: Übersicht über die Eltern Steuerungs-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0aa88592f2262b89f98cfd5baaac5ad2f35f959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366192"
---
# <a name="parental-controls-api-overview"></a><span data-ttu-id="ede93-103">Übersicht über die Eltern Steuerungs-API</span><span class="sxs-lookup"><span data-stu-id="ede93-103">Parental Controls API Overview</span></span>

<span data-ttu-id="ede93-104">APIs, die für Eltern Steuerelemente verwendet werden, machen die Richtlinien-und EinstellungenEinstellungen sowie die Protokollierungs Funktionalität verfügbar</span><span class="sxs-lookup"><span data-stu-id="ede93-104">APIs used for Parental Controls expose the policy and in-box restrictions settings, and logging functionality.</span></span>

## <a name="settings"></a><span data-ttu-id="ede93-105">Einstellungen</span><span class="sxs-lookup"><span data-stu-id="ede93-105">Settings</span></span>

<span data-ttu-id="ede93-106">Es werden zwei öffentliche APIs bereitgestellt:</span><span class="sxs-lookup"><span data-stu-id="ede93-106">Two public APIs are provided:</span></span>

-   <span data-ttu-id="ede93-107">Eine vereinfachte com-basierte API für minimale Konformität (die als Kompatibilitäts-API bezeichnet wird), um zu bestimmen, ob die Protokollierung aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ede93-107">A lightweight COM-based minimum compliance API (called the Compliance API) primarily for applications to determine whether logging should be turned on.</span></span> <span data-ttu-id="ede93-108">Außerdem werden einfache Methoden für Folgendes bereitgestellt:</span><span class="sxs-lookup"><span data-stu-id="ede93-108">In addition, simple methods are provided for:</span></span>
    -   <span data-ttu-id="ede93-109">Das Abrufen des Einschränkungs Zustands für Webeinschränkungen, Zeitlimits, Spiele Einschränkungen und Anwendungs Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="ede93-109">Retrieving the restrictions state for web restrictions, time limits, games restrictions, and application restrictions.</span></span>
    -   <span data-ttu-id="ede93-110">Die ID des aktiven Webinhalts Filters wird abgerufen.</span><span class="sxs-lookup"><span data-stu-id="ede93-110">Retrieving the ID of the active Web content filter.</span></span>
    -   <span data-ttu-id="ede93-111">Festlegen, ob die Benutzeroberflächen Elemente des Anbieters auf eine Weise angezeigt werden sollen, die mit dem in einer Domäne verbundenen eingeblendeten ausblenden übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="ede93-111">Determining whether vendor user interface elements should be shown, in a manner consistent with the in-box hiding when joined to a domain.</span></span>
    -   <span data-ttu-id="ede93-112">Der Zeitpunkt der letzten Änderung einer Einstellung für einen Benutzer wird abgerufen.</span><span class="sxs-lookup"><span data-stu-id="ede93-112">Retrieving the last time a setting has been changed for a user.</span></span>
    -   <span data-ttu-id="ede93-113">Abrufen, ob Browser-oder Browser ähnliche Dateidownloads für einen Benutzer blockiert werden müssen, und die Möglichkeit, eine URL anzufordern, die für den Webinhalts Filter dieses Benutzers explizit zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="ede93-113">Retrieving whether browser-based or browser-like file downloads need to be blocked for a user, and the ability to request a URL to be specifically allowed by the Web Content Filter for that user.</span></span>
    -   <span data-ttu-id="ede93-114">Es wird ermittelt, ob ein bestimmtes Spiel für einen Benutzer blockiert ist.</span><span class="sxs-lookup"><span data-stu-id="ede93-114">Determining whether a given game is blocked for a user.</span></span>
-   <span data-ttu-id="ede93-115">Windows-Verwaltungsinstrumentation (WMI)-API-Zugriff auf einen Eltern Steuerungs Namespace, um vollständigen Schreib-und Lesezugriff auf alle verfügbar gemachten Einstellungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ede93-115">Windows Management Instrumentation (WMI) API access to a Parental Controls namespace for full write and read access to all exposed settings.</span></span> <span data-ttu-id="ede93-116">Mit der Jugendschutz Steuerung wird ein WMI-Anbieter bereitgestellt, um Lese-/Schreibberechtigungen für den zugrunde liegenden Einstellungs Speicher mit ordnungsgemäßer Erzwingung von Berechtigungen für Administratoren und kontrollierte Benutzer</span><span class="sxs-lookup"><span data-stu-id="ede93-116">Parental Controls deploys a WMI Provider to manage read/write permissions to the underlying settings store with proper enforcement of privileges for administrators and controlled users.</span></span>

<span data-ttu-id="ede93-117">ISVs werden aufgefordert, die Kompatibilitäts-API und ggf. die WMI-API zu verwenden, um die Einschränkungen für die untergeordnete Sicherheit basierend auf der Funktionalität der Anwendung oder Lösung zu steuern.</span><span class="sxs-lookup"><span data-stu-id="ede93-117">ISVs are requested to use the Compliance API, and the WMI API as necessary, to control restrictions as appropriate for child safety based on the functionality of the application or solution.</span></span>

## <a name="logging"></a><span data-ttu-id="ede93-118">Protokollierung</span><span class="sxs-lookup"><span data-stu-id="ede93-118">Logging</span></span>

-   <span data-ttu-id="ede93-119">Die Aktivitäts Überwachung von Windows-Standard Ereignissen wird für die Überwachung von Eltern Steuerelementen verwendet.</span><span class="sxs-lookup"><span data-stu-id="ede93-119">Windows standard event publishing and consuming APIs are used for Parental Controls activity monitoring.</span></span> <span data-ttu-id="ede93-120">Das Windows Vista-Ereignis Berichterstattungs-und-Ablauf Verfolgungssystem hat gegenüber der früheren etw-Funktionalität (Event Tracing for Windows) eine bessere Leistung erzielt.</span><span class="sxs-lookup"><span data-stu-id="ede93-120">The Windows Vista Event Reporting and Tracing system has improved performance over previous Event Tracing for Windows (ETW) functionality.</span></span> <span data-ttu-id="ede93-121">Eltern Steuerelemente definieren einen eindeutigen Kanal für Ihre Daten in etw.</span><span class="sxs-lookup"><span data-stu-id="ede93-121">Parental Controls defines a unique channel for its data in ETW.</span></span>
-   <span data-ttu-id="ede93-122">ISVs werden aufgefordert, die Ereignis Veröffentlichungs-API zum Protokollieren von Benutzeraktivitäten zu verwenden, wie im Abschnitt using Jugend Steuerungs-APIs angegeben.</span><span class="sxs-lookup"><span data-stu-id="ede93-122">ISVs are requested to use the event publishing API to log user activity as specified in the Using Parental Controls APIs section.</span></span>

 

 



