---
description: Verwenden von Eltern Steuerungs-APIs
ms.assetid: 3d0bb750-0882-4b95-a595-38611f161ca9
title: Verwenden von Eltern Steuerungs-APIs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4ed69815bc04e00a3cae07f16530f8ea837f24a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367915"
---
# <a name="using-parental-controls-apis"></a><span data-ttu-id="5eccb-103">Verwenden von Eltern Steuerungs-APIs</span><span class="sxs-lookup"><span data-stu-id="5eccb-103">Using Parental Controls APIs</span></span>

## <a name="api-selection"></a><span data-ttu-id="5eccb-104">API-Auswahl</span><span class="sxs-lookup"><span data-stu-id="5eccb-104">API Selection</span></span>

<span data-ttu-id="5eccb-105">Wie im Abschnitt Übersicht erwähnt, umfasst die Entwicklung die Verwendung von bis zu drei APIs:</span><span class="sxs-lookup"><span data-stu-id="5eccb-105">As noted in the overview section, development involves use of up to three APIs:</span></span>

-   <span data-ttu-id="5eccb-106">Zugriff auf grundlegende Einstellungen: die in "wpcapi. h" definierte mindestrecompliance-com-API (Compliance-API) für den einfachen Zugriff auf eine Schlüssel Teilmenge des Zustands der Jugend Steuerungs Zustände.</span><span class="sxs-lookup"><span data-stu-id="5eccb-106">Basic settings access: the Parental Controls minimum compliance COM API (Compliance API) defined in Wpcapi.h for simple access to a key subset of Parental Controls state.</span></span>
-   <span data-ttu-id="5eccb-107">Lese-/Schreibzugriff für vollständige Einstellungen: die Verwendung einer kleinen Teilmenge der WMI-com-API für den Vollzugriff ist nur erforderlich, wenn der ISV Einstellungen ändern muss.</span><span class="sxs-lookup"><span data-stu-id="5eccb-107">Full settings write/read access: use of a small subset of the WMI COM API for full access is only required if the ISV needs to modify settings.</span></span> <span data-ttu-id="5eccb-108">Das Hinzufügen eines Benutzeroberflächen-Erweiterbarkeits Links, das Ersetzen des Webinhalts Filters oder Ergänzungen der Computer weiten http-Anwendung oder der Ausnahmeliste für die URL-Filterung sind die Hauptgründe für die Verwendung der API.</span><span class="sxs-lookup"><span data-stu-id="5eccb-108">Addition of a UI extensibility link, replacement of the Web Content Filter, or additions to the computer-wide HTTP application or URL filtering exemption lists are the primarily reasons to use the API.</span></span> <span data-ttu-id="5eccb-109">Da die Verwendung des Namespace für die WMI-Jugendschutz-Namespace Rohdaten Zugriff auf den zugrunde liegenden Einstellungs Speicher bietet, sollten die ISVs bei der Interpretation des Zustands aus den einzelnen Einstellungen, die tatsächlich möglicherweise Abhängigkeiten von anderen Einstellungen aufweisen, vorsichtig vorgehen.</span><span class="sxs-lookup"><span data-stu-id="5eccb-109">As the WMI Parental Controls namespace usage provides raw access to the underlying settings store, ISVs should proceed with caution in interpreting state from individual settings that may in fact have gating dependencies on other settings.</span></span> <span data-ttu-id="5eccb-110">Daher wird empfohlen, die Kompatibilitäts-API zum Lesen des Zustands für alle Werte zu verwenden, die von dieser API verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="5eccb-110">It is therefore recommended to use the Compliance API for reading state for all values exposed by that API.</span></span>
-   <span data-ttu-id="5eccb-111">Protokollierung: die Ereignis Ablauf Verfolgung und die Berichterstattungs System-API von Windows Vista (auch als etw bezeichnet) zum Veröffentlichen von Aktivitäts Ereignissen in den Eltern Steuerungs Protokollen, zusammen mit Ereignis Deskriptoren und Array Enumerationen, die in wpcevent. h definiert sind.</span><span class="sxs-lookup"><span data-stu-id="5eccb-111">Logging: the Windows Vista Event Tracing and Reporting system API (also referred to as ETW) for publishing activity events into the Parental Controls logs, in conjunction with event descriptors and array enumerations defined in WpcEvent.h.</span></span>

