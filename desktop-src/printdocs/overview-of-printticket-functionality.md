---
description: In dieser Übersicht über die PrintTicket-Funktionalität wird das Format für das Ausdrücken von Gerätekonfigurationsinformationen und die Verwendung eines PrintTickets beschrieben.
ms.assetid: c48b9821-9194-47d9-a3ec-b10dbbdf14cc
title: Übersicht über die PrintTicket-Funktionalität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e90aa6f967f5fce25977b52a4d0bec7e9e1ea705
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408543"
---
# <a name="overview-of-printticket-functionality"></a><span data-ttu-id="409e2-103">Übersicht über die PrintTicket-Funktionalität</span><span class="sxs-lookup"><span data-stu-id="409e2-103">Overview of PrintTicket Functionality</span></span>

<span data-ttu-id="409e2-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="409e2-104">This topic is not current.</span></span> <span data-ttu-id="409e2-105">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="409e2-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="409e2-106">PrintTicket verwendet ein XML-basiertes Format zum Ausdrücken von Gerätekonfigurationsinformationen mithilfe der Feature-/Options- und Parameterkonstrukte des Druckschemaframeworks.</span><span class="sxs-lookup"><span data-stu-id="409e2-106">The PrintTicket utilizes an XML-based format for expressing device configuration information using the Feature/Option and parameter constructs of the Print Schema Framework.</span></span> <span data-ttu-id="409e2-107">Dies umfasst alle Standardelementtypen sowie die Erweiterbarkeitsfunktionen des Druckschemaframeworks.</span><span class="sxs-lookup"><span data-stu-id="409e2-107">This includes all of the standard element types as well as the extensibility capabilities of the Print Schema Framework.</span></span> <span data-ttu-id="409e2-108">Ein PrintTicket wird als eigenständige Beschreibung der Verarbeitung einer einzelnen Seite angenommen.</span><span class="sxs-lookup"><span data-stu-id="409e2-108">A PrintTicket is assumed to be a self-contained description of how a single page is to be processed.</span></span> <span data-ttu-id="409e2-109">Die Schritte zum Extrahieren und Erstellen eines solchen PrintTickets aus einem bestimmten Dokumentformat werden hier nicht behandelt.</span><span class="sxs-lookup"><span data-stu-id="409e2-109">The steps involved in extracting and constructing such a PrintTicket from a particular document format are not covered here.</span></span>

<span data-ttu-id="409e2-110">Ein PrintTicket kann verwendet werden, um ein PrintCapabilities-Dokument abzurufen, das die Merkmale des Geräts für eine bestimmte Konfiguration beschreibt.</span><span class="sxs-lookup"><span data-stu-id="409e2-110">A PrintTicket can be used to obtain a PrintCapabilities document describing the characteristics of the device for a particular configuration.</span></span> <span data-ttu-id="409e2-111">Alternativ kann das PrintTicket mit einer Reihe von Renderinganweisungen übermittelt werden, um eine Ausgabeseite zu erzeugen, die gemäß der im PrintTicket angegebenen Konfiguration gerendert und verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="409e2-111">Alternatively, the PrintTicket can be submitted with a set of rendering instructions to produce a page of output rendered and processed according to the configuration specified in the PrintTicket.</span></span>

## <a name="related-topics"></a><span data-ttu-id="409e2-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="409e2-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="409e2-113">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="409e2-113">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



