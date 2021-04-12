---
description: Die in der folgenden Tabelle aufgeführten Funktionen sind Einstiegspunkte für parserdlls. Die Funktionen sind die Einstiegspunkte für Aufrufe vom Betriebssystem und Netzwerkmonitor.
ms.assetid: 67811ddb-1961-4306-a62f-b9fd2d2d2b55
title: Export Funktionen der Parser-DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 929541a1eda60740fe219352fee285a5a34a89df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393406"
---
# <a name="parser-dll-export-functions"></a><span data-ttu-id="9386e-104">Export Funktionen der Parser-DLL</span><span class="sxs-lookup"><span data-stu-id="9386e-104">Parser DLL Export Functions</span></span>

<span data-ttu-id="9386e-105">Die in der folgenden Tabelle aufgeführten Funktionen sind Einstiegspunkte für parserdlls.</span><span class="sxs-lookup"><span data-stu-id="9386e-105">The functions, listed in the following table, are entry points for parser DLLs.</span></span> <span data-ttu-id="9386e-106">Die Funktionen sind die Einstiegspunkte für Aufrufe vom Betriebssystem und Netzwerkmonitor.</span><span class="sxs-lookup"><span data-stu-id="9386e-106">The functions are the entry points for calls from the operating system and Network Monitor.</span></span>



| <span data-ttu-id="9386e-107">Funktion</span><span class="sxs-lookup"><span data-stu-id="9386e-107">Function</span></span>                                           | <span data-ttu-id="9386e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9386e-108">Description</span></span>                                                                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9386e-109">DllMain-Parser</span><span class="sxs-lookup"><span data-stu-id="9386e-109">DllMain Parser</span></span>](dllmain-parser.md)               | <span data-ttu-id="9386e-110">Gibt an, dass die Parser-DLL geladen oder entladen wurde.</span><span class="sxs-lookup"><span data-stu-id="9386e-110">Indicates to the parser DLL that it is loaded or unloaded.</span></span> <span data-ttu-id="9386e-111">Das Betriebssystem Ruft die **DllMain-parserfunktion** auf, wenn ein Prozess die dll lädt oder entlädt.</span><span class="sxs-lookup"><span data-stu-id="9386e-111">The operating system calls the **DllMain Parser** function when a process loads or unloads the DLL.</span></span> |
| [<span data-ttu-id="9386e-112">Attachproperties</span><span class="sxs-lookup"><span data-stu-id="9386e-112">AttachProperties</span></span>](attachproperties.md)           | <span data-ttu-id="9386e-113">Benachrichtigt den Parser, alle Eigenschaften anzufügen, die in einem Frame vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="9386e-113">Notifies the parser to attach any properties that exist in a frame.</span></span>                                                                                            |
| [<span data-ttu-id="9386e-114">Registrierung aufheben</span><span class="sxs-lookup"><span data-stu-id="9386e-114">Deregister</span></span>](deregister.md)                       | <span data-ttu-id="9386e-115">Benachrichtigt den Parser, eine Bereinigung durchzusetzen.</span><span class="sxs-lookup"><span data-stu-id="9386e-115">Notifies the parser to clean up.</span></span>                                                                                                                               |
| [<span data-ttu-id="9386e-116">Formatproperties</span><span class="sxs-lookup"><span data-stu-id="9386e-116">FormatProperties</span></span>](formatproperties.md)           | <span data-ttu-id="9386e-117">Benachrichtigt den Parser, alle Eigenschaften Instanzen in zu übernehmen und den **szpropertytext** -Member jeder **propertyinst** -Struktur zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9386e-117">Notifies the parser to take all of the property instances in and build the **szPropertyText** member of each **PROPERTYINST** structure.</span></span>                       |
| [<span data-ttu-id="9386e-118">Erkenzeframe</span><span class="sxs-lookup"><span data-stu-id="9386e-118">RecognizeFrame</span></span>](recognizeframe.md)               | <span data-ttu-id="9386e-119">Bestimmt, ob der Parser die nicht verarbeiteten Frame Daten mit dem angegebenen Protokoll interpretieren kann.</span><span class="sxs-lookup"><span data-stu-id="9386e-119">Determines whether the parser can interpret the unprocessed frame data with the specified protocol.</span></span>                                                            |
| [<span data-ttu-id="9386e-120">Parser registrieren</span><span class="sxs-lookup"><span data-stu-id="9386e-120">Register Parser</span></span>](register-parser.md)             | <span data-ttu-id="9386e-121">Bestimmt grundlegende Informationen über den Parser in der dll.</span><span class="sxs-lookup"><span data-stu-id="9386e-121">Determines basic information about the parser within the DLL.</span></span> <span data-ttu-id="9386e-122">Netzwerkmonitor Ruft die **Register Parser** -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="9386e-122">Network Monitor calls the **Register Parser** function.</span></span>                                          |
| [<span data-ttu-id="9386e-123">"Parameserautoinstallinfo"</span><span class="sxs-lookup"><span data-stu-id="9386e-123">ParserAutoInstallInfo</span></span>](parserautoinstallinfo.md) | <span data-ttu-id="9386e-124">Installiert einen Parser automatisch.</span><span class="sxs-lookup"><span data-stu-id="9386e-124">Installs a parser automatically.</span></span>                                                                                                                               |



 

<span data-ttu-id="9386e-125">Netzwerkmonitor stellt Strukturen und Hilfsfunktionen bereit, die der Parser abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="9386e-125">Network Monitor provides structures and helper functions that the parser can call.</span></span>



| <span data-ttu-id="9386e-126">Weitere Informationen über</span><span class="sxs-lookup"><span data-stu-id="9386e-126">For more information about</span></span>                          | <span data-ttu-id="9386e-127">Siehe</span><span class="sxs-lookup"><span data-stu-id="9386e-127">See</span></span>                                                                          |
|-----------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="9386e-128">Hilfsfunktionen, die von Experten und Parser aufgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="9386e-128">Helper functions that experts and parsers can call.</span></span> | [<span data-ttu-id="9386e-129">Allgemeine Funktionen für Experten und Parser</span><span class="sxs-lookup"><span data-stu-id="9386e-129">Expert and Parser Common Functions</span></span>](expert-and-parser-common-functions.md) |
| <span data-ttu-id="9386e-130">Hilfsfunktionen, die nur von den Parser aufgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="9386e-130">Helper functions that only parsers can call.</span></span>        | [<span data-ttu-id="9386e-131">Parser-Funktionen</span><span class="sxs-lookup"><span data-stu-id="9386e-131">Parser Functions</span></span>](parser-functions.md)                                     |
| <span data-ttu-id="9386e-132">Strukturen, die von Parserfunktionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9386e-132">Structures that parser functions use.</span></span>               | [<span data-ttu-id="9386e-133">Parserstrukturen</span><span class="sxs-lookup"><span data-stu-id="9386e-133">Parser Structures</span></span>](parser-structures.md)                                   |



 

 

 