<span data-ttu-id="5eccb-112">Alle APIs können als Standardbenutzer aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="5eccb-112">All of the APIs are callable as a standard user.</span></span> <span data-ttu-id="5eccb-113">Für die Protokollierung kann jeder Benutzerprotokoll Ereignisse als Quelle durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="5eccb-113">For logging, any user may source log events.</span></span> <span data-ttu-id="5eccb-114">Das Aufrufen von zum Abrufen oder Ändern von Einstellungen für einen anderen Benutzer schlägt fehl, wenn der Aufrufer nicht über Administratorrechte verfügt.</span><span class="sxs-lookup"><span data-stu-id="5eccb-114">Calling to retrieve or change settings for another user will fail if the caller does not have administrator privileges.</span></span> <span data-ttu-id="5eccb-115">Anders ausgedrückt: ein Standardbenutzer kann nur auf seine eigenen Einstellungen zugreifen und nur zum Lesen.</span><span class="sxs-lookup"><span data-stu-id="5eccb-115">In other words, a standard user can access his or her own settings only, and only for reading.</span></span>

<span data-ttu-id="5eccb-116">Die Einstellungen und die Verwendung der Protokollierungs-API werden in den folgenden Abschnitten ausführlicher erläutert:</span><span class="sxs-lookup"><span data-stu-id="5eccb-116">Settings and logging API usage are discussed further in these sections:</span></span>

-   [<span data-ttu-id="5eccb-117">Verwenden von Einstellungen für die Jugend Steuerungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="5eccb-117">Using Parental Controls Settings APIs</span></span>](using-parental-controls-settings-apis.md)
-   [<span data-ttu-id="5eccb-118">Verwenden von Protokollierungs-APIs für Eltern Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="5eccb-118">Using Logging APIs for Parental Controls</span></span>](using-logging-apis-for-parental-controls.md)

## <a name="development-environment"></a><span data-ttu-id="5eccb-119">Entwicklungsumgebung</span><span class="sxs-lookup"><span data-stu-id="5eccb-119">Development Environment</span></span>

<span data-ttu-id="5eccb-120">Die Entwicklung für Jugendschutz Steuerelemente erfordert Zugriff auf drei Header Dateien: wpc. h, wpcapi. h und wpcevent. h.</span><span class="sxs-lookup"><span data-stu-id="5eccb-120">Developing for Parental Controls requires access to three header files: Wpc.h, WpcApi.h, and WpcEvent.h.</span></span> <span data-ttu-id="5eccb-121">WPC. h ist ein Collector, der die Einstellungen der öffentlichen Kompatibilitäts-API und der Ereignis Header enthält. Daher genügt es, wpc. h in den Anwendungscode einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="5eccb-121">Wpc.h is a collector that includes the settings public compliance API and event headers, so it is sufficient to include Wpc.h in application code.</span></span>

<span data-ttu-id="5eccb-122">Lese-/Schreibberechtigungen für die WMI-API werden in der Datei "wpcsprov. mof" angegeben.</span><span class="sxs-lookup"><span data-stu-id="5eccb-122">Read/write permissions to the WMI API is specified by the Wpcsprov.mof file.</span></span> <span data-ttu-id="5eccb-123">Diese Datei wird im WBEM-Unterverzeichnis unter dem Verzeichnis Windows System32 installiert.</span><span class="sxs-lookup"><span data-stu-id="5eccb-123">This file is installed to the WBEM subdirectory under the Windows System32 directory.</span></span>

<span data-ttu-id="5eccb-124">Das Microsoft Windows Software Development Kit (SDK) enthält Beispielcode, mit dem Sie den hier gezeigten Beispielcode verstärken und einfache Befehlszeilen gesteuerte Tools zum Durchsuchen von APIs und zum Integrieren von Tests bereitstellen können.</span><span class="sxs-lookup"><span data-stu-id="5eccb-124">The Microsoft Windows Software Development Kit (SDK) contains sample code to reinforce example code shown here and provide simple command-line driven tools for API exploration or integration testing.</span></span>

 

 



