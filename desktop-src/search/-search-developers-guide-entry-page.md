---
description: Drittanbieter können Anwendungen erstellen, die den Index für Daten Programm gesteuert Abfragen und Windows Search so erweitern, dass Daten aus benutzerdefinierten Dateiformaten und Daten speichern indiziert werden.
ms.assetid: 70046df0-ce48-472d-b24b-8231ea3a43c0
title: Entwicklerhandbuch für Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61593f47e081059966936a99a7d2baea114df92a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484443"
---
# <a name="windows-search-developers-guide"></a><span data-ttu-id="bb428-103">Entwicklerhandbuch für Windows Search</span><span class="sxs-lookup"><span data-stu-id="bb428-103">Windows Search Developer's Guide</span></span>

<span data-ttu-id="bb428-104">Drittanbieter können Anwendungen erstellen, die den Index für Daten Programm gesteuert Abfragen und Windows Search so erweitern, dass Daten aus benutzerdefinierten Dateiformaten und Daten speichern indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="bb428-104">Third parties can create applications that query the index for data programmatically and can extend Windows Search to index data from custom file formats and data stores.</span></span> <span data-ttu-id="bb428-105">Um Windows Search-Anwendungen zu erstellen, müssen Entwickler von Drittanbietern zuerst einen Shell-Datenspeicher implementieren, um eine sinnvolle Benutzer Leistung zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="bb428-105">To create Windows Search applications, third-party developers must first implement a Shell data store to a achieve a reasonable user experience.</span></span> <span data-ttu-id="bb428-106">Weitere Informationen finden Sie unter [Implementieren der grundlegenden Ordner Objekt Schnittstellen](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bb428-106">For more information, see [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span></span>

<span data-ttu-id="bb428-107">Sie müssen auch die [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) für die Windows Search-Bibliotheken herunterladen.</span><span class="sxs-lookup"><span data-stu-id="bb428-107">You must also download the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) for the Windows Search libraries.</span></span> <span data-ttu-id="bb428-108">Die [Beispiele für Windows Search SDK](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8) enthalten nützliche Codebeispiele und eine Interoperabilität-Assembly für die Entwicklung mit verwaltetem Code.</span><span class="sxs-lookup"><span data-stu-id="bb428-108">The [Windows Search SDK Samples](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8) contains useful code samples and an interopability assembly for developing with managed code.</span></span> <span data-ttu-id="bb428-109">Weitere Informationen zur Verwendung der Codebeispiele finden Sie unter [Codebeispiele für Windows-Suche](-search-3x-wds-sampleentry.md).</span><span class="sxs-lookup"><span data-stu-id="bb428-109">For more information on using the code samples, see [Windows Search Code Samples](-search-3x-wds-sampleentry.md).</span></span>

<span data-ttu-id="bb428-110">Dieser Abschnitt ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="bb428-110">This section is organized as follows:</span></span>

- [<span data-ttu-id="bb428-111">Verwalten des Indexes</span><span class="sxs-lookup"><span data-stu-id="bb428-111">Managing the Index</span></span>](-search-3x-wds-mngidx-overview.md)
- [<span data-ttu-id="bb428-112">Programm gesteuertes Abfragen des Indexes</span><span class="sxs-lookup"><span data-stu-id="bb428-112">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
- [<span data-ttu-id="bb428-113">Erweitern des Indexes</span><span class="sxs-lookup"><span data-stu-id="bb428-113">Extending the Index</span></span>](-search-3x-wds-extidx-overview.md)
- [<span data-ttu-id="bb428-114">Erweitern von Sprachressourcen</span><span class="sxs-lookup"><span data-stu-id="bb428-114">Extending Language Resources</span></span>](extending-language-resources-in-windows-search.md)

## <a name="additional-resources"></a><span data-ttu-id="bb428-115">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bb428-115">Additional Resources</span></span>

- <span data-ttu-id="bb428-116">Informationen zu den von der Community unterstützten Frage-und Diskussions Nachrichten für Suchtechnologien finden Sie im [MSDN-Forum: Entwicklung von Windows-Desktop-suchen](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).</span><span class="sxs-lookup"><span data-stu-id="bb428-116">For community-supported question and discussion message boards on Search technologies, see [MSDN Forum: Windows Desktop Search Development](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).</span></span>
- <span data-ttu-id="bb428-117">So laden Sie die Such Code Beispiele herunter:</span><span class="sxs-lookup"><span data-stu-id="bb428-117">To download the Search Code Samples:</span></span>
  - [<span data-ttu-id="bb428-118">Beispiele für Windows-Suche</span><span class="sxs-lookup"><span data-stu-id="bb428-118">Windows Search Samples</span></span>](-search-samples-ovw.md)
- <span data-ttu-id="bb428-119">So laden Sie die Windows SDK herunter:</span><span class="sxs-lookup"><span data-stu-id="bb428-119">To download the Windows SDK:</span></span>
  - <span data-ttu-id="bb428-120">Für Windows 10: [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)</span><span class="sxs-lookup"><span data-stu-id="bb428-120">For Windows 10: [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)</span></span>
  - <span data-ttu-id="bb428-121">Für Windows 7: [Windows SDK für Windows 7 und .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span><span class="sxs-lookup"><span data-stu-id="bb428-121">For Windows 7: [Windows SDK for Windows 7 and .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb428-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bb428-122">Related topics</span></span>

[<span data-ttu-id="bb428-123">Übersicht über Windows Search</span><span class="sxs-lookup"><span data-stu-id="bb428-123">Windows Search Overview</span></span>](-search-3x-wds-overview.md)

[<span data-ttu-id="bb428-124">Referenz zur Windows-Suche</span><span class="sxs-lookup"><span data-stu-id="bb428-124">Windows Search Reference</span></span>](-search-reference-entry-page.md)

[<span data-ttu-id="bb428-125">Code Beispiele für Windows Search</span><span class="sxs-lookup"><span data-stu-id="bb428-125">Windows Search Code Samples</span></span>](-search-samples-ovw.md)

[<span data-ttu-id="bb428-126">Verbundsuche in Windows 10</span><span class="sxs-lookup"><span data-stu-id="bb428-126">Federated Search in Windows</span></span>](-search-federated-search-overview.md)

[<span data-ttu-id="bb428-127">Verwandte Suchtechnologien</span><span class="sxs-lookup"><span data-stu-id="bb428-127">Related Search Technologies</span></span>](-search-3x-wds-sampleentry.md)

[<span data-ttu-id="bb428-128">Glossar für Windows-Suche</span><span class="sxs-lookup"><span data-stu-id="bb428-128">Windows Search Glossary</span></span>](search-glossary.md)
