---
title: Windows-Ereignisprotokoll
description: Die Windows-Ereignisprotokoll-API definiert das Schema, das Sie zum Schreiben eines Instrumentierungs Manifests verwenden.
ms.assetid: 738c8afa-4714-4d4f-9231-b8fbdb5159c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9df51efc878af2770ad056e6e1f84b8f4f2566
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858461"
---
# <a name="windows-event-log"></a><span data-ttu-id="cb1de-103">Windows-Ereignisprotokoll</span><span class="sxs-lookup"><span data-stu-id="cb1de-103">Windows Event Log</span></span>

## <a name="purpose"></a><span data-ttu-id="cb1de-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="cb1de-104">Purpose</span></span>

<span data-ttu-id="cb1de-105">Die Windows-Ereignisprotokoll-API definiert das Schema, das Sie zum Schreiben eines Instrumentierungs Manifests verwenden.</span><span class="sxs-lookup"><span data-stu-id="cb1de-105">The Windows Event Log API defines the schema that you use to write an instrumentation manifest.</span></span> <span data-ttu-id="cb1de-106">Ein Instrumentations Manifest identifiziert den Ereignis Anbieter und die Ereignisse, die er protokolliert.</span><span class="sxs-lookup"><span data-stu-id="cb1de-106">An instrumentation manifest identifies your event provider and the events that it logs.</span></span> <span data-ttu-id="cb1de-107">Die API enthält auch die Funktionen, die ein Ereignisconsumer, z. b. die [Ereignisanzeige](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11)), zum Lesen und Rendering der Ereignisse verwenden würde.</span><span class="sxs-lookup"><span data-stu-id="cb1de-107">The API also includes the functions that an event consumer, such as the [Event Viewer](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11)), would use to read and render the events.</span></span> <span data-ttu-id="cb1de-108">Um die im Manifest definierten Ereignisse zu schreiben, verwenden Sie die Funktionen der API für die [Ereignis Ablauf Verfolgung](/windows/desktop/ETW/event-tracing-portal) (ETW).</span><span class="sxs-lookup"><span data-stu-id="cb1de-108">To write the events defined in the manifest, use the functions included in the [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) API.</span></span>

<span data-ttu-id="cb1de-109">Das Windows-Ereignisprotokoll ersetzt die [Ereignisprotokollierungs](/windows/desktop/EventLog/event-logging) -API, beginnend mit dem Betriebssystem Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cb1de-109">Windows Event Log supersedes the [Event Logging](/windows/desktop/EventLog/event-logging) API beginning with the Windows Vista operating system.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="cb1de-110">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="cb1de-110">Developer audience</span></span>

<span data-ttu-id="cb1de-111">Das Windows-Ereignisprotokoll ist für C/C++-Programmierer konzipiert.</span><span class="sxs-lookup"><span data-stu-id="cb1de-111">Windows Event Log is designed for C/C++ programmers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="cb1de-112">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="cb1de-112">Run-time requirements</span></span>

<span data-ttu-id="cb1de-113">Das Windows-Ereignisprotokoll ist ab Windows Vista und Windows Server 2008 im Betriebssystem enthalten.</span><span class="sxs-lookup"><span data-stu-id="cb1de-113">Windows Event Log is included in the operating system beginning with Windows Vista and Windows Server 2008.</span></span>

<span data-ttu-id="cb1de-114">Informationen zu den Lauf Zeitanforderungen für ein bestimmtes Programmier Element finden Sie im Abschnitt "Anforderungen" der Referenzseite für dieses Element.</span><span class="sxs-lookup"><span data-stu-id="cb1de-114">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

<span data-ttu-id="cb1de-115">Den vollständigen Versionsverlauf finden Sie unter [Neuerungen](what-s-new.md).</span><span class="sxs-lookup"><span data-stu-id="cb1de-115">For complete version history, see [What's New](what-s-new.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="cb1de-116">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="cb1de-116">In this section</span></span>


| <span data-ttu-id="cb1de-117">Thema</span><span class="sxs-lookup"><span data-stu-id="cb1de-117">Topic</span></span>                                                        | <span data-ttu-id="cb1de-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cb1de-118">Description</span></span>                                                                                       |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cb1de-119">Verwenden des Windows-Ereignis Protokolls</span><span class="sxs-lookup"><span data-stu-id="cb1de-119">Using Windows Event Log</span></span>](using-windows-event-log.md)        | <span data-ttu-id="cb1de-120">Verfahrens Leit Faden, in dem die Verwendung der Windows-Ereignisprotokoll-API veranschaulicht wird.</span><span class="sxs-lookup"><span data-stu-id="cb1de-120">Procedural guide that shows how to use the Windows Event Log API.</span></span>                                 |
| [<span data-ttu-id="cb1de-121">Referenz zum Windows-Ereignisprotokoll</span><span class="sxs-lookup"><span data-stu-id="cb1de-121">Windows Event Log Reference</span></span>](windows-event-log-reference.md)| <span data-ttu-id="cb1de-122">Die Datentypen, Funktionen, Enumerationen, Strukturen, Konstanten und Schemas, die die API enthält.</span><span class="sxs-lookup"><span data-stu-id="cb1de-122">The data types, functions, enumerations, structures, constants, and schemas that the API includes.</span></span>|