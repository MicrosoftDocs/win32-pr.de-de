---
description: Tablet PC umfasst Technologie zum Erkennen von frei Hand Eingaben, die in der Regel in Form von Handschrift vorliegt.
ms.assetid: 614971a8-2b56-40d4-abb6-aba5ded01883
title: Informationen zur Handschrifterkennung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ff794f018cd0019a5013bacf8b9edfbe45018d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352798"
---
# <a name="about-handwriting-recognition"></a><span data-ttu-id="f5623-103">Informationen zur Handschrifterkennung</span><span class="sxs-lookup"><span data-stu-id="f5623-103">About Handwriting Recognition</span></span>

<span data-ttu-id="f5623-104">Tablet PC umfasst Technologie zum Erkennen von frei Hand Eingaben, die in der Regel in Form von Handschrift vorliegt.</span><span class="sxs-lookup"><span data-stu-id="f5623-104">Tablet PC includes technology for recognizing ink input that is most commonly in the form of handwriting.</span></span> <span data-ttu-id="f5623-105">Das Softwaremodul, das die Erkennung bereitstellt, wird als Erkennungs Modul bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="f5623-105">The software module that provides the recognition is called a recognizer.</span></span> <span data-ttu-id="f5623-106">Eine Erkennung erkennt eine Sprache, eine Gruppe verwandter Sprachen oder eine Klasse verwandter Objekte wie z. b. Musik Notizen, System Gesten oder geometrische Formen.</span><span class="sxs-lookup"><span data-stu-id="f5623-106">A recognizer recognizes one language, a group of related languages, or a class of related objects such as musical notes, system gestures, or geometric shapes.</span></span> <span data-ttu-id="f5623-107">Sie können erkenungen dynamisch dem Ink Services-System hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f5623-107">You can dynamically add recognizers to the ink services system.</span></span>

## <a name="recognition-steps"></a><span data-ttu-id="f5623-108">Erkennungs Schritte</span><span class="sxs-lookup"><span data-stu-id="f5623-108">Recognition Steps</span></span>

<span data-ttu-id="f5623-109">Die Erkennung wird durch die Verwendung eines Erkennungs Kontexts behandelt.</span><span class="sxs-lookup"><span data-stu-id="f5623-109">Recognition is handled through the use of a recognizer context.</span></span> <span data-ttu-id="f5623-110">Die Erkennung besteht aus vier grundlegenden Schritten:</span><span class="sxs-lookup"><span data-stu-id="f5623-110">Recognition consists of four basic steps:</span></span>

1.  <span data-ttu-id="f5623-111">Einrichten der Erkennungs Einschränkungen durch:</span><span class="sxs-lookup"><span data-stu-id="f5623-111">Setting up the recognition constraints by:</span></span>
    -   <span data-ttu-id="f5623-112">Auswählen der Erkennungs-und Eingabemodus (geometrische Einschränkungen).</span><span class="sxs-lookup"><span data-stu-id="f5623-112">Selecting the recognizer and input mode (geometric constraints).</span></span>
    -   <span data-ttu-id="f5623-113">Festlegen der Spracheinschränkungen.</span><span class="sxs-lookup"><span data-stu-id="f5623-113">Setting the language constraints.</span></span> <span data-ttu-id="f5623-114">Beispielsweise können Sie die Eingabe auf alphanumerische Zeichen einschränken oder Schemas übergeben, um die Erkennung zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="f5623-114">For example, you can restrict input to alphanumeric characters or you can pass schemas to assist the recognizer.</span></span>
2.  <span data-ttu-id="f5623-115">Senden von frei Hand Eingaben an die Erkennung.</span><span class="sxs-lookup"><span data-stu-id="f5623-115">Sending ink to the recognizer.</span></span>
3.  <span data-ttu-id="f5623-116">Verarbeiten der Eingabe (erkennen).</span><span class="sxs-lookup"><span data-stu-id="f5623-116">Processing the input (recognizing).</span></span>
4.  <span data-ttu-id="f5623-117">Zurückgeben der Ergebnisse der Erkennung.</span><span class="sxs-lookup"><span data-stu-id="f5623-117">Returning the results of the recognition.</span></span>

<span data-ttu-id="f5623-118">Die Schritte 2 und 3 werden möglicherweise in einer Schleife wiederholt, oder alle frei Hand Eingaben werden möglicherweise dem frei Hand Eingaben hinzugefügt, bevor ein Erkennungs Versuch erfolgt.</span><span class="sxs-lookup"><span data-stu-id="f5623-118">Steps 2 and 3 may be repeated in a loop, or all of the ink strokes may be added to the ink before recognition is attempted.</span></span>

