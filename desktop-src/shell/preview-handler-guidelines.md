---
description: Wenn Sie eine Vorschauversion bereitstellen, sollten die folgenden Richtlinien befolgt werden.
title: Vorschau der handlerrichtlinien
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 3538cc5d-afb6-4d43-b527-6c6e1d773b41
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e725d561056e78a88bd9eeabd00d90abda1f0343
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866152"
---
# <a name="preview-handler-guidelines"></a><span data-ttu-id="9272a-103">Vorschau der handlerrichtlinien</span><span class="sxs-lookup"><span data-stu-id="9272a-103">Preview Handler Guidelines</span></span>

<span data-ttu-id="9272a-104">Wenn Sie eine Vorschauversion bereitstellen, sollten die folgenden Richtlinien befolgt werden.</span><span class="sxs-lookup"><span data-stu-id="9272a-104">When you provide a preview, the following guidelines should be followed.</span></span>

-   <span data-ttu-id="9272a-105">Eine Vorschauversion sollte eine minimale Benutzeroberfläche enthalten – es handelt sich einfach um eine Vorschauversion.</span><span class="sxs-lookup"><span data-stu-id="9272a-105">A preview should contain minimal UI—it is simply a preview.</span></span> <span data-ttu-id="9272a-106">Es sollte nur der Inhalt der Datei angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="9272a-106">It should display only the file content.</span></span> <span data-ttu-id="9272a-107">Es sollten keine Dialogfelder, Begrüßungs Bildschirme, Symbolleisten oder Aufgabenbereiche angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="9272a-107">It should not display dialogs, splash screens, toolbars, or task panes.</span></span> <span data-ttu-id="9272a-108">Der Lesebereich wird in der Regel zusammen mit der Suche verwendet, um eine Datei schnell zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="9272a-108">The reading pane will commonly be used in conjunction with search to quickly identify a file.</span></span> <span data-ttu-id="9272a-109">Alle Elemente, die den Lesebereich gruppieren oder anderweitig aus Dateiinhalten entfernt oder Verzögerungen in der Vorschau Anzeige verursachen, sollten vermieden werden.</span><span class="sxs-lookup"><span data-stu-id="9272a-109">Anything that clutters the reading pane or otherwise detracts from file content or causes delays in preview display should be avoided.</span></span>
-   <span data-ttu-id="9272a-110">Die Vorschau sollte dem Benutzer ermöglichen, im Dokument zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="9272a-110">The preview should allow the user to navigate in the document.</span></span> <span data-ttu-id="9272a-111">Der Benutzer sollte außerdem in der Lage sein, Text auszuwählen und zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="9272a-111">The user should also be able to select and copy text.</span></span>
-   <span data-ttu-id="9272a-112">Die Vorschau sollte nicht Arbeitsspeicher intensiv sein, sollte nur minimale Ressourcen beanspruchen und sollte über eine schnelle Startzeit verfügen.</span><span class="sxs-lookup"><span data-stu-id="9272a-112">The preview should not be memory-intensive, should consume minimal resources, and should have a fast startup time.</span></span>
-   <span data-ttu-id="9272a-113">Alle Skripts und Makros in der Datei, die in der Vorschau angezeigt werden, sollten aus Sicherheits-und Datenschutzgründen nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9272a-113">All script and macros in the file being previewed should be blocked from running for security and privacy purposes.</span></span>
-   <span data-ttu-id="9272a-114">Die Vorschauversion sollte die von der Anwendung unterstützten Tastaturbeschleuniger für Navigation und Auswahl unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9272a-114">The preview should support keyboard accelerators for navigation and selection as supported by the application.</span></span> <span data-ttu-id="9272a-115">Es sollte auch ein Kontextmenü angezeigt werden, wenn mit der rechten Maustaste geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="9272a-115">It should also display a context menu when right-clicked.</span></span>
-   <span data-ttu-id="9272a-116">Wenn eine Datei als Vorschau angezeigt wird, sollte die Vorschau der Datei nicht gesperrt werden.</span><span class="sxs-lookup"><span data-stu-id="9272a-116">When a file is displayed as a preview, the preview should not lock the file itself.</span></span> <span data-ttu-id="9272a-117">Eine Datei kann in der zugehörigen Anwendung in der Vorschau angezeigt und geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="9272a-117">A file can be previewed and opened in its associated application at the same time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9272a-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9272a-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9272a-119">Vorschau Handler und Shell-Vorschau Host</span><span class="sxs-lookup"><span data-stu-id="9272a-119">Preview Handlers and Shell Preview Host</span></span>](preview-handlers.md)
</dt> <dt>

[<span data-ttu-id="9272a-120">Entwickeln von Vorschau Handlern</span><span class="sxs-lookup"><span data-stu-id="9272a-120">Building Preview Handlers</span></span>](building-preview-handlers.md)
</dt> </dl>

 

 



