---
description: Installiert Gerätetreiber aus Programmen mit einem Setup Skript und INF-Dateien. Schreiben Sie ein Setup Programm für Geräte Einrichtung und Treiberinstallation. Diese API wird nicht mehr zum Zweck der Installation von Softwareanwendungen empfohlen.
ms.assetid: 96a9e472-9b92-4976-9379-dc0c96524963
title: Setup-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6101c2673e72095d0cf4ebe59c1cece83449d647
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360595"
---
# <a name="setup-api"></a><span data-ttu-id="8a958-105">Setup-API</span><span class="sxs-lookup"><span data-stu-id="8a958-105">Setup API</span></span>

## <a name="purpose"></a><span data-ttu-id="8a958-106">Zweck</span><span class="sxs-lookup"><span data-stu-id="8a958-106">Purpose</span></span>

<span data-ttu-id="8a958-107">Die Setup-API bietet eine Reihe von Funktionen, die von einer Setup Anwendung zum Ausführen von Installations Vorgängen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8a958-107">The Setup API provides a set of functions that a setup application calls to perform installation operations.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="8a958-108">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="8a958-108">Where applicable</span></span>

<span data-ttu-id="8a958-109">Diese Setup Funktionen sind zum Entwickeln einer Setup Anwendung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8a958-109">These setup functions are available to develop a setup application.</span></span> <span data-ttu-id="8a958-110">Die Setup-API sollte nicht mehr zum Installieren von Anwendungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8a958-110">Setup API should no longer be used for installing applications.</span></span> <span data-ttu-id="8a958-111">Verwenden Sie stattdessen die [Windows Installer](/windows/desktop/Msi/windows-installer-portal)zum Entwickeln von anwendungsinstallern.</span><span class="sxs-lookup"><span data-stu-id="8a958-111">Instead, use the [Windows Installer](/windows/desktop/Msi/windows-installer-portal)for developing application installers.</span></span> <span data-ttu-id="8a958-112">Die Setup-API wird weiterhin zum Installieren von Gerätetreibern verwendet.</span><span class="sxs-lookup"><span data-stu-id="8a958-112">Setup API continues to be used for installing device drivers.</span></span>

<span data-ttu-id="8a958-113">Die Setup-API ist für die Entwicklung von Anwendungen im Desktop Stil vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="8a958-113">The Setup API is intended for the development of desktop style applications.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="8a958-114">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="8a958-114">Developer audience</span></span>

<span data-ttu-id="8a958-115">Ein Entwickler kann die Setup-API verwenden, wenn die Setup Anwendung die folgenden Funktionen erfordert:</span><span class="sxs-lookup"><span data-stu-id="8a958-115">A developer can use the Setup API if their setup application requires the following functionality:</span></span>

-   <span data-ttu-id="8a958-116">Dateien werden in die Warteschlange gestellt.</span><span class="sxs-lookup"><span data-stu-id="8a958-116">Queuing of files.</span></span>
-   <span data-ttu-id="8a958-117">Installation von Dateien.</span><span class="sxs-lookup"><span data-stu-id="8a958-117">Installation of files.</span></span>
-   <span data-ttu-id="8a958-118">Behandlung von Installationsfehlern und Eingabeaufforderung für Medien.</span><span class="sxs-lookup"><span data-stu-id="8a958-118">Handling of installation errors and prompting for media.</span></span>
-   <span data-ttu-id="8a958-119">Registrierungseinträge werden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="8a958-119">Updating registry entries.</span></span>
-   <span data-ttu-id="8a958-120">Protokollierung von Dateien, während Sie installiert werden.</span><span class="sxs-lookup"><span data-stu-id="8a958-120">Logging of files as they are installed.</span></span>
-   <span data-ttu-id="8a958-121">Speicherung der zuletzt verwendeten Quell Pfade.</span><span class="sxs-lookup"><span data-stu-id="8a958-121">Storage of the most recently used source paths.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="8a958-122">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="8a958-122">Run-time requirements</span></span>

<span data-ttu-id="8a958-123">Informationen dazu, welche Betriebssysteme für die Verwendung einer bestimmten Funktion erforderlich sind, finden Sie im Abschnitt "Anforderungen" in der Dokumentation für die Funktion.</span><span class="sxs-lookup"><span data-stu-id="8a958-123">For information about which operating systems are required to use a particular function, see the Requirements section of the documentation for the function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8a958-124">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="8a958-124">In this section</span></span>



| <span data-ttu-id="8a958-125">Thema</span><span class="sxs-lookup"><span data-stu-id="8a958-125">Topic</span></span>                                 | <span data-ttu-id="8a958-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8a958-126">Description</span></span>                                                                                 |
|---------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8a958-127">Übersicht</span><span class="sxs-lookup"><span data-stu-id="8a958-127">Overview</span></span>](overview.md)<br/>   | <span data-ttu-id="8a958-128">Allgemeine Informationen zur Setup-API.</span><span class="sxs-lookup"><span data-stu-id="8a958-128">General information about Setup API.</span></span><br/>                                             |
| [<span data-ttu-id="8a958-129">Verweis</span><span class="sxs-lookup"><span data-stu-id="8a958-129">Reference</span></span>](reference.md)<br/> | <span data-ttu-id="8a958-130">Dokumentation der Setup-API-Datentypen,-Strukturen,-Funktionen und-Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="8a958-130">Documentation of Setup API data types, structures, functions, and notifications.</span></span><br/> |



 

 