## <a name="samples-and-related-topics"></a><span data-ttu-id="f5623-119">Beispiele und Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="f5623-119">Samples and Related Topics</span></span>

<span data-ttu-id="f5623-120">Das [Beispiel "Advanced Recognition](advanced-recognition-sample.md) " veranschaulicht, wie Erkennungs [**Tools mit frei**](inkdisp-class.md) Hand Objekten verwendet werden, um eine frei Handerkennung auszuführen</span><span class="sxs-lookup"><span data-stu-id="f5623-120">[Advanced Recognition Sample](advanced-recognition-sample.md) demonstrates how to use recognizers with [**Ink**](inkdisp-class.md) objects to perform ink recognition.</span></span>

<span data-ttu-id="f5623-121">Die [Beispiel Vorlage der Erkennungs](recognizer-dll-sample-template.md) Modul-dll enthält eine Vorlage zum Erstellen einer Erkennungs-DLL.</span><span class="sxs-lookup"><span data-stu-id="f5623-121">[Recognizer DLL Sample Template](recognizer-dll-sample-template.md) contains a template for creating a recognizer DLL.</span></span> <span data-ttu-id="f5623-122">Die Vorlage enthält Funktionen zum Registrieren und Aufheben der Registrierung des Servers sowie zu den Skeletten für primäre Erkennungsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="f5623-122">The template contains functions for registering and unregistering the server, as well as skeletons for primary recognizer functions.</span></span>

<span data-ttu-id="f5623-123">In den folgenden Abschnitten werden die grundlegenden Konzepte hinter der Tablet PC-Erkennungstechnologie beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f5623-123">The following sections describe the basic concepts behind the Tablet PC recognition technology.</span></span> <span data-ttu-id="f5623-124">Ausführliche Informationen zum Erstellen von benutzerdefinierten erkenzern finden Sie unter [Erstellen einer Erkennung](creating-a-recognizer.md).</span><span class="sxs-lookup"><span data-stu-id="f5623-124">For detailed information about creating custom recognizers, see [Creating a Recognizer](creating-a-recognizer.md).</span></span>

-   [<span data-ttu-id="f5623-125">Text erkenzer</span><span class="sxs-lookup"><span data-stu-id="f5623-125">Text Recognizers</span></span>](text-recognizers.md)
-   [<span data-ttu-id="f5623-126">Objekterkenzer</span><span class="sxs-lookup"><span data-stu-id="f5623-126">Object Recognizers</span></span>](object-recognizers.md)
-   [<span data-ttu-id="f5623-127">Verwenden der Erkennungs Sammlung</span><span class="sxs-lookup"><span data-stu-id="f5623-127">Using the Recognizers Collection</span></span>](using-the-recognizers-collection.md)
-   [<span data-ttu-id="f5623-128">Erkennungs Kontext</span><span class="sxs-lookup"><span data-stu-id="f5623-128">Recognizer Context</span></span>](recognizer-context.md)
-   [<span data-ttu-id="f5623-129">Erkennungs Segmente</span><span class="sxs-lookup"><span data-stu-id="f5623-129">Recognition Segments</span></span>](recognition-segments.md)
-   [<span data-ttu-id="f5623-130">Erkennung von Abgewinkelter Text</span><span class="sxs-lookup"><span data-stu-id="f5623-130">Recognition of Angled Text</span></span>](recognition-of-angled-text.md)
-   [<span data-ttu-id="f5623-131">Unterstützung für das Unterzeichnen von Stroke-Befehlen</span><span class="sxs-lookup"><span data-stu-id="f5623-131">Recognizer Stroke Reordering Support</span></span>](recognizer-stroke-reordering-support.md)
-   [<span data-ttu-id="f5623-132">Wörterbücher und Faktoide</span><span class="sxs-lookup"><span data-stu-id="f5623-132">Dictionaries and Factoids</span></span>](dictionaries-and-factoids.md)
-   <span data-ttu-id="f5623-133">[Vertrauens Eigenschaft \[ für die Erkennung\]](confidence-property--about-recognition.md)</span><span class="sxs-lookup"><span data-stu-id="f5623-133">[Confidence Property \[About Recognition\]](confidence-property--about-recognition.md)</span></span>
-   [<span data-ttu-id="f5623-134">Alternative Stile</span><span class="sxs-lookup"><span data-stu-id="f5623-134">Alternates</span></span>](alternates.md)
-   [<span data-ttu-id="f5623-135">Frei Hand Segmente und-Alternativen</span><span class="sxs-lookup"><span data-stu-id="f5623-135">Ink Segments and Alternates</span></span>](ink-segments-and-alternates.md)

 

 



