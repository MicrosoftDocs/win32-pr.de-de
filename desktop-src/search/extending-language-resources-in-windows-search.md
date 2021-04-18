---
description: Windows Search verwendet Sprachressourcen wie Wörter Trennungen und Wort Stamm Erkennungen, um den Text im systemeigenen Gebiets Schema während der Indexerstellung und der Abfrage Verarbeitung zu unterbrechen.
ms.assetid: 6e8ab091-c22c-4425-b8b9-211d53816304
title: Erweitern von Sprachressourcen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 727f5812d0aee370c96d98f1c57dfffcbea5bc8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343653"
---
# <a name="extending-language-resources"></a><span data-ttu-id="c7643-103">Erweitern von Sprachressourcen</span><span class="sxs-lookup"><span data-stu-id="c7643-103">Extending Language Resources</span></span>

<span data-ttu-id="c7643-104">Windows Search verwendet Sprachressourcen wie Wörter Trennungen und Wort Stamm Erkennungen, um den Text im systemeigenen Gebiets Schema während der Indexerstellung und der Abfrage Verarbeitung zu unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="c7643-104">Windows Search uses language resources such as word breakers and stemmers to break text in its native locale during index creation and query processing.</span></span> <span data-ttu-id="c7643-105">Microsoft stellt Wörter Trennungen und Wort Stamm Erkennungen für verschiedene Sprachen bereit.</span><span class="sxs-lookup"><span data-stu-id="c7643-105">Microsoft provides word breakers and stemmers for several languages.</span></span> <span data-ttu-id="c7643-106">In diesem Abschnitt wird beschrieben, wie benutzerdefinierte Wörter Trennungen und Wort Stamm Erkennungen für Sprachen und Gebiets Schemas implementiert und verwendet werden, die über die von Microsoft</span><span class="sxs-lookup"><span data-stu-id="c7643-106">This section describes how to implement and use custom word breakers and stemmers for languages and locales beyond those provided by Microsoft.</span></span>

-   [<span data-ttu-id="c7643-107">Grundlegendes zu Sprachressourcen Komponenten</span><span class="sxs-lookup"><span data-stu-id="c7643-107">Understanding Language Resource Components</span></span>](understanding-language-resource-components.md)
-   [<span data-ttu-id="c7643-108">Implementieren von Wörter Trennungen und Wort Stamm Erkennungen</span><span class="sxs-lookup"><span data-stu-id="c7643-108">Implementing a Word Breaker and Stemmer</span></span>](implementing-a-word-breaker-and-stemmer.md)
-   [<span data-ttu-id="c7643-109">Überlegungen zu linguistischer und Unicode</span><span class="sxs-lookup"><span data-stu-id="c7643-109">Linguistic and Unicode Considerations</span></span>](linguistic-and-unicode-considerations.md)
-   [<span data-ttu-id="c7643-110">Problembehandlung bei Sprachressourcen und bewährten Methoden</span><span class="sxs-lookup"><span data-stu-id="c7643-110">Troubleshooting Language Resources and Best Practices</span></span>](troubleshooting-language-resources.md)

## <a name="additional-resources"></a><span data-ttu-id="c7643-111">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c7643-111">Additional Resources</span></span>

-   <span data-ttu-id="c7643-112">Eine Liste der von der Wörter Trennung unterstützten lanuages finden Sie unter [von Windows Search unterstützte Sprachen](-search-3x-wds-language-support.md).</span><span class="sxs-lookup"><span data-stu-id="c7643-112">For a list of lanuages supported by word breakers, see [Languages Supported by Windows Search](-search-3x-wds-language-support.md).</span></span>
-   <span data-ttu-id="c7643-113">Wenn Sie die Sprache eines Texts identifizieren müssen, können Sie die automatische Erkennung von Sprachen (LAD) verwenden, die in Windows 7 und höher verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="c7643-113">If you need to identify the language of a piece of text, you can use Language Auto-Detection (LAD), which is available in Windows 7 and later.</span></span> <span data-ttu-id="c7643-114">Weitere Informationen finden Sie unter [Erweiterte linguistische Dienste](../intl/extended-linguistic-services.md) (STS).</span><span class="sxs-lookup"><span data-stu-id="c7643-114">For more information, see [Extended Linguistic Services](../intl/extended-linguistic-services.md) (ELS).</span></span>
-   <span data-ttu-id="c7643-115">Die entsprechende Referenz Dokumentation finden [Sie unter Daten-Add-in-Schnittstellen](-search-data-addins-interfaces-entry-page.md).</span><span class="sxs-lookup"><span data-stu-id="c7643-115">For applicable reference documentation, see [Data Add-in Interfaces](-search-data-addins-interfaces-entry-page.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c7643-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c7643-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7643-117">Verwalten des Indexes</span><span class="sxs-lookup"><span data-stu-id="c7643-117">Managing the Index</span></span>](-search-3x-wds-mngidx-overview.md)
</dt> <dt>

[<span data-ttu-id="c7643-118">Programm gesteuertes Abfragen des Indexes</span><span class="sxs-lookup"><span data-stu-id="c7643-118">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="c7643-119">Erweitern des Indexes</span><span class="sxs-lookup"><span data-stu-id="c7643-119">Extending the Index</span></span>](-search-3x-wds-extidx-overview.md)
</dt> </dl>

 

 
