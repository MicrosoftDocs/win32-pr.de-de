---
description: Wenn Sie sich dafür entscheiden, kann die Anwendung eigene Erkennungs Implementierungen bereitstellen. In diesem Abschnitt werden die Anforderungen zum Erstellen einer benutzerdefinierten Anwendungs Erkennung für Ihre Anwendung beschrieben, die Sie mit der Tablet PC Platform-API verwenden können.
ms.assetid: 502ef3fb-ba45-4f8b-bbd5-19c24e313439
title: Erstellen einer Erkennung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc71f56dc7095c6c72d18b36c3a12caa493ec9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342784"
---
# <a name="creating-a-recognizer"></a><span data-ttu-id="3173d-104">Erstellen einer Erkennung</span><span class="sxs-lookup"><span data-stu-id="3173d-104">Creating a Recognizer</span></span>

<span data-ttu-id="3173d-105">Wenn Sie sich dafür entscheiden, kann die Anwendung eigene Erkennungs Implementierungen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="3173d-105">If you choose to do so, your application can provide its own recognizer implementations.</span></span> <span data-ttu-id="3173d-106">In diesem Abschnitt werden die Anforderungen zum Erstellen einer benutzerdefinierten Anwendungs Erkennung für Ihre Anwendung beschrieben, die Sie mit der Tablet PC Platform-API verwenden können.</span><span class="sxs-lookup"><span data-stu-id="3173d-106">This section describes the requirements for creating a custom application recognizer for your application that you can use with the Tablet PC Platform API.</span></span>

> [!Note]  
> <span data-ttu-id="3173d-107">Benutzerdefinierte Anwendungs Erkennungs Tools werden nicht vom Tablet PC-Eingabebereich oder Microsoft Windows-Journal verwendet.</span><span class="sxs-lookup"><span data-stu-id="3173d-107">Custom application recognizers are not used by the Tablet PC Input Panel or Microsoft Windows Journal.</span></span> <span data-ttu-id="3173d-108">Diese Zubehör verwenden nur Erkennungs Tools, mit denen Sie getestet wurden.</span><span class="sxs-lookup"><span data-stu-id="3173d-108">These accessories use only recognizers with which they have been tested.</span></span>

 

<span data-ttu-id="3173d-109">In den folgenden Abschnitten wird die Implementierung einer benutzerdefinierten Erkennung ausführlich erläutert:</span><span class="sxs-lookup"><span data-stu-id="3173d-109">The following sections detail the implementation of a custom recognizer:</span></span>

-   [<span data-ttu-id="3173d-110">Erkennungs-API-Architektur</span><span class="sxs-lookup"><span data-stu-id="3173d-110">Recognition API Architecture</span></span>](recognition-api-architecture.md)
-   <span data-ttu-id="3173d-111">[Erforderliche Erkennungs-APIs](/previous-versions//ms701664(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3173d-111">[Required Recognition APIs](/previous-versions//ms701664(v=vs.85))</span></span>
-   [<span data-ttu-id="3173d-112">Herkenzer und hrecocontext</span><span class="sxs-lookup"><span data-stu-id="3173d-112">HRECOGNIZER and HRECOCONTEXT</span></span>](hrecognizer-and-hrecocontext.md)
-   [<span data-ttu-id="3173d-113">Gitterstruktur der Erkennungsfunktion</span><span class="sxs-lookup"><span data-stu-id="3173d-113">Recognizer Lattice Structure</span></span>](recognizer-lattice-structure.md)
-   [<span data-ttu-id="3173d-114">Registrieren der Erkennungs-DLL</span><span class="sxs-lookup"><span data-stu-id="3173d-114">Registering Your Recognizer DLL</span></span>](registering-your-recognizer-dll.md)
-   [<span data-ttu-id="3173d-115">Überlegungen zum Erkennungs Thread</span><span class="sxs-lookup"><span data-stu-id="3173d-115">Recognizer Threading Considerations</span></span>](recognizer-threading-considerations.md)
-   [<span data-ttu-id="3173d-116">Typische Aufruf Sequenz</span><span class="sxs-lookup"><span data-stu-id="3173d-116">Typical Calling Sequence</span></span>](typical-calling-sequence.md)
-   [<span data-ttu-id="3173d-117">Beispiel Vorlage für Erkennungs Modul-dll</span><span class="sxs-lookup"><span data-stu-id="3173d-117">Recognizer DLL Sample Template</span></span>](recognizer-dll-sample-template.md)
-   [<span data-ttu-id="3173d-118">Unicode-Bereichs Werte von Gesten</span><span class="sxs-lookup"><span data-stu-id="3173d-118">Unicode Range Values of Gestures</span></span>](unicode-range-values-of-gestures.md)
-   [<span data-ttu-id="3173d-119">Erkennungs-APIs</span><span class="sxs-lookup"><span data-stu-id="3173d-119">Recognizer APIs</span></span>](recognizer-apis.md)

 

 
