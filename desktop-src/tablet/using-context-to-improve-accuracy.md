---
description: Ein Handschrifterkennungs-Engine oder eine Erkennungsfunktion ist Software, die frei Hand Eingaben verarbeitet und diese frei Hand Eingaben in Text umwandelt
ms.assetid: b64f6856-453c-4080-84e0-0a9e69e79de7
title: Verwenden des Kontexts zur Verbesserung der Genauigkeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd5c807804c1855e0be56b09f08448e3dc2967d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346303"
---
# <a name="using-context-to-improve-accuracy"></a><span data-ttu-id="031a6-103">Verwenden des Kontexts zur Verbesserung der Genauigkeit</span><span class="sxs-lookup"><span data-stu-id="031a6-103">Using Context to Improve Accuracy</span></span>

<span data-ttu-id="031a6-104">Ein Handschrifterkennungs-Engine oder eine Erkennungsfunktion ist Software, die frei Hand Eingaben verarbeitet und diese frei Hand Eingaben in Text umwandelt</span><span class="sxs-lookup"><span data-stu-id="031a6-104">A handwriting recognition engine, or recognizer, is software that processes ink and converts that ink into text.</span></span> <span data-ttu-id="031a6-105">Ein Kontext ist relevant, anwendungsspezifische Informationen, die Sie für eine Erkennung bereitstellen, um die Erkennungsgenauigkeit zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="031a6-105">A context is relevant, application-specific information that you provide to a recognizer to improve recognition accuracy.</span></span> <span data-ttu-id="031a6-106">Mit anderen Worten: der Kontext ist ein beliebiger Informationselement, mit dem die Erkennung bei der exakten Verarbeitung der frei Hand Eingaben in einem Feld unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="031a6-106">In other words, context is any piece of information about input that aids the recognizer in accurately processing the ink in a field.</span></span>

<span data-ttu-id="031a6-107">In diesem Abschnitt werden die verschiedenen Methoden beschrieben, mit denen Sie den Kontext in ihrer Tablet PC-Anwendung nutzen können, um den Schwerpunkt auf das bevorzugte programmgesteuerte Verfahren für Anwendungen zu setzen, die nicht frei Hand Eingaben sind</span><span class="sxs-lookup"><span data-stu-id="031a6-107">This section describes the different ways you can take advantage of context in your Tablet PC application, placing emphasis on the preferred programmatic technique for applications that are not ink enabled.</span></span>

> [!Note]  
> <span data-ttu-id="031a6-108">In den Bereichen der Tablet PC-Technologie des Windows Vista Software Development Kit (SDK) gibt es den Begriff "Kontext", der in Bezug auf das [**erkennnulcontext**](inkrecognizercontext-class.md) -Objekt und seine [**PrefixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_prefixtext) -und [**SuffixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_suffixtext) -Eigenschaften verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="031a6-108">There are places in the Tablet PC Technology sections of the Windows Vista Software Development Kit (SDK) where the term "context" is used in regard to the [**RecognizerContext**](inkrecognizercontext-class.md) object and its [**PrefixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_prefixtext) and [**SuffixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_suffixtext) properties.</span></span> <span data-ttu-id="031a6-109">Verwechseln Sie diese anderen Verwendungen von "Context" nicht mit der Definition in diesem Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="031a6-109">Do not confuse these other usages of "context" with the definition in this section.</span></span>

 

 

 



