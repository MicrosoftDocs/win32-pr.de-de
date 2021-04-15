---
description: Standardmäßig verwendet die Erkennung ein System Wörterbuch, das alle häufig geschriebenen Wörter in einer Sprache enthält.
ms.assetid: 2ddf04dd-613b-4570-9474-0e33208c4012
title: Anwendungs Wörterbücher verwenden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74dfda443a688af9dfcec44a81f0e5ed2d50846c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484787"
---
# <a name="using-application-dictionaries"></a><span data-ttu-id="880ff-103">Anwendungs Wörterbücher verwenden</span><span class="sxs-lookup"><span data-stu-id="880ff-103">Using Application Dictionaries</span></span>

<span data-ttu-id="880ff-104">Standardmäßig verwendet die Erkennung ein System Wörterbuch, das alle häufig geschriebenen Wörter in einer Sprache enthält.</span><span class="sxs-lookup"><span data-stu-id="880ff-104">By default, the recognizer uses a system dictionary that contains all of the commonly written words in a language.</span></span> <span data-ttu-id="880ff-105">Außerdem verfügt die Erkennung über ein Benutzerwörterbuch, das Wörter enthält, die der Benutzer dem Wörterbuch hinzugefügt hat.</span><span class="sxs-lookup"><span data-stu-id="880ff-105">In addition, the recognizer has a user dictionary that contains words that the user has added to the dictionary.</span></span> <span data-ttu-id="880ff-106">Benutzer fügen dem Benutzerwörterbuch über den Tablet PC-Eingabebereich ein Wort hinzu, indem Sie Folgendes auswählen:</span><span class="sxs-lookup"><span data-stu-id="880ff-106">Users add a word to the user dictionary through Tablet PC Input Panel through selections in:</span></span>

-   <span data-ttu-id="880ff-107">Die Alternative Liste (beim Schreiben).</span><span class="sxs-lookup"><span data-stu-id="880ff-107">The alternate list (when writing).</span></span>
-   <span data-ttu-id="880ff-108">Das Sprach Tools-Menü (bei der Sprache).</span><span class="sxs-lookup"><span data-stu-id="880ff-108">The Speech Tools menu (when speaking).</span></span>

<span data-ttu-id="880ff-109">Wenn Sie eine Anwendung entwerfen, in die Sie erwarten, dass der Benutzer Wörter schreibt, die nicht im System Wörterbuch oder im Benutzerwörterbuch gefunden werden, erstellen Sie ein Anwendungs Wörterbuch.</span><span class="sxs-lookup"><span data-stu-id="880ff-109">If you are designing an application into which you anticipate the user will write words that are not found in either the system dictionary or the user dictionary, create an application dictionary.</span></span> <span data-ttu-id="880ff-110">Ein Anwendungs Wörterbuch verbessert die Erkennungsgenauigkeit weiter, indem dem Erkennungs Modul eine zusätzliche angepasste Liste von Wörtern bereitgestellt wird, die wahrscheinlich als Handschrift in eine Anwendung eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="880ff-110">An application dictionary further improves recognition accuracy by providing the recognizer with an additional customized list of words likely to be entered as handwriting into an application.</span></span>

<span data-ttu-id="880ff-111">Sie erstellen ein Anwendungs Wörterbuch mit dem [**WordList**](inkwordlist-class.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="880ff-111">You create an application dictionary by using the [**WordList**](inkwordlist-class.md) object.</span></span> <span data-ttu-id="880ff-112">Das resultierende Anwendungs Wörterbuch erhöht die Erkennungsgenauigkeit, indem der Erkennungs Modul eine Liste erwarteter Wörter bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="880ff-112">The ensuing application dictionary increases recognition accuracy by providing the recognizer with a list of expected words.</span></span> <span data-ttu-id="880ff-113">Beispielsweise erhöht ein Anwendungs Wörterbuch, das die medizinische Terminologie enthält, die Erkennungsgenauigkeit innerhalb einer Anwendung, die für die medizinische Branche entwickelt wurde, in die die Begriffe wahrscheinlich geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="880ff-113">For example, an application dictionary that contains medical terminology increases recognition accuracy within an application developed for the medical industry into which the terms are likely to be written.</span></span>

<span data-ttu-id="880ff-114">Ein weiteres Beispiel: Wenn Sie ein Formular für jemanden zum Sortieren von Musikinstrumenten entwerfen, erstellen Sie ein [**WordList**](inkwordlist-class.md) -Objekt, das die Namen der am häufigsten erstellten Instrumentations Hersteller enthält.</span><span class="sxs-lookup"><span data-stu-id="880ff-114">As another example, when designing a form for someone to order musical instruments, create a [**WordList**](inkwordlist-class.md) object that contains the names of the most common instrument manufacturers.</span></span> <span data-ttu-id="880ff-115">Legen Sie die [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) -Eigenschaft des [**erkenzercontext**](inkrecognizercontext-class.md) -Objekts auf das von Ihnen erstellte **WordList** -Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="880ff-115">Set the [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) property of the [**RecognizerContext**](inkrecognizercontext-class.md) object to the **WordList** object you created.</span></span> <span data-ttu-id="880ff-116">Diese Liste von Wörtern wird dann vom **erkenzercontext** -Objekt an die Erkennung weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="880ff-116">This list of words is then passed to the recognizer by the **RecognizerContext** object.</span></span> <span data-ttu-id="880ff-117">Das Anwendungs Wörterbuch erhöht die Erkennungsgenauigkeit, wenn diese Namen in einem Feld in der Anwendung geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="880ff-117">The application dictionary increases recognition accuracy when those names are written in a field in the application.</span></span>

<span data-ttu-id="880ff-118">In den folgenden Themen wird die Verwendung von Anwendungs Wörterbüchern beschrieben.</span><span class="sxs-lookup"><span data-stu-id="880ff-118">The following topics describe how to use application dictionaries.</span></span>

-   [<span data-ttu-id="880ff-119">Grundlegendes zu Wortlisten, Erkennungs Kontext und Faktoiden</span><span class="sxs-lookup"><span data-stu-id="880ff-119">Understanding Word Lists, Recognizer Context, and Factoids</span></span>](understanding-wordlists--the-recognizercontext--and-factoids.md)
-   [<span data-ttu-id="880ff-120">Verwenden von Anwendungs Wörterbüchern mit den Tablet PC Platform-APIs</span><span class="sxs-lookup"><span data-stu-id="880ff-120">Using Application Dictionaries with the Tablet PC Platform APIs</span></span>](using-application-dictionaries-with-the-tablet-pc-platform-apis.md)
-   [<span data-ttu-id="880ff-121">Erstellen benutzerdefinierter Wörterbücher für die Handschrifterkennung</span><span class="sxs-lookup"><span data-stu-id="880ff-121">Creating Custom Dictionaries for Handwriting Recognition</span></span>](creating-custom-dictionaries-for-handwriting-recognition-in-windows-7-and-windows-server-2008-r2.md)

 

 



