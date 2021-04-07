---
description: Protokollierungs Fehler
ms.assetid: 690ea91b-5bc0-45f0-8354-ec625709f7bd
title: Protokollierungs Fehler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76cded9d4cfaedd93e846fec52b07bf5d4eef9a5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745969"
---
# <a name="logging-errors"></a><span data-ttu-id="cde57-103">Protokollierungs Fehler</span><span class="sxs-lookup"><span data-stu-id="cde57-103">Logging Errors</span></span>

<span data-ttu-id="cde57-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="cde57-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="cde57-105">[DirectShow-Bearbeitungs Dienste (DirectShow-Bearbeitungs Dienste](directshow-editing-services.md) ) bieten einen integrierten Mechanismus zum Protokollieren von Fehlern, die beim Laden, erstellen oder Rendern eines des-Projekts auftreten.</span><span class="sxs-lookup"><span data-stu-id="cde57-105">[DirectShow Editing Services](directshow-editing-services.md) (DES) provides a built-in mechanism for logging errors that occur when loading, constructing, or rendering a DES project.</span></span> <span data-ttu-id="cde57-106">Dieser Artikel enthält eine Beispiel Konsolenanwendung, die eine XML-Projektdatei lädt und versucht, Sie zu Rendering.</span><span class="sxs-lookup"><span data-stu-id="cde57-106">This article presents a sample console application that loads an XML project file and attempts to render it.</span></span> <span data-ttu-id="cde57-107">Wenn ein Fehler auftritt, gibt die Anwendung im Konsolenfenster eine Fehlermeldung aus.</span><span class="sxs-lookup"><span data-stu-id="cde57-107">If an error occurs, the application prints an error message in the console window.</span></span> <span data-ttu-id="cde57-108">Der Beispielcode in diesem Artikel baut auf dem Beispiel auf, das beim [Laden und Anzeigen der Vorschau eines Projekts](loading-and-previewing-a-project.md)angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="cde57-108">The sample code presented in this article builds on the example given in [Loading and Previewing a Project](loading-and-previewing-a-project.md).</span></span>

> [!Note]  
> <span data-ttu-id="cde57-109">Es ist nicht erforderlich, dass Ihre Anwendung die Fehler Protokollierung implementiert.</span><span class="sxs-lookup"><span data-stu-id="cde57-109">Your application is not required to implement error logging.</span></span> <span data-ttu-id="cde57-110">DES protokolliert keine Fehler, es sei denn, Sie fordern Sie explizit an.</span><span class="sxs-lookup"><span data-stu-id="cde57-110">DES does not log errors unless you explicitly request it.</span></span>

 

<span data-ttu-id="cde57-111">In diesem Artikel wird davon ausgegangen, dass Sie die com-Client Programmierung und das des-Zeitachsen Modells verstehen</span><span class="sxs-lookup"><span data-stu-id="cde57-111">This article assumes that you understand COM client programming and the DES timeline model.</span></span> <span data-ttu-id="cde57-112">Außerdem müssen Sie die Grundlagen der COM-Objekt Programmierung verstehen.</span><span class="sxs-lookup"><span data-stu-id="cde57-112">In addition, you need to understand the basics of COM object programming.</span></span> <span data-ttu-id="cde57-113">Informationen zu Zeitachsen in des finden Sie [unter Zeitachsen Modell](the-timeline-model.md).</span><span class="sxs-lookup"><span data-stu-id="cde57-113">For information about timelines in DES, see [The Timeline Model](the-timeline-model.md).</span></span>

<span data-ttu-id="cde57-114">Dieser Artikel enthält folgende Abschnitte.</span><span class="sxs-lookup"><span data-stu-id="cde57-114">This article contains the following sections.</span></span>

-   [<span data-ttu-id="cde57-115">Übersicht über die Fehler Protokollierung</span><span class="sxs-lookup"><span data-stu-id="cde57-115">Overview of Error Logging</span></span>](overview-of-error-logging.md)
-   [<span data-ttu-id="cde57-116">Erstellen einer Fehler Protokollierungs Klasse</span><span class="sxs-lookup"><span data-stu-id="cde57-116">Creating an Error Logging Class</span></span>](creating-an-error-logging-class.md)
-   [<span data-ttu-id="cde57-117">Implementieren von iamerrorlog</span><span class="sxs-lookup"><span data-stu-id="cde57-117">Implementing IAMErrorLog</span></span>](implementing-iamerrorlog.md)
-   [<span data-ttu-id="cde57-118">Festlegen des Fehler Protokolls</span><span class="sxs-lookup"><span data-stu-id="cde57-118">Setting the Error Log</span></span>](setting-the-error-log.md)
-   [<span data-ttu-id="cde57-119">DES-Fehler Protokollierung: Beispiel Code</span><span class="sxs-lookup"><span data-stu-id="cde57-119">DES Error Logging: Example Code</span></span>](des-error-logging--example-code.md)

## <a name="related-topics"></a><span data-ttu-id="cde57-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cde57-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cde57-121">Verwenden von DirectShow-Bearbeitungs Diensten</span><span class="sxs-lookup"><span data-stu-id="cde57-121">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 



